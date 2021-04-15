---
title: THEME. openView
description: O método openView abre uma exibição em uma nova janela.
ms.assetid: 2aa63c29-dafe-4942-a010-076f1503862b
keywords:
- TEMA. openView do Windows Media Player
topic_type:
- apiref
api_name:
- THEME.openView
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d66ff2cf47004c7687a37f1f22a87bdeb534d344
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105760732"
---
# <a name="themeopenview"></a><span data-ttu-id="6ed02-104">THEME. openView</span><span class="sxs-lookup"><span data-stu-id="6ed02-104">THEME.openView</span></span>

<span data-ttu-id="6ed02-105">O método **openView** abre uma **exibição** em uma nova janela.</span><span class="sxs-lookup"><span data-stu-id="6ed02-105">The **openView** method opens a **VIEW** in a new window.</span></span>

``` syntax
        theme.openView(view)
```

## <a name="parameters"></a><span data-ttu-id="6ed02-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6ed02-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6ed02-107"><span id="view"></span><span id="VIEW"></span>*exibição*</span><span class="sxs-lookup"><span data-stu-id="6ed02-107"><span id="view"></span><span id="VIEW"></span>*view*</span></span>
</dt> <dd>

<span data-ttu-id="6ed02-108">Uma **cadeia de caracteres** que especifica a **ID** da **exibição** a ser aberta.</span><span class="sxs-lookup"><span data-stu-id="6ed02-108">A **String** specifying the **id** of the **VIEW** to open.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6ed02-109">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="6ed02-109">Return Value</span></span>

<span data-ttu-id="6ed02-110">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="6ed02-110">This method does not return a value.</span></span>

## <a name="examples"></a><span data-ttu-id="6ed02-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="6ed02-111">Examples</span></span>


```JScript
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



## <a name="requirements"></a><span data-ttu-id="6ed02-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6ed02-112">Requirements</span></span>



| <span data-ttu-id="6ed02-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="6ed02-113">Requirement</span></span> | <span data-ttu-id="6ed02-114">Valor</span><span class="sxs-lookup"><span data-stu-id="6ed02-114">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="6ed02-115">Versão</span><span class="sxs-lookup"><span data-stu-id="6ed02-115">Version</span></span><br/> | <span data-ttu-id="6ed02-116">Windows Media Player versão 7,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="6ed02-116">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="6ed02-117">Confira também</span><span class="sxs-lookup"><span data-stu-id="6ed02-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6ed02-118">**Elemento THEME**</span><span class="sxs-lookup"><span data-stu-id="6ed02-118">**THEME Element**</span></span>](theme-element.md)
</dt> <dt>

[<span data-ttu-id="6ed02-119">**THEME. closeView**</span><span class="sxs-lookup"><span data-stu-id="6ed02-119">**THEME.closeView**</span></span>](theme-closeview.md)
</dt> <dt>

[<span data-ttu-id="6ed02-120">**THEME. openViewRelative**</span><span class="sxs-lookup"><span data-stu-id="6ed02-120">**THEME.openViewRelative**</span></span>](theme-openviewrelative.md)
</dt> </dl>

 

 





