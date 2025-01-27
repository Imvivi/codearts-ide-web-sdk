# @huawei-ide/codearts
用于集成CodeArts IDE Web

## 如何使用

1. 安装 @huawei-ide/codearts  
   `npm install @huawei-ide/codearts`

2. 引入 @huawei-ide/codearts  
   `const ide = require('@huawei-ide/codearts');`

3. 预加载IDE, 返回Promise：     
   `await ide.preload();`

4. 展示IDE  
   其中id参数为挂载节点id, 返回Promise：
   `ide.show(id: string, {width：string,height: string}).then(() => {});`

5. 打开文件，默认可编辑    
   参数content为文件内容，类型为string，path是工程内文件的唯一路径，例如'src', 'src/tool', name为带后缀的文件名：
   ```
   ide.openFile({
        content: '## ReadME',
        path:'src',
        name: 'README.md'
    });
   ```

6. 设置文件是否为预览(只读)状态    
   `ide.setPreview(preview: boolean)`  
   
7. 获取当前文件最新内容，返回Promise：  
   `await ide.getContent();`

8. 设置Token：  
   `ide.setToken();`   
   
9.  销毁IDE     
   `ide.dispose();`
