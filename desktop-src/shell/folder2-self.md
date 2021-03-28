---
description: Contém o objeto FolderItem da pasta.
ms.assetid: 0964505d-4138-4444-91d4-46c707c45688
title: Folder2. Self Property (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Folder2.Self
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: f49666096f35f9871f8a3b3c141d4bc169dea0c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164179"
---
# <a name="folder2self-property"></a><span data-ttu-id="ca7b2-103">Propriedade Pasta2. Self</span><span class="sxs-lookup"><span data-stu-id="ca7b2-103">Folder2.Self property</span></span>

<span data-ttu-id="ca7b2-104">Contém o objeto [**FolderItem**](folderitem.md) da pasta.</span><span class="sxs-lookup"><span data-stu-id="ca7b2-104">Contains the folder's [**FolderItem**](folderitem.md) object.</span></span>

<span data-ttu-id="ca7b2-105">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="ca7b2-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="ca7b2-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ca7b2-106">Syntax</span></span>


```JScript
Self = Folder2.Self
```



## <a name="property-value"></a><span data-ttu-id="ca7b2-107">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="ca7b2-107">Property value</span></span>

<span data-ttu-id="ca7b2-108">O objeto que é avaliado para o objeto [**FolderItem**](folderitem.md) da pasta.</span><span class="sxs-lookup"><span data-stu-id="ca7b2-108">The object that evaluates to the folder's [**FolderItem**](folderitem.md) object.</span></span>

## <a name="examples"></a><span data-ttu-id="ca7b2-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="ca7b2-109">Examples</span></span>

<span data-ttu-id="ca7b2-110">O exemplo a seguir usa **Self** para recuperar o [**FolderItem**](folderitem.md) para a pasta C: \\ Windows.</span><span class="sxs-lookup"><span data-stu-id="ca7b2-110">The following example uses **Self** to retrieve the [**FolderItem**](folderitem.md) for the C:\\Windows folder.</span></span> <span data-ttu-id="ca7b2-111">O uso adequado é mostrado para JScript, VBScript e Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="ca7b2-111">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="ca7b2-112">JScript</span><span class="sxs-lookup"><span data-stu-id="ca7b2-112">JScript:</span></span>


```JScript
<script language="JScript">
    function fnFolder2ObjectSelfJ()
    {
        var objShell  = new ActiveXObject("shell.application");
        var objFolder2 = new Object;
        
        objFolder2 = objShell.NameSpace("C:\\WINDOWS");
        if (objFolder2 != null)
        {
            var objFolderItem = new Object;
            
            objFolderItem = objFolder2.Self;
            if (objFolderItem != null)
            {
                //Add code here.
            }
        }
    }
</script>
```



<span data-ttu-id="ca7b2-113">VBScript</span><span class="sxs-lookup"><span data-stu-id="ca7b2-113">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnFolder2ObjectSelfVB()
        dim objShell
        dim objFolder2

        set objShell = CreateObject("shell.application")
        set objFolder2 = objShell.NameSpace("C:\WINDOWS")

        if (not objFolder2 is nothing) then
            dim objFolderItem
            
            set objFolderItem = objFolder2.Self

            if (not objFolderItem is nothing) then
                'Add code here.
            end if
        end if

        set objFolder2 = nothing
        set objShell = nothing
    end function
</script>
```



<span data-ttu-id="ca7b2-114">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="ca7b2-114">Visual Basic:</span></span>


```VB
Private Sub btnFolder2Self_Click()
    Dim objShell   As Shell
    Dim objFolder2 As Folder2

    Set objShell = New Shell
    Set objFolder2 = objShell.NameSpace("C:\WINDOWS")

    If (Not objFolder2 Is Nothing) Then
        Dim objFolderItem As FolderItem
        
        Set objFolderItem = objFolder2.Self()

        If (Not objFolderItem Is Nothing) Then
            'Add code here.
        End If

        Set objFolderItem = Nothing
    End If

    Set objFolder2 = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="ca7b2-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ca7b2-115">Requirements</span></span>



| <span data-ttu-id="ca7b2-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="ca7b2-116">Requirement</span></span> | <span data-ttu-id="ca7b2-117">Valor</span><span class="sxs-lookup"><span data-stu-id="ca7b2-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ca7b2-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ca7b2-118">Minimum supported client</span></span><br/> | <span data-ttu-id="ca7b2-119">Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="ca7b2-119">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ca7b2-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ca7b2-120">Minimum supported server</span></span><br/> | <span data-ttu-id="ca7b2-121">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="ca7b2-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="ca7b2-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ca7b2-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="ca7b2-123"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="ca7b2-123"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="ca7b2-124">INSERI</span><span class="sxs-lookup"><span data-stu-id="ca7b2-124">IDL</span></span><br/>                      | <dl> <span data-ttu-id="ca7b2-125"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="ca7b2-125"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="ca7b2-126">DLL</span><span class="sxs-lookup"><span data-stu-id="ca7b2-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ca7b2-127"><dt>Shell32.dll (versão 5,0 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="ca7b2-127"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ca7b2-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="ca7b2-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ca7b2-129">**Pasta2**</span><span class="sxs-lookup"><span data-stu-id="ca7b2-129">**Folder2**</span></span>](folder2-object.md)
</dt> <dt>

[<span data-ttu-id="ca7b2-130">**Pasta**</span><span class="sxs-lookup"><span data-stu-id="ca7b2-130">**Folder**</span></span>](folder.md)
</dt> </dl>

 

 




