---
title: THEME. closeView
description: O método closeView fecha um modo de exibição aberto.
ms.assetid: 37b56a7d-8031-4055-95ad-0510105e1c1f
keywords:
- THEME. closeView Windows Media Player
topic_type:
- apiref
api_name:
- THEME.closeView
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b39083979809fc2e747c54569db8d03298a951c6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751971"
---
# <a name="themecloseview"></a><span data-ttu-id="991ae-104">THEME. closeView</span><span class="sxs-lookup"><span data-stu-id="991ae-104">THEME.closeView</span></span>

<span data-ttu-id="991ae-105">O método **closeView** fecha um **modo de exibição** aberto.</span><span class="sxs-lookup"><span data-stu-id="991ae-105">The **closeView** method closes an open **VIEW**.</span></span>

``` syntax
        theme.closeView(theView)
```

## <a name="parameters"></a><span data-ttu-id="991ae-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="991ae-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="991ae-107"><span id="theView"></span><span id="theview"></span><span id="THEVIEW"></span>*Exibição*</span><span class="sxs-lookup"><span data-stu-id="991ae-107"><span id="theView"></span><span id="theview"></span><span id="THEVIEW"></span>*theView*</span></span>
</dt> <dd>

<span data-ttu-id="991ae-108">Uma **cadeia de caracteres** que especifica a **ID** da **exibição** a ser fechada.</span><span class="sxs-lookup"><span data-stu-id="991ae-108">A **String** specifying the **id** of the **VIEW** to close.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="991ae-109">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="991ae-109">Return Value</span></span>

<span data-ttu-id="991ae-110">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="991ae-110">This method does not return a value.</span></span>

## <a name="examples"></a><span data-ttu-id="991ae-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="991ae-111">Examples</span></span>


```C++
<THEME>
  <VIEW>
    <TEXT value="open" 
        onclick="jscript:theme.openView('newView')"/>
    <TEXT top="30" value="close"
        onclick="jscript:theme.closeView('newView')"/>
  </VIEW>
  <VIEW id="newView"/>
</THEME>
```



## <a name="requirements"></a><span data-ttu-id="991ae-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="991ae-112">Requirements</span></span>



| <span data-ttu-id="991ae-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="991ae-113">Requirement</span></span> | <span data-ttu-id="991ae-114">Valor</span><span class="sxs-lookup"><span data-stu-id="991ae-114">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="991ae-115">Versão</span><span class="sxs-lookup"><span data-stu-id="991ae-115">Version</span></span><br/> | <span data-ttu-id="991ae-116">Windows Media Player versão 7,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="991ae-116">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="991ae-117">Confira também</span><span class="sxs-lookup"><span data-stu-id="991ae-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="991ae-118">**Elemento THEME**</span><span class="sxs-lookup"><span data-stu-id="991ae-118">**THEME Element**</span></span>](theme-element.md)
</dt> <dt>

[<span data-ttu-id="991ae-119">**THEME. openView**</span><span class="sxs-lookup"><span data-stu-id="991ae-119">**THEME.openView**</span></span>](theme-openview.md)
</dt> </dl>

 

 





