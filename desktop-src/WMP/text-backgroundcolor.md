---
title: TEXT. backgroundColor
description: O atributo backgroundColor especifica ou recupera a cor do plano de fundo do controle de texto.
ms.assetid: 0c16318f-bf57-4c5f-85c1-46641124d431
keywords:
- TEXT. backgroundColor Windows Media Player
topic_type:
- apiref
api_name:
- TEXT.backgroundColor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bff833fad0b5ad60b49479c57dc51cbe82f48dbd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105771308"
---
# <a name="textbackgroundcolor"></a><span data-ttu-id="fbfbe-104">TEXT. backgroundColor</span><span class="sxs-lookup"><span data-stu-id="fbfbe-104">TEXT.backgroundColor</span></span>

<span data-ttu-id="fbfbe-105">O atributo **backgroundColor** especifica ou recupera a cor do plano de fundo do controle de texto.</span><span class="sxs-lookup"><span data-stu-id="fbfbe-105">The **backgroundColor** attribute specifies or retrieves the background color for the Text control.</span></span>

``` syntax
        elementID.backgroundColor
```

## <a name="possible-values"></a><span data-ttu-id="fbfbe-106">Valores possíveis</span><span class="sxs-lookup"><span data-stu-id="fbfbe-106">Possible Values</span></span>

<span data-ttu-id="fbfbe-107">Esse atributo é uma **cadeia de caracteres** de leitura/gravação que contém qualquer valor de cor do Microsoft Internet Explorer ou o valor "None".</span><span class="sxs-lookup"><span data-stu-id="fbfbe-107">This attribute is a read/write **String** containing any Microsoft Internet Explorer color value or the value "none".</span></span> <span data-ttu-id="fbfbe-108">Ele tem um valor padrão de "None", o que significa que o plano de fundo é transparente.</span><span class="sxs-lookup"><span data-stu-id="fbfbe-108">It has a default value of "none", which means the background is transparent.</span></span>

## <a name="remarks"></a><span data-ttu-id="fbfbe-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="fbfbe-109">Remarks</span></span>

<span data-ttu-id="fbfbe-110">A cor do plano de fundo é definida para a altura e a largura do controle.</span><span class="sxs-lookup"><span data-stu-id="fbfbe-110">The background color is set for the height and width of the control.</span></span> <span data-ttu-id="fbfbe-111">Se a altura e a largura não forem definidas, a cor do plano de fundo será definida com a altura e a largura do texto.</span><span class="sxs-lookup"><span data-stu-id="fbfbe-111">If height and width are not set, the background color is set to the height and width of the text.</span></span>

<span data-ttu-id="fbfbe-112">Quando você usa **alphaBlend** ou **alphaBlendTo** com um elemento de **texto** que não tem o **backgroundColor** especificado, uma cor de plano de fundo de preto será usada.</span><span class="sxs-lookup"><span data-stu-id="fbfbe-112">When you use **alphaBlend** or **alphaBlendTo** with a **TEXT** element that does not have the **backgroundColor** specified, a background color of black will be used.</span></span> <span data-ttu-id="fbfbe-113">Se a cor de primeiro plano também for preta (que é o valor padrão para o atributo **foregroundColor** ), seu texto poderá ficar ilegível.</span><span class="sxs-lookup"><span data-stu-id="fbfbe-113">If the foreground color is also black (which is the default value for the **foregroundColor** attribute), your text may become unreadable.</span></span> <span data-ttu-id="fbfbe-114">Para evitar isso, sempre especifique o atributo **backgroundColor** ou defina **foregroundColor** como uma cor diferente de preto.</span><span class="sxs-lookup"><span data-stu-id="fbfbe-114">To prevent this, always specify the **backgroundColor** attribute, or set **foregroundColor** to a color other than black.</span></span>

<span data-ttu-id="fbfbe-115">Consulte o atributo [Value](text-value.md) para ver um exemplo ilustrando como os atributos do elemento **Text** são usados.</span><span class="sxs-lookup"><span data-stu-id="fbfbe-115">See the [value](text-value.md) attribute for a sample illustrating how the attributes of the **TEXT** element are used.</span></span>

## <a name="requirements"></a><span data-ttu-id="fbfbe-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fbfbe-116">Requirements</span></span>



| <span data-ttu-id="fbfbe-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="fbfbe-117">Requirement</span></span> | <span data-ttu-id="fbfbe-118">Valor</span><span class="sxs-lookup"><span data-stu-id="fbfbe-118">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="fbfbe-119">Versão</span><span class="sxs-lookup"><span data-stu-id="fbfbe-119">Version</span></span><br/> | <span data-ttu-id="fbfbe-120">Windows Media Player versão 7,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="fbfbe-120">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="fbfbe-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="fbfbe-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fbfbe-122">**Ambienteattributes. alphaBlend**</span><span class="sxs-lookup"><span data-stu-id="fbfbe-122">**AmbientAttributes.alphaBlend**</span></span>](ambientattributes-alphablend.md)
</dt> <dt>

[<span data-ttu-id="fbfbe-123">**Ambienteattributes. alphaBlendTo**</span><span class="sxs-lookup"><span data-stu-id="fbfbe-123">**AmbientAttributes.alphaBlendTo**</span></span>](ambientattributes-alphablendto.md)
</dt> <dt>

[<span data-ttu-id="fbfbe-124">**Referência de cor**</span><span class="sxs-lookup"><span data-stu-id="fbfbe-124">**Color Reference**</span></span>](color-reference.md)
</dt> <dt>

[<span data-ttu-id="fbfbe-125">**Elemento de texto**</span><span class="sxs-lookup"><span data-stu-id="fbfbe-125">**TEXT Element**</span></span>](text-element.md)
</dt> <dt>

[<span data-ttu-id="fbfbe-126">**TEXT. foregroundColor**</span><span class="sxs-lookup"><span data-stu-id="fbfbe-126">**TEXT.foregroundColor**</span></span>](text-foregroundcolor.md)
</dt> </dl>

 

 





