---
title: EQUALIZERSETTINGS.gainLevels
description: O atributo gainLevels especifica ou recupera o nível de lucro da faixa correspondente ao índice fornecido.
ms.assetid: fb70e2ef-4cee-457e-a06b-7a1ae6930986
keywords:
- EQUALIZERSETTINGS. gainLevels Windows Media Player
topic_type:
- apiref
api_name:
- EQUALIZERSETTINGS.gainLevels
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d083ac829582f2abc45837cf441b2f0a565ee03a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105800143"
---
# <a name="equalizersettingsgainlevels"></a><span data-ttu-id="2065b-104">EQUALIZERSETTINGS.gainLevels</span><span class="sxs-lookup"><span data-stu-id="2065b-104">EQUALIZERSETTINGS.gainLevels</span></span>

<span data-ttu-id="2065b-105">O atributo **gainLevels** especifica ou recupera o nível de lucro da faixa correspondente ao índice fornecido.</span><span class="sxs-lookup"><span data-stu-id="2065b-105">The **gainLevels** attribute specifies or retrieves the gain level of the band corresponding to the index provided.</span></span>

``` syntax
        elementID.gainLevels(theBand)
```

## <a name="possible-values"></a><span data-ttu-id="2065b-106">Valores possíveis</span><span class="sxs-lookup"><span data-stu-id="2065b-106">Possible Values</span></span>

<span data-ttu-id="2065b-107">Esse atributo é um **número** de leitura/gravação (**float**) com um valor normalmente que varia de 20 a + 20.</span><span class="sxs-lookup"><span data-stu-id="2065b-107">This attribute is a read/write **Number** (**float**) with a value normally ranging from  20 to +20.</span></span>

## <a name="parameters"></a><span data-ttu-id="2065b-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2065b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2065b-109"><span id="theBand"></span><span id="theband"></span><span id="THEBAND"></span>*a banda*</span><span class="sxs-lookup"><span data-stu-id="2065b-109"><span id="theBand"></span><span id="theband"></span><span id="THEBAND"></span>*theBand*</span></span>
</dt> <dd>

<span data-ttu-id="2065b-110">**Número**(**longo**) entre 1 e 10 indicando o índice da banda.</span><span class="sxs-lookup"><span data-stu-id="2065b-110">**Number**(**long**) between 1 and 10 indicating the index of the band.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2065b-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="2065b-111">Remarks</span></span>

<span data-ttu-id="2065b-112">Esse atributo usa um parâmetro, mas seu valor é especificado no código do script da mesma forma que outros valores de atributo.</span><span class="sxs-lookup"><span data-stu-id="2065b-112">This attribute takes a parameter, but its value is specified in script code the same way as other attribute values.</span></span> <span data-ttu-id="2065b-113">Ele não pode ser especificado no elemento EQUALIZERSETTINGS, nem pode ser usado com o atributo de escuta **wmpprop** .</span><span class="sxs-lookup"><span data-stu-id="2065b-113">It cannot be specified in the EQUALIZERSETTINGS element, nor can it be used with the **wmpprop** listening attribute.</span></span> <span data-ttu-id="2065b-114">Em vez disso, os atributos de nível de lucro numerados são fornecidos para essas situações.</span><span class="sxs-lookup"><span data-stu-id="2065b-114">Instead, the numbered gain level attributes are provided for these situations.</span></span>

## <a name="requirements"></a><span data-ttu-id="2065b-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2065b-115">Requirements</span></span>



| <span data-ttu-id="2065b-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="2065b-116">Requirement</span></span> | <span data-ttu-id="2065b-117">Valor</span><span class="sxs-lookup"><span data-stu-id="2065b-117">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="2065b-118">Versão</span><span class="sxs-lookup"><span data-stu-id="2065b-118">Version</span></span><br/> | <span data-ttu-id="2065b-119">Windows Media Player versão 7,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="2065b-119">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="2065b-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="2065b-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2065b-121">**Elemento EQUALIZERSETTINGS**</span><span class="sxs-lookup"><span data-stu-id="2065b-121">**EQUALIZERSETTINGS Element**</span></span>](equalizersettings-element.md)
</dt> <dt>

[<span data-ttu-id="2065b-122">**Atributos de escuta**</span><span class="sxs-lookup"><span data-stu-id="2065b-122">**Listening Attributes**</span></span>](listening-attributes.md)
</dt> </dl>

 

 





