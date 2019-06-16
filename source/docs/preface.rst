使用说明
========

一、文档撰写前提
~~~~~~~~~~~~~~~~

.. note:: 环境部署::  

  > git clone https://gitee.com/zhyantao/readthedocs.git
  > pip install sphinx recommonmark sphinx-autobuild sphinx_rtd_theme -i http://mirrors.aliyun.com/pypi/simple/ --trusted-host=mirrors.aliyun.com

二、撰写博文并发表
~~~~~~~~~~~~~~~~~~~~~~

1. 把你要发表的博文放在 *demo-readthedocs/source/docs* 文件夹中
2. CMD中输入 ``make html`` 回车，打开 *build/html/index.html* 预览效果
3. 提交代码（博文）到 Github 仓库 [`git简易指南 <http://www.bootcss.com/p/git-guide/>`__\ ]
4. 在 `Read the Docs <https://readthedocs.org/>`__\ 中导入 Github 项目
5. 导入成功后，点击 View the documentation 查看最终效果 [`示例 <https://demo-read-the-docs.readthedocs.io/>`__\ ]

.. warning:: 除了 *demo-readthedocs/source/docs* 下的文件和 *source/index.rst* 可以修改外，其他位置的文件不要修改，否则可能会引起错误。另外，**务必在 source/index.rst 文件中添加你的博文的路径**
