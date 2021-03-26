---
description: Obtém ou define o diretório de trabalho especificado no link.
ms.assetid: c3820deb-9f00-42a9-ab0e-c0f6389e9f29
title: Propriedade ShellLinkObject. WorkingDirectory (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellLinkObject.WorkingDirectory
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: d8788899a06179056cd871b68e4e64566bcd5ee6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104296874"
---
# <a name="shelllinkobjectworkingdirectory-property"></a><span data-ttu-id="b27e4-103">Propriedade ShellLinkObject. WorkingDirectory</span><span class="sxs-lookup"><span data-stu-id="b27e4-103">ShellLinkObject.WorkingDirectory property</span></span>

<span data-ttu-id="b27e4-104">Obtém ou define o diretório de trabalho especificado no link.</span><span class="sxs-lookup"><span data-stu-id="b27e4-104">Gets or sets the working directory specified in the link.</span></span>

<span data-ttu-id="b27e4-105">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="b27e4-105">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="b27e4-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="b27e4-106">Syntax</span></span>


```JScript
strWorkingDirectory = ShellLinkObject.WorkingDirectory
ShellLinkObject.WorkingDirectory(sWorkingDirectory) = strWorkingDirectory
```



## <a name="property-value"></a><span data-ttu-id="b27e4-107">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="b27e4-107">Property value</span></span>

<span data-ttu-id="b27e4-108">o caminho totalmente qualificado do diretório de trabalho do link.</span><span class="sxs-lookup"><span data-stu-id="b27e4-108">the fully qualified path of the link's working directory.</span></span>

## <a name="examples"></a><span data-ttu-id="b27e4-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="b27e4-109">Examples</span></span>

<span data-ttu-id="b27e4-110">O exemplo a seguir mostra o uso apropriado dessa propriedade em JScript, VBScript e Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="b27e4-110">The following example shows the proper usage of this property in JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="b27e4-111">JScript</span><span class="sxs-lookup"><span data-stu-id="b27e4-111">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellShellLinkObjectWorkingDirectoryJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var objFolder;
        var ssfPROGRAMS = 2;
        
        objFolder = objShell.NameSpace(ssfPROGRAMS);
        if (objFolder != null)
        {
            var objFolderItem;
            
            objFolderItem = objFolder.ParseName("Internet Explorer.lnk");
            if (objFolderItem != null)
            {
                var objShellLink;
                
                objShellLink = objFolderItem.GetLink;
                if (objShellLink != null)
                {
                    var szDirectory;
                    
                    // Get the working directory for the ShellLinkObject.
                    szDirectory = objShellLink.WorkingDirectory;
                    alert(szDirectory);
                    
                    // Set the working directory for the ShellLinkObject.
                    objShellLink.WorkingDirectory = "";
                }
            }
        }
    }
</script>
```



<span data-ttu-id="b27e4-112">VBScript</span><span class="sxs-lookup"><span data-stu-id="b27e4-112">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellLinkObjectWorkingDirectoryVB()
        dim objShell
        dim objFolder
        dim ssfPROGRAMS
        
        ssfPROGRAMS = 2
        set objShell = CreateObject("shell.application")
        set objFolder = objShell.NameSpace(ssfPROGRAMS)
            if (not objFolder is nothing) then
                dim objFolderItem
                
                set objFolderItem = objFolder.ParseName("Internet Explorer.lnk")
                    if (not objFolderItem is nothing) then
                        dim objShellLink
                        
                        set objShellLink = objFolderItem.GetLink
                            if (not objShellLink is nothing) then
                                dim szDirectory
                                
                                'Get the working directory.
                                szDirectory = objShellLink.WorkingDirectory
                                alert(szDirectory)
                                
                                'Set the working directory.
                                objShellLink.WorkingDirectory = ""
                            end if
                        set objShellLink = nothing
                    end if
                set objFolderItem = nothing
            end if
        set objFolder = nothing
        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="b27e4-113">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="b27e4-113">Visual Basic:</span></span>


```VB
Private Sub fnShellLinkObjectWorkingDirectoryVB()
    Dim objShell  As Shell
    Dim objFolder As Folder
    
    Set objShell = New Shell
    Set objFolder = objShell.NameSpace(ssfPROGRAMS)
        If (Not objFolder Is Nothing) Then
            Dim objFolderItem As FolderItem
            
            Set objFolderItem = objFolder.ParseName("Internet Explorer.lnk")
                If (Not objFolderItem Is Nothing) Then
                    Dim objShellLink As ShellLinkObject
                    
                    Set objShellLink = objFolderItem.GetLink
                        If (Not objShellLink Is Nothing) Then
                            Dim szDirectory As String
                            
                            'Get the working directory.
                            szDirectory = objShellLink.WorkingDirectory
                            Debug.Print szDirectory
                            
                            'Set the working directory.
                            objShellLink.WorkingDirectory = ""
                        End If
                    Set objShellLink = Nothing
                End If
            Set objFolderItem = Nothing
        End If
    Set objFolder = Nothing
    Set objShell = Nothing
```



## <a name="requirements"></a><span data-ttu-id="b27e4-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b27e4-114">Requirements</span></span>



| <span data-ttu-id="b27e4-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="b27e4-115">Requirement</span></span> | <span data-ttu-id="b27e4-116">Valor</span><span class="sxs-lookup"><span data-stu-id="b27e4-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b27e4-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b27e4-117">Minimum supported client</span></span><br/> | <span data-ttu-id="b27e4-118">Somente aplicativos de área de trabalho do Windows 2000 Professional com SP3 \[\]</span><span class="sxs-lookup"><span data-stu-id="b27e4-118">Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="b27e4-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b27e4-119">Minimum supported server</span></span><br/> | <span data-ttu-id="b27e4-120">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="b27e4-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="b27e4-121">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="b27e4-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="b27e4-122"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="b27e4-122"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="b27e4-123">INSERI</span><span class="sxs-lookup"><span data-stu-id="b27e4-123">IDL</span></span><br/>                      | <dl> <span data-ttu-id="b27e4-124"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="b27e4-124"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="b27e4-125">DLL</span><span class="sxs-lookup"><span data-stu-id="b27e4-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b27e4-126"><dt>Shell32.dll (versão 5,0 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="b27e4-126"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 




