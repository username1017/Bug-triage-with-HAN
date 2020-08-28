# Bug-triage-with-HAN
![](https://img.shields.io/badge/python-3.6-green)
### Data sets:
* [Chromium](http://bugtriage.mybluemix.net/)
* [Mozilla Core](http://bugtriage.mybluemix.net/)
* [Mozilla Firefox](http://bugtriage.mybluemix.net/)
* [NetBeans](http://2011.msrconf.org/msr-challenge.html)
* [eclipse](http://2011.msrconf.org/msr-challenge.html)
### Usage：
**Note**: The code works with `python 3.6`, `tensorflow 1.14` and `keras 2.3.1`.
1. You need download data sets mentioned above first.
2. For ***Chromium***, ***Mozilla Core*** and ***Mozilla Firefox***, you can directly use after upziping under `data` folder.
3. For ***NetBeans*** and ***eclipse***, you need run the SQL file in ***MySQL***. Then `big_id`, `short_desc`, `assigned_to`, `bug_status` and `resolution` field in table `bugs` and `bug_id`, `bug_when` and `thetext` field in table `longdescs` are extracted in a `json` format. Note that the format of `bug_when` field is set to a sortable style like `yymmdd 00-00-00`. After that you can put the file under `data` folder.
4. Run `HAN-XXX.ipynb` file in ***Jupyter Notebook***.
5. ***GloVe*** word vectors need to be trained separately, cleck [here](https://github.com/stanfordnlp/GloVe) for concrete manner.
