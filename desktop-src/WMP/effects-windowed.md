---
title: EFEITOS. em janela
description: O atributo em janela especifica ou recupera um valor que indica se a visualização será em janelas ou sem janela, ou seja, se todo o retângulo do controle estará visível sempre ou se ele pode ser recortado.
ms.assetid: bc535274-8bc3-43bb-aab0-11899134d71e
keywords:
- EFEITOS. Windows Media Player em janelas
topic_type:
- apiref
api_name:
- EFFECTS.windowed
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b3e30ae511c3e80e5e560f864baa8d797903fe2a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105800148"
---
# <a name="effectswindowed"></a><span data-ttu-id="af0d5-104">EFEITOS. em janela</span><span class="sxs-lookup"><span data-stu-id="af0d5-104">EFFECTS.windowed</span></span>

<span data-ttu-id="af0d5-105">O atributo em **janela** especifica ou recupera um valor que indica se a visualização será em janelas ou sem janela, ou seja, se todo o retângulo do controle estará visível sempre ou se ele pode ser recortado.</span><span class="sxs-lookup"><span data-stu-id="af0d5-105">The **windowed** attribute specifies or retrieves a value indicating whether the visualization will be windowed or windowless, that is, whether the entire rectangle of the control will be visible at all times, or whether it can be clipped.</span></span> <span data-ttu-id="af0d5-106">Esse atributo só pode ser definido em tempo de design.</span><span class="sxs-lookup"><span data-stu-id="af0d5-106">This attribute can only be set at design time.</span></span>

``` syntax
        elementID.windowed
```

## <a name="possible-values"></a><span data-ttu-id="af0d5-107">Valores possíveis</span><span class="sxs-lookup"><span data-stu-id="af0d5-107">Possible Values</span></span>

<span data-ttu-id="af0d5-108">Esse atributo é um **booliano** especificado em tempo de design e somente leitura depois.</span><span class="sxs-lookup"><span data-stu-id="af0d5-108">This attribute is a **Boolean** specified at design time and read-only thereafter.</span></span>



| <span data-ttu-id="af0d5-109">Valor</span><span class="sxs-lookup"><span data-stu-id="af0d5-109">Value</span></span> | <span data-ttu-id="af0d5-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="af0d5-110">Description</span></span>                              |
|-------|------------------------------------------|
| <span data-ttu-id="af0d5-111">true</span><span class="sxs-lookup"><span data-stu-id="af0d5-111">true</span></span>  | <span data-ttu-id="af0d5-112">O controle será janelas.</span><span class="sxs-lookup"><span data-stu-id="af0d5-112">The control will be windowed.</span></span>            |
| <span data-ttu-id="af0d5-113">false</span><span class="sxs-lookup"><span data-stu-id="af0d5-113">false</span></span> | <span data-ttu-id="af0d5-114">Padrão.</span><span class="sxs-lookup"><span data-stu-id="af0d5-114">Default.</span></span> <span data-ttu-id="af0d5-115">O controle não terá janela.</span><span class="sxs-lookup"><span data-stu-id="af0d5-115">The control will be windowless.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="af0d5-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="af0d5-116">Remarks</span></span>

<span data-ttu-id="af0d5-117">Se uma janela de visualização não retangular for desejada ou se alguma parte da janela for coberta por uma imagem, esse atributo deverá ser definido como false.</span><span class="sxs-lookup"><span data-stu-id="af0d5-117">If a non-rectangular visualization window is desired, or if any part of the window is covered by an image, this attribute must be set to false.</span></span> <span data-ttu-id="af0d5-118">Isso sacrificaria algum desempenho para fazer o recorte necessário.</span><span class="sxs-lookup"><span data-stu-id="af0d5-118">This sacrifices some performance to do the necessary clipping.</span></span>

<span data-ttu-id="af0d5-119">Se a **janela** estiver definida como true, qualquer imagem que abranja a janela de visualização será ignorada e a janela de visualização terá a ordem z de nível mais alto.</span><span class="sxs-lookup"><span data-stu-id="af0d5-119">If **windowed** is set to true, any image covering the visualization window is ignored, and the visualization window has the highest-level z-order.</span></span>

## <a name="requirements"></a><span data-ttu-id="af0d5-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="af0d5-120">Requirements</span></span>



| <span data-ttu-id="af0d5-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="af0d5-121">Requirement</span></span> | <span data-ttu-id="af0d5-122">Valor</span><span class="sxs-lookup"><span data-stu-id="af0d5-122">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="af0d5-123">Versão</span><span class="sxs-lookup"><span data-stu-id="af0d5-123">Version</span></span><br/> | <span data-ttu-id="af0d5-124">Windows Media Player versão 7,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="af0d5-124">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="af0d5-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="af0d5-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="af0d5-126">**Elemento EFFECTs**</span><span class="sxs-lookup"><span data-stu-id="af0d5-126">**EFFECTS Element**</span></span>](effects-element.md)
</dt> </dl>

 

 





