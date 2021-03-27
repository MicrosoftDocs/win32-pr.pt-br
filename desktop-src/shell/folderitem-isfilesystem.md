---
description: Indica se o item faz parte do sistema de arquivos.
ms.assetid: 321a2109-88b5-4a41-9a67-dab3e82e95d8
title: Propriedade FolderItem. isfilesystem (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FolderItem.IsFileSystem
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 852f022e1c24fa24c158ee4eb68dca44e6f010a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967277"
---
# <a name="folderitemisfilesystem-property"></a><span data-ttu-id="d43e5-103">Propriedade FolderItem. isfilesystem</span><span class="sxs-lookup"><span data-stu-id="d43e5-103">FolderItem.IsFileSystem property</span></span>

<span data-ttu-id="d43e5-104">Indica se o item faz parte do sistema de arquivos.</span><span class="sxs-lookup"><span data-stu-id="d43e5-104">Indicates if the item is part of the file system.</span></span>

<span data-ttu-id="d43e5-105">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="d43e5-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="d43e5-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d43e5-106">Syntax</span></span>


```JScript
bIsFileSystem = FolderItem.IsFileSystem
```



## <a name="property-value"></a><span data-ttu-id="d43e5-107">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="d43e5-107">Property value</span></span>

<span data-ttu-id="d43e5-108">Um **booliano** que recebe **true** se o item fizer parte do sistema de arquivos ou **false** se não.</span><span class="sxs-lookup"><span data-stu-id="d43e5-108">A **Boolean** that receives **true** if the item is part of the file system or **false** if not.</span></span>

## <a name="examples"></a><span data-ttu-id="d43e5-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="d43e5-109">Examples</span></span>

<span data-ttu-id="d43e5-110">O exemplo a seguir usa **isfilesystem** para determinar se a pasta do Windows faz parte do sistema de arquivos.</span><span class="sxs-lookup"><span data-stu-id="d43e5-110">The following example uses **IsFileSystem** to determine whether the Windows folder is a part of the file system.</span></span> <span data-ttu-id="d43e5-111">O uso adequado é mostrado para JScript, VBScript e Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="d43e5-111">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="d43e5-112">JScript</span><span class="sxs-lookup"><span data-stu-id="d43e5-112">JScript:</span></span>


```JScript
<script language="JScript">
    function fnIsFileSystemJ()
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
                
                bReturn = objFolderItem.IsFileSystem;
            }
        }
    }
</script>
```



<span data-ttu-id="d43e5-113">VBScript</span><span class="sxs-lookup"><span data-stu-id="d43e5-113">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnIsFileSystemVB()
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
                                
                    bReturn = objFolderItem.IsFileSystem
                end if
                set objFolderItem = nothing
            end if
            set objFolder2 = nothing
        end if
        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="d43e5-114">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="d43e5-114">Visual Basic:</span></span>


```VB
Private Sub fnIsFileSystemVB()
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
                    
                    bReturn = objFolderItem.IsFileSystem
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



## <a name="requirements"></a><span data-ttu-id="d43e5-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d43e5-115">Requirements</span></span>



| <span data-ttu-id="d43e5-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="d43e5-116">Requirement</span></span> | <span data-ttu-id="d43e5-117">Valor</span><span class="sxs-lookup"><span data-stu-id="d43e5-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d43e5-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d43e5-118">Minimum supported client</span></span><br/> | <span data-ttu-id="d43e5-119">Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="d43e5-119">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="d43e5-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d43e5-120">Minimum supported server</span></span><br/> | <span data-ttu-id="d43e5-121">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="d43e5-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="d43e5-122">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="d43e5-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="d43e5-123"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="d43e5-123"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="d43e5-124">INSERI</span><span class="sxs-lookup"><span data-stu-id="d43e5-124">IDL</span></span><br/>                      | <dl> <span data-ttu-id="d43e5-125"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="d43e5-125"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="d43e5-126">DLL</span><span class="sxs-lookup"><span data-stu-id="d43e5-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d43e5-127"><dt>Shell32.dll (versão 4,71 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="d43e5-127"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




