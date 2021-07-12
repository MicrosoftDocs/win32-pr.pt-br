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
# <a name="scriptable-shell-objects"></a><span data-ttu-id="07119-105">Objetos shell programáveis</span><span class="sxs-lookup"><span data-stu-id="07119-105">Scriptable Shell Objects</span></span>

<span data-ttu-id="07119-106">o Shell de Windows fornece um conjunto poderoso de objetos de automação que permitem que você programe o Shell com o microsoft Visual Basic e linguagens de script, como o microsoft JScript (compatível com a especificação de linguagem ECMA 262) e o microsoft Visual Basic scripting Edition (VBScript).</span><span class="sxs-lookup"><span data-stu-id="07119-106">The Windows Shell provides a powerful set of automation objects that enable you to program the Shell with Microsoft Visual Basic and scripting languages such as Microsoft JScript (compatible with ECMA 262 language specification) and Microsoft Visual Basic Scripting Edition (VBScript).</span></span> <span data-ttu-id="07119-107">Você pode usar esses objetos para acessar muitos dos recursos e caixas de diálogo do Shell.</span><span class="sxs-lookup"><span data-stu-id="07119-107">You can use these objects to access many of the Shell's features and dialog boxes.</span></span> <span data-ttu-id="07119-108">Por exemplo, você pode acessar o sistema de arquivos, iniciar programas e alterar as configurações do sistema.</span><span class="sxs-lookup"><span data-stu-id="07119-108">For example, you can access the file system, launch programs, and change system settings.</span></span>

<span data-ttu-id="07119-109">Esta seção apresenta os objetos shell programáveis.</span><span class="sxs-lookup"><span data-stu-id="07119-109">This section introduces the scriptable Shell objects.</span></span>

-   [<span data-ttu-id="07119-110">Versões do Shell</span><span class="sxs-lookup"><span data-stu-id="07119-110">Shell Versions</span></span>](#shell-versions)
-   [<span data-ttu-id="07119-111">Instanciando objetos do Shell</span><span class="sxs-lookup"><span data-stu-id="07119-111">Instantiating Shell Objects</span></span>](#instantiating-shell-objects)
    -   [<span data-ttu-id="07119-112">Associação tardia</span><span class="sxs-lookup"><span data-stu-id="07119-112">Late Binding</span></span>](#late-binding)
    -   [<span data-ttu-id="07119-113">Elemento de objeto HTML</span><span class="sxs-lookup"><span data-stu-id="07119-113">HTML OBJECT Element</span></span>](#html-object-element)
-   [<span data-ttu-id="07119-114">Objeto Shell</span><span class="sxs-lookup"><span data-stu-id="07119-114">Shell Object</span></span>](#shell-object)
    -   [<span data-ttu-id="07119-115">Segurança</span><span class="sxs-lookup"><span data-stu-id="07119-115">Security</span></span>](#security)
-   [<span data-ttu-id="07119-116">Objetos de pasta</span><span class="sxs-lookup"><span data-stu-id="07119-116">Folder Objects</span></span>](#folder-objects)

## <a name="shell-versions"></a><span data-ttu-id="07119-117">Versões do Shell</span><span class="sxs-lookup"><span data-stu-id="07119-117">Shell Versions</span></span>

<span data-ttu-id="07119-118">Muitos dos objetos shell foram disponibilizados na [versão 4,71](versions.md) do Shell.</span><span class="sxs-lookup"><span data-stu-id="07119-118">Many of the Shell objects became available in [version 4.71](versions.md) of the Shell.</span></span> <span data-ttu-id="07119-119">Outras estão disponíveis na versão 5, 0 e posterior.</span><span class="sxs-lookup"><span data-stu-id="07119-119">Others are available in version 5.00 and later.</span></span> <span data-ttu-id="07119-120">a versão 5, 0 tornou-se disponível com o Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="07119-120">Version 5.00 became available with Windows 2000.</span></span> <span data-ttu-id="07119-121">A tabela a seguir lista cada objeto Shell na versão do Shell em que o objeto ficou disponível.</span><span class="sxs-lookup"><span data-stu-id="07119-121">The following table lists each Shell object under the version of the Shell in which the object became available.</span></span>



| <span data-ttu-id="07119-122">Versão 4,71</span><span class="sxs-lookup"><span data-stu-id="07119-122">Version 4.71</span></span>                                            | <span data-ttu-id="07119-123">Versão 5, 0</span><span class="sxs-lookup"><span data-stu-id="07119-123">Version 5.00</span></span>                                          |
|---------------------------------------------------------|-------------------------------------------------------|
| [<span data-ttu-id="07119-124">**Pasta**</span><span class="sxs-lookup"><span data-stu-id="07119-124">**Folder**</span></span>](folder.md)                                | [<span data-ttu-id="07119-125">**DIDiskQuotaUser**</span><span class="sxs-lookup"><span data-stu-id="07119-125">**DIDiskQuotaUser**</span></span>](didiskquotauser-object.md)     |
| [<span data-ttu-id="07119-126">**FolderItemVerb**</span><span class="sxs-lookup"><span data-stu-id="07119-126">**FolderItemVerb**</span></span>](folderitemverb.md)                | [<span data-ttu-id="07119-127">**DiskQuotaControl**</span><span class="sxs-lookup"><span data-stu-id="07119-127">**DiskQuotaControl**</span></span>](diskquotacontrol-object.md)   |
| [<span data-ttu-id="07119-128">**FolderItemVerbs**</span><span class="sxs-lookup"><span data-stu-id="07119-128">**FolderItemVerbs**</span></span>](folderitemverbs.md)              | [<span data-ttu-id="07119-129">**Pasta2**</span><span class="sxs-lookup"><span data-stu-id="07119-129">**Folder2**</span></span>](folder2-object.md)                     |
| [<span data-ttu-id="07119-130">**Shell**</span><span class="sxs-lookup"><span data-stu-id="07119-130">**Shell**</span></span>](shell.md)                                  | [<span data-ttu-id="07119-131">**FolderItem**</span><span class="sxs-lookup"><span data-stu-id="07119-131">**FolderItem**</span></span>](folderitem.md)                      |
| [<span data-ttu-id="07119-132">**ShellFolderView**</span><span class="sxs-lookup"><span data-stu-id="07119-132">**ShellFolderView**</span></span>](shellfolderview.md)              | [<span data-ttu-id="07119-133">**FolderItems**</span><span class="sxs-lookup"><span data-stu-id="07119-133">**FolderItems**</span></span>](folderitems.md)                    |
| [<span data-ttu-id="07119-134">**ShellUIHelper**</span><span class="sxs-lookup"><span data-stu-id="07119-134">**ShellUIHelper**</span></span>](shelluihelper.md)                  | [<span data-ttu-id="07119-135">**FolderItems2**</span><span class="sxs-lookup"><span data-stu-id="07119-135">**FolderItems2**</span></span>](folderitems2-object.md)           |
| [<span data-ttu-id="07119-136">**ShellWindows**</span><span class="sxs-lookup"><span data-stu-id="07119-136">**ShellWindows**</span></span>](shellwindows.md)                    | [<span data-ttu-id="07119-137">**IShellDispatch2**</span><span class="sxs-lookup"><span data-stu-id="07119-137">**IShellDispatch2**</span></span>](ishelldispatch2-object.md)     |
| [<span data-ttu-id="07119-138">**WebViewFolderContents**</span><span class="sxs-lookup"><span data-stu-id="07119-138">**WebViewFolderContents**</span></span>](../lwef/webviewfoldercontents.md) | [<span data-ttu-id="07119-139">**IShellLinkDual2**</span><span class="sxs-lookup"><span data-stu-id="07119-139">**IShellLinkDual2**</span></span>](ishelllinkdual2-object.md)     |
|                                                         | [<span data-ttu-id="07119-140">**ShellFolderItem**</span><span class="sxs-lookup"><span data-stu-id="07119-140">**ShellFolderItem**</span></span>](shellfolderitem-object.md)     |
|                                                         | [<span data-ttu-id="07119-141">**ShellFolderViewOC**</span><span class="sxs-lookup"><span data-stu-id="07119-141">**ShellFolderViewOC**</span></span>](shellfolderviewoc-object.md) |
|                                                         | [<span data-ttu-id="07119-142">**ShellLinkObject**</span><span class="sxs-lookup"><span data-stu-id="07119-142">**ShellLinkObject**</span></span>](shelllinkobject-object.md)     |



 

## <a name="instantiating-shell-objects"></a><span data-ttu-id="07119-143">Instanciando objetos do Shell</span><span class="sxs-lookup"><span data-stu-id="07119-143">Instantiating Shell Objects</span></span>

<span data-ttu-id="07119-144">para instanciar os objetos do Shell em aplicativos Visual Basic com associação inicial, adicione referências às seguintes bibliotecas em seu projeto:</span><span class="sxs-lookup"><span data-stu-id="07119-144">To instantiate the Shell objects in Visual Basic applications with early binding, add references to the following libraries in your project:</span></span>

-   <span data-ttu-id="07119-145">Microsoft Internet Controls (SHDocVw)</span><span class="sxs-lookup"><span data-stu-id="07119-145">Microsoft Internet Controls (SHDocVw)</span></span>
-   <span data-ttu-id="07119-146">Microsoft Shell Controls and Automation (shell32)</span><span class="sxs-lookup"><span data-stu-id="07119-146">Microsoft Shell Controls and Automation (Shell32)</span></span>

### <a name="late-binding"></a><span data-ttu-id="07119-147">Associação tardia</span><span class="sxs-lookup"><span data-stu-id="07119-147">Late Binding</span></span>

<span data-ttu-id="07119-148">Você também pode criar uma instância de muitos dos objetos do shell com associação tardia.</span><span class="sxs-lookup"><span data-stu-id="07119-148">You can also instantiate many of the Shell objects with late binding.</span></span> <span data-ttu-id="07119-149">essa abordagem funciona em Visual Basic aplicativos e no script.</span><span class="sxs-lookup"><span data-stu-id="07119-149">This approach works in Visual Basic applications and in script.</span></span> <span data-ttu-id="07119-150">O exemplo a seguir mostra como criar uma instância do objeto [**shell**](shell.md) no JScript.</span><span class="sxs-lookup"><span data-stu-id="07119-150">The following example shows how to instantiate the [**Shell**](shell.md) object in JScript.</span></span>


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



<span data-ttu-id="07119-151">O exemplo a seguir mostra como criar uma instância do objeto de [**pasta**](folder.md) no VBScript.</span><span class="sxs-lookup"><span data-stu-id="07119-151">The following example shows how to instantiate the [**Folder**](folder.md) object in VBScript.</span></span>


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



<span data-ttu-id="07119-152">No exemplo anterior, *sDir* é o caminho para o objeto [**Folder**](folder.md) .</span><span class="sxs-lookup"><span data-stu-id="07119-152">In the preceding example, *sDir* is the path to the [**Folder**](folder.md) object.</span></span> <span data-ttu-id="07119-153">Observe que os valores de enumeração [**ShellSpecialFolderConstants**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) não estão disponíveis no script.</span><span class="sxs-lookup"><span data-stu-id="07119-153">Note that the [**ShellSpecialFolderConstants**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) enumeration values are not available in script.</span></span>

<span data-ttu-id="07119-154">O ProgID de cada um dos objetos do Shell é mostrado na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="07119-154">The ProgID for each of the Shell objects is shown in the following table.</span></span>



| <span data-ttu-id="07119-155">Objeto</span><span class="sxs-lookup"><span data-stu-id="07119-155">Object</span></span>                                                  | <span data-ttu-id="07119-156">ProgID</span><span class="sxs-lookup"><span data-stu-id="07119-156">ProgID</span></span>                                                                                  |
|---------------------------------------------------------|-----------------------------------------------------------------------------------------|
| [<span data-ttu-id="07119-157">**DIDiskQuotaUser**</span><span class="sxs-lookup"><span data-stu-id="07119-157">**DIDiskQuotaUser**</span></span>](didiskquotauser-object.md)       | <span data-ttu-id="07119-158">Microsoft. DiskQuota. 1</span><span class="sxs-lookup"><span data-stu-id="07119-158">Microsoft.DiskQuota.1</span></span>                                                                   |
| [<span data-ttu-id="07119-159">**DiskQuotaControl**</span><span class="sxs-lookup"><span data-stu-id="07119-159">**DiskQuotaControl**</span></span>](diskquotacontrol-object.md)     | <span data-ttu-id="07119-160">Não é possível associar tardiamente</span><span class="sxs-lookup"><span data-stu-id="07119-160">Cannot late bind</span></span>                                                                        |
| [<span data-ttu-id="07119-161">**Pasta**</span><span class="sxs-lookup"><span data-stu-id="07119-161">**Folder**</span></span>](folder.md)                                | <span data-ttu-id="07119-162">Shell. Shell \_ Application. Namespace ("...")</span><span class="sxs-lookup"><span data-stu-id="07119-162">shell.Shell\_Application.NameSpace("...")</span></span>                                               |
| [<span data-ttu-id="07119-163">**Pasta2**</span><span class="sxs-lookup"><span data-stu-id="07119-163">**Folder2**</span></span>](folder2-object.md)                       | <span data-ttu-id="07119-164">Shell. Shell \_ Application. Namespace ("...")</span><span class="sxs-lookup"><span data-stu-id="07119-164">shell.Shell\_Application.NameSpace("...")</span></span>                                               |
| [<span data-ttu-id="07119-165">**FolderItem**</span><span class="sxs-lookup"><span data-stu-id="07119-165">**FolderItem**</span></span>](folderitem.md)                        | <span data-ttu-id="07119-166">Shell. Shell \_ Application. Namespace ("..."). Self ou Folder. Items. itens ou pasta. ParseName</span><span class="sxs-lookup"><span data-stu-id="07119-166">shell.Shell\_Application.NameSpace("...").Self or Folder.Items.Item or Folder.ParseName</span></span> |
| [<span data-ttu-id="07119-167">**FolderItems**</span><span class="sxs-lookup"><span data-stu-id="07119-167">**FolderItems**</span></span>](folderitems.md)                      | <span data-ttu-id="07119-168">Pasta. itens</span><span class="sxs-lookup"><span data-stu-id="07119-168">Folder.Items</span></span>                                                                            |
| [<span data-ttu-id="07119-169">**FolderItems2**</span><span class="sxs-lookup"><span data-stu-id="07119-169">**FolderItems2**</span></span>](folderitems2-object.md)             | <span data-ttu-id="07119-170">Pasta. itens</span><span class="sxs-lookup"><span data-stu-id="07119-170">Folder.Items</span></span>                                                                            |
| [<span data-ttu-id="07119-171">**FolderItemVerb**</span><span class="sxs-lookup"><span data-stu-id="07119-171">**FolderItemVerb**</span></span>](folderitemverb.md)                | <span data-ttu-id="07119-172">Shell. NameSpace ("..."). Auto. Verbs. Item ()</span><span class="sxs-lookup"><span data-stu-id="07119-172">Shell.NameSpace("...").Self.Verbs.Item()</span></span>                                                |
| [<span data-ttu-id="07119-173">**FolderItemVerbs**</span><span class="sxs-lookup"><span data-stu-id="07119-173">**FolderItemVerbs**</span></span>](folderitemverbs.md)              | <span data-ttu-id="07119-174">FolderItem. Verbs ou Shell. NameSpace ("..."). Verbos Self.</span><span class="sxs-lookup"><span data-stu-id="07119-174">FolderItem.Verbs or Shell.NameSpace("...").Self.Verbs</span></span>                                   |
| [<span data-ttu-id="07119-175">**IShellDispatch2**</span><span class="sxs-lookup"><span data-stu-id="07119-175">**IShellDispatch2**</span></span>](ishelldispatch2-object.md)       | <span data-ttu-id="07119-176">Shell. Aplicativo de shell \_</span><span class="sxs-lookup"><span data-stu-id="07119-176">shell.Shell\_Application</span></span>                                                                |
| [<span data-ttu-id="07119-177">**IShellLinkDual2**</span><span class="sxs-lookup"><span data-stu-id="07119-177">**IShellLinkDual2**</span></span>](ishelllinkdual2-object.md)       | <span data-ttu-id="07119-178">Shell. NameSpace ("..."). Self. GetLink ou Shell. NameSpace ("..."). Itens (). GetLink</span><span class="sxs-lookup"><span data-stu-id="07119-178">Shell.NameSpace("...").Self.GetLink or Shell.NameSpace("...").Items().GetLink</span></span>           |
| [<span data-ttu-id="07119-179">**Shell**</span><span class="sxs-lookup"><span data-stu-id="07119-179">**Shell**</span></span>](shell.md)                                  | <span data-ttu-id="07119-180">Shell. Aplicativo de shell \_</span><span class="sxs-lookup"><span data-stu-id="07119-180">shell.Shell\_Application</span></span>                                                                |
| [<span data-ttu-id="07119-181">**ShellFolderItem**</span><span class="sxs-lookup"><span data-stu-id="07119-181">**ShellFolderItem**</span></span>](shellfolderitem-object.md)       | <span data-ttu-id="07119-182">Shell. NameSpace ("..."). Self ou Shell. NameSpace ("..."). Itens ()</span><span class="sxs-lookup"><span data-stu-id="07119-182">Shell.NameSpace("...").Self or Shell.NameSpace("...").Items()</span></span>                           |
| [<span data-ttu-id="07119-183">**ShellFolderView**</span><span class="sxs-lookup"><span data-stu-id="07119-183">**ShellFolderView**</span></span>](shellfolderview.md)              | <span data-ttu-id="07119-184">Não é possível associar tardiamente</span><span class="sxs-lookup"><span data-stu-id="07119-184">Cannot late bind</span></span>                                                                        |
| [<span data-ttu-id="07119-185">**ShellFolderViewOC**</span><span class="sxs-lookup"><span data-stu-id="07119-185">**ShellFolderViewOC**</span></span>](shellfolderviewoc-object.md)   | <span data-ttu-id="07119-186">Não é possível associar tardiamente</span><span class="sxs-lookup"><span data-stu-id="07119-186">Cannot late bind</span></span>                                                                        |
| [<span data-ttu-id="07119-187">**ShellLinkObject**</span><span class="sxs-lookup"><span data-stu-id="07119-187">**ShellLinkObject**</span></span>](shelllinkobject-object.md)       | <span data-ttu-id="07119-188">Shell. NameSpace ("..."). Self. GetLink ou Shell. NameSpace ("..."). Itens (). GetLink</span><span class="sxs-lookup"><span data-stu-id="07119-188">Shell.NameSpace("...").Self.GetLink or Shell.NameSpace("...").Items().GetLink</span></span>           |
| [<span data-ttu-id="07119-189">**ShellUIHelper**</span><span class="sxs-lookup"><span data-stu-id="07119-189">**ShellUIHelper**</span></span>](shelluihelper.md)                  | <span data-ttu-id="07119-190">Não é possível associar tardiamente</span><span class="sxs-lookup"><span data-stu-id="07119-190">Cannot late bind</span></span>                                                                        |
| [<span data-ttu-id="07119-191">**ShellWindows**</span><span class="sxs-lookup"><span data-stu-id="07119-191">**ShellWindows**</span></span>](shellwindows.md)                    | <span data-ttu-id="07119-192">Shell. Shell \_ Windows ou ShellWindows. \_ NewEnum</span><span class="sxs-lookup"><span data-stu-id="07119-192">shell.Shell\_Windows or ShellWindows.\_NewEnum</span></span>                                          |
| [<span data-ttu-id="07119-193">**WebViewFolderContents**</span><span class="sxs-lookup"><span data-stu-id="07119-193">**WebViewFolderContents**</span></span>](../lwef/webviewfoldercontents.md) | <span data-ttu-id="07119-194">Não é possível associar tardiamente</span><span class="sxs-lookup"><span data-stu-id="07119-194">Cannot late bind</span></span>                                                                        |



 

### <a name="html-object-element"></a><span data-ttu-id="07119-195">Elemento de objeto HTML</span><span class="sxs-lookup"><span data-stu-id="07119-195">HTML OBJECT Element</span></span>

<span data-ttu-id="07119-196">Você também pode usar o elemento [**Object**](https://msdn.microsoft.com/library/ms535859(v=VS.85).aspx) para instanciar objetos do Shell em uma página HTML.</span><span class="sxs-lookup"><span data-stu-id="07119-196">You can also use the [**OBJECT**](https://msdn.microsoft.com/library/ms535859(v=VS.85).aspx) element to instantiate Shell objects on an HTML page.</span></span> <span data-ttu-id="07119-197">Para fazer isso, defina o atributo de **ID** do elemento de **objeto** como o nome da variável que você usará em seus scripts e identifique o objeto usando seu número registrado (ClassID).</span><span class="sxs-lookup"><span data-stu-id="07119-197">To do this, set the **OBJECT** element's **ID** attribute to the variable name you will use in your scripts, and identify the object using its registered number (CLASSID).</span></span> <span data-ttu-id="07119-198">O HTML a seguir cria uma instância do objeto [**ShellFolderItem**](shellfolderitem-object.md) usando o elemento **Object** .</span><span class="sxs-lookup"><span data-stu-id="07119-198">The following HTML creates an instance of the [**ShellFolderItem**](shellfolderitem-object.md) object using the **OBJECT** element.</span></span>


```
<OBJECT ID="oShFolderItem" 
    NAME="Shell Folder Item Object"
    CLASSID="clsid:2fe352ea-fd1f-11d2-b1f4-00c04f8eeb3e">
</OBJECT>
```



<span data-ttu-id="07119-199">A tabela a seguir lista cada objeto Shell e seu respectivo ClassID.</span><span class="sxs-lookup"><span data-stu-id="07119-199">The following table lists each Shell object and its respective CLASSID.</span></span>



| <span data-ttu-id="07119-200">Objeto Shell</span><span class="sxs-lookup"><span data-stu-id="07119-200">Shell object</span></span>                                           | <span data-ttu-id="07119-201">CLASSID</span><span class="sxs-lookup"><span data-stu-id="07119-201">CLASSID</span></span>                              |
|--------------------------------------------------------|--------------------------------------|
| [<span data-ttu-id="07119-202">**DIDiskQuotaUser**</span><span class="sxs-lookup"><span data-stu-id="07119-202">**DIDiskQuotaUser**</span></span>](didiskquotauser-object.md)       | <span data-ttu-id="07119-203">7988B571-EC89-11cf-9C00-00AA00A14F56</span><span class="sxs-lookup"><span data-stu-id="07119-203">7988B571-EC89-11cf-9C00-00AA00A14F56</span></span> |
| [<span data-ttu-id="07119-204">**DiskQuotaControl**</span><span class="sxs-lookup"><span data-stu-id="07119-204">**DiskQuotaControl**</span></span>](diskquotacontrol-object.md)     | <span data-ttu-id="07119-205">7988B571-EC89-11cf-9C00-00AA00A14F56</span><span class="sxs-lookup"><span data-stu-id="07119-205">7988B571-EC89-11cf-9C00-00AA00A14F56</span></span> |
| [<span data-ttu-id="07119-206">**Pasta**</span><span class="sxs-lookup"><span data-stu-id="07119-206">**Folder**</span></span>](folder.md)                                | <span data-ttu-id="07119-207">BBCBDE60-C3FF-11CE-8350-444553540000</span><span class="sxs-lookup"><span data-stu-id="07119-207">BBCBDE60-C3FF-11CE-8350-444553540000</span></span> |
| [<span data-ttu-id="07119-208">**Pasta2**</span><span class="sxs-lookup"><span data-stu-id="07119-208">**Folder2**</span></span>](folder2-object.md)                       | <span data-ttu-id="07119-209">f0d2d8ef-3890-11d2-bf8b-00c04fb93661</span><span class="sxs-lookup"><span data-stu-id="07119-209">f0d2d8ef-3890-11d2-bf8b-00c04fb93661</span></span> |
| [<span data-ttu-id="07119-210">**FolderItem**</span><span class="sxs-lookup"><span data-stu-id="07119-210">**FolderItem**</span></span>](folderitem.md)                        | <span data-ttu-id="07119-211">744129E0-CBE5-11CE-8350-444553540000</span><span class="sxs-lookup"><span data-stu-id="07119-211">744129E0-CBE5-11CE-8350-444553540000</span></span> |
| [<span data-ttu-id="07119-212">**FolderItems**</span><span class="sxs-lookup"><span data-stu-id="07119-212">**FolderItems**</span></span>](folderitems.md)                      | <span data-ttu-id="07119-213">744129E0-CBE5-11CE-8350-444553540000</span><span class="sxs-lookup"><span data-stu-id="07119-213">744129E0-CBE5-11CE-8350-444553540000</span></span> |
| [<span data-ttu-id="07119-214">**FolderItems2**</span><span class="sxs-lookup"><span data-stu-id="07119-214">**FolderItems2**</span></span>](folderitems2-object.md)             | <span data-ttu-id="07119-215">C94F0AD0-F363-11d2-A327-00C04F8EEC7F</span><span class="sxs-lookup"><span data-stu-id="07119-215">C94F0AD0-F363-11d2-A327-00C04F8EEC7F</span></span> |
| [<span data-ttu-id="07119-216">**FolderItemVerb**</span><span class="sxs-lookup"><span data-stu-id="07119-216">**FolderItemVerb**</span></span>](folderitemverb.md)                | <span data-ttu-id="07119-217">08EC3E00-50B0-11CF-960C-0080C7F4EE85</span><span class="sxs-lookup"><span data-stu-id="07119-217">08EC3E00-50B0-11CF-960C-0080C7F4EE85</span></span> |
| [<span data-ttu-id="07119-218">**FolderItemVerbs**</span><span class="sxs-lookup"><span data-stu-id="07119-218">**FolderItemVerbs**</span></span>](folderitemverbs.md)              | <span data-ttu-id="07119-219">1F8352C0-50B0-11CF-960C-0080C7F4EE85</span><span class="sxs-lookup"><span data-stu-id="07119-219">1F8352C0-50B0-11CF-960C-0080C7F4EE85</span></span> |
| [<span data-ttu-id="07119-220">**IShellDispatch2**</span><span class="sxs-lookup"><span data-stu-id="07119-220">**IShellDispatch2**</span></span>](ishelldispatch2-object.md)       | <span data-ttu-id="07119-221">A4C6892C-3BA9-11d2-9DEA-00C04FB16162</span><span class="sxs-lookup"><span data-stu-id="07119-221">A4C6892C-3BA9-11d2-9DEA-00C04FB16162</span></span> |
| [<span data-ttu-id="07119-222">**IShellLinkDual2**</span><span class="sxs-lookup"><span data-stu-id="07119-222">**IShellLinkDual2**</span></span>](ishelllinkdual2-object.md)       | <span data-ttu-id="07119-223">317EE249-F12E-11d2-B1E4-00C04F8EEB3E</span><span class="sxs-lookup"><span data-stu-id="07119-223">317EE249-F12E-11d2-B1E4-00C04F8EEB3E</span></span> |
| [<span data-ttu-id="07119-224">**Shell**</span><span class="sxs-lookup"><span data-stu-id="07119-224">**Shell**</span></span>](shell.md)                                  | <span data-ttu-id="07119-225">13709620-C279-11CE-A49E-444553540000</span><span class="sxs-lookup"><span data-stu-id="07119-225">13709620-C279-11CE-A49E-444553540000</span></span> |
| [<span data-ttu-id="07119-226">**ShellFolderItem**</span><span class="sxs-lookup"><span data-stu-id="07119-226">**ShellFolderItem**</span></span>](shellfolderitem-object.md)       | <span data-ttu-id="07119-227">2fe352ea-fd1f-11d2-b1f4-00c04f8eeb3e</span><span class="sxs-lookup"><span data-stu-id="07119-227">2fe352ea-fd1f-11d2-b1f4-00c04f8eeb3e</span></span> |
| [<span data-ttu-id="07119-228">**ShellFolderView**</span><span class="sxs-lookup"><span data-stu-id="07119-228">**ShellFolderView**</span></span>](shellfolderview.md)              | <span data-ttu-id="07119-229">62112AA1-EBE4-11cf-A5FB-0020AFE7292D</span><span class="sxs-lookup"><span data-stu-id="07119-229">62112AA1-EBE4-11cf-A5FB-0020AFE7292D</span></span> |
| [<span data-ttu-id="07119-230">**ShellFolderViewOC**</span><span class="sxs-lookup"><span data-stu-id="07119-230">**ShellFolderViewOC**</span></span>](shellfolderviewoc-object.md)   | <span data-ttu-id="07119-231">4a3df050-23bd-11d2-939f-00a0c91eedba</span><span class="sxs-lookup"><span data-stu-id="07119-231">4a3df050-23bd-11d2-939f-00a0c91eedba</span></span> |
| [<span data-ttu-id="07119-232">**ShellLinkObject**</span><span class="sxs-lookup"><span data-stu-id="07119-232">**ShellLinkObject**</span></span>](shelllinkobject-object.md)       | <span data-ttu-id="07119-233">11219420-1768-11d1-95BE-00609797EA4F</span><span class="sxs-lookup"><span data-stu-id="07119-233">11219420-1768-11d1-95BE-00609797EA4F</span></span> |
| [<span data-ttu-id="07119-234">**ShellUIHelper**</span><span class="sxs-lookup"><span data-stu-id="07119-234">**ShellUIHelper**</span></span>](shelluihelper.md)                  | <span data-ttu-id="07119-235">64AB4BB7-111E-11D1-8F79-00C04FC2FBE1</span><span class="sxs-lookup"><span data-stu-id="07119-235">64AB4BB7-111E-11D1-8F79-00C04FC2FBE1</span></span> |
| [<span data-ttu-id="07119-236">**ShellWindows**</span><span class="sxs-lookup"><span data-stu-id="07119-236">**ShellWindows**</span></span>](shellwindows.md)                    | <span data-ttu-id="07119-237">9BA05972-F6A8-11CF-A442-00A0C90A8F39</span><span class="sxs-lookup"><span data-stu-id="07119-237">9BA05972-F6A8-11CF-A442-00A0C90A8F39</span></span> |
| [<span data-ttu-id="07119-238">**WebViewFolderContents**</span><span class="sxs-lookup"><span data-stu-id="07119-238">**WebViewFolderContents**</span></span>](../lwef/webviewfoldercontents.md) | <span data-ttu-id="07119-239">1820FED0-473E-11D0-A96C-00C04FD705A2</span><span class="sxs-lookup"><span data-stu-id="07119-239">1820FED0-473E-11D0-A96C-00C04FD705A2</span></span> |



 

## <a name="shell-object"></a><span data-ttu-id="07119-240">Objeto Shell</span><span class="sxs-lookup"><span data-stu-id="07119-240">Shell Object</span></span>

<span data-ttu-id="07119-241">O objeto [**shell**](shell.md) representa os objetos no Shell.</span><span class="sxs-lookup"><span data-stu-id="07119-241">The [**Shell**](shell.md) object represents the objects in the Shell.</span></span> <span data-ttu-id="07119-242">Você pode usar os métodos expostos pelo objeto Shell para:</span><span class="sxs-lookup"><span data-stu-id="07119-242">You can use the methods exposed by the Shell object to:</span></span>

-   <span data-ttu-id="07119-243">Abra, explore e procure pastas.</span><span class="sxs-lookup"><span data-stu-id="07119-243">Open, explore, and browse for folders.</span></span>
-   <span data-ttu-id="07119-244">Minimizar, restaurar, colocar em cascata ou janelas abertas.</span><span class="sxs-lookup"><span data-stu-id="07119-244">Minimize, restore, cascade, or tile open windows.</span></span>
-   <span data-ttu-id="07119-245">Inicie aplicativos do painel de controle.</span><span class="sxs-lookup"><span data-stu-id="07119-245">Launch Control Panel applications.</span></span>
-   <span data-ttu-id="07119-246">Exibir caixas de diálogo do sistema.</span><span class="sxs-lookup"><span data-stu-id="07119-246">Display system dialog boxes.</span></span>

<span data-ttu-id="07119-247">Os usuários talvez estejam mais familiarizados com os comandos que acessam no menu **Iniciar** e no menu de atalho da barra de tarefas.</span><span class="sxs-lookup"><span data-stu-id="07119-247">Users are perhaps most familiar with the commands they access from the **Start** menu and the taskbar's shortcut menu.</span></span> <span data-ttu-id="07119-248">O menu de atalho da barra de tarefas aparece quando os usuários clicam com o botão direito na barra de tarefas.</span><span class="sxs-lookup"><span data-stu-id="07119-248">The taskbar's shortcut menu appears when users right-click the taskbar.</span></span> <span data-ttu-id="07119-249">O HTA (aplicativo HTML) a seguir produz uma página inicial com botões que implementam muitos dos métodos do objeto [**shell**](shell.md) .</span><span class="sxs-lookup"><span data-stu-id="07119-249">The following HTML Application (HTA) produces a start page with buttons that implement many of the [**Shell**](shell.md) object's methods.</span></span> <span data-ttu-id="07119-250">Alguns desses métodos implementam recursos no menu **Iniciar** e no menu de atalho da barra de tarefas.</span><span class="sxs-lookup"><span data-stu-id="07119-250">Some of these methods implement features on the **Start** menu and the taskbar's shortcut menu.</span></span>


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



### <a name="security"></a><span data-ttu-id="07119-251">Segurança</span><span class="sxs-lookup"><span data-stu-id="07119-251">Security</span></span>

<span data-ttu-id="07119-252">Como um aplicativo, um HTA é executado em um modelo de segurança diferente de uma página da Web.</span><span class="sxs-lookup"><span data-stu-id="07119-252">As an application, an HTA runs under a different security model than a webpage.</span></span> <span data-ttu-id="07119-253">para interagir com uma página da web que implementa a funcionalidade dos objetos do Shell, os usuários devem habilitar os **controles de ActiveX de inicialização e script não marcados como seguros** para a zona de segurança na qual estão exibindo a página.</span><span class="sxs-lookup"><span data-stu-id="07119-253">To interact with a webpage that implements the functionality of the Shell objects, users must enable the **Initialize and script ActiveX Controls not marked as safe** option for the security zone in which they are viewing the page.</span></span>

## <a name="folder-objects"></a><span data-ttu-id="07119-254">Objetos de pasta</span><span class="sxs-lookup"><span data-stu-id="07119-254">Folder Objects</span></span>

<span data-ttu-id="07119-255">O objeto [**Folder**](folder.md) representa uma pasta Shell.</span><span class="sxs-lookup"><span data-stu-id="07119-255">The [**Folder**](folder.md) object represents a Shell folder.</span></span> <span data-ttu-id="07119-256">Você pode usar os métodos expostos pelo objeto Folder para:</span><span class="sxs-lookup"><span data-stu-id="07119-256">You can use the methods exposed by the Folder object to:</span></span>

-   <span data-ttu-id="07119-257">Obter informações sobre uma pasta.</span><span class="sxs-lookup"><span data-stu-id="07119-257">Get information about a folder.</span></span>
-   <span data-ttu-id="07119-258">Criar subpastas.</span><span class="sxs-lookup"><span data-stu-id="07119-258">Create subfolders.</span></span>
-   <span data-ttu-id="07119-259">Copie e mova objetos de arquivo para a pasta.</span><span class="sxs-lookup"><span data-stu-id="07119-259">Copy and move file objects into the folder.</span></span>

<span data-ttu-id="07119-260">O objeto [**FolderItem**](folderitem.md) representa um item em uma pasta do Shell.</span><span class="sxs-lookup"><span data-stu-id="07119-260">The [**FolderItem**](folderitem.md) object represents an item in a Shell folder.</span></span> <span data-ttu-id="07119-261">Suas propriedades permitem que você recupere informações sobre o item.</span><span class="sxs-lookup"><span data-stu-id="07119-261">Its properties enable you to retrieve information about the item.</span></span> <span data-ttu-id="07119-262">Você pode usar os métodos expostos por esse objeto para executar os verbos de um item ou para recuperar informações sobre o objeto [**FolderItemVerbs**](folderitemverbs.md) de um item.</span><span class="sxs-lookup"><span data-stu-id="07119-262">You can use the methods exposed by this object to run an item's verbs, or to retrieve information about an item's [**FolderItemVerbs**](folderitemverbs.md) object.</span></span>

<span data-ttu-id="07119-263">O objeto [**FolderItems**](folderitems.md) representa uma coleção de itens em uma pasta do Shell.</span><span class="sxs-lookup"><span data-stu-id="07119-263">The [**FolderItems**](folderitems.md) object represents a collection of items in a Shell folder.</span></span> <span data-ttu-id="07119-264">Seus métodos e propriedades permitem que você recupere informações sobre a coleção.</span><span class="sxs-lookup"><span data-stu-id="07119-264">Its methods and properties enable you to retrieve information about the collection.</span></span>

<span data-ttu-id="07119-265">o exemplo a seguir Visual Basic mostra a relação entre vários objetos de pasta e como eles podem ser usados juntos.</span><span class="sxs-lookup"><span data-stu-id="07119-265">The following Visual Basic example shows the relationship between several of the folder objects and how they can be used together.</span></span> <span data-ttu-id="07119-266">Quando o usuário clica no botão de comando chamado **cmdGetPath**, o programa exibe uma caixa de diálogo que permite ao usuário selecionar uma pasta de **meu computador**, em que ssfDRIVES é o valor de enumeração [**ShellSpecialFolderConstants**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) para **meu computador**.</span><span class="sxs-lookup"><span data-stu-id="07119-266">When the user clicks the command button called **cmdGetPath**, the program displays a dialog box that enables the user to select a folder from **My Computer**, where ssfDRIVES is the [**ShellSpecialFolderConstants**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) enumeration value for **My Computer**.</span></span> <span data-ttu-id="07119-267">Quando o usuário escolhe uma pasta, o caminho da pasta é exibido na caixa de texto chamada **txtPath**.</span><span class="sxs-lookup"><span data-stu-id="07119-267">When the user chooses a folder, the folder's path is displayed in the text box called **txtPath**.</span></span>


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



<span data-ttu-id="07119-268">No VBScript, essa função é ligeiramente diferente porque os valores de enumeração [**ShellSpecialFolderConstants**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) não estão disponíveis no script.</span><span class="sxs-lookup"><span data-stu-id="07119-268">In VBScript, this function is slightly different because the [**ShellSpecialFolderConstants**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) enumeration values are not available in script.</span></span> <span data-ttu-id="07119-269">O exemplo a seguir mostra o VBScript equivalente do exemplo anterior.</span><span class="sxs-lookup"><span data-stu-id="07119-269">The following example shows the VBScript equivalent of the previous example.</span></span>


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



<span data-ttu-id="07119-270">no exemplo a seguir JScript, que é uma tradução direta do exemplo anterior do VBScript, observe como os parênteses vazios ' () ' são usados para invocar os [**itens**](folder-items.md) e os métodos de [**Item**](folderitems-item.md) .</span><span class="sxs-lookup"><span data-stu-id="07119-270">In the following JScript example, which is a direct translation of the preceding VBScript example, note how the empty parentheses '()' are used to invoke the [**Items**](folder-items.md) and [**Item**](folderitems-item.md) methods.</span></span>


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



 

 
