---
title: Ambiente. altura
description: O atributo Height Especifica ou recupera a altura do controle.
ms.assetid: a5c85d86-15d4-451d-b8bc-ed3b6e0dfd7d
keywords:
- Windows Media Player de ambiente. altura
topic_type:
- apiref
api_name:
- AmbientAttributes.height
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 662268bfeaf00b3185d531ff10d8dd17c9127a66
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105770529"
---
# <a name="ambientattributesheight"></a><span data-ttu-id="7c90d-104">Ambiente. altura</span><span class="sxs-lookup"><span data-stu-id="7c90d-104">AmbientAttributes.height</span></span>

<span data-ttu-id="7c90d-105">O atributo **Height** especifica ou recupera a altura do controle.</span><span class="sxs-lookup"><span data-stu-id="7c90d-105">The **height** attribute specifies or retrieves the height of the control.</span></span>

``` syntax
        elementID.height
```

## <a name="possible-values"></a><span data-ttu-id="7c90d-106">Valores possíveis</span><span class="sxs-lookup"><span data-stu-id="7c90d-106">Possible Values</span></span>

<span data-ttu-id="7c90d-107">Esse atributo é um **número** de leitura/gravação (**longo**) que representa a altura do controle em pixels.</span><span class="sxs-lookup"><span data-stu-id="7c90d-107">This attribute is a read/write **Number** (**long**) representing the height of the control in pixels.</span></span> <span data-ttu-id="7c90d-108">O valor padrão é zero ou a altura da imagem especificada no atributo de **imagem** do controle.</span><span class="sxs-lookup"><span data-stu-id="7c90d-108">The default value is zero or the height of the image specified in the control's **image** attribute.</span></span>

## <a name="remarks"></a><span data-ttu-id="7c90d-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="7c90d-109">Remarks</span></span>

<span data-ttu-id="7c90d-110">Se a altura especificada for menor do que a altura da imagem fornecida, a imagem será recortada.</span><span class="sxs-lookup"><span data-stu-id="7c90d-110">If the height specified is smaller than the height of the image provided, then the image will be clipped.</span></span> <span data-ttu-id="7c90d-111">Se a altura for maior que a altura da imagem, a região de clique vai além do limite da imagem.</span><span class="sxs-lookup"><span data-stu-id="7c90d-111">If the height is larger than the height of the image, then the click region will go beyond the image boundary.</span></span> <span data-ttu-id="7c90d-112">Não importa qual valor é fornecido a esse atributo, a imagem não pode aumentar além de sua **exibição** ou **subexibição** pai.</span><span class="sxs-lookup"><span data-stu-id="7c90d-112">No matter what value is given to this attribute, the image cannot grow beyond its parent **VIEW** or **SUBVIEW**.</span></span>

## <a name="requirements"></a><span data-ttu-id="7c90d-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7c90d-113">Requirements</span></span>



| <span data-ttu-id="7c90d-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="7c90d-114">Requirement</span></span> | <span data-ttu-id="7c90d-115">Valor</span><span class="sxs-lookup"><span data-stu-id="7c90d-115">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="7c90d-116">Versão</span><span class="sxs-lookup"><span data-stu-id="7c90d-116">Version</span></span><br/> | <span data-ttu-id="7c90d-117">Windows Media Player versão 7,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="7c90d-117">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="7c90d-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="7c90d-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7c90d-119">**Atributos de ambiente**</span><span class="sxs-lookup"><span data-stu-id="7c90d-119">**Ambient Attributes**</span></span>](ambient-attributes.md)
</dt> </dl>

 

 





