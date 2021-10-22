
[Overview of main packages](https://github.com/otosense/omisc/wiki/Overview-of-main-tools)

[Our dev packages](https://github.com/otosense/omisc/wiki/Our-dev-packages)


# Package uses

![image](https://user-images.githubusercontent.com/1906276/138504761-3dd4c916-d74d-42d8-b250-6d6c33172472.png)





# Appendix

## Code for package-uses graph

```python
from qo import dgdisp

dgdisp("""
embody, slink, hum -> forged
slink, embody -> hum

embody [label="--embody--\ntemplated trees gen" shape="box"]
slink [label="--slink--\nlinked sequences gen" shape="box"]
hum [label="--hum--\naudio gen" shape="box"]
forged [label="--forged--\ngenerate test data" shape="box"]

embody -> verb
verb [label="--verb--\nmake mini-languages" shape="box"]

verb -> handle_user_inputs, lang_binding
handle_user_inputs [label="safely handle\ncomplex user inputs" shape="oval"]
lang_binding [label="language binders" shape="oval"]

forged -> test_code
test_code [label="Test code on\nrealistic data" shape="oval"]

""")
```
