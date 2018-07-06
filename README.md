# magento2-module-stockpush

This idea came up to me and seemed quite interesting to me, it's 100% educational and will help me study for Magento Certification this summer. 
It would be really cool, however, if this ends up becoming 'production ready'. We'll see :).

## Scenario
- Lots of stock changes
- A lot of traffic
- Page cache shouldn't be cleared based on stock changes

## Ideas
- Let stock be loaded using JS components.
- JS components communicate with Magento through a standalone websocket.
- Websocket subscribes to a Redis instance to receive stock update events from Magento.
- JS components can request websocket for stock as well.

## Difficulties
- Disable cache busting on inventory changes.
- Replace stock labels with JS components on front-end.
- Persist socket connection, this would probably go with a service/web worker.
