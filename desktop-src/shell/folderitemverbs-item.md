---
description: Recupera o objeto FolderItemVerb para um item especificado na coleção.
ms.assetid: 65871926-0920-4ad6-82da-7aba0a3c0fab
title: Método FolderItemVerbs. Item (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FolderItemVerbs.Item
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 013215af3f5005e68b396312d0ef13fa974d8a32
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967927"
---
# <a name="folderitemverbsitem-method"></a><span data-ttu-id="b514a-103">Método FolderItemVerbs. Item</span><span class="sxs-lookup"><span data-stu-id="b514a-103">FolderItemVerbs.Item method</span></span>

<span data-ttu-id="b514a-104">Recupera o objeto [**FolderItemVerb**](folderitemverb.md) para um item especificado na coleção.</span><span class="sxs-lookup"><span data-stu-id="b514a-104">Retrieves the [**FolderItemVerb**](folderitemverb.md) object for a specified item in the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="b514a-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b514a-105">Syntax</span></span>


```JScript
retVal = FolderItemVerbs.Item(
  iIndex
)
```



## <a name="parameters"></a><span data-ttu-id="b514a-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b514a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b514a-107">*iIndex* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b514a-107">*iIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b514a-108">Tipo: **variante**</span><span class="sxs-lookup"><span data-stu-id="b514a-108">Type: **Variant**</span></span>

<span data-ttu-id="b514a-109">O índice com base em zero do item a ser recuperado.</span><span class="sxs-lookup"><span data-stu-id="b514a-109">The zero-based index of the item to retrieve.</span></span> <span data-ttu-id="b514a-110">Esse valor deve ser menor que o valor da propriedade [**Count**](folderitemverbs-count.md) .</span><span class="sxs-lookup"><span data-stu-id="b514a-110">This value must be less than the value of the [**Count**](folderitemverbs-count.md) property.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b514a-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b514a-111">Return value</span></span>

<span data-ttu-id="b514a-112">Tipo: **[ **IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)\*\***</span><span class="sxs-lookup"><span data-stu-id="b514a-112">Type: **[**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)\*\***</span></span>

<span data-ttu-id="b514a-113">Objeto que recebe o objeto [**FolderItemVerb**](folderitemverb.md) .</span><span class="sxs-lookup"><span data-stu-id="b514a-113">Object that receives the [**FolderItemVerb**](folderitemverb.md) object.</span></span>

## <a name="examples"></a><span data-ttu-id="b514a-114">Exemplos</span><span class="sxs-lookup"><span data-stu-id="b514a-114">Examples</span></span>

<span data-ttu-id="b514a-115">O exemplo a seguir usa **Item** para recuperar os primeiros verbos na coleção disponível para a pasta do painel de controle e exibe seu nome.</span><span class="sxs-lookup"><span data-stu-id="b514a-115">The following example uses **Item** to retrieve the first verbs in the collection available to the Control Panel folder and displays its name.</span></span> <span data-ttu-id="b514a-116">O uso adequado é mostrado para JScript, VBScript e Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="b514a-116">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="b514a-117">JScript</span><span class="sxs-lookup"><span data-stu-id="b514a-117">JScript:</span></span>


```JScript
<script language="JScript">
    function fnFolderItemVerbsItemJ()
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
                var objFolderItemVerb;
                objFolderItemVerb = objVerbs.Item(0);
 
                if (objFolderItemVerb != null)
                {
                    alert(objFolderItemVerb.Name);
                }
            }
        }
    }
</script>
```



<span data-ttu-id="b514a-118">VBScript</span><span class="sxs-lookup"><span data-stu-id="b514a-118">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnFolderItemVerbsItemVB()
        dim objShell
        dim objFolder2
        dim ssfCONTROLS
        
        ssfCONTROLS = 3
        set objShell = CreateObject("shell.application")
        set objFolder2 = objShell.NameSpace(ssfCONTROLS)
        if (not objFolder2 is nothing) then
            dim objVerbs
            set objVerbs = objFolder2.Self.Verbs

            if (not objVerbs is nothing) then
                dim objFolderItemVerb
                set objFolderItemVerb = objVerbs.Item(0)

                if (not objFolderItemVerb is nothing) then
                    alert(objFolderItemVerb.Name)
                end if

                set objFolderItemVerb = nothing
            end if

            set objVerbs = nothing
        end if

        set objFolder2 = nothing
        set objShell = nothing
    end function
</script>
```



<span data-ttu-id="b514a-119">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="b514a-119">Visual Basic:</span></span>


```VB
Private Sub fnFolderItemVerbsItemVB()
    Dim objShell    As Shell
    Dim objFolder2  As Folder2
    Dim ssfCONTROLS As Long
            
    ssfCONTROLS = 3
    Set objShell = New Shell
    Set objFolder2 = objShell.NameSpace(ssfPROGRAMS)

    If (Not objFolder2 Is Nothing) Then
        Dim objVerbs As FolderItemVerbs
        Set objVerbs = objFolder2.Self.Verbs

        If (Not objVerbs Is Nothing) Then
            Dim objFolderItemVerb As FolderItemVerb
            Set objFolderItemVerb = objVerbs.Item(0)

            If (Not objFolderItemVerb Is Nothing) Then
                Debug.Print objFolderItemVerb.Name
            End If

            Set objFolderItemVerb = Nothing
        End If

        Set objVerbs = Nothing
    End If

    Set objFolder2 = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="b514a-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b514a-120">Requirements</span></span>



| <span data-ttu-id="b514a-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="b514a-121">Requirement</span></span> | <span data-ttu-id="b514a-122">Valor</span><span class="sxs-lookup"><span data-stu-id="b514a-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b514a-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b514a-123">Minimum supported client</span></span><br/> | <span data-ttu-id="b514a-124">Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="b514a-124">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="b514a-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b514a-125">Minimum supported server</span></span><br/> | <span data-ttu-id="b514a-126">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="b514a-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="b514a-127">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="b514a-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="b514a-128"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="b514a-128"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="b514a-129">INSERI</span><span class="sxs-lookup"><span data-stu-id="b514a-129">IDL</span></span><br/>                      | <dl> <span data-ttu-id="b514a-130"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="b514a-130"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="b514a-131">DLL</span><span class="sxs-lookup"><span data-stu-id="b514a-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b514a-132"><dt>Shell32.dll (versão 4,71 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="b514a-132"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 
