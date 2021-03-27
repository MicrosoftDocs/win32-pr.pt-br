---
description: Obtém ou define o estado de exibição inicial (dimensionado, minimizado ou maximizado) do comando do link.
ms.assetid: 139c6924-f554-4fde-9ed0-bc117bafbb16
title: Propriedade ShellLinkObject. AddCommand (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellLinkObject.ShowCommand
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 9bacdf98a24d749b5128bc286f06e99299aef437
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104989104"
---
# <a name="shelllinkobjectshowcommand-property"></a><span data-ttu-id="c714c-103">Propriedade ShellLinkObject. AddCommand</span><span class="sxs-lookup"><span data-stu-id="c714c-103">ShellLinkObject.ShowCommand property</span></span>

<span data-ttu-id="c714c-104">Obtém ou define o estado de exibição inicial (dimensionado, minimizado ou maximizado) do comando do link.</span><span class="sxs-lookup"><span data-stu-id="c714c-104">Gets or sets the initial display state (sized, minimized, or maximized) of the link's command.</span></span>

<span data-ttu-id="c714c-105">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="c714c-105">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="c714c-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="c714c-106">Syntax</span></span>


```JScript
iShowCommand = ShellLinkObject.ShowCommand
ShellLinkObject.ShowCommand(intShowCommand) = iShowCommand
```



## <a name="property-value"></a><span data-ttu-id="c714c-107">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="c714c-107">Property value</span></span>

<span data-ttu-id="c714c-108">o estado de exibição do link.</span><span class="sxs-lookup"><span data-stu-id="c714c-108">the link's display state.</span></span> <span data-ttu-id="c714c-109">Esse valor pode ser um dos seguintes:</span><span class="sxs-lookup"><span data-stu-id="c714c-109">This can be one of the following values:</span></span>

<dt>



 <span data-ttu-id="c714c-110">(1)</span><span class="sxs-lookup"><span data-stu-id="c714c-110">(1)</span></span>


</dt> <dd>

<span data-ttu-id="c714c-111">Ativa e exibe uma janela.</span><span class="sxs-lookup"><span data-stu-id="c714c-111">Activates and displays a window.</span></span> <span data-ttu-id="c714c-112">Se a janela for minimizada ou maximizada, o sistema a restaurará para seu tamanho e posição originais.</span><span class="sxs-lookup"><span data-stu-id="c714c-112">If the window is minimized or maximized, the system restores it to its original size and position.</span></span>

</dd> <dt>



 <span data-ttu-id="c714c-113">(2)</span><span class="sxs-lookup"><span data-stu-id="c714c-113">(2)</span></span>


</dt> <dd>

<span data-ttu-id="c714c-114">Ativa a janela e a exibe como uma janela minimizada.</span><span class="sxs-lookup"><span data-stu-id="c714c-114">Activates the window and displays it as a minimized window.</span></span>

</dd> <dt>



 <span data-ttu-id="c714c-115">(3)</span><span class="sxs-lookup"><span data-stu-id="c714c-115">(3)</span></span>


</dt> <dd>

<span data-ttu-id="c714c-116">Ativa a janela e a exibe como uma janela maximizada.</span><span class="sxs-lookup"><span data-stu-id="c714c-116">Activates the window and displays it as a maximized window.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="c714c-117">Exemplos</span><span class="sxs-lookup"><span data-stu-id="c714c-117">Examples</span></span>

<span data-ttu-id="c714c-118">O exemplo a seguir mostra o uso apropriado dessa propriedade em JScript, VBScript e Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="c714c-118">The following example shows the proper usage of this property in JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="c714c-119">JScript</span><span class="sxs-lookup"><span data-stu-id="c714c-119">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellShellLinkObjectShowCommandJ()
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
                    var nShow;
                    
                    // Get the ShowCommand for the ShellLinkObject.
                    nShow = objShellLink.ShowCommand;
                    alert(nShow);
                    
                    // Set the ShowCommand for the ShellLinkObject.
                    objShellLink.ShowCommand = 1
                }
            }
        }
    }
</script>
```



<span data-ttu-id="c714c-120">VBScript</span><span class="sxs-lookup"><span data-stu-id="c714c-120">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellLinkObjectShowCommandVB()
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
                                dim nShow
                                
                                'Get the ShowCommand for the ShellLinkObject.
                                nShow = objShellLink.ShowCommand
                                alert(nShow)
                                
                                'Set the ShowCommand for the ShellLinkObject.
                                objShellLink.ShowCommand = 1
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



<span data-ttu-id="c714c-121">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="c714c-121">Visual Basic:</span></span>


```VB
Private Sub fnShellLinkObjectShowCommandVB()
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
                            Dim nShow As Integer
                            
                            'Get the ShowCommand for the ShellLinkObject.
                            nShow = objShellLink.ShowCommand
                            Debug.Print nShow
                            
                            'Set the ShowCommand for the ShellLinkObject.
                            objShellLink.ShowCommand = 1
                        End If
                    Set objShellLink = Nothing
                End If
            Set objFolderItem = Nothing
        End If
    Set objFolder = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="c714c-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c714c-122">Requirements</span></span>



| <span data-ttu-id="c714c-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="c714c-123">Requirement</span></span> | <span data-ttu-id="c714c-124">Valor</span><span class="sxs-lookup"><span data-stu-id="c714c-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c714c-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c714c-125">Minimum supported client</span></span><br/> | <span data-ttu-id="c714c-126">Somente aplicativos de área de trabalho do Windows 2000 Professional com SP3 \[\]</span><span class="sxs-lookup"><span data-stu-id="c714c-126">Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="c714c-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c714c-127">Minimum supported server</span></span><br/> | <span data-ttu-id="c714c-128">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="c714c-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="c714c-129">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="c714c-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="c714c-130"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="c714c-130"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="c714c-131">INSERI</span><span class="sxs-lookup"><span data-stu-id="c714c-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="c714c-132"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="c714c-132"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="c714c-133">DLL</span><span class="sxs-lookup"><span data-stu-id="c714c-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c714c-134"><dt>Shell32.dll (versão 5,0 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="c714c-134"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 




