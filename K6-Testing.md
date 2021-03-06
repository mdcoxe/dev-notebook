# K6 Testing notes/trials/experiments

### Run command
``` k6 run --out influxdb=http://localhost:8086/<db name> script.js ```
--out tag indicates output to influxDB

[K6 Notes](https://gist.github.com/mdcoxe/0d1e208238689ee90c71cfaec108fe6d)

## Successful smoke-test of Greenstands wallet API
- The options block:
``` 
export let options = {
  vus: 1, //
  duration: '1m', //length of test
  thresholds: {
      http_req_duration: ['p(99)<1500'],//Set failure treshold at 1500ms
  },
};
```
- The route block:
``` 
export default () => {   
    let response = http.post(
        (BASE_URL + "/transfers"),
        '{\n    "bundle": {\n   "bundle_size": 1\n  },\n    "sender_wallet": "Wendell_Boyle43",\n    "receiver_wallet": "Rae35"\n}',
        {
            headers: {
                "Authorization": `Bearer ${BEARER_TOKEN}`,
                "TREETRACKER-API-KEY": `${API_KEY}`,
                "Content-Type": "application/json"
            },
        } 
    )
   
    sleep(1);//add 1 second sleep at end of iteration
}
```
- Results shown in Grafana
![](https://imgur.com/m18hZSe.png)

## Stepped Load test 
- Results shown in Grafana
![](https://imgur.com/Gf7FyNH.png)

## Load Test
``` stages: [
        { duration: '1m', target: 40 }, // ramp up
        { duration: '5m', target: 40 }, // peak
        { duration: '1m', target: 0 }, // ramp down
    ],
    thresholds: {
        http_req_duration: ['p(99)<1500'],//Set failure treshold at 1.5s
    }, 
```
![](https://imgur.com/kwH4Hkw.png)

