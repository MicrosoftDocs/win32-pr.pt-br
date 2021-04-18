---
title: Ambiente. largura
description: O atributo width especifica ou recupera a largura do controle.
ms.assetid: f246958a-563c-40c0-8a74-4511103b95b2
keywords:
- Windows Media Player de ambiente ambiental. de largura
topic_type:
- apiref
api_name:
- AmbientAttributes.width
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c3f91ee47277dc511d54747197edfa44e80e251
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105761491"
---
# <a name="ambientattributeswidth"></a><span data-ttu-id="c6e0a-104">Ambiente. largura</span><span class="sxs-lookup"><span data-stu-id="c6e0a-104">AmbientAttributes.width</span></span>

<span data-ttu-id="c6e0a-105">O atributo **Width** especifica ou recupera a largura do controle.</span><span class="sxs-lookup"><span data-stu-id="c6e0a-105">The **width** attribute specifies or retrieves the width of the control.</span></span>

``` syntax
        elementID.width
```

## <a name="possible-values"></a><span data-ttu-id="c6e0a-106">Valores possíveis</span><span class="sxs-lookup"><span data-stu-id="c6e0a-106">Possible Values</span></span>

<span data-ttu-id="c6e0a-107">Esse atributo é um **inteiro** de leitura/gravação de 16 bits (0 a 32.767) que representa a largura do controle em pixels.</span><span class="sxs-lookup"><span data-stu-id="c6e0a-107">This attribute is a read/write 16-bit **Integer** (0 to 32,767) representing the width of the control in pixels.</span></span> <span data-ttu-id="c6e0a-108">O valor padrão é zero ou a largura da imagem especificada no atributo de **imagem** do controle.</span><span class="sxs-lookup"><span data-stu-id="c6e0a-108">The default value is zero or the width of the image specified in the control's **image** attribute.</span></span>

## <a name="remarks"></a><span data-ttu-id="c6e0a-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="c6e0a-109">Remarks</span></span>

<span data-ttu-id="c6e0a-110">Se a largura especificada for mais estreita do que a largura da imagem fornecida, a imagem será recortada.</span><span class="sxs-lookup"><span data-stu-id="c6e0a-110">If the width specified is narrower than the width of the image provided, then the image will be clipped.</span></span> <span data-ttu-id="c6e0a-111">Se a largura for maior que a largura da imagem, a região de clique vai além do limite da imagem.</span><span class="sxs-lookup"><span data-stu-id="c6e0a-111">If the width is wider than the width of the image, then the click region will go beyond the image boundary.</span></span> <span data-ttu-id="c6e0a-112">Não importa qual valor é fornecido a esse atributo, a imagem não pode aumentar além de sua **exibição** ou **subexibição** pai.</span><span class="sxs-lookup"><span data-stu-id="c6e0a-112">No matter what value is given to this attribute, the image cannot grow beyond its parent **VIEW** or **SUBVIEW**.</span></span>

## <a name="requirements"></a><span data-ttu-id="c6e0a-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c6e0a-113">Requirements</span></span>



| <span data-ttu-id="c6e0a-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="c6e0a-114">Requirement</span></span> | <span data-ttu-id="c6e0a-115">Valor</span><span class="sxs-lookup"><span data-stu-id="c6e0a-115">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="c6e0a-116">Versão</span><span class="sxs-lookup"><span data-stu-id="c6e0a-116">Version</span></span><br/> | <span data-ttu-id="c6e0a-117">Windows Media Player versão 7,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="c6e0a-117">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c6e0a-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="c6e0a-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c6e0a-119">**Atributos de ambiente**</span><span class="sxs-lookup"><span data-stu-id="c6e0a-119">**Ambient Attributes**</span></span>](ambient-attributes.md)
</dt> </dl>

 

 





