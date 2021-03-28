---
description: Contém uma representação de cadeia de caracteres do tipo do item.
ms.assetid: e851d632-9562-4194-a24c-12e757227b5b
title: Propriedade FolderItem. Type (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FolderItem.Type
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 12c3ffe3b32a6d2b2f3021312905839bc5cc1744
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010303"
---
# <a name="folderitemtype-property"></a><span data-ttu-id="f564d-103">Propriedade FolderItem. Type</span><span class="sxs-lookup"><span data-stu-id="f564d-103">FolderItem.Type property</span></span>

<span data-ttu-id="f564d-104">Contém uma representação de cadeia de caracteres do tipo do item.</span><span class="sxs-lookup"><span data-stu-id="f564d-104">Contains a string representation of the item's type.</span></span>

<span data-ttu-id="f564d-105">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="f564d-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="f564d-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f564d-106">Syntax</span></span>


```JScript
strType = FolderItem.Type
```



## <a name="property-value"></a><span data-ttu-id="f564d-107">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="f564d-107">Property value</span></span>

<span data-ttu-id="f564d-108">Uma variável do tipo [**BSTR**](/previous-versions/windows/desktop/automat/bstr) que recebe o tipo do item.</span><span class="sxs-lookup"><span data-stu-id="f564d-108">A variable of type [**BSTR**](/previous-versions/windows/desktop/automat/bstr) that receives the item's type.</span></span>

## <a name="examples"></a><span data-ttu-id="f564d-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="f564d-109">Examples</span></span>

<span data-ttu-id="f564d-110">O exemplo a seguir usa o **tipo** para recuperar o tipo do item.</span><span class="sxs-lookup"><span data-stu-id="f564d-110">The following example uses **Type** to retrieve the item's type.</span></span> <span data-ttu-id="f564d-111">O uso adequado é mostrado para JScript, VBScript e Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="f564d-111">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="f564d-112">JScript</span><span class="sxs-lookup"><span data-stu-id="f564d-112">JScript:</span></span>


```JScript
<script language="JScript">
    function fnFolderItemTypeJ()
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
                var szReturn;
                
                szReturn = objFolderItem.Type;
                alert(szReturn);
            }
        }
    }
</script>
```



<span data-ttu-id="f564d-113">VBScript</span><span class="sxs-lookup"><span data-stu-id="f564d-113">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnFolderItemTypeVB()
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
                    dim szReturn
                                
                    szReturn = objFolderItem.Type
                end if
                set objFolderItem = nothing
            end if
            set objFolder2 = nothing
        end if
        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="f564d-114">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="f564d-114">Visual Basic:</span></span>


```VB
Private Sub fnFolderItemTypeVB()
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
                    Dim szReturn As String
                    
                    szReturn = objFolderItem.Type
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



## <a name="requirements"></a><span data-ttu-id="f564d-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f564d-115">Requirements</span></span>



| <span data-ttu-id="f564d-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="f564d-116">Requirement</span></span> | <span data-ttu-id="f564d-117">Valor</span><span class="sxs-lookup"><span data-stu-id="f564d-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f564d-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f564d-118">Minimum supported client</span></span><br/> | <span data-ttu-id="f564d-119">Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="f564d-119">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="f564d-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f564d-120">Minimum supported server</span></span><br/> | <span data-ttu-id="f564d-121">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="f564d-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="f564d-122">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="f564d-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="f564d-123"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="f564d-123"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="f564d-124">INSERI</span><span class="sxs-lookup"><span data-stu-id="f564d-124">IDL</span></span><br/>                      | <dl> <span data-ttu-id="f564d-125"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="f564d-125"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="f564d-126">DLL</span><span class="sxs-lookup"><span data-stu-id="f564d-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f564d-127"><dt>Shell32.dll (versão 4,71 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="f564d-127"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 
