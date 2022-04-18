## what is FLASK ?

# Flask :

Flask is a web application framework written in **Python**. ` Flask` is based on the **Werkzeug WSGI** *toolkit* and *Jinja2* temolate engine. Both are ` Pocco projects. `



![blog3.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1649999280843/IJcYA_y8e.png)


# Modules :

> There are many modules or frameworks which allow building your **webpage** using *Python* like : 


- Bottle
- Django
- Web2py
- Cherrypy
- Flask
- Etc.

But the real popular ones are ` Flask ` & ` Django `


![Blog 3.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1649999351527/jlfRKLR8Q.png)

# What to Use & Why ?

> Django is easy to use as compared to Flask but,


> **Flask** provides you the *versatility* to program with.

# - WSGI : 
`Web Server Gateway Interface [WSGI]` has been adopted as a standard for **python** *web application development*


![wsgi.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1650002014285/5YgFgQ6bT.png)

# -  Werkzueg :
 It is a WSGI toolkit, which implements requests, response objects, and other utility functions.


![werkzeug_flow_diagram.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1650002022585/eIc23u_LR.png)

 # -  jinja2 : 
`jinja2` is a popular templating engine for **python**. A web templating system combines a template with a certain data source to render *dynamic web pages*


![Workflow-of-our-TLeague-developing-and-training-See-the-text-for-detailed-explanations.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1650002031889/Fc3raA89y.png)

# Simple Flask app :


``` python
from flask import Flask

app = Flask(__name__)
@app.route('/')
def hello_world():
      return 'Hello Xs"

#main driver function 

if __name__ = '__main__':
app.run()
``` 

# Flask Workflow Chart :


![flask_workflow.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1650002847034/684JzHNyY.png)

# Workflow Automation with Python and *Flask* 

[Do it by your self here !](https://www.twilio.com/docs/sms/tutorials/workflow-automation-python-flask) 

> So that's it all about Flask and it's workflow
comment down and share this blog with your peoples too if you find this blog valuable for you.


> <p>Thanks for reading </p>

> <p> Happy Coding </p>
> <p>Have a nice day :)</p>