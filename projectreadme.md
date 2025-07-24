
# Fruit and vegetables classification

Fruit and vegetable classification model trained to classify 36 different types of fruits and vegetables

#download yolov8
pip install untralytics 

 
#train
yolo task=classify mode=train model=yolov8n-cls.pt data=finalproject/dataset/train epochs=50 imgsz=224 

 
#validation
yolo task=classify mode=val model=runs/classify/train6/weights/best.pt data=finalproject/dataset/val 

 
#test
yolo task=classify mode=predict model=finalproject/runs/classification/train6/weights/best.pt source=finalproject/dataset/test/apple 

 
#export
yolo export model=finalproject/runs/classify/train6/weights/best.pt format=onnx 

## API Reference

#### Get all items

```http
  GET /api/items
```

| Parameter | Type     | Description                |
| :-------- | :------- | :------------------------- |
| `api_key` | `string` | **Required**. Your API key |

#### Get item

```http
  GET /api/items/${id}
```

| Parameter | Type     | Description                       |
| :-------- | :------- | :-------------------------------- |
| `id`      | `string` | **Required**. Id of item to fetch |

#### add(num1, num2)

Takes two numbers and returns the sum.


## Authors

- [@octokatherine](https://www.github.com/octokatherine)


## Roadmap

- Additional browser support

- Add more integrations

