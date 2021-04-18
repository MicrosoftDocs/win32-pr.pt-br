---
description: Obtém ou define o atalho de teclado para o link.
ms.assetid: edc65fe8-c7f3-46d0-86ca-1c0c93e7ca64
title: Propriedade ShellLinkObject. tecla de atalho (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellLinkObject.Hotkey
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 23ab8615421eee7289e5f0bb58582bf8e0d48f17
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104968161"
---
# <a name="shelllinkobjecthotkey-property"></a><span data-ttu-id="33d54-103">Propriedade ShellLinkObject. tecla de atalho</span><span class="sxs-lookup"><span data-stu-id="33d54-103">ShellLinkObject.Hotkey property</span></span>

<span data-ttu-id="33d54-104">Obtém ou define o atalho de teclado para o link.</span><span class="sxs-lookup"><span data-stu-id="33d54-104">Gets or sets the keyboard shortcut for the link.</span></span>

<span data-ttu-id="33d54-105">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="33d54-105">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="33d54-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="33d54-106">Syntax</span></span>


```JScript
iHotkey = ShellLinkObject.Hotkey
ShellLinkObject.Hotkey(iHotkey) = iHotkey
```



## <a name="property-value"></a><span data-ttu-id="33d54-107">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="33d54-107">Property value</span></span>

<span data-ttu-id="33d54-108">o atalho de teclado do link.</span><span class="sxs-lookup"><span data-stu-id="33d54-108">the link's keyboard shortcut.</span></span> <span data-ttu-id="33d54-109">O atalho de teclado virtual está no byte de ordem inferior e os sinalizadores de modificador estão no byte de ordem superior.</span><span class="sxs-lookup"><span data-stu-id="33d54-109">The virtual keyboard shortcut is in the low-order byte, and the modifier flags are in the high-order byte.</span></span> <span data-ttu-id="33d54-110">Os sinalizadores de modificadores podem ser uma combinação dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="33d54-110">The modifier flags can be a combination of the following values.</span></span>

<dt>



 <span data-ttu-id="33d54-111">(1)</span><span class="sxs-lookup"><span data-stu-id="33d54-111">(1)</span></span>


</dt> <dd>

<span data-ttu-id="33d54-112">Tecla SHIFT</span><span class="sxs-lookup"><span data-stu-id="33d54-112">SHIFT key</span></span>

</dd> <dt>



 <span data-ttu-id="33d54-113">(2)</span><span class="sxs-lookup"><span data-stu-id="33d54-113">(2)</span></span>


</dt> <dd>

<span data-ttu-id="33d54-114">Tecla CTRL</span><span class="sxs-lookup"><span data-stu-id="33d54-114">CTRL key</span></span>

</dd> <dt>



 <span data-ttu-id="33d54-115">(4)</span><span class="sxs-lookup"><span data-stu-id="33d54-115">(4)</span></span>


</dt> <dd>

<span data-ttu-id="33d54-116">tecla ALT</span><span class="sxs-lookup"><span data-stu-id="33d54-116">ALT key</span></span>

</dd> <dt>



 <span data-ttu-id="33d54-117">(8)</span><span class="sxs-lookup"><span data-stu-id="33d54-117">(8)</span></span>


</dt> <dd>

<span data-ttu-id="33d54-118">Chave estendida</span><span class="sxs-lookup"><span data-stu-id="33d54-118">Extended key</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="33d54-119">Exemplos</span><span class="sxs-lookup"><span data-stu-id="33d54-119">Examples</span></span>

<span data-ttu-id="33d54-120">O exemplo a seguir mostra o uso apropriado dessa propriedade em JScript, VBScript e Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="33d54-120">The following example shows the proper usage of this property in JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="33d54-121">JScript</span><span class="sxs-lookup"><span data-stu-id="33d54-121">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellShellLinkObjectHotkeyJ()
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
                    var nHotkey;
                    
                    // Get the keyboard shortcut for the ShellLinkObject.
                    nHotkey = objShellLink.Hotkey;
                    alert(nHotkey);
                    
                    // Set the keyboard shortcut for the ShellLinkObject.
                    objShellLink.Hotkey = 4;
                }
            }
        }
    }
</script>
```



<span data-ttu-id="33d54-122">VBScript</span><span class="sxs-lookup"><span data-stu-id="33d54-122">VBScript:</span></span>


```VB
<script language="VBScript">
     function fnShellLinkObjectHotkeyVB()
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
                                dim nHotkey
                                
                                'Get the keyboard shortcut for the ShellLinkObject.
                                nHotkey = objShellLink.Hotkey
                                alert(nHotkey)
                                
                                'Set the keyboard shortcut for the ShellLinkObject.
                                objShellLink.Hotkey = 4
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



<span data-ttu-id="33d54-123">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="33d54-123">Visual Basic:</span></span>


```VB
Private Sub fnShellLinkObjectHotkeyVB()
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
                            Dim nHotkey As Integer
                            
                            'Get the keyboard shortcut for the ShellLinkObject.
                            nHotkey = objShellLink.Hotkey
                            Debug.Print nHotkey
                            
                            'Set the keyboard shortcut for the ShellLinkObject.
                            objShellLink.Hotkey = 4
                        End If
                    Set objShellLink = Nothing
                End If
            Set objFolderItem = Nothing
        End If
    Set objFolder = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="33d54-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="33d54-124">Requirements</span></span>



| <span data-ttu-id="33d54-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="33d54-125">Requirement</span></span> | <span data-ttu-id="33d54-126">Valor</span><span class="sxs-lookup"><span data-stu-id="33d54-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="33d54-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="33d54-127">Minimum supported client</span></span><br/> | <span data-ttu-id="33d54-128">Somente aplicativos de área de trabalho do Windows 2000 Professional com SP3 \[\]</span><span class="sxs-lookup"><span data-stu-id="33d54-128">Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="33d54-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="33d54-129">Minimum supported server</span></span><br/> | <span data-ttu-id="33d54-130">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="33d54-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="33d54-131">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="33d54-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="33d54-132"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="33d54-132"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="33d54-133">INSERI</span><span class="sxs-lookup"><span data-stu-id="33d54-133">IDL</span></span><br/>                      | <dl> <span data-ttu-id="33d54-134"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="33d54-134"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="33d54-135">DLL</span><span class="sxs-lookup"><span data-stu-id="33d54-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="33d54-136"><dt>Shell32.dll (versão 5,0 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="33d54-136"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 




