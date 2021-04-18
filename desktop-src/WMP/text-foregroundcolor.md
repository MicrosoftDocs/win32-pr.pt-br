---
title: TEXT. foregroundColor
description: O atributo foregroundColor especifica ou recupera a cor do texto para o controle de texto.
ms.assetid: 1ddbad93-fbff-4be6-9797-6594b5f09a1e
keywords:
- TEXT. foregroundColor Windows Media Player
topic_type:
- apiref
api_name:
- TEXT.foregroundColor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e452a18a085337e8cbf0ec88567d6a57a0a498a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105810751"
---
# <a name="textforegroundcolor"></a><span data-ttu-id="5036c-104">TEXT. foregroundColor</span><span class="sxs-lookup"><span data-stu-id="5036c-104">TEXT.foregroundColor</span></span>

<span data-ttu-id="5036c-105">O atributo **foregroundColor** especifica ou recupera a cor do texto para o controle de texto.</span><span class="sxs-lookup"><span data-stu-id="5036c-105">The **foregroundColor** attribute specifies or retrieves the text color for the Text control.</span></span>

``` syntax
        elementID.foregroundColor
```

## <a name="possible-values"></a><span data-ttu-id="5036c-106">Valores possíveis</span><span class="sxs-lookup"><span data-stu-id="5036c-106">Possible Values</span></span>

<span data-ttu-id="5036c-107">Esse atributo é uma **cadeia de caracteres** de leitura/gravação que contém qualquer valor de cor do Microsoft Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="5036c-107">This attribute is a read/write **String** containing any Microsoft Internet Explorer color value.</span></span> <span data-ttu-id="5036c-108">O valor padrão é "Black".</span><span class="sxs-lookup"><span data-stu-id="5036c-108">The default value is "black".</span></span>

<span data-ttu-id="5036c-109">Consulte o atributo [Value](text-value.md) para ver um exemplo ilustrando como os atributos do elemento **Text** são usados.</span><span class="sxs-lookup"><span data-stu-id="5036c-109">See the [value](text-value.md) attribute for a sample illustrating how the attributes of the **TEXT** element are used.</span></span>

<span data-ttu-id="5036c-110">Quando você usa **alphaBlend** ou **alphaBlendTo** com um elemento de **texto** que não tem o **backgroundColor** especificado, uma cor de plano de fundo de preto será usada.</span><span class="sxs-lookup"><span data-stu-id="5036c-110">When you use **alphaBlend** or **alphaBlendTo** with a **TEXT** element that does not have the **backgroundColor** specified, a background color of black will be used.</span></span> <span data-ttu-id="5036c-111">Se a cor de primeiro plano também for preta (que é o valor padrão para o atributo **foregroundColor** ), seu texto poderá ficar ilegível.</span><span class="sxs-lookup"><span data-stu-id="5036c-111">If the foreground color is also black (which is the default value for the **foregroundColor** attribute), your text may become unreadable.</span></span> <span data-ttu-id="5036c-112">Para evitar isso, sempre especifique o atributo **backgroundColor** ou defina **foregroundColor** como uma cor diferente de preto.</span><span class="sxs-lookup"><span data-stu-id="5036c-112">To prevent this, always specify the **backgroundColor** attribute, or set **foregroundColor** to a color other than black.</span></span>

## <a name="requirements"></a><span data-ttu-id="5036c-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5036c-113">Requirements</span></span>



| <span data-ttu-id="5036c-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="5036c-114">Requirement</span></span> | <span data-ttu-id="5036c-115">Valor</span><span class="sxs-lookup"><span data-stu-id="5036c-115">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="5036c-116">Versão</span><span class="sxs-lookup"><span data-stu-id="5036c-116">Version</span></span><br/> | <span data-ttu-id="5036c-117">Windows Media Player versão 7,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="5036c-117">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="5036c-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="5036c-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5036c-119">**Ambienteattributes. alphaBlend**</span><span class="sxs-lookup"><span data-stu-id="5036c-119">**AmbientAttributes.alphaBlend**</span></span>](ambientattributes-alphablend.md)
</dt> <dt>

[<span data-ttu-id="5036c-120">**Ambienteattributes. alphaBlendTo**</span><span class="sxs-lookup"><span data-stu-id="5036c-120">**AmbientAttributes.alphaBlendTo**</span></span>](ambientattributes-alphablendto.md)
</dt> <dt>

[<span data-ttu-id="5036c-121">**Referência de cor**</span><span class="sxs-lookup"><span data-stu-id="5036c-121">**Color Reference**</span></span>](color-reference.md)
</dt> <dt>

[<span data-ttu-id="5036c-122">**Elemento de texto**</span><span class="sxs-lookup"><span data-stu-id="5036c-122">**TEXT Element**</span></span>](text-element.md)
</dt> <dt>

[<span data-ttu-id="5036c-123">**TEXT. backgroundColor**</span><span class="sxs-lookup"><span data-stu-id="5036c-123">**TEXT.backgroundColor**</span></span>](text-backgroundcolor.md)
</dt> </dl>

 

 





