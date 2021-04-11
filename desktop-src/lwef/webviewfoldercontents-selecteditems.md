---
title: Método WebViewFolderContents.SelectedItems (Shldisp.h)
description: Obtém um objeto FolderItems que representa todos os itens selecionados na exibição.
ms.assetid: 683acac4-f157-4a75-a3f8-c693887c1ea5
keywords:
- Método SelectedItems recursos de ambiente herdado do Windows
- Método SelectedItems herdado recursos de ambiente do Windows, objeto WebViewFolderContents
- Recursos do ambiente Windows herdado do objeto WebViewFolderContents, método SelectedItems
topic_type:
- apiref
api_name:
- WebViewFolderContents.SelectedItems
api_location:
- Shell32.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cee4b7f34cdcabec637671af79775fc1fa546790
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009677"
---
# <a name="webviewfoldercontentsselecteditems-method"></a><span data-ttu-id="ed90f-106">Método WebViewFolderContents. SelectedItems</span><span class="sxs-lookup"><span data-stu-id="ed90f-106">WebViewFolderContents.SelectedItems method</span></span>

<span data-ttu-id="ed90f-107">Obtém um objeto [**FolderItems**](../shell/folderitems.md) que representa todos os itens selecionados na exibição.</span><span class="sxs-lookup"><span data-stu-id="ed90f-107">Gets a [**FolderItems**](../shell/folderitems.md) object that represents all of the selected items in the view.</span></span>

## <a name="syntax"></a><span data-ttu-id="ed90f-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ed90f-108">Syntax</span></span>


```JScript
retVal = WebViewFolderContents.SelectedItems()
```



## <a name="parameters"></a><span data-ttu-id="ed90f-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ed90f-109">Parameters</span></span>

<span data-ttu-id="ed90f-110">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="ed90f-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="ed90f-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ed90f-111">Return value</span></span>

<span data-ttu-id="ed90f-112">Tipo: **[ **FolderItems**](../shell/folderitems.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="ed90f-112">Type: **[**FolderItems**](../shell/folderitems.md)\*\***</span></span>

<span data-ttu-id="ed90f-113">Uma referência de objeto para o objeto [**FolderItems**](../shell/folderitems.md) .</span><span class="sxs-lookup"><span data-stu-id="ed90f-113">An object reference to the [**FolderItems**](../shell/folderitems.md) object.</span></span>

## <a name="examples"></a><span data-ttu-id="ed90f-114">Exemplos</span><span class="sxs-lookup"><span data-stu-id="ed90f-114">Examples</span></span>

<span data-ttu-id="ed90f-115">O exemplo a seguir mostra o uso correto desse método para JScript Embedded em HTML.</span><span class="sxs-lookup"><span data-stu-id="ed90f-115">The following example shows the proper usage of this method for JScript embedded in HTML.</span></span>


```HTML
<html>
<head>

...

<script language="JavaScript">
    function fnWebViewFolderContentsSelectedItemsJ()
    {
        var objFolderItems;

        objFolderItems = FileList.SelectedItems();
        if (objFolderItems != null)
        {
            alert(objFolderItems.Count);
        }
    }
</script>

</head>
<body>

...

<object id=FileList classid="clsid:1820FED0-473E-11D0-A96C-00C04FD705A2" tabIndex=1>
</body>
</html>
```



## <a name="requirements"></a><span data-ttu-id="ed90f-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ed90f-116">Requirements</span></span>



| <span data-ttu-id="ed90f-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="ed90f-117">Requirement</span></span> | <span data-ttu-id="ed90f-118">Valor</span><span class="sxs-lookup"><span data-stu-id="ed90f-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ed90f-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ed90f-119">Minimum supported client</span></span><br/> | <span data-ttu-id="ed90f-120">Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="ed90f-120">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="ed90f-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ed90f-121">Minimum supported server</span></span><br/> | <span data-ttu-id="ed90f-122">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="ed90f-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="ed90f-123">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="ed90f-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="ed90f-124"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="ed90f-124"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="ed90f-125">INSERI</span><span class="sxs-lookup"><span data-stu-id="ed90f-125">IDL</span></span><br/>                      | <dl> <span data-ttu-id="ed90f-126"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="ed90f-126"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="ed90f-127">DLL</span><span class="sxs-lookup"><span data-stu-id="ed90f-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ed90f-128"><dt>Shell32.dll (versão 4,71 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="ed90f-128"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

