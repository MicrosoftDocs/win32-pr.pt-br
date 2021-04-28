---
description: Propriedade FolderItemVerbs. Count – contém o número de itens na coleção.
ms.assetid: a676593b-ea78-433d-a622-221028245c3a
title: Propriedade FolderItemVerbs. Count (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FolderItemVerbs.Count
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 5545ea64da914188226fbdabf7cc6301baa695af
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108089544"
---
# <a name="folderitemverbscount-property"></a><span data-ttu-id="341f9-103">Propriedade FolderItemVerbs. Count</span><span class="sxs-lookup"><span data-stu-id="341f9-103">FolderItemVerbs.Count property</span></span>

<span data-ttu-id="341f9-104">Contém o número de itens na coleção.</span><span class="sxs-lookup"><span data-stu-id="341f9-104">Contains the number of items in the collection.</span></span>

<span data-ttu-id="341f9-105">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="341f9-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="341f9-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="341f9-106">Syntax</span></span>


```JScript
iCount = FolderItemVerbs.Count
```



## <a name="property-value"></a><span data-ttu-id="341f9-107">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="341f9-107">Property value</span></span>

<span data-ttu-id="341f9-108">Um **inteiro** que recebe a propriedade **Count** .</span><span class="sxs-lookup"><span data-stu-id="341f9-108">An **Integer** that receives the **Count** property.</span></span>

## <a name="examples"></a><span data-ttu-id="341f9-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="341f9-109">Examples</span></span>

<span data-ttu-id="341f9-110">O exemplo a seguir usa **Count** para recuperar a contagem de verbos disponíveis para a pasta do painel de controle.</span><span class="sxs-lookup"><span data-stu-id="341f9-110">The following example uses **Count** to retrieve the count of verbs available for the Control Panel folder.</span></span> <span data-ttu-id="341f9-111">O uso adequado é mostrado para JScript, VBScript e Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="341f9-111">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="341f9-112">JScript</span><span class="sxs-lookup"><span data-stu-id="341f9-112">JScript:</span></span>


```JScript
<script language="JScript">
    function fnFolderItemVerbsCountJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var objFolder2;
        var ssfCONTROLS = 3;
        
        objFolder2 = objShell.NameSpace(ssfCONTROLS);
        if (objFolder2 != null)
        {
            var objVerbs;
            
            objVerbs = objFolder2.Self.Verbs();

            if (objVerbs != null)
            {
                var nCount;
                nCount = objVerbs.Count;

                alert(nCount);
            }
        }
    }
</script>
```



<span data-ttu-id="341f9-113">VBScript</span><span class="sxs-lookup"><span data-stu-id="341f9-113">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnFolderItemsCountVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        if (not objShell is nothing) then
            dim objFolder
            dim ssfWINDOWS
                
            ssfWINDOWS = 36
            set objFolder = objShell.NameSpace(ssfWINDOWS)
            if (not objFolder is nothing) then
                dim objFolderItems
                        
                set objFolderItems = objFolder.Items()
                if (not objFolderItems is nothing) then
                    dim nCount
                    
                    nCount = objFolderItems.Count
                    alert(nCount)
                end if
                set objFolderItems = nothing
            end if
            set objFolder = nothing
        end if
        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="341f9-114">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="341f9-114">Visual Basic:</span></span>


```VB
Private Sub fnFolderItemsCountVB()
    Dim objShell   As Shell
    Dim objFolder  As Folder
    Dim ssfWINDOWS As Long
    
    ssfWINDOWS = 36
    Set objShell = New Shell
    Set objFolder = objShell.NameSpace(ssfWINDOWS)
        If (Not objFolder Is Nothing) Then
            Dim objFolderItems As FolderItems
            
            Set objFolderItems = objFolder.Items
                If (Not objFolderItems Is Nothing) Then
                    Dim nCount As Integer
                    
                    nCount = objFolderItems.Count
                    Debug.Print nCount
                End If
            Set objFolderItems = Nothing
        End If
    Set objFolder = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="341f9-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="341f9-115">Requirements</span></span>



| <span data-ttu-id="341f9-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="341f9-116">Requirement</span></span> | <span data-ttu-id="341f9-117">Valor</span><span class="sxs-lookup"><span data-stu-id="341f9-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="341f9-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="341f9-118">Minimum supported client</span></span><br/> | <span data-ttu-id="341f9-119">Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="341f9-119">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="341f9-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="341f9-120">Minimum supported server</span></span><br/> | <span data-ttu-id="341f9-121">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="341f9-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="341f9-122">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="341f9-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="341f9-123"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="341f9-123"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="341f9-124">INSERI</span><span class="sxs-lookup"><span data-stu-id="341f9-124">IDL</span></span><br/>                      | <dl> <span data-ttu-id="341f9-125"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="341f9-125"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="341f9-126">DLL</span><span class="sxs-lookup"><span data-stu-id="341f9-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="341f9-127"><dt>Shell32.dll (versão 4,71 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="341f9-127"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




