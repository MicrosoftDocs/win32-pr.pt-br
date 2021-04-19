---
title: TEXT. fontSmoothing
description: O atributo fontSmoothing especifica ou recupera um valor que indica se a suavização de fontes está habilitada.
ms.assetid: bd6f0468-285e-44b3-a5e8-361744c5ce4a
keywords:
- TEXT. fontSmoothing Windows Media Player
topic_type:
- apiref
api_name:
- TEXT.fontSmoothing
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fcdf285572b4edda0f514cb3519b6953f9e94677
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105813548"
---
# <a name="textfontsmoothing"></a><span data-ttu-id="907ea-104">TEXT. fontSmoothing</span><span class="sxs-lookup"><span data-stu-id="907ea-104">TEXT.fontSmoothing</span></span>

<span data-ttu-id="907ea-105">O atributo **fontSmoothing** especifica ou recupera um valor que indica se a suavização de fontes está habilitada.</span><span class="sxs-lookup"><span data-stu-id="907ea-105">The **fontSmoothing** attribute specifies or retrieves a value indicating whether font smoothing is enabled.</span></span>

``` syntax
        elementID.fontSmoothing
```

## <a name="possible-values"></a><span data-ttu-id="907ea-106">Valores possíveis</span><span class="sxs-lookup"><span data-stu-id="907ea-106">Possible Values</span></span>

<span data-ttu-id="907ea-107">Esse atributo é um **booliano** de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="907ea-107">This attribute is a read/write **Boolean**.</span></span>



| <span data-ttu-id="907ea-108">Valor</span><span class="sxs-lookup"><span data-stu-id="907ea-108">Value</span></span> | <span data-ttu-id="907ea-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="907ea-109">Description</span></span>                          |
|-------|--------------------------------------|
| <span data-ttu-id="907ea-110">true</span><span class="sxs-lookup"><span data-stu-id="907ea-110">true</span></span>  | <span data-ttu-id="907ea-111">A suavização de fontes está habilitada.</span><span class="sxs-lookup"><span data-stu-id="907ea-111">Font smoothing is enabled.</span></span>           |
| <span data-ttu-id="907ea-112">false</span><span class="sxs-lookup"><span data-stu-id="907ea-112">false</span></span> | <span data-ttu-id="907ea-113">Padrão.</span><span class="sxs-lookup"><span data-stu-id="907ea-113">Default.</span></span> <span data-ttu-id="907ea-114">A suavização de fontes está desabilitada.</span><span class="sxs-lookup"><span data-stu-id="907ea-114">Font smoothing is disabled.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="907ea-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="907ea-115">Remarks</span></span>

<span data-ttu-id="907ea-116">A suavização de fontes usa o recurso de suavização de serrilhado do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="907ea-116">Font smoothing uses the anti-aliasing feature of the operating system.</span></span> <span data-ttu-id="907ea-117">Se a suavização de fontes estiver habilitada e o sistema operacional oferecer suporte a suavização de serrilhado, o Windows Media Player tentará suavizar o texto.</span><span class="sxs-lookup"><span data-stu-id="907ea-117">If font smoothing is enabled and the operating system supports anti-aliasing, Windows Media Player attempts to smooth the text.</span></span> <span data-ttu-id="907ea-118">Nem todas as fontes dão suporte à suavização de serrilhado.</span><span class="sxs-lookup"><span data-stu-id="907ea-118">Not all fonts support anti-aliasing.</span></span> <span data-ttu-id="907ea-119">O Windows Media Player 10 usa o método de suavização de serrilhado Windows XP ClearType.</span><span class="sxs-lookup"><span data-stu-id="907ea-119">Windows Media Player 10 uses the Windows XP ClearType anti-aliasing method.</span></span>

-   <span data-ttu-id="907ea-120">**Aviso** A suavização de fontes em uma cor transparente pode fazer com que a cor transparente seja mesclada nos caracteres.</span><span class="sxs-lookup"><span data-stu-id="907ea-120">**Warning** Font smoothing over a transparent color may cause the transparent color to blend into the characters.</span></span> <span data-ttu-id="907ea-121">Não é recomendável que você use **fontSmoothing** se o texto for exibido em uma transparência.</span><span class="sxs-lookup"><span data-stu-id="907ea-121">It is not recommended that you use **fontSmoothing** if the text will display over a transparency.</span></span>

<span data-ttu-id="907ea-122">Consulte o atributo [Value](text-value.md) para ver um exemplo ilustrando como os atributos do elemento **Text** são usados.</span><span class="sxs-lookup"><span data-stu-id="907ea-122">See the [value](text-value.md) attribute for a sample illustrating how the attributes of the **TEXT** element are used.</span></span>

## <a name="requirements"></a><span data-ttu-id="907ea-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="907ea-123">Requirements</span></span>



| <span data-ttu-id="907ea-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="907ea-124">Requirement</span></span> | <span data-ttu-id="907ea-125">Valor</span><span class="sxs-lookup"><span data-stu-id="907ea-125">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="907ea-126">Versão</span><span class="sxs-lookup"><span data-stu-id="907ea-126">Version</span></span><br/> | <span data-ttu-id="907ea-127">Windows Media Player versão 7,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="907ea-127">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="907ea-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="907ea-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="907ea-129">**Elemento de texto**</span><span class="sxs-lookup"><span data-stu-id="907ea-129">**TEXT Element**</span></span>](text-element.md)
</dt> </dl>

 

 





