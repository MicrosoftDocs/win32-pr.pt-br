---
description: Contém o objeto ShellLinkObject do item, se o item for um atalho.
ms.assetid: 6444476a-a065-4f69-9330-584e30dbe30d
title: Propriedade FolderItem. GetLink (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FolderItem.GetLink
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: d12c0fbd296610174c8b8363602288f59fcb9714
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089722"
---
# <a name="folderitemgetlink-property"></a><span data-ttu-id="88d9b-103">Propriedade FolderItem. GetLink</span><span class="sxs-lookup"><span data-stu-id="88d9b-103">FolderItem.GetLink property</span></span>

<span data-ttu-id="88d9b-104">Contém o objeto [**ShellLinkObject**](shelllinkobject-object.md) do item, se o item for um atalho.</span><span class="sxs-lookup"><span data-stu-id="88d9b-104">Contains the item's [**ShellLinkObject**](shelllinkobject-object.md) object, if the item is a shortcut.</span></span>

<span data-ttu-id="88d9b-105">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="88d9b-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="88d9b-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="88d9b-106">Syntax</span></span>


```JScript
objGetLink = FolderItem.GetLink
```



## <a name="property-value"></a><span data-ttu-id="88d9b-107">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="88d9b-107">Property value</span></span>

<span data-ttu-id="88d9b-108">Uma variável do tipo [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) que recebe o objeto [**ShellLinkObject**](shelllinkobject-object.md) .</span><span class="sxs-lookup"><span data-stu-id="88d9b-108">A variable of type [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) that receives the [**ShellLinkObject**](shelllinkobject-object.md) object.</span></span>

## <a name="examples"></a><span data-ttu-id="88d9b-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="88d9b-109">Examples</span></span>

<span data-ttu-id="88d9b-110">O exemplo a seguir usa **GetLink** para recuperar o objeto [**ShellLinkObject**](shelllinkobject-object.md) para um atalho para o Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="88d9b-110">The following example uses **GetLink** to retrieve the [**ShellLinkObject**](shelllinkobject-object.md) object for a shortcut to Internet Explorer.</span></span> <span data-ttu-id="88d9b-111">O uso adequado é mostrado para JScript, VBScript e Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="88d9b-111">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="88d9b-112">JScript</span><span class="sxs-lookup"><span data-stu-id="88d9b-112">JScript:</span></span>


```JScript
<script language="JScript">
    function fnGetLinkJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var objFolder2;
        var ssfPROGRAMS = 2;
        
        objFolder2 = objShell.NameSpace(ssfPROGRAMS);
        if (objFolder2 != null)
        {
            var objFolderItem;
            
            objFolderItem = objFolder2.ParseName("Internet Explorer.lnk");
            if (objFolderItem != null)
            {
                var objLink;
                
                objLink = objFolderItem.GetLink;
                if (objLink != null)
                {
                    // Add code here
                }
            }
        }
    }
</script>
```



<span data-ttu-id="88d9b-113">VBScript</span><span class="sxs-lookup"><span data-stu-id="88d9b-113">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnGetLinkVB()
        dim objShell
        dim bReturn

        set objShell = CreateObject("shell.application")
        if (not objShell is nothing) then
            dim objFolder2
            dim ssfPROGRAMS
                
            ssfPROGRAMS = 2
            set objFolder2 = objShell.NameSpace(ssfPROGRAMS)
            if (not objFolder2 is nothing) then
                dim objFolderItem
                        
                set objFolderItem = objFolder2.ParseName("Internet Explorer.lnk")
                if (not objFolderItem is nothing) then
                    dim objLink
                                
                    set objLink = objFolderItem.GetLink
                    if (not objLink is nothing) then
                        'Add code here          
                    end if
                    set objLink = nothing
                end if
                set objFolderItem = nothing
            end if
            set objFolder2 = nothing
        end if
        set objShell = nothing
    end function
</script>
```



<span data-ttu-id="88d9b-114">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="88d9b-114">Visual Basic:</span></span>


```VB
Private Sub fnGetLinkVB()
    Dim objShell   As Shell
    Dim objFolder2 As Folder2
    Dim ssfPROGRAMS As Long
    
    ssfPROGRAMS = 2
    Set objShell = New Shell
    Set objFolder2 = objShell.NameSpace(ssfPROGRAMS)
        If (Not objFolder2 Is Nothing) Then
            Dim objFolderItem As FolderItem
            
            Set objFolderItem = objFolder2.ParseName("Internet Explorer.lnk")
                If (Not objFolderItem Is Nothing) Then
                    Dim objLink As ShellLinkObject
                    
                    Set objLink = objFolderItem.GetLink
                        If (Not objLink Is Nothing) Then
                            'Add code here
                        Else
                            'Folder object returned nothing
                        End If
                    Set objLink = Nothing
                Else
                    'FolderItem object returned nothing.
                End If
            Set objFolderItem = Nothing
        Else
            'Folder object returned nothing.
        End If
    Set objFolder2 = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="88d9b-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="88d9b-115">Requirements</span></span>



| <span data-ttu-id="88d9b-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="88d9b-116">Requirement</span></span> | <span data-ttu-id="88d9b-117">Valor</span><span class="sxs-lookup"><span data-stu-id="88d9b-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="88d9b-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="88d9b-118">Minimum supported client</span></span><br/> | <span data-ttu-id="88d9b-119">Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="88d9b-119">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="88d9b-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="88d9b-120">Minimum supported server</span></span><br/> | <span data-ttu-id="88d9b-121">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="88d9b-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="88d9b-122">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="88d9b-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="88d9b-123"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="88d9b-123"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="88d9b-124">INSERI</span><span class="sxs-lookup"><span data-stu-id="88d9b-124">IDL</span></span><br/>                      | <dl> <span data-ttu-id="88d9b-125"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="88d9b-125"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="88d9b-126">DLL</span><span class="sxs-lookup"><span data-stu-id="88d9b-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="88d9b-127"><dt>Shell32.dll (versão 4,71 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="88d9b-127"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="88d9b-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="88d9b-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="88d9b-129">**FolderItem**</span><span class="sxs-lookup"><span data-stu-id="88d9b-129">**FolderItem**</span></span>](folderitem.md)
</dt> <dt>

[<span data-ttu-id="88d9b-130">**IsLink**</span><span class="sxs-lookup"><span data-stu-id="88d9b-130">**IsLink**</span></span>](folderitem-islink.md)
</dt> </dl>

 

 
