---
description: Indica se o item é uma pasta.
ms.assetid: fb080c8f-04b1-4f9a-9219-0951a2e950ea
title: Propriedade FolderItem. IsFolder (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FolderItem.IsFolder
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 9bf0bd4eb9b7964620fe705d6e8f4d10644ca234
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967276"
---
# <a name="folderitemisfolder-property"></a><span data-ttu-id="1d253-103">Propriedade FolderItem. IsFolder</span><span class="sxs-lookup"><span data-stu-id="1d253-103">FolderItem.IsFolder property</span></span>

<span data-ttu-id="1d253-104">Indica se o item é uma pasta.</span><span class="sxs-lookup"><span data-stu-id="1d253-104">Indicates if the item is a folder.</span></span>

<span data-ttu-id="1d253-105">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="1d253-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="1d253-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1d253-106">Syntax</span></span>


```JScript
bIsFolder = FolderItem.IsFolder
```



## <a name="property-value"></a><span data-ttu-id="1d253-107">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="1d253-107">Property value</span></span>

<span data-ttu-id="1d253-108">Um **booliano** que recebe **true** se o item for uma pasta ou **false** se não.</span><span class="sxs-lookup"><span data-stu-id="1d253-108">A **Boolean** that receives **true** if the item is a folder or **false** if not.</span></span>

## <a name="examples"></a><span data-ttu-id="1d253-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="1d253-109">Examples</span></span>

<span data-ttu-id="1d253-110">O exemplo a seguir usa **IsFolder** para determinar se o diretório do Windows é uma pasta.</span><span class="sxs-lookup"><span data-stu-id="1d253-110">The following example uses **IsFolder** to determine whether the Windows directory is a folder.</span></span> <span data-ttu-id="1d253-111">O uso adequado é mostrado para JScript, VBScript e Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="1d253-111">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="1d253-112">JScript</span><span class="sxs-lookup"><span data-stu-id="1d253-112">JScript:</span></span>


```JScript
<script language="JScript">
    function fnIsFolderJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var objFolder2;
        var ssfWINDOWS = 36;
        
        objFolder2 = objShell.NameSpace(ssfWINDOWS);
        if (objFolder2 != null)
        {
            var objFolderItem;
            
            objFolderItem = objFolder2.Self;
            if (objFolderItem != null)
            {
                var bReturn;
                
                bReturn = objFolderItem.IsFolder;
            }
        }
    }
</script>
```



<span data-ttu-id="1d253-113">VBScript</span><span class="sxs-lookup"><span data-stu-id="1d253-113">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnIsFolderVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        if (not objShell is nothing) then
            dim objFolder2
            dim ssfWINDOWS
                
            ssfWINDOWS = 36
            set objFolder2 = objShell.NameSpace(ssfWINDOWS)
            if (not objFolder2 is nothing) then
                dim objFolderItem
                        
                set objFolderItem = objFolder2.Self
                if (not objFolderItem is nothing) then
                    dim bReturn
                                
                    bReturn = objFolderItem.IsFolder
                end if
                set objFolderItem = nothing
            end if
            set objFolder2 = nothing
        end if
        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="1d253-114">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="1d253-114">Visual Basic:</span></span>


```VB
Private Sub fnIsFolderVB()
    Dim objShell   As Shell
    Dim objFolder2 As Folder2
    Dim ssfWINDOWS As Long
    
    ssfWINDOWS = 36
    Set objShell = New Shell
    Set objFolder2 = objShell.NameSpace(ssfWINDOWS)
        If (Not objFolder2 Is Nothing) Then
            Dim objFolderItem As FolderItem
            
            Set objFolderItem = objFolder2.Self
                If (Not objFolderItem Is Nothing) Then
                    Dim bReturn As Boolean
                    
                    bReturn = objFolderItem.IsFolder
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



## <a name="requirements"></a><span data-ttu-id="1d253-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1d253-115">Requirements</span></span>



| <span data-ttu-id="1d253-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="1d253-116">Requirement</span></span> | <span data-ttu-id="1d253-117">Valor</span><span class="sxs-lookup"><span data-stu-id="1d253-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1d253-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1d253-118">Minimum supported client</span></span><br/> | <span data-ttu-id="1d253-119">Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="1d253-119">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="1d253-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1d253-120">Minimum supported server</span></span><br/> | <span data-ttu-id="1d253-121">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="1d253-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="1d253-122">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="1d253-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="1d253-123"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="1d253-123"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="1d253-124">INSERI</span><span class="sxs-lookup"><span data-stu-id="1d253-124">IDL</span></span><br/>                      | <dl> <span data-ttu-id="1d253-125"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="1d253-125"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="1d253-126">DLL</span><span class="sxs-lookup"><span data-stu-id="1d253-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1d253-127"><dt>Shell32.dll (versão 4,71 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="1d253-127"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




