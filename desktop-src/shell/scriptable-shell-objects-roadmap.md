---
description: O Shell do Windows fornece um conjunto poderoso de objetos de automação que permitem que você programe o shell com o Microsoft Visual Basic e linguagens de script, como o Microsoft JScript (compatível com a especificação de linguagem ECMA 262) e o Microsoft Visual Basic Scripting Edition (VBScript). Você pode usar esses objetos para acessar muitos dos recursos e caixas de diálogo do Shell. Por exemplo, você pode acessar o sistema de arquivos, iniciar programas e alterar as configurações do sistema.
title: Objetos shell programáveis
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 09455fad-a769-42ef-83ba-b745ac819bf3
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 4c39e7e58a9715598056fb74aa154ed8a850f523
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104968129"
---
# <a name="scriptable-shell-objects"></a><span data-ttu-id="c6121-105">Objetos shell programáveis</span><span class="sxs-lookup"><span data-stu-id="c6121-105">Scriptable Shell Objects</span></span>

<span data-ttu-id="c6121-106">O Shell do Windows fornece um conjunto poderoso de objetos de automação que permitem que você programe o shell com o Microsoft Visual Basic e linguagens de script, como o Microsoft JScript (compatível com a especificação de linguagem ECMA 262) e o Microsoft Visual Basic Scripting Edition (VBScript).</span><span class="sxs-lookup"><span data-stu-id="c6121-106">The Windows Shell provides a powerful set of automation objects that enable you to program the Shell with Microsoft Visual Basic and scripting languages such as Microsoft JScript (compatible with ECMA 262 language specification) and Microsoft Visual Basic Scripting Edition (VBScript).</span></span> <span data-ttu-id="c6121-107">Você pode usar esses objetos para acessar muitos dos recursos e caixas de diálogo do Shell.</span><span class="sxs-lookup"><span data-stu-id="c6121-107">You can use these objects to access many of the Shell's features and dialog boxes.</span></span> <span data-ttu-id="c6121-108">Por exemplo, você pode acessar o sistema de arquivos, iniciar programas e alterar as configurações do sistema.</span><span class="sxs-lookup"><span data-stu-id="c6121-108">For example, you can access the file system, launch programs, and change system settings.</span></span>

<span data-ttu-id="c6121-109">Esta seção apresenta os objetos shell programáveis.</span><span class="sxs-lookup"><span data-stu-id="c6121-109">This section introduces the scriptable Shell objects.</span></span>

-   [<span data-ttu-id="c6121-110">Versões do Shell</span><span class="sxs-lookup"><span data-stu-id="c6121-110">Shell Versions</span></span>](#shell-versions)
-   [<span data-ttu-id="c6121-111">Instanciando objetos do Shell</span><span class="sxs-lookup"><span data-stu-id="c6121-111">Instantiating Shell Objects</span></span>](#instantiating-shell-objects)
    -   [<span data-ttu-id="c6121-112">Associação tardia</span><span class="sxs-lookup"><span data-stu-id="c6121-112">Late Binding</span></span>](#late-binding)
    -   [<span data-ttu-id="c6121-113">Elemento de objeto HTML</span><span class="sxs-lookup"><span data-stu-id="c6121-113">HTML OBJECT Element</span></span>](#html-object-element)
-   [<span data-ttu-id="c6121-114">Objeto Shell</span><span class="sxs-lookup"><span data-stu-id="c6121-114">Shell Object</span></span>](#shell-object)
    -   [<span data-ttu-id="c6121-115">Segurança</span><span class="sxs-lookup"><span data-stu-id="c6121-115">Security</span></span>](#security)
-   [<span data-ttu-id="c6121-116">Objetos de pasta</span><span class="sxs-lookup"><span data-stu-id="c6121-116">Folder Objects</span></span>](#folder-objects)

## <a name="shell-versions"></a><span data-ttu-id="c6121-117">Versões do Shell</span><span class="sxs-lookup"><span data-stu-id="c6121-117">Shell Versions</span></span>

<span data-ttu-id="c6121-118">Muitos dos objetos shell foram disponibilizados na [versão 4,71](versions.md) do Shell.</span><span class="sxs-lookup"><span data-stu-id="c6121-118">Many of the Shell objects became available in [version 4.71](versions.md) of the Shell.</span></span> <span data-ttu-id="c6121-119">Outras estão disponíveis na versão 5, 0 e posterior.</span><span class="sxs-lookup"><span data-stu-id="c6121-119">Others are available in version 5.00 and later.</span></span> <span data-ttu-id="c6121-120">A versão 5, 0 tornou-se disponível com o Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="c6121-120">Version 5.00 became available with Windows 2000.</span></span> <span data-ttu-id="c6121-121">A tabela a seguir lista cada objeto Shell na versão do Shell em que o objeto ficou disponível.</span><span class="sxs-lookup"><span data-stu-id="c6121-121">The following table lists each Shell object under the version of the Shell in which the object became available.</span></span>



| <span data-ttu-id="c6121-122">Versão 4,71</span><span class="sxs-lookup"><span data-stu-id="c6121-122">Version 4.71</span></span>                                            | <span data-ttu-id="c6121-123">Versão 5, 0</span><span class="sxs-lookup"><span data-stu-id="c6121-123">Version 5.00</span></span>                                          |
|---------------------------------------------------------|-------------------------------------------------------|
| [<span data-ttu-id="c6121-124">**Pasta**</span><span class="sxs-lookup"><span data-stu-id="c6121-124">**Folder**</span></span>](folder.md)                                | [<span data-ttu-id="c6121-125">**DIDiskQuotaUser**</span><span class="sxs-lookup"><span data-stu-id="c6121-125">**DIDiskQuotaUser**</span></span>](didiskquotauser-object.md)     |
| [<span data-ttu-id="c6121-126">**FolderItemVerb**</span><span class="sxs-lookup"><span data-stu-id="c6121-126">**FolderItemVerb**</span></span>](folderitemverb.md)                | [<span data-ttu-id="c6121-127">**DiskQuotaControl**</span><span class="sxs-lookup"><span data-stu-id="c6121-127">**DiskQuotaControl**</span></span>](diskquotacontrol-object.md)   |
| [<span data-ttu-id="c6121-128">**FolderItemVerbs**</span><span class="sxs-lookup"><span data-stu-id="c6121-128">**FolderItemVerbs**</span></span>](folderitemverbs.md)              | [<span data-ttu-id="c6121-129">**Pasta2**</span><span class="sxs-lookup"><span data-stu-id="c6121-129">**Folder2**</span></span>](folder2-object.md)                     |
| [<span data-ttu-id="c6121-130">**Shell**</span><span class="sxs-lookup"><span data-stu-id="c6121-130">**Shell**</span></span>](shell.md)                                  | [<span data-ttu-id="c6121-131">**FolderItem**</span><span class="sxs-lookup"><span data-stu-id="c6121-131">**FolderItem**</span></span>](folderitem.md)                      |
| [<span data-ttu-id="c6121-132">**ShellFolderView**</span><span class="sxs-lookup"><span data-stu-id="c6121-132">**ShellFolderView**</span></span>](shellfolderview.md)              | [<span data-ttu-id="c6121-133">**FolderItems**</span><span class="sxs-lookup"><span data-stu-id="c6121-133">**FolderItems**</span></span>](folderitems.md)                    |
| [<span data-ttu-id="c6121-134">**ShellUIHelper**</span><span class="sxs-lookup"><span data-stu-id="c6121-134">**ShellUIHelper**</span></span>](shelluihelper.md)                  | [<span data-ttu-id="c6121-135">**FolderItems2**</span><span class="sxs-lookup"><span data-stu-id="c6121-135">**FolderItems2**</span></span>](folderitems2-object.md)           |
| [<span data-ttu-id="c6121-136">**ShellWindows**</span><span class="sxs-lookup"><span data-stu-id="c6121-136">**ShellWindows**</span></span>](shellwindows.md)                    | [<span data-ttu-id="c6121-137">**IShellDispatch2**</span><span class="sxs-lookup"><span data-stu-id="c6121-137">**IShellDispatch2**</span></span>](ishelldispatch2-object.md)     |
| [<span data-ttu-id="c6121-138">**WebViewFolderContents**</span><span class="sxs-lookup"><span data-stu-id="c6121-138">**WebViewFolderContents**</span></span>](../lwef/webviewfoldercontents.md) | [<span data-ttu-id="c6121-139">**IShellLinkDual2**</span><span class="sxs-lookup"><span data-stu-id="c6121-139">**IShellLinkDual2**</span></span>](ishelllinkdual2-object.md)     |
|                                                         | [<span data-ttu-id="c6121-140">**ShellFolderItem**</span><span class="sxs-lookup"><span data-stu-id="c6121-140">**ShellFolderItem**</span></span>](shellfolderitem-object.md)     |
|                                                         | [<span data-ttu-id="c6121-141">**ShellFolderViewOC**</span><span class="sxs-lookup"><span data-stu-id="c6121-141">**ShellFolderViewOC**</span></span>](shellfolderviewoc-object.md) |
|                                                         | [<span data-ttu-id="c6121-142">**ShellLinkObject**</span><span class="sxs-lookup"><span data-stu-id="c6121-142">**ShellLinkObject**</span></span>](shelllinkobject-object.md)     |



 

## <a name="instantiating-shell-objects"></a><span data-ttu-id="c6121-143">Instanciando objetos do Shell</span><span class="sxs-lookup"><span data-stu-id="c6121-143">Instantiating Shell Objects</span></span>

<span data-ttu-id="c6121-144">Para instanciar os objetos do Shell em aplicativos Visual Basic com associação inicial, adicione referências às seguintes bibliotecas em seu projeto:</span><span class="sxs-lookup"><span data-stu-id="c6121-144">To instantiate the Shell objects in Visual Basic applications with early binding, add references to the following libraries in your project:</span></span>

-   <span data-ttu-id="c6121-145">Microsoft Internet Controls (SHDocVw)</span><span class="sxs-lookup"><span data-stu-id="c6121-145">Microsoft Internet Controls (SHDocVw)</span></span>
-   <span data-ttu-id="c6121-146">Microsoft Shell Controls and Automation (shell32)</span><span class="sxs-lookup"><span data-stu-id="c6121-146">Microsoft Shell Controls and Automation (Shell32)</span></span>

### <a name="late-binding"></a><span data-ttu-id="c6121-147">Associação tardia</span><span class="sxs-lookup"><span data-stu-id="c6121-147">Late Binding</span></span>

<span data-ttu-id="c6121-148">Você também pode criar uma instância de muitos dos objetos do shell com associação tardia.</span><span class="sxs-lookup"><span data-stu-id="c6121-148">You can also instantiate many of the Shell objects with late binding.</span></span> <span data-ttu-id="c6121-149">Essa abordagem funciona em Visual Basic aplicativos e no script.</span><span class="sxs-lookup"><span data-stu-id="c6121-149">This approach works in Visual Basic applications and in script.</span></span> <span data-ttu-id="c6121-150">O exemplo a seguir mostra como criar uma instância do objeto [**shell**](shell.md) no JScript.</span><span class="sxs-lookup"><span data-stu-id="c6121-150">The following example shows how to instantiate the [**Shell**](shell.md) object in JScript.</span></span>


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



<span data-ttu-id="c6121-151">O exemplo a seguir mostra como criar uma instância do objeto de [**pasta**](folder.md) no VBScript.</span><span class="sxs-lookup"><span data-stu-id="c6121-151">The following example shows how to instantiate the [**Folder**](folder.md) object in VBScript.</span></span>


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



<span data-ttu-id="c6121-152">No exemplo anterior, *sDir* é o caminho para o objeto [**Folder**](folder.md) .</span><span class="sxs-lookup"><span data-stu-id="c6121-152">In the preceding example, *sDir* is the path to the [**Folder**](folder.md) object.</span></span> <span data-ttu-id="c6121-153">Observe que os valores de enumeração [**ShellSpecialFolderConstants**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) não estão disponíveis no script.</span><span class="sxs-lookup"><span data-stu-id="c6121-153">Note that the [**ShellSpecialFolderConstants**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) enumeration values are not available in script.</span></span>

<span data-ttu-id="c6121-154">O ProgID de cada um dos objetos do Shell é mostrado na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="c6121-154">The ProgID for each of the Shell objects is shown in the following table.</span></span>



| <span data-ttu-id="c6121-155">Objeto</span><span class="sxs-lookup"><span data-stu-id="c6121-155">Object</span></span>                                                  | <span data-ttu-id="c6121-156">ProgID</span><span class="sxs-lookup"><span data-stu-id="c6121-156">ProgID</span></span>                                                                                  |
|---------------------------------------------------------|-----------------------------------------------------------------------------------------|
| [<span data-ttu-id="c6121-157">**DIDiskQuotaUser**</span><span class="sxs-lookup"><span data-stu-id="c6121-157">**DIDiskQuotaUser**</span></span>](didiskquotauser-object.md)       | <span data-ttu-id="c6121-158">Microsoft. DiskQuota. 1</span><span class="sxs-lookup"><span data-stu-id="c6121-158">Microsoft.DiskQuota.1</span></span>                                                                   |
| [<span data-ttu-id="c6121-159">**DiskQuotaControl**</span><span class="sxs-lookup"><span data-stu-id="c6121-159">**DiskQuotaControl**</span></span>](diskquotacontrol-object.md)     | <span data-ttu-id="c6121-160">Não é possível associar tardiamente</span><span class="sxs-lookup"><span data-stu-id="c6121-160">Cannot late bind</span></span>                                                                        |
| [<span data-ttu-id="c6121-161">**Pasta**</span><span class="sxs-lookup"><span data-stu-id="c6121-161">**Folder**</span></span>](folder.md)                                | <span data-ttu-id="c6121-162">Shell. Shell \_ Application. Namespace ("...")</span><span class="sxs-lookup"><span data-stu-id="c6121-162">shell.Shell\_Application.NameSpace("...")</span></span>                                               |
| [<span data-ttu-id="c6121-163">**Pasta2**</span><span class="sxs-lookup"><span data-stu-id="c6121-163">**Folder2**</span></span>](folder2-object.md)                       | <span data-ttu-id="c6121-164">Shell. Shell \_ Application. Namespace ("...")</span><span class="sxs-lookup"><span data-stu-id="c6121-164">shell.Shell\_Application.NameSpace("...")</span></span>                                               |
| [<span data-ttu-id="c6121-165">**FolderItem**</span><span class="sxs-lookup"><span data-stu-id="c6121-165">**FolderItem**</span></span>](folderitem.md)                        | <span data-ttu-id="c6121-166">Shell. Shell \_ Application. Namespace ("..."). Self ou Folder. Items. itens ou pasta. ParseName</span><span class="sxs-lookup"><span data-stu-id="c6121-166">shell.Shell\_Application.NameSpace("...").Self or Folder.Items.Item or Folder.ParseName</span></span> |
| [<span data-ttu-id="c6121-167">**FolderItems**</span><span class="sxs-lookup"><span data-stu-id="c6121-167">**FolderItems**</span></span>](folderitems.md)                      | <span data-ttu-id="c6121-168">Pasta. itens</span><span class="sxs-lookup"><span data-stu-id="c6121-168">Folder.Items</span></span>                                                                            |
| [<span data-ttu-id="c6121-169">**FolderItems2**</span><span class="sxs-lookup"><span data-stu-id="c6121-169">**FolderItems2**</span></span>](folderitems2-object.md)             | <span data-ttu-id="c6121-170">Pasta. itens</span><span class="sxs-lookup"><span data-stu-id="c6121-170">Folder.Items</span></span>                                                                            |
| [<span data-ttu-id="c6121-171">**FolderItemVerb**</span><span class="sxs-lookup"><span data-stu-id="c6121-171">**FolderItemVerb**</span></span>](folderitemverb.md)                | <span data-ttu-id="c6121-172">Shell. NameSpace ("..."). Auto. Verbs. Item ()</span><span class="sxs-lookup"><span data-stu-id="c6121-172">Shell.NameSpace("...").Self.Verbs.Item()</span></span>                                                |
| [<span data-ttu-id="c6121-173">**FolderItemVerbs**</span><span class="sxs-lookup"><span data-stu-id="c6121-173">**FolderItemVerbs**</span></span>](folderitemverbs.md)              | <span data-ttu-id="c6121-174">FolderItem. Verbs ou Shell. NameSpace ("..."). Verbos Self.</span><span class="sxs-lookup"><span data-stu-id="c6121-174">FolderItem.Verbs or Shell.NameSpace("...").Self.Verbs</span></span>                                   |
| [<span data-ttu-id="c6121-175">**IShellDispatch2**</span><span class="sxs-lookup"><span data-stu-id="c6121-175">**IShellDispatch2**</span></span>](ishelldispatch2-object.md)       | <span data-ttu-id="c6121-176">Shell. Aplicativo de shell \_</span><span class="sxs-lookup"><span data-stu-id="c6121-176">shell.Shell\_Application</span></span>                                                                |
| [<span data-ttu-id="c6121-177">**IShellLinkDual2**</span><span class="sxs-lookup"><span data-stu-id="c6121-177">**IShellLinkDual2**</span></span>](ishelllinkdual2-object.md)       | <span data-ttu-id="c6121-178">Shell. NameSpace ("..."). Self. GetLink ou Shell. NameSpace ("..."). Itens (). GetLink</span><span class="sxs-lookup"><span data-stu-id="c6121-178">Shell.NameSpace("...").Self.GetLink or Shell.NameSpace("...").Items().GetLink</span></span>           |
| [<span data-ttu-id="c6121-179">**Shell**</span><span class="sxs-lookup"><span data-stu-id="c6121-179">**Shell**</span></span>](shell.md)                                  | <span data-ttu-id="c6121-180">Shell. Aplicativo de shell \_</span><span class="sxs-lookup"><span data-stu-id="c6121-180">shell.Shell\_Application</span></span>                                                                |
| [<span data-ttu-id="c6121-181">**ShellFolderItem**</span><span class="sxs-lookup"><span data-stu-id="c6121-181">**ShellFolderItem**</span></span>](shellfolderitem-object.md)       | <span data-ttu-id="c6121-182">Shell. NameSpace ("..."). Self ou Shell. NameSpace ("..."). Itens ()</span><span class="sxs-lookup"><span data-stu-id="c6121-182">Shell.NameSpace("...").Self or Shell.NameSpace("...").Items()</span></span>                           |
| [<span data-ttu-id="c6121-183">**ShellFolderView**</span><span class="sxs-lookup"><span data-stu-id="c6121-183">**ShellFolderView**</span></span>](shellfolderview.md)              | <span data-ttu-id="c6121-184">Não é possível associar tardiamente</span><span class="sxs-lookup"><span data-stu-id="c6121-184">Cannot late bind</span></span>                                                                        |
| [<span data-ttu-id="c6121-185">**ShellFolderViewOC**</span><span class="sxs-lookup"><span data-stu-id="c6121-185">**ShellFolderViewOC**</span></span>](shellfolderviewoc-object.md)   | <span data-ttu-id="c6121-186">Não é possível associar tardiamente</span><span class="sxs-lookup"><span data-stu-id="c6121-186">Cannot late bind</span></span>                                                                        |
| [<span data-ttu-id="c6121-187">**ShellLinkObject**</span><span class="sxs-lookup"><span data-stu-id="c6121-187">**ShellLinkObject**</span></span>](shelllinkobject-object.md)       | <span data-ttu-id="c6121-188">Shell. NameSpace ("..."). Self. GetLink ou Shell. NameSpace ("..."). Itens (). GetLink</span><span class="sxs-lookup"><span data-stu-id="c6121-188">Shell.NameSpace("...").Self.GetLink or Shell.NameSpace("...").Items().GetLink</span></span>           |
| [<span data-ttu-id="c6121-189">**ShellUIHelper**</span><span class="sxs-lookup"><span data-stu-id="c6121-189">**ShellUIHelper**</span></span>](shelluihelper.md)                  | <span data-ttu-id="c6121-190">Não é possível associar tardiamente</span><span class="sxs-lookup"><span data-stu-id="c6121-190">Cannot late bind</span></span>                                                                        |
| [<span data-ttu-id="c6121-191">**ShellWindows**</span><span class="sxs-lookup"><span data-stu-id="c6121-191">**ShellWindows**</span></span>](shellwindows.md)                    | <span data-ttu-id="c6121-192">Shell. \_Janelas de shell ou ShellWindows. \_ NewEnum</span><span class="sxs-lookup"><span data-stu-id="c6121-192">shell.Shell\_Windows or ShellWindows.\_NewEnum</span></span>                                          |
| [<span data-ttu-id="c6121-193">**WebViewFolderContents**</span><span class="sxs-lookup"><span data-stu-id="c6121-193">**WebViewFolderContents**</span></span>](../lwef/webviewfoldercontents.md) | <span data-ttu-id="c6121-194">Não é possível associar tardiamente</span><span class="sxs-lookup"><span data-stu-id="c6121-194">Cannot late bind</span></span>                                                                        |



 

### <a name="html-object-element"></a><span data-ttu-id="c6121-195">Elemento de objeto HTML</span><span class="sxs-lookup"><span data-stu-id="c6121-195">HTML OBJECT Element</span></span>

<span data-ttu-id="c6121-196">Você também pode usar o elemento [**Object**](https://msdn.microsoft.com/library/ms535859(v=VS.85).aspx) para instanciar objetos do Shell em uma página HTML.</span><span class="sxs-lookup"><span data-stu-id="c6121-196">You can also use the [**OBJECT**](https://msdn.microsoft.com/library/ms535859(v=VS.85).aspx) element to instantiate Shell objects on an HTML page.</span></span> <span data-ttu-id="c6121-197">Para fazer isso, defina o atributo de **ID** do elemento de **objeto** como o nome da variável que você usará em seus scripts e identifique o objeto usando seu número registrado (ClassID).</span><span class="sxs-lookup"><span data-stu-id="c6121-197">To do this, set the **OBJECT** element's **ID** attribute to the variable name you will use in your scripts, and identify the object using its registered number (CLASSID).</span></span> <span data-ttu-id="c6121-198">O HTML a seguir cria uma instância do objeto [**ShellFolderItem**](shellfolderitem-object.md) usando o elemento **Object** .</span><span class="sxs-lookup"><span data-stu-id="c6121-198">The following HTML creates an instance of the [**ShellFolderItem**](shellfolderitem-object.md) object using the **OBJECT** element.</span></span>


```
<OBJECT ID="oShFolderItem" 
    NAME="Shell Folder Item Object"
    CLASSID="clsid:2fe352ea-fd1f-11d2-b1f4-00c04f8eeb3e">
</OBJECT>
```



<span data-ttu-id="c6121-199">A tabela a seguir lista cada objeto Shell e seu respectivo ClassID.</span><span class="sxs-lookup"><span data-stu-id="c6121-199">The following table lists each Shell object and its respective CLASSID.</span></span>



|                                                         |                                      |
|---------------------------------------------------------|--------------------------------------|
| [<span data-ttu-id="c6121-200">**DIDiskQuotaUser**</span><span class="sxs-lookup"><span data-stu-id="c6121-200">**DIDiskQuotaUser**</span></span>](didiskquotauser-object.md)       | <span data-ttu-id="c6121-201">7988B571-EC89-11cf-9C00-00AA00A14F56</span><span class="sxs-lookup"><span data-stu-id="c6121-201">7988B571-EC89-11cf-9C00-00AA00A14F56</span></span> |
| [<span data-ttu-id="c6121-202">**DiskQuotaControl**</span><span class="sxs-lookup"><span data-stu-id="c6121-202">**DiskQuotaControl**</span></span>](diskquotacontrol-object.md)     | <span data-ttu-id="c6121-203">7988B571-EC89-11cf-9C00-00AA00A14F56</span><span class="sxs-lookup"><span data-stu-id="c6121-203">7988B571-EC89-11cf-9C00-00AA00A14F56</span></span> |
| [<span data-ttu-id="c6121-204">**Pasta**</span><span class="sxs-lookup"><span data-stu-id="c6121-204">**Folder**</span></span>](folder.md)                                | <span data-ttu-id="c6121-205">BBCBDE60-C3FF-11CE-8350-444553540000</span><span class="sxs-lookup"><span data-stu-id="c6121-205">BBCBDE60-C3FF-11CE-8350-444553540000</span></span> |
| [<span data-ttu-id="c6121-206">**Pasta2**</span><span class="sxs-lookup"><span data-stu-id="c6121-206">**Folder2**</span></span>](folder2-object.md)                       | <span data-ttu-id="c6121-207">f0d2d8ef-3890-11d2-bf8b-00c04fb93661</span><span class="sxs-lookup"><span data-stu-id="c6121-207">f0d2d8ef-3890-11d2-bf8b-00c04fb93661</span></span> |
| [<span data-ttu-id="c6121-208">**FolderItem**</span><span class="sxs-lookup"><span data-stu-id="c6121-208">**FolderItem**</span></span>](folderitem.md)                        | <span data-ttu-id="c6121-209">744129E0-CBE5-11CE-8350-444553540000</span><span class="sxs-lookup"><span data-stu-id="c6121-209">744129E0-CBE5-11CE-8350-444553540000</span></span> |
| [<span data-ttu-id="c6121-210">**FolderItems**</span><span class="sxs-lookup"><span data-stu-id="c6121-210">**FolderItems**</span></span>](folderitems.md)                      | <span data-ttu-id="c6121-211">744129E0-CBE5-11CE-8350-444553540000</span><span class="sxs-lookup"><span data-stu-id="c6121-211">744129E0-CBE5-11CE-8350-444553540000</span></span> |
| [<span data-ttu-id="c6121-212">**FolderItems2**</span><span class="sxs-lookup"><span data-stu-id="c6121-212">**FolderItems2**</span></span>](folderitems2-object.md)             | <span data-ttu-id="c6121-213">C94F0AD0-F363-11d2-A327-00C04F8EEC7F</span><span class="sxs-lookup"><span data-stu-id="c6121-213">C94F0AD0-F363-11d2-A327-00C04F8EEC7F</span></span> |
| [<span data-ttu-id="c6121-214">**FolderItemVerb**</span><span class="sxs-lookup"><span data-stu-id="c6121-214">**FolderItemVerb**</span></span>](folderitemverb.md)                | <span data-ttu-id="c6121-215">08EC3E00-50B0-11CF-960C-0080C7F4EE85</span><span class="sxs-lookup"><span data-stu-id="c6121-215">08EC3E00-50B0-11CF-960C-0080C7F4EE85</span></span> |
| [<span data-ttu-id="c6121-216">**FolderItemVerbs**</span><span class="sxs-lookup"><span data-stu-id="c6121-216">**FolderItemVerbs**</span></span>](folderitemverbs.md)              | <span data-ttu-id="c6121-217">1F8352C0-50B0-11CF-960C-0080C7F4EE85</span><span class="sxs-lookup"><span data-stu-id="c6121-217">1F8352C0-50B0-11CF-960C-0080C7F4EE85</span></span> |
| [<span data-ttu-id="c6121-218">**IShellDispatch2**</span><span class="sxs-lookup"><span data-stu-id="c6121-218">**IShellDispatch2**</span></span>](ishelldispatch2-object.md)       | <span data-ttu-id="c6121-219">A4C6892C-3BA9-11d2-9DEA-00C04FB16162</span><span class="sxs-lookup"><span data-stu-id="c6121-219">A4C6892C-3BA9-11d2-9DEA-00C04FB16162</span></span> |
| [<span data-ttu-id="c6121-220">**IShellLinkDual2**</span><span class="sxs-lookup"><span data-stu-id="c6121-220">**IShellLinkDual2**</span></span>](ishelllinkdual2-object.md)       | <span data-ttu-id="c6121-221">317EE249-F12E-11d2-B1E4-00C04F8EEB3E</span><span class="sxs-lookup"><span data-stu-id="c6121-221">317EE249-F12E-11d2-B1E4-00C04F8EEB3E</span></span> |
| [<span data-ttu-id="c6121-222">**Shell**</span><span class="sxs-lookup"><span data-stu-id="c6121-222">**Shell**</span></span>](shell.md)                                  | <span data-ttu-id="c6121-223">13709620-C279-11CE-A49E-444553540000</span><span class="sxs-lookup"><span data-stu-id="c6121-223">13709620-C279-11CE-A49E-444553540000</span></span> |
| [<span data-ttu-id="c6121-224">**ShellFolderItem**</span><span class="sxs-lookup"><span data-stu-id="c6121-224">**ShellFolderItem**</span></span>](shellfolderitem-object.md)       | <span data-ttu-id="c6121-225">2fe352ea-fd1f-11d2-b1f4-00c04f8eeb3e</span><span class="sxs-lookup"><span data-stu-id="c6121-225">2fe352ea-fd1f-11d2-b1f4-00c04f8eeb3e</span></span> |
| [<span data-ttu-id="c6121-226">**ShellFolderView**</span><span class="sxs-lookup"><span data-stu-id="c6121-226">**ShellFolderView**</span></span>](shellfolderview.md)              | <span data-ttu-id="c6121-227">62112AA1-EBE4-11cf-A5FB-0020AFE7292D</span><span class="sxs-lookup"><span data-stu-id="c6121-227">62112AA1-EBE4-11cf-A5FB-0020AFE7292D</span></span> |
| [<span data-ttu-id="c6121-228">**ShellFolderViewOC**</span><span class="sxs-lookup"><span data-stu-id="c6121-228">**ShellFolderViewOC**</span></span>](shellfolderviewoc-object.md)   | <span data-ttu-id="c6121-229">4a3df050-23bd-11d2-939f-00a0c91eedba</span><span class="sxs-lookup"><span data-stu-id="c6121-229">4a3df050-23bd-11d2-939f-00a0c91eedba</span></span> |
| [<span data-ttu-id="c6121-230">**ShellLinkObject**</span><span class="sxs-lookup"><span data-stu-id="c6121-230">**ShellLinkObject**</span></span>](shelllinkobject-object.md)       | <span data-ttu-id="c6121-231">11219420-1768-11d1-95BE-00609797EA4F</span><span class="sxs-lookup"><span data-stu-id="c6121-231">11219420-1768-11d1-95BE-00609797EA4F</span></span> |
| [<span data-ttu-id="c6121-232">**ShellUIHelper**</span><span class="sxs-lookup"><span data-stu-id="c6121-232">**ShellUIHelper**</span></span>](shelluihelper.md)                  | <span data-ttu-id="c6121-233">64AB4BB7-111E-11D1-8F79-00C04FC2FBE1</span><span class="sxs-lookup"><span data-stu-id="c6121-233">64AB4BB7-111E-11D1-8F79-00C04FC2FBE1</span></span> |
| [<span data-ttu-id="c6121-234">**ShellWindows**</span><span class="sxs-lookup"><span data-stu-id="c6121-234">**ShellWindows**</span></span>](shellwindows.md)                    | <span data-ttu-id="c6121-235">9BA05972-F6A8-11CF-A442-00A0C90A8F39</span><span class="sxs-lookup"><span data-stu-id="c6121-235">9BA05972-F6A8-11CF-A442-00A0C90A8F39</span></span> |
| [<span data-ttu-id="c6121-236">**WebViewFolderContents**</span><span class="sxs-lookup"><span data-stu-id="c6121-236">**WebViewFolderContents**</span></span>](../lwef/webviewfoldercontents.md) | <span data-ttu-id="c6121-237">1820FED0-473E-11D0-A96C-00C04FD705A2</span><span class="sxs-lookup"><span data-stu-id="c6121-237">1820FED0-473E-11D0-A96C-00C04FD705A2</span></span> |



 

## <a name="shell-object"></a><span data-ttu-id="c6121-238">Objeto Shell</span><span class="sxs-lookup"><span data-stu-id="c6121-238">Shell Object</span></span>

<span data-ttu-id="c6121-239">O objeto [**shell**](shell.md) representa os objetos no Shell.</span><span class="sxs-lookup"><span data-stu-id="c6121-239">The [**Shell**](shell.md) object represents the objects in the Shell.</span></span> <span data-ttu-id="c6121-240">Você pode usar os métodos expostos pelo objeto Shell para:</span><span class="sxs-lookup"><span data-stu-id="c6121-240">You can use the methods exposed by the Shell object to:</span></span>

-   <span data-ttu-id="c6121-241">Abra, explore e procure pastas.</span><span class="sxs-lookup"><span data-stu-id="c6121-241">Open, explore, and browse for folders.</span></span>
-   <span data-ttu-id="c6121-242">Minimizar, restaurar, colocar em cascata ou janelas abertas.</span><span class="sxs-lookup"><span data-stu-id="c6121-242">Minimize, restore, cascade, or tile open windows.</span></span>
-   <span data-ttu-id="c6121-243">Inicie aplicativos do painel de controle.</span><span class="sxs-lookup"><span data-stu-id="c6121-243">Launch Control Panel applications.</span></span>
-   <span data-ttu-id="c6121-244">Exibir caixas de diálogo do sistema.</span><span class="sxs-lookup"><span data-stu-id="c6121-244">Display system dialog boxes.</span></span>

<span data-ttu-id="c6121-245">Os usuários talvez estejam mais familiarizados com os comandos que acessam no menu **Iniciar** e no menu de atalho da barra de tarefas.</span><span class="sxs-lookup"><span data-stu-id="c6121-245">Users are perhaps most familiar with the commands they access from the **Start** menu and the taskbar's shortcut menu.</span></span> <span data-ttu-id="c6121-246">O menu de atalho da barra de tarefas aparece quando os usuários clicam com o botão direito na barra de tarefas.</span><span class="sxs-lookup"><span data-stu-id="c6121-246">The taskbar's shortcut menu appears when users right-click the taskbar.</span></span> <span data-ttu-id="c6121-247">O HTA (aplicativo HTML) a seguir produz uma página inicial com botões que implementam muitos dos métodos do objeto [**shell**](shell.md) .</span><span class="sxs-lookup"><span data-stu-id="c6121-247">The following HTML Application (HTA) produces a start page with buttons that implement many of the [**Shell**](shell.md) object's methods.</span></span> <span data-ttu-id="c6121-248">Alguns desses métodos implementam recursos no menu **Iniciar** e no menu de atalho da barra de tarefas.</span><span class="sxs-lookup"><span data-stu-id="c6121-248">Some of these methods implement features on the **Start** menu and the taskbar's shortcut menu.</span></span>


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



### <a name="security"></a><span data-ttu-id="c6121-249">Segurança</span><span class="sxs-lookup"><span data-stu-id="c6121-249">Security</span></span>

<span data-ttu-id="c6121-250">Como um aplicativo, um HTA é executado em um modelo de segurança diferente de uma página da Web.</span><span class="sxs-lookup"><span data-stu-id="c6121-250">As an application, an HTA runs under a different security model than a webpage.</span></span> <span data-ttu-id="c6121-251">Para interagir com uma página da Web que implementa a funcionalidade dos objetos do Shell, os usuários devem habilitar a opção **inicializar e gerar script de controles ActiveX não marcados como seguros** para a zona de segurança na qual estão exibindo a página.</span><span class="sxs-lookup"><span data-stu-id="c6121-251">To interact with a webpage that implements the functionality of the Shell objects, users must enable the **Initialize and script ActiveX Controls not marked as safe** option for the security zone in which they are viewing the page.</span></span>

## <a name="folder-objects"></a><span data-ttu-id="c6121-252">Objetos de pasta</span><span class="sxs-lookup"><span data-stu-id="c6121-252">Folder Objects</span></span>

<span data-ttu-id="c6121-253">O objeto [**Folder**](folder.md) representa uma pasta Shell.</span><span class="sxs-lookup"><span data-stu-id="c6121-253">The [**Folder**](folder.md) object represents a Shell folder.</span></span> <span data-ttu-id="c6121-254">Você pode usar os métodos expostos pelo objeto Folder para:</span><span class="sxs-lookup"><span data-stu-id="c6121-254">You can use the methods exposed by the Folder object to:</span></span>

-   <span data-ttu-id="c6121-255">Obter informações sobre uma pasta.</span><span class="sxs-lookup"><span data-stu-id="c6121-255">Get information about a folder.</span></span>
-   <span data-ttu-id="c6121-256">Criar subpastas.</span><span class="sxs-lookup"><span data-stu-id="c6121-256">Create subfolders.</span></span>
-   <span data-ttu-id="c6121-257">Copie e mova objetos de arquivo para a pasta.</span><span class="sxs-lookup"><span data-stu-id="c6121-257">Copy and move file objects into the folder.</span></span>

<span data-ttu-id="c6121-258">O objeto [**FolderItem**](folderitem.md) representa um item em uma pasta do Shell.</span><span class="sxs-lookup"><span data-stu-id="c6121-258">The [**FolderItem**](folderitem.md) object represents an item in a Shell folder.</span></span> <span data-ttu-id="c6121-259">Suas propriedades permitem que você recupere informações sobre o item.</span><span class="sxs-lookup"><span data-stu-id="c6121-259">Its properties enable you to retrieve information about the item.</span></span> <span data-ttu-id="c6121-260">Você pode usar os métodos expostos por esse objeto para executar os verbos de um item ou para recuperar informações sobre o objeto [**FolderItemVerbs**](folderitemverbs.md) de um item.</span><span class="sxs-lookup"><span data-stu-id="c6121-260">You can use the methods exposed by this object to run an item's verbs, or to retrieve information about an item's [**FolderItemVerbs**](folderitemverbs.md) object.</span></span>

<span data-ttu-id="c6121-261">O objeto [**FolderItems**](folderitems.md) representa uma coleção de itens em uma pasta do Shell.</span><span class="sxs-lookup"><span data-stu-id="c6121-261">The [**FolderItems**](folderitems.md) object represents a collection of items in a Shell folder.</span></span> <span data-ttu-id="c6121-262">Seus métodos e propriedades permitem que você recupere informações sobre a coleção.</span><span class="sxs-lookup"><span data-stu-id="c6121-262">Its methods and properties enable you to retrieve information about the collection.</span></span>

<span data-ttu-id="c6121-263">O exemplo a seguir Visual Basic mostra a relação entre vários objetos de pasta e como eles podem ser usados juntos.</span><span class="sxs-lookup"><span data-stu-id="c6121-263">The following Visual Basic example shows the relationship between several of the folder objects and how they can be used together.</span></span> <span data-ttu-id="c6121-264">Quando o usuário clica no botão de comando chamado **cmdGetPath**, o programa exibe uma caixa de diálogo que permite ao usuário selecionar uma pasta de **meu computador**, em que ssfDRIVES é o valor de enumeração [**ShellSpecialFolderConstants**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) para **meu computador**.</span><span class="sxs-lookup"><span data-stu-id="c6121-264">When the user clicks the command button called **cmdGetPath**, the program displays a dialog box that enables the user to select a folder from **My Computer**, where ssfDRIVES is the [**ShellSpecialFolderConstants**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) enumeration value for **My Computer**.</span></span> <span data-ttu-id="c6121-265">Quando o usuário escolhe uma pasta, o caminho da pasta é exibido na caixa de texto chamada **txtPath**.</span><span class="sxs-lookup"><span data-stu-id="c6121-265">When the user chooses a folder, the folder's path is displayed in the text box called **txtPath**.</span></span>


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



<span data-ttu-id="c6121-266">No VBScript, essa função é ligeiramente diferente porque os valores de enumeração [**ShellSpecialFolderConstants**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) não estão disponíveis no script.</span><span class="sxs-lookup"><span data-stu-id="c6121-266">In VBScript, this function is slightly different because the [**ShellSpecialFolderConstants**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) enumeration values are not available in script.</span></span> <span data-ttu-id="c6121-267">O exemplo a seguir mostra o VBScript equivalente do exemplo anterior.</span><span class="sxs-lookup"><span data-stu-id="c6121-267">The following example shows the VBScript equivalent of the previous example.</span></span>


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



<span data-ttu-id="c6121-268">No exemplo de JScript a seguir, que é uma tradução direta do exemplo anterior do VBScript, observe como os parênteses vazios ' () ' são usados para invocar os [**itens**](folder-items.md) e os métodos de [**Item**](folderitems-item.md) .</span><span class="sxs-lookup"><span data-stu-id="c6121-268">In the following JScript example, which is a direct translation of the preceding VBScript example, note how the empty parentheses '()' are used to invoke the [**Items**](folder-items.md) and [**Item**](folderitems-item.md) methods.</span></span>


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



 

 
