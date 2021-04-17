---
title: Ambienteattributes. alphaBlend
description: O atributo alphaBlend especifica ou recupera um valor para a mistura alfa de qualquer exibição, subexibição ou widget de interface do usuário.
ms.assetid: a6c47d32-a497-4bfa-8fa3-ef94e267d94b
keywords:
- AlphaBlend do Windows Media Player de ambiente.
topic_type:
- apiref
api_name:
- AmbientAttributes.alphaBlend
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8c0f0cb9d885f643b39acfbc5148403a5c8b788
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105763382"
---
# <a name="ambientattributesalphablend"></a><span data-ttu-id="118fa-104">Ambienteattributes. alphaBlend</span><span class="sxs-lookup"><span data-stu-id="118fa-104">AmbientAttributes.alphaBlend</span></span>

<span data-ttu-id="118fa-105">O atributo **alphaBlend** especifica ou recupera um valor para a mistura alfa de qualquer **exibição**, **subexibição** ou widget de interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="118fa-105">The **alphaBlend** attribute specifies or retrieves a value for alpha blending any **VIEW**, **SUBVIEW**, or UI widget.</span></span>

``` syntax
        elementID.alphaBlend
```

## <a name="possible-values"></a><span data-ttu-id="118fa-106">Valores possíveis</span><span class="sxs-lookup"><span data-stu-id="118fa-106">Possible Values</span></span>

<span data-ttu-id="118fa-107">Esse atributo é um **número** de leitura/gravação (**longo**) com um valor que varia de 0 (sem opacidade) a 255 (opacidade total) e um valor padrão de 255.</span><span class="sxs-lookup"><span data-stu-id="118fa-107">This attribute is a read/write **Number** (**long**) with a value ranging from 0 (no opacity) to 255 (full opacity) and a default value of 255.</span></span>

## <a name="remarks"></a><span data-ttu-id="118fa-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="118fa-108">Remarks</span></span>

<span data-ttu-id="118fa-109">Esse atributo permite que um elemento apareça semitransparente, dependendo da quantidade de opacidade definida.</span><span class="sxs-lookup"><span data-stu-id="118fa-109">This attribute allows an element to appear semitransparent, depending on the amount of opacity set.</span></span> <span data-ttu-id="118fa-110">Quanto menor a opacidade, mais transparente será a aparência do elemento.</span><span class="sxs-lookup"><span data-stu-id="118fa-110">The less opacity, the more transparent the element will appear.</span></span> <span data-ttu-id="118fa-111">Cada elemento na capa pode ter um valor de opacidade separado, exceto os elementos de botão em um controle de **botão** .</span><span class="sxs-lookup"><span data-stu-id="118fa-111">Each element in the skin can have a separate opacity value except for button elements in a **BUTTONGROUP** control.</span></span> <span data-ttu-id="118fa-112">Quando **alphaBlend** é definido na **exibição**, a opacidade de toda a capa será definida.</span><span class="sxs-lookup"><span data-stu-id="118fa-112">When **alphaBlend** is set in **VIEW**, the opacity of the entire skin will be set.</span></span> <span data-ttu-id="118fa-113">O Alpha Blend não funcionará para controles em janela, incluindo **playlist**, **Effects**, **ListBox**,  **Popup**, e **Video** (se **sem janelas** estiver definido como false).</span><span class="sxs-lookup"><span data-stu-id="118fa-113">Alpha blend will not work for windowed controls, including **PLAYLIST**, **EFFECTS**, **LISTBOX**, **POPUP**, **EDITBOX**, and **VIDEO** (if **windowless** is set to false).</span></span> <span data-ttu-id="118fa-114">Quando **alphaBlend** é definido na **exibição**, toda a capa torna-se transparente.</span><span class="sxs-lookup"><span data-stu-id="118fa-114">When **alphaBlend** is set on **VIEW**, the whole skin becomes transparent.</span></span> <span data-ttu-id="118fa-115">Os atributos **transparencyColor** usados por vários elementos não têm suporte com **alphaBlend**.</span><span class="sxs-lookup"><span data-stu-id="118fa-115">The **transparencyColor** attributes used by several elements are not supported with **alphaBlend**.</span></span>

<span data-ttu-id="118fa-116">Quando você usa **alphaBlend** com um elemento de **texto** que não tem o **backgroundColor** especificado, uma cor de plano de fundo de preto será usada.</span><span class="sxs-lookup"><span data-stu-id="118fa-116">When you use **alphaBlend** with a **TEXT** element that does not have the **backgroundColor** specified, a background color of black will be used.</span></span> <span data-ttu-id="118fa-117">Se a cor de primeiro plano também for preta (que é o valor padrão para *texto*.**foregroundColor**), seu texto pode se tornar ilegível.</span><span class="sxs-lookup"><span data-stu-id="118fa-117">If the foreground color is also black (which is the default value for *TEXT*.**foregroundColor**), your text may become unreadable.</span></span> <span data-ttu-id="118fa-118">Para evitar isso, sempre especifique o atributo **backgroundColor** ou defina **foregroundColor** como uma cor diferente de preto.</span><span class="sxs-lookup"><span data-stu-id="118fa-118">To prevent this, always specify the **backgroundColor** attribute, or set **foregroundColor** to a color other than black.</span></span>

> [!Note]  
> <span data-ttu-id="118fa-119">Não há suporte para esse atributo no Windows 98.</span><span class="sxs-lookup"><span data-stu-id="118fa-119">This attribute is not supported in Windows 98.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="118fa-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="118fa-120">Requirements</span></span>



| <span data-ttu-id="118fa-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="118fa-121">Requirement</span></span> | <span data-ttu-id="118fa-122">Valor</span><span class="sxs-lookup"><span data-stu-id="118fa-122">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="118fa-123">Versão</span><span class="sxs-lookup"><span data-stu-id="118fa-123">Version</span></span><br/> | <span data-ttu-id="118fa-124">Windows Media Player 9 Series ou posterior</span><span class="sxs-lookup"><span data-stu-id="118fa-124">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="118fa-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="118fa-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="118fa-126">**Atributos de ambiente**</span><span class="sxs-lookup"><span data-stu-id="118fa-126">**Ambient Attributes**</span></span>](ambient-attributes.md)
</dt> <dt>

[<span data-ttu-id="118fa-127">**Ambienteattributes. alphaBlendTo**</span><span class="sxs-lookup"><span data-stu-id="118fa-127">**AmbientAttributes.alphaBlendTo**</span></span>](ambientattributes-alphablendto.md)
</dt> <dt>

[<span data-ttu-id="118fa-128">**Elemento de texto**</span><span class="sxs-lookup"><span data-stu-id="118fa-128">**TEXT Element**</span></span>](text-element.md)
</dt> <dt>

[<span data-ttu-id="118fa-129">**TEXT. backgroundColor**</span><span class="sxs-lookup"><span data-stu-id="118fa-129">**TEXT.backgroundColor**</span></span>](text-backgroundcolor.md)
</dt> <dt>

[<span data-ttu-id="118fa-130">**TEXT. foregroundColor**</span><span class="sxs-lookup"><span data-stu-id="118fa-130">**TEXT.foregroundColor**</span></span>](text-foregroundcolor.md)
</dt> </dl>

 

 





