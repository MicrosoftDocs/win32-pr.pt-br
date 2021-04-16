---
title: Método WebViewFolderContents. SelectItem (shldisp. h)
description: Define o estado de seleção de um item na exibição.
ms.assetid: c0e163ee-1951-476c-807a-781e26766d99
keywords:
- Recursos do ambiente Windows herdado do método SelectItem
- Método SelectItem recursos de ambiente herdados do Windows, objeto WebViewFolderContents
- Recursos do ambiente Windows herdado do objeto WebViewFolderContents, método SelectItem
topic_type:
- apiref
api_name:
- WebViewFolderContents.SelectItem
api_location:
- Shell32.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e491fb27db2d6e1e9b449be4aa2924684021539a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105765362"
---
# <a name="webviewfoldercontentsselectitem-method"></a><span data-ttu-id="8263a-106">Método WebViewFolderContents. SelectItem</span><span class="sxs-lookup"><span data-stu-id="8263a-106">WebViewFolderContents.SelectItem method</span></span>

<span data-ttu-id="8263a-107">Define o estado de seleção de um item na exibição.</span><span class="sxs-lookup"><span data-stu-id="8263a-107">Sets the selection state of an item in the view.</span></span>

## <a name="syntax"></a><span data-ttu-id="8263a-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8263a-108">Syntax</span></span>


```JScript
WebViewFolderContents.SelectItem(
  vItem,
  dwFlags
)
```



## <a name="parameters"></a><span data-ttu-id="8263a-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8263a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8263a-110">*vItem* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="8263a-110">*vItem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8263a-111">Tipo: \**Variant \** _</span><span class="sxs-lookup"><span data-stu-id="8263a-111">Type: \**Variant\** _</span></span>

<span data-ttu-id="8263a-112">O objeto [_ *FolderItem* \*](../shell/folderitem.md) para o qual o estado de seleção será definido.</span><span class="sxs-lookup"><span data-stu-id="8263a-112">The [_ *FolderItem*\*](../shell/folderitem.md) object for which the selection state will be set.</span></span>

</dd> <dt>

<span data-ttu-id="8263a-113">*dwFlags* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="8263a-113">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8263a-114">Tipo: **inteiro**</span><span class="sxs-lookup"><span data-stu-id="8263a-114">Type: **Integer**</span></span>

<span data-ttu-id="8263a-115">Um conjunto de sinalizadores que indicam o novo estado de seleção.</span><span class="sxs-lookup"><span data-stu-id="8263a-115">A set of flags that indicate the new selection state.</span></span> <span data-ttu-id="8263a-116">Pode ser um ou mais dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="8263a-116">This can be one or more of the following values.</span></span>

<dt>



 <span data-ttu-id="8263a-117"> acima (0)</span><span class="sxs-lookup"><span data-stu-id="8263a-117">(0)</span></span>


</dt> <dd>

<span data-ttu-id="8263a-118">Desmarque o item.</span><span class="sxs-lookup"><span data-stu-id="8263a-118">Deselect the item.</span></span>

</dd> <dt>



 <span data-ttu-id="8263a-119">(1)</span><span class="sxs-lookup"><span data-stu-id="8263a-119">(1)</span></span>


</dt> <dd>

<span data-ttu-id="8263a-120">Selecione o item.</span><span class="sxs-lookup"><span data-stu-id="8263a-120">Select the item.</span></span>

</dd> <dt>



 <span data-ttu-id="8263a-121">(3)</span><span class="sxs-lookup"><span data-stu-id="8263a-121">(3)</span></span>


</dt> <dd>

<span data-ttu-id="8263a-122">Coloque o item no modo de edição.</span><span class="sxs-lookup"><span data-stu-id="8263a-122">Put the item in edit mode.</span></span>

</dd> <dt>



 <span data-ttu-id="8263a-123">(4)</span><span class="sxs-lookup"><span data-stu-id="8263a-123">(4)</span></span>


</dt> <dd>

<span data-ttu-id="8263a-124">Anular seleção de todos, exceto o item especificado.</span><span class="sxs-lookup"><span data-stu-id="8263a-124">Deselect all but the specified item.</span></span>

</dd> <dt>



 <span data-ttu-id="8263a-125">(8)</span><span class="sxs-lookup"><span data-stu-id="8263a-125">(8)</span></span>


</dt> <dd>

<span data-ttu-id="8263a-126">Verifique se o item é exibido na exibição.</span><span class="sxs-lookup"><span data-stu-id="8263a-126">Ensure the item is displayed in the view.</span></span>

</dd> <dt>



 <span data-ttu-id="8263a-127">(16)</span><span class="sxs-lookup"><span data-stu-id="8263a-127">(16)</span></span>


</dt> <dd>

<span data-ttu-id="8263a-128">Dê o foco ao item.</span><span class="sxs-lookup"><span data-stu-id="8263a-128">Give the item the focus.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8263a-129">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="8263a-129">Return value</span></span>

<span data-ttu-id="8263a-130">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="8263a-130">This method does not return a value.</span></span>

## <a name="examples"></a><span data-ttu-id="8263a-131">Exemplos</span><span class="sxs-lookup"><span data-stu-id="8263a-131">Examples</span></span>

<span data-ttu-id="8263a-132">O exemplo a seguir mostra o uso correto desse método para JScript Embedded em HTML.</span><span class="sxs-lookup"><span data-stu-id="8263a-132">The following example shows the proper usage of this method for JScript embedded in HTML.</span></span>


```HTML
<html>
<head>

...

<script language="JavaScript">
    function fnWebViewFolderContentsSelectItemJ()
    {
        var objFolderItem;

        objFolderItem = FileList.FocusedItem;
        if (objFolderItem != null)
        {
            FileList.SelectItem(objFolderItem, 1);
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



## <a name="requirements"></a><span data-ttu-id="8263a-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8263a-133">Requirements</span></span>



| <span data-ttu-id="8263a-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="8263a-134">Requirement</span></span> | <span data-ttu-id="8263a-135">Valor</span><span class="sxs-lookup"><span data-stu-id="8263a-135">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8263a-136">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8263a-136">Minimum supported client</span></span><br/> | <span data-ttu-id="8263a-137">Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="8263a-137">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="8263a-138">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8263a-138">Minimum supported server</span></span><br/> | <span data-ttu-id="8263a-139">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="8263a-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="8263a-140">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="8263a-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="8263a-141"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="8263a-141"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="8263a-142">INSERI</span><span class="sxs-lookup"><span data-stu-id="8263a-142">IDL</span></span><br/>                      | <dl> <span data-ttu-id="8263a-143"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="8263a-143"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="8263a-144">DLL</span><span class="sxs-lookup"><span data-stu-id="8263a-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8263a-145"><dt>Shell32.dll (versão 4,71 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="8263a-145"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

