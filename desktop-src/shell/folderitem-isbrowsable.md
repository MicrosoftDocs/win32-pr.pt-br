---
description: Indica se o item pode ser hospedado dentro de um navegador ou quadro do Windows Explorer.
ms.assetid: 472e0906-9561-4390-a503-c5e490245ea0
title: Propriedade FolderItem. isnavegáment (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FolderItem.IsBrowsable
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: d7c5f7a9cbde54647c299646bb6350c3be6aa2a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104370514"
---
# <a name="folderitemisbrowsable-property"></a><span data-ttu-id="e0d11-103">Propriedade FolderItem. isnavegável</span><span class="sxs-lookup"><span data-stu-id="e0d11-103">FolderItem.IsBrowsable property</span></span>

<span data-ttu-id="e0d11-104">Indica se o item pode ser hospedado dentro de um navegador ou quadro do Windows Explorer.</span><span class="sxs-lookup"><span data-stu-id="e0d11-104">Indicates if the item can be hosted inside a browser or Windows Explorer frame.</span></span>

<span data-ttu-id="e0d11-105">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="e0d11-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="e0d11-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e0d11-106">Syntax</span></span>


```JScript
bIsBrowsable = FolderItem.IsBrowsable
```



## <a name="property-value"></a><span data-ttu-id="e0d11-107">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="e0d11-107">Property value</span></span>

<span data-ttu-id="e0d11-108">Um **booliano** que recebe **true** se o item puder ser procurado ou **false** se não.</span><span class="sxs-lookup"><span data-stu-id="e0d11-108">A **Boolean** that receives **true** if the item can be browsed or **false** if not.</span></span>

## <a name="examples"></a><span data-ttu-id="e0d11-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="e0d11-109">Examples</span></span>

<span data-ttu-id="e0d11-110">O exemplo a seguir usa **Isnavegável** para determinar o estado navegável da pasta do Windows.</span><span class="sxs-lookup"><span data-stu-id="e0d11-110">The following example uses **IsBrowsable** to determine the browsable state of the Windows folder.</span></span> <span data-ttu-id="e0d11-111">O uso adequado é mostrado para JScript, VBScript e Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="e0d11-111">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="e0d11-112">JScript</span><span class="sxs-lookup"><span data-stu-id="e0d11-112">JScript:</span></span>


```JScript
<script language="JScript">
    function fnIsBrowsableJ()
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
                
                bReturn = objFolderItem.IsBrowsable;
            }
        }
    }
</script>
```



<span data-ttu-id="e0d11-113">VBScript</span><span class="sxs-lookup"><span data-stu-id="e0d11-113">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnIsBrowsableVB()
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
                                
                    bReturn = objFolderItem.IsBrowsable
                end if
                set objFolderItem = nothing
            end if
            set objFolder2 = nothing
        end if
        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="e0d11-114">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="e0d11-114">Visual Basic:</span></span>


```VB
Private Sub fnIsBrowsableVB()
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
                    
                    bReturn = objFolderItem.IsBrowsable
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



## <a name="requirements"></a><span data-ttu-id="e0d11-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e0d11-115">Requirements</span></span>



| <span data-ttu-id="e0d11-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="e0d11-116">Requirement</span></span> | <span data-ttu-id="e0d11-117">Valor</span><span class="sxs-lookup"><span data-stu-id="e0d11-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e0d11-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e0d11-118">Minimum supported client</span></span><br/> | <span data-ttu-id="e0d11-119">Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="e0d11-119">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="e0d11-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e0d11-120">Minimum supported server</span></span><br/> | <span data-ttu-id="e0d11-121">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="e0d11-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="e0d11-122">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="e0d11-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="e0d11-123"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="e0d11-123"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="e0d11-124">INSERI</span><span class="sxs-lookup"><span data-stu-id="e0d11-124">IDL</span></span><br/>                      | <dl> <span data-ttu-id="e0d11-125"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="e0d11-125"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="e0d11-126">DLL</span><span class="sxs-lookup"><span data-stu-id="e0d11-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e0d11-127"><dt>Shell32.dll (versão 4,71 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="e0d11-127"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




