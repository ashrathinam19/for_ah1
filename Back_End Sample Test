import requests
from urllib.error import HTTPError

url = "https://digisaving.com/api"
query = {"userId" : "1"}
# obj = urllib.request.urlopen(url).getcode()
obj = requests.get(url, params=query)
def get_response():
    # response = urllib.request.urlopen(url).getcode()
    try:
        response = obj.status_code
        if(response == 200):
            print("Test case pass  and executing next test case")
            data_validation(obj)
        else:
            print(" This test case failed with" , response , "response code")
    except HTTPError as e:
            print(" This test case failed "+ str(type(e))+" with message " +e.message)


def data_validation(var):
    data = var.json()
    if (data['stamp_saved']== 1):
        print("test case pass")
    else:
        print("Test case is failed")



if __name__ == "__main__":
    get_response()
