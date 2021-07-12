---
description: o Shell de Windows fornece um conjunto poderoso de objetos de automação que permitem que você programe o Shell com o microsoft Visual Basic e linguagens de script, como o microsoft JScript (compatível com a especificação de linguagem ECMA 262) e o microsoft Visual Basic scripting Edition (VBScript). Você pode usar esses objetos para acessar muitos dos recursos e caixas de diálogo do Shell. Por exemplo, você pode acessar o sistema de arquivos, iniciar programas e alterar as configurações do sistema.
title: Objetos shell programáveis
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 09455fad-a769-42ef-83ba-b745ac819bf3
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: e8685b44d00d3f48e8de2a567218ef08c1cb5070
ms.sourcegitcommit: 822413efb4a70dd464e5db4d9e8693ef74f8132f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/09/2021
ms.locfileid: "113581774"
---
# <a name="scriptable-shell-objects"></a>Objetos shell programáveis

o Shell de Windows fornece um conjunto poderoso de objetos de automação que permitem que você programe o Shell com o microsoft Visual Basic e linguagens de script, como o microsoft JScript (compatível com a especificação de linguagem ECMA 262) e o microsoft Visual Basic scripting Edition (VBScript). Você pode usar esses objetos para acessar muitos dos recursos e caixas de diálogo do Shell. Por exemplo, você pode acessar o sistema de arquivos, iniciar programas e alterar as configurações do sistema.

Esta seção apresenta os objetos shell programáveis.

-   [Versões do Shell](#shell-versions)
-   [Instanciando objetos do Shell](#instantiating-shell-objects)
    -   [Associação tardia](#late-binding)
    -   [Elemento de objeto HTML](#html-object-element)
-   [Objeto Shell](#shell-object)
    -   [Segurança](#security)
-   [Objetos de pasta](#folder-objects)

## <a name="shell-versions"></a>Versões do Shell

Muitos dos objetos shell foram disponibilizados na [versão 4,71](versions.md) do Shell. Outras estão disponíveis na versão 5, 0 e posterior. a versão 5, 0 tornou-se disponível com o Windows 2000. A tabela a seguir lista cada objeto Shell na versão do Shell em que o objeto ficou disponível.



| Versão 4,71                                            | Versão 5, 0                                          |
|---------------------------------------------------------|-------------------------------------------------------|
| [**Pasta**](folder.md)                                | [**DIDiskQuotaUser**](didiskquotauser-object.md)     |
| [**FolderItemVerb**](folderitemverb.md)                | [**DiskQuotaControl**](diskquotacontrol-object.md)   |
| [**FolderItemVerbs**](folderitemverbs.md)              | [**Pasta2**](folder2-object.md)                     |
| [**Shell**](shell.md)                                  | [**FolderItem**](folderitem.md)                      |
| [**ShellFolderView**](shellfolderview.md)              | [**FolderItems**](folderitems.md)                    |
| [**ShellUIHelper**](shelluihelper.md)                  | [**FolderItems2**](folderitems2-object.md)           |
| [**ShellWindows**](shellwindows.md)                    | [**IShellDispatch2**](ishelldispatch2-object.md)     |
| [**WebViewFolderContents**](../lwef/webviewfoldercontents.md) | [**IShellLinkDual2**](ishelllinkdual2-object.md)     |
|                                                         | [**ShellFolderItem**](shellfolderitem-object.md)     |
|                                                         | [**ShellFolderViewOC**](shellfolderviewoc-object.md) |
|                                                         | [**ShellLinkObject**](shelllinkobject-object.md)     |



 

## <a name="instantiating-shell-objects"></a>Instanciando objetos do Shell

para instanciar os objetos do Shell em aplicativos Visual Basic com associação inicial, adicione referências às seguintes bibliotecas em seu projeto:

-   Microsoft Internet Controls (SHDocVw)
-   Microsoft Shell Controls and Automation (shell32)

### <a name="late-binding"></a>Associação tardia

Você também pode criar uma instância de muitos dos objetos do shell com associação tardia. essa abordagem funciona em Visual Basic aplicativos e no script. O exemplo a seguir mostra como criar uma instância do objeto [**shell**](shell.md) no JScript.


```
<SCRIPT LANGUAGE="JScript">
<!--
    function fnCreateShell()    
    {
        // Instantiate the Shell object and invoke its FileRun method.
        var oShell = new ActiveXObject("shell.application");
        oshell.FileRun;
    }
-->
</SCRIPT>
```



O exemplo a seguir mostra como criar uma instância do objeto de [**pasta**](folder.md) no VBScript.


```
<SCRIPT LANGUAGE="VBScript">
<!--
    function fnCreateFolder()
        dim oShell    
        dim oFolder
        dim sDir

        sDir = "C:\SomePath" 
        set oShell = CreateObject("shell.application")
        set oFolder = oShell.NameSpace(sDir)  
    end function
-->  
</SCRIPT>
```



No exemplo anterior, *sDir* é o caminho para o objeto [**Folder**](folder.md) . Observe que os valores de enumeração [**ShellSpecialFolderConstants**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) não estão disponíveis no script.

O ProgID de cada um dos objetos do Shell é mostrado na tabela a seguir.



| Objeto                                                  | ProgID                                                                                  |
|---------------------------------------------------------|-----------------------------------------------------------------------------------------|
| [**DIDiskQuotaUser**](didiskquotauser-object.md)       | Microsoft. DiskQuota. 1                                                                   |
| [**DiskQuotaControl**](diskquotacontrol-object.md)     | Não é possível associar tardiamente                                                                        |
| [**Pasta**](folder.md)                                | Shell. Shell \_ Application. Namespace ("...")                                               |
| [**Pasta2**](folder2-object.md)                       | Shell. Shell \_ Application. Namespace ("...")                                               |
| [**FolderItem**](folderitem.md)                        | Shell. Shell \_ Application. Namespace ("..."). Self ou Folder. Items. itens ou pasta. ParseName |
| [**FolderItems**](folderitems.md)                      | Pasta. itens                                                                            |
| [**FolderItems2**](folderitems2-object.md)             | Pasta. itens                                                                            |
| [**FolderItemVerb**](folderitemverb.md)                | Shell. NameSpace ("..."). Auto. Verbs. Item ()                                                |
| [**FolderItemVerbs**](folderitemverbs.md)              | FolderItem. Verbs ou Shell. NameSpace ("..."). Verbos Self.                                   |
| [**IShellDispatch2**](ishelldispatch2-object.md)       | Shell. Aplicativo de shell \_                                                                |
| [**IShellLinkDual2**](ishelllinkdual2-object.md)       | Shell. NameSpace ("..."). Self. GetLink ou Shell. NameSpace ("..."). Itens (). GetLink           |
| [**Shell**](shell.md)                                  | Shell. Aplicativo de shell \_                                                                |
| [**ShellFolderItem**](shellfolderitem-object.md)       | Shell. NameSpace ("..."). Self ou Shell. NameSpace ("..."). Itens ()                           |
| [**ShellFolderView**](shellfolderview.md)              | Não é possível associar tardiamente                                                                        |
| [**ShellFolderViewOC**](shellfolderviewoc-object.md)   | Não é possível associar tardiamente                                                                        |
| [**ShellLinkObject**](shelllinkobject-object.md)       | Shell. NameSpace ("..."). Self. GetLink ou Shell. NameSpace ("..."). Itens (). GetLink           |
| [**ShellUIHelper**](shelluihelper.md)                  | Não é possível associar tardiamente                                                                        |
| [**ShellWindows**](shellwindows.md)                    | Shell. Shell \_ Windows ou ShellWindows. \_ NewEnum                                          |
| [**WebViewFolderContents**](../lwef/webviewfoldercontents.md) | Não é possível associar tardiamente                                                                        |



 

### <a name="html-object-element"></a>Elemento de objeto HTML

Você também pode usar o elemento [**Object**](https://msdn.microsoft.com/library/ms535859(v=VS.85).aspx) para instanciar objetos do Shell em uma página HTML. Para fazer isso, defina o atributo de **ID** do elemento de **objeto** como o nome da variável que você usará em seus scripts e identifique o objeto usando seu número registrado (ClassID). O HTML a seguir cria uma instância do objeto [**ShellFolderItem**](shellfolderitem-object.md) usando o elemento **Object** .


```
<OBJECT ID="oShFolderItem" 
    NAME="Shell Folder Item Object"
    CLASSID="clsid:2fe352ea-fd1f-11d2-b1f4-00c04f8eeb3e">
</OBJECT>
```



A tabela a seguir lista cada objeto Shell e seu respectivo ClassID.



| Objeto Shell                                           | CLASSID                              |
|--------------------------------------------------------|--------------------------------------|
| [**DIDiskQuotaUser**](didiskquotauser-object.md)       | 7988B571-EC89-11cf-9C00-00AA00A14F56 |
| [**DiskQuotaControl**](diskquotacontrol-object.md)     | 7988B571-EC89-11cf-9C00-00AA00A14F56 |
| [**Pasta**](folder.md)                                | BBCBDE60-C3FF-11CE-8350-444553540000 |
| [**Pasta2**](folder2-object.md)                       | f0d2d8ef-3890-11d2-bf8b-00c04fb93661 |
| [**FolderItem**](folderitem.md)                        | 744129E0-CBE5-11CE-8350-444553540000 |
| [**FolderItems**](folderitems.md)                      | 744129E0-CBE5-11CE-8350-444553540000 |
| [**FolderItems2**](folderitems2-object.md)             | C94F0AD0-F363-11d2-A327-00C04F8EEC7F |
| [**FolderItemVerb**](folderitemverb.md)                | 08EC3E00-50B0-11CF-960C-0080C7F4EE85 |
| [**FolderItemVerbs**](folderitemverbs.md)              | 1F8352C0-50B0-11CF-960C-0080C7F4EE85 |
| [**IShellDispatch2**](ishelldispatch2-object.md)       | A4C6892C-3BA9-11d2-9DEA-00C04FB16162 |
| [**IShellLinkDual2**](ishelllinkdual2-object.md)       | 317EE249-F12E-11d2-B1E4-00C04F8EEB3E |
| [**Shell**](shell.md)                                  | 13709620-C279-11CE-A49E-444553540000 |
| [**ShellFolderItem**](shellfolderitem-object.md)       | 2fe352ea-fd1f-11d2-b1f4-00c04f8eeb3e |
| [**ShellFolderView**](shellfolderview.md)              | 62112AA1-EBE4-11cf-A5FB-0020AFE7292D |
| [**ShellFolderViewOC**](shellfolderviewoc-object.md)   | 4a3df050-23bd-11d2-939f-00a0c91eedba |
| [**ShellLinkObject**](shelllinkobject-object.md)       | 11219420-1768-11d1-95BE-00609797EA4F |
| [**ShellUIHelper**](shelluihelper.md)                  | 64AB4BB7-111E-11D1-8F79-00C04FC2FBE1 |
| [**ShellWindows**](shellwindows.md)                    | 9BA05972-F6A8-11CF-A442-00A0C90A8F39 |
| [**WebViewFolderContents**](../lwef/webviewfoldercontents.md) | 1820FED0-473E-11D0-A96C-00C04FD705A2 |



 

## <a name="shell-object"></a>Objeto Shell

O objeto [**shell**](shell.md) representa os objetos no Shell. Você pode usar os métodos expostos pelo objeto Shell para:

-   Abra, explore e procure pastas.
-   Minimizar, restaurar, colocar em cascata ou janelas abertas.
-   Inicie aplicativos do painel de controle.
-   Exibir caixas de diálogo do sistema.

Os usuários talvez estejam mais familiarizados com os comandos que acessam no menu **Iniciar** e no menu de atalho da barra de tarefas. O menu de atalho da barra de tarefas aparece quando os usuários clicam com o botão direito na barra de tarefas. O HTA (aplicativo HTML) a seguir produz uma página inicial com botões que implementam muitos dos métodos do objeto [**shell**](shell.md) . Alguns desses métodos implementam recursos no menu **Iniciar** e no menu de atalho da barra de tarefas.


```
<HTML>
<HEAD>
    <TITLE>Start Page</TITLE>
    
    <OBJECT ID="oShell"
        CLASSID="clsid:13709620-C279-11CE-A49E-444553540000">
    </OBJECT>
    
    <STYLE>
        INPUT {width: 200} 
    </STYLE>  
    
    <SCRIPT LANGUAGE="VBScript">
    <!--
        function fnStart(sMethod)
            select case sMethod
              case 0    
                  'Minimizes all windows on the desktop
                oshell.Shell_MinimizeAll
              case 1  
                  'Displays the Run dialog box
                oshell.FileRun
              case 2  
                  'Displays the Shut Down Windows dialog box
                oshell.Shell_ShutdownWindows
              case 3  
                  'Displays the Find dialog box
                oshell.Shell_FindFilesr
              case 4  
                  'Displays the Date/Time dialog box
                oshell.Shell_SetTime 
              case 5  
                  'Displays the Internet Properties dialog box
                oshell.Shell_ControlPanelItem "INETCPL.cpl"
              case 6  
                  'Explores the My Documents folder
                oshell.Shell_Explore "C:\My Documents"
              case 7  
                  'Enables user to select folder from Program Files
                oshell.Shell_BrowseForFolder 0, "My Programs", 0, "C:\Program Files" 
              case 8  
                  'Opens the Favorites folder
                oshell.Shell_Open "C:\WINDOWS\Favorites"
              case 9  
                  'Displays the Taskbar Properties dialog box
                oshell.Shell_TrayProperties
            end select  
        end function      
    -->
    </SCRIPT>
</HEAD>

<BODY>
    <H1>Start...</H1>
    <INPUT type="button" value="Edit Taskbar Properties" onclick="fnStart(9)"><br>
    <INPUT type="button" value="Open Favorites Folder" onclick="fnStart(8)"><br>
    <INPUT type="button" value="Browse Program Files" onclick="fnStart(7)"><br>
    <INPUT type="button" value="Explore My Documents" onclick="fnStart(6)"><br>
    <INPUT type="button" value="Modify Internet Properties" onclick="fnStart(5)"><br>
    <INPUT type="button" value="Set System Time" onclick="fnStart(4)"><br>
    <INPUT type="button" value="Find a File or Folder" onclick="fnStart(3)"><br>
    <INPUT type="button" value="Shut Down Windows" onclick="fnStart(2)"><br>
    <INPUT type="button" value="Run" onclick="fnStart(1)">     
    <INPUT type="button" value="Minimize All Windows" onclick="fnStart(0)">     
</BODY>
</HTML>
```



### <a name="security"></a>Segurança

Como um aplicativo, um HTA é executado em um modelo de segurança diferente de uma página da Web. para interagir com uma página da web que implementa a funcionalidade dos objetos do Shell, os usuários devem habilitar os **controles de ActiveX de inicialização e script não marcados como seguros** para a zona de segurança na qual estão exibindo a página.

## <a name="folder-objects"></a>Objetos de pasta

O objeto [**Folder**](folder.md) representa uma pasta Shell. Você pode usar os métodos expostos pelo objeto Folder para:

-   Obter informações sobre uma pasta.
-   Criar subpastas.
-   Copie e mova objetos de arquivo para a pasta.

O objeto [**FolderItem**](folderitem.md) representa um item em uma pasta do Shell. Suas propriedades permitem que você recupere informações sobre o item. Você pode usar os métodos expostos por esse objeto para executar os verbos de um item ou para recuperar informações sobre o objeto [**FolderItemVerbs**](folderitemverbs.md) de um item.

O objeto [**FolderItems**](folderitems.md) representa uma coleção de itens em uma pasta do Shell. Seus métodos e propriedades permitem que você recupere informações sobre a coleção.

o exemplo a seguir Visual Basic mostra a relação entre vários objetos de pasta e como eles podem ser usados juntos. Quando o usuário clica no botão de comando chamado **cmdGetPath**, o programa exibe uma caixa de diálogo que permite ao usuário selecionar uma pasta de **meu computador**, em que ssfDRIVES é o valor de enumeração [**ShellSpecialFolderConstants**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) para **meu computador**. Quando o usuário escolhe uma pasta, o caminho da pasta é exibido na caixa de texto chamada **txtPath**.


```
Private Sub cmdGetPath_Click()
    Dim oShell As New Shell
    Dim oFolder As Folder
    Dim oFolderItem As FolderItem
 
    Set oFolder = oshell.Shell_BrowseForFolder(Me.hWnd, "Select a Folder", 0, ssfDrives)
   
    Set oFolderItem = oFolderItems.Item

    txtPath.Text = oFolderItem.Path
End Sub
```



No VBScript, essa função é ligeiramente diferente porque os valores de enumeração [**ShellSpecialFolderConstants**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) não estão disponíveis no script. O exemplo a seguir mostra o VBScript equivalente do exemplo anterior.


```
<SCRIPT LANGUAGE="VBScript">
<!--
    function fnGetMyPathVB() 
        dim oShell
        dim oFolder
        dim oFolderItem
        
        set oShell = CreateObject("shell.application")      
        set oFolder = oshell.Shell_BrowseForFolder(0, "Choose a Folder", 0)             
        set oFolderItem = oFolder.Items.Item         
        
        document.all.item("myPath").innerText = oFolderItem.Path                                
    end function
-->
</SCRIPT>
```



no exemplo a seguir JScript, que é uma tradução direta do exemplo anterior do VBScript, observe como os parênteses vazios ' () ' são usados para invocar os [**itens**](folder-items.md) e os métodos de [**Item**](folderitems-item.md) .


```
<SCRIPT LANGUAGE="JavaScript">
<!--
    function fnGetMyPathJ() 
    {       
        var oShell = new ActiveXObject("shell.application");
                    
        var oFolder = new Object;                   
        oFolder = oshell.Shell_BrowseForFolder(0, "Choose a folder", 0);
                                
        var oFolderItem = new Object;       
        oFolderItem = oFolder.Items().Item();                               
        
        document.all.item("myPath").innerText = oFolderItem.Path;
    }    
-->
</SCRIPT>
```



 

 
