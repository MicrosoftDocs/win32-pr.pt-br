---
description: Recupera o objeto FolderItemVerbs do item. Esse objeto é a coleção de verbos que podem ser executados no item.
ms.assetid: e31160cd-093a-45a6-a066-58120c44eb2c
title: Método FolderItem. Verbs (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FolderItem.Verbs
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: f15c2471f749748f7928a45aa03037d955c75d4a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089717"
---
# <a name="folderitemverbs-method"></a><span data-ttu-id="c649f-104">Método FolderItem. Verbs</span><span class="sxs-lookup"><span data-stu-id="c649f-104">FolderItem.Verbs method</span></span>

<span data-ttu-id="c649f-105">Recupera o objeto [**FolderItemVerbs**](folderitemverbs.md) do item.</span><span class="sxs-lookup"><span data-stu-id="c649f-105">Retrieves the item's [**FolderItemVerbs**](folderitemverbs.md) object.</span></span> <span data-ttu-id="c649f-106">Esse objeto é a coleção de verbos que podem ser executados no item.</span><span class="sxs-lookup"><span data-stu-id="c649f-106">This object is the collection of verbs that can be executed on the item.</span></span>

## <a name="syntax"></a><span data-ttu-id="c649f-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c649f-107">Syntax</span></span>


```JScript
retVal = FolderItem.Verbs()
```



## <a name="parameters"></a><span data-ttu-id="c649f-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c649f-108">Parameters</span></span>

<span data-ttu-id="c649f-109">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="c649f-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="c649f-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c649f-110">Return value</span></span>

<span data-ttu-id="c649f-111">Tipo: **[ **FolderItemVerbs**](folderitemverbs.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="c649f-111">Type: **[**FolderItemVerbs**](folderitemverbs.md)\*\***</span></span>

<span data-ttu-id="c649f-112">Uma referência de objeto para o objeto [**FolderItemVerbs**](folderitemverbs.md) .</span><span class="sxs-lookup"><span data-stu-id="c649f-112">An object reference to the [**FolderItemVerbs**](folderitemverbs.md) object.</span></span>

## <a name="examples"></a><span data-ttu-id="c649f-113">Exemplos</span><span class="sxs-lookup"><span data-stu-id="c649f-113">Examples</span></span>

<span data-ttu-id="c649f-114">O exemplo a seguir usa **verbos** para recuperar o objeto [**FolderItemVerbs**](folderitemverbs.md) que representa o conjunto de verbos que podem ser executados na pasta do Windows.</span><span class="sxs-lookup"><span data-stu-id="c649f-114">The following example uses **Verbs** to retrieve the [**FolderItemVerbs**](folderitemverbs.md) object representing the set of verbs that can be executed on the Windows folder.</span></span> <span data-ttu-id="c649f-115">O uso adequado é mostrado para JScript, VBScript e Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="c649f-115">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="c649f-116">JScript</span><span class="sxs-lookup"><span data-stu-id="c649f-116">JScript:</span></span>


```JScript
<script language="JScript">
    function fnFolderItemVerbsJ()
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
                var objItemVerbs;
                
                objItemVerbs = objFolderItem.Verbs();
                if (objItemVerbs != null)
                {
                    // Add code here
                }
            }
        }
    }
</script>
```



<span data-ttu-id="c649f-117">VBScript</span><span class="sxs-lookup"><span data-stu-id="c649f-117">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnFolderItemVerbsVB()
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
                    dim objItemVerbs
                    
                    set objItemVerbs = objFolderItem.Verbs
                        if (not objItemVerbs is nothing) then
                            'Add code here
                        end if
                    set objItemVerbs = nothing
                end if
                set objFolderItem = nothing
            end if
            set objFolder2 = nothing
        end if
        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="c649f-118">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="c649f-118">Visual Basic:</span></span>


```VB
Private Sub fnFolderItemVerbsVB()
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
                    Dim objItemVerbs As FolderItemVerbs
                    
                    Set objItemVerbs = objFolderItem.Verbs
                        If (Not objItemVerbs Is Nothing) Then
                            'Add code here
                        End If
                    Set objItemVerbs = Nothing
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



## <a name="requirements"></a><span data-ttu-id="c649f-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c649f-119">Requirements</span></span>



| <span data-ttu-id="c649f-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="c649f-120">Requirement</span></span> | <span data-ttu-id="c649f-121">Valor</span><span class="sxs-lookup"><span data-stu-id="c649f-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c649f-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c649f-122">Minimum supported client</span></span><br/> | <span data-ttu-id="c649f-123">Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="c649f-123">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="c649f-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c649f-124">Minimum supported server</span></span><br/> | <span data-ttu-id="c649f-125">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="c649f-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="c649f-126">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="c649f-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="c649f-127"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="c649f-127"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="c649f-128">INSERI</span><span class="sxs-lookup"><span data-stu-id="c649f-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="c649f-129"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="c649f-129"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="c649f-130">DLL</span><span class="sxs-lookup"><span data-stu-id="c649f-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c649f-131"><dt>Shell32.dll (versão 4,71 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="c649f-131"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c649f-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="c649f-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c649f-133">**FolderItem**</span><span class="sxs-lookup"><span data-stu-id="c649f-133">**FolderItem**</span></span>](folderitem.md)
</dt> <dt>

[<span data-ttu-id="c649f-134">**InvokeVerb**</span><span class="sxs-lookup"><span data-stu-id="c649f-134">**InvokeVerb**</span></span>](folderitem-invokeverb.md)
</dt> <dt>

[<span data-ttu-id="c649f-135">**DoIt**</span><span class="sxs-lookup"><span data-stu-id="c649f-135">**DoIt**</span></span>](folderitemverb-doit.md)
</dt> </dl>

 

 




