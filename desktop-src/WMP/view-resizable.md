---
title: Exibir. redimensionável
description: O atributo redimensionável recupera um valor que indica se a exibição pode ser redimensionada.
ms.assetid: 4f0e4f31-cf16-498f-823f-da43566043b1
keywords:
- Exibir. redimensionável do Windows Media Player
topic_type:
- apiref
api_name:
- VIEW.resizable
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed4d61973e34891d336ea5729ea40478c6c32808
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105793876"
---
# <a name="viewresizable"></a><span data-ttu-id="38f38-104">Exibir. redimensionável</span><span class="sxs-lookup"><span data-stu-id="38f38-104">VIEW.resizable</span></span>

<span data-ttu-id="38f38-105">O atributo **redimensionável** recupera um valor que indica se a **exibição** pode ser redimensionada.</span><span class="sxs-lookup"><span data-stu-id="38f38-105">The **resizable** attribute retrieves a value indicating whether the **VIEW** can be resized.</span></span>

``` syntax
        elementID.resizable
```

## <a name="possible-values"></a><span data-ttu-id="38f38-106">Valores possíveis</span><span class="sxs-lookup"><span data-stu-id="38f38-106">Possible Values</span></span>

<span data-ttu-id="38f38-107">Esse atributo é um **booliano** somente leitura com um valor padrão igual ao atributo **TitleBar** .</span><span class="sxs-lookup"><span data-stu-id="38f38-107">This attribute is a read-only **Boolean** with a default value equal to the **titlebar** attribute.</span></span>



| <span data-ttu-id="38f38-108">Valores</span><span class="sxs-lookup"><span data-stu-id="38f38-108">Values</span></span> | <span data-ttu-id="38f38-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="38f38-109">Description</span></span>             |
|--------|-------------------------|
| <span data-ttu-id="38f38-110">true</span><span class="sxs-lookup"><span data-stu-id="38f38-110">true</span></span>   | <span data-ttu-id="38f38-111">A exibição pode ser redimensionada.</span><span class="sxs-lookup"><span data-stu-id="38f38-111">View can be resized.</span></span>    |
| <span data-ttu-id="38f38-112">false</span><span class="sxs-lookup"><span data-stu-id="38f38-112">false</span></span>  | <span data-ttu-id="38f38-113">A exibição não pode ser redimensionada.</span><span class="sxs-lookup"><span data-stu-id="38f38-113">View cannot be resized.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="38f38-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="38f38-114">Remarks</span></span>

<span data-ttu-id="38f38-115">Se não houver nenhuma **TitleBar** e, portanto, nenhuma janela ou borda, você deverá usar o método **size** para redimensionar o elemento **View** .</span><span class="sxs-lookup"><span data-stu-id="38f38-115">If there is no **titlebar**, and therefore no window or border, you must use the **size** method to resize the **VIEW** element.</span></span>

## <a name="requirements"></a><span data-ttu-id="38f38-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="38f38-116">Requirements</span></span>



| <span data-ttu-id="38f38-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="38f38-117">Requirement</span></span> | <span data-ttu-id="38f38-118">Valor</span><span class="sxs-lookup"><span data-stu-id="38f38-118">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="38f38-119">Versão</span><span class="sxs-lookup"><span data-stu-id="38f38-119">Version</span></span><br/> | <span data-ttu-id="38f38-120">Windows Media Player versão 7,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="38f38-120">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="38f38-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="38f38-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="38f38-122">**Elemento VIEW**</span><span class="sxs-lookup"><span data-stu-id="38f38-122">**VIEW Element**</span></span>](view-element.md)
</dt> </dl>

 

 





