---
title: VÍDEO. sem janela
description: O atributo sem janela especifica ou recupera um valor que indica se o controle de vídeo será em janelas ou sem janela; ou seja, se todo o retângulo do controle estará visível sempre ou puder ser recortado.
ms.assetid: d59e6baf-374b-48f6-b99f-35a83af7feb6
keywords:
- VÍDEO. Windows Media Player sem janela
topic_type:
- apiref
api_name:
- VIDEO.windowless
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3a17d905d2ba8c11254476337d656890469b2b6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105763937"
---
# <a name="videowindowless"></a><span data-ttu-id="f4f89-104">VÍDEO. sem janela</span><span class="sxs-lookup"><span data-stu-id="f4f89-104">VIDEO.windowless</span></span>

<span data-ttu-id="f4f89-105">O atributo **sem janela** especifica ou recupera um valor que indica se o controle de vídeo será em janelas ou sem janela; ou seja, se todo o retângulo do controle estará visível sempre ou puder ser recortado.</span><span class="sxs-lookup"><span data-stu-id="f4f89-105">The **windowless** attribute specifies or retrieves a value indicating whether the Video control will be windowed or windowless; that is, whether the entire rectangle of the control will be visible at all times or can be clipped.</span></span> <span data-ttu-id="f4f89-106">Só pode ser definido em tempo de design.</span><span class="sxs-lookup"><span data-stu-id="f4f89-106">Can only be set at design time.</span></span>

``` syntax
        elementID.windowless
```

## <a name="possible-values"></a><span data-ttu-id="f4f89-107">Valores possíveis</span><span class="sxs-lookup"><span data-stu-id="f4f89-107">Possible Values</span></span>

<span data-ttu-id="f4f89-108">Esse atributo é um **booliano** especificado em tempo de design e somente leitura depois.</span><span class="sxs-lookup"><span data-stu-id="f4f89-108">This attribute is a **Boolean** specified at design time and read-only thereafter.</span></span>



| <span data-ttu-id="f4f89-109">Valor</span><span class="sxs-lookup"><span data-stu-id="f4f89-109">Value</span></span> | <span data-ttu-id="f4f89-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="f4f89-110">Description</span></span>                              |
|-------|------------------------------------------|
| <span data-ttu-id="f4f89-111">true</span><span class="sxs-lookup"><span data-stu-id="f4f89-111">true</span></span>  | <span data-ttu-id="f4f89-112">O controle de vídeo não terá janela.</span><span class="sxs-lookup"><span data-stu-id="f4f89-112">Video control will be windowless.</span></span>        |
| <span data-ttu-id="f4f89-113">false</span><span class="sxs-lookup"><span data-stu-id="f4f89-113">false</span></span> | <span data-ttu-id="f4f89-114">Padrão.</span><span class="sxs-lookup"><span data-stu-id="f4f89-114">Default.</span></span> <span data-ttu-id="f4f89-115">O controle de vídeo será janelas.</span><span class="sxs-lookup"><span data-stu-id="f4f89-115">Video control will be windowed.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="f4f89-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="f4f89-116">Remarks</span></span>

<span data-ttu-id="f4f89-117">Se uma janela de vídeo não retangular for desejada ou se você quiser cobrir qualquer parte da janela de vídeo com uma imagem, esse atributo deverá ser definido como true.</span><span class="sxs-lookup"><span data-stu-id="f4f89-117">If a non-rectangular video window is desired, or if you want to cover any part of the video window with an image, this attribute must be set to true.</span></span> <span data-ttu-id="f4f89-118">Isso sacrificaria algum desempenho para fazer o recorte necessário.</span><span class="sxs-lookup"><span data-stu-id="f4f89-118">This sacrifices some performance to do the necessary clipping.</span></span>

<span data-ttu-id="f4f89-119">A reprodução de vídeo é otimizada para reprodução não recortada.</span><span class="sxs-lookup"><span data-stu-id="f4f89-119">Video playback is optimized for unclipped playback.</span></span> <span data-ttu-id="f4f89-120">Nesse caso, o atributo **sem janela** é definido como false e todo o retângulo de vídeo é sempre exibido.</span><span class="sxs-lookup"><span data-stu-id="f4f89-120">In this case, the **windowless** attribute is set to false, and the entire video rectangle is always displayed.</span></span> <span data-ttu-id="f4f89-121">Qualquer imagem que abranja a janela de vídeo é ignorada e a janela de vídeo tem a ordem z de nível mais alto.</span><span class="sxs-lookup"><span data-stu-id="f4f89-121">Any image covering the video window is ignored, and the video window has the highest-level z-order.</span></span>

## <a name="requirements"></a><span data-ttu-id="f4f89-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f4f89-122">Requirements</span></span>



| <span data-ttu-id="f4f89-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="f4f89-123">Requirement</span></span> | <span data-ttu-id="f4f89-124">Valor</span><span class="sxs-lookup"><span data-stu-id="f4f89-124">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="f4f89-125">Versão</span><span class="sxs-lookup"><span data-stu-id="f4f89-125">Version</span></span><br/> | <span data-ttu-id="f4f89-126">Windows Media Player versão 7,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="f4f89-126">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f4f89-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="f4f89-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f4f89-128">**Elemento VIDEO**</span><span class="sxs-lookup"><span data-stu-id="f4f89-128">**VIDEO Element**</span></span>](video-element.md)
</dt> </dl>

 

 





