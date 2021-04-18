---
title: EFEITOS. tela inteira
description: O atributo fullScreen especifica ou recupera um valor que indica se a visualização atual é exibida em tela inteira. Esse atributo só pode ser definido em tempo de execução.
ms.assetid: 319b46a4-b6c2-4dda-8285-f12af6836b25
keywords:
- EFEITOS. tela inteira do Windows Media Player
topic_type:
- apiref
api_name:
- EFFECTS.fullScreen
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 64e1824e35793a083eb88ea42de0eb8858a4b76f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105784205"
---
# <a name="effectsfullscreen"></a><span data-ttu-id="3c3a0-105">EFEITOS. tela inteira</span><span class="sxs-lookup"><span data-stu-id="3c3a0-105">EFFECTS.fullScreen</span></span>

<span data-ttu-id="3c3a0-106">O atributo **fullscreen** especifica ou recupera um valor que indica se a visualização atual é exibida em tela inteira.</span><span class="sxs-lookup"><span data-stu-id="3c3a0-106">The **fullScreen** attribute specifies or retrieves a value indicating whether the current visualization is displayed full-screen.</span></span> <span data-ttu-id="3c3a0-107">Esse atributo só pode ser definido em tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="3c3a0-107">This attribute can only be set at run time.</span></span>

``` syntax
        elementID.fullScreen
```

## <a name="possible-values"></a><span data-ttu-id="3c3a0-108">Valores possíveis</span><span class="sxs-lookup"><span data-stu-id="3c3a0-108">Possible Values</span></span>

<span data-ttu-id="3c3a0-109">Esse atributo é um **booliano** de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="3c3a0-109">This attribute is a read/write **Boolean**.</span></span>



| <span data-ttu-id="3c3a0-110">Valor</span><span class="sxs-lookup"><span data-stu-id="3c3a0-110">Value</span></span> | <span data-ttu-id="3c3a0-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="3c3a0-111">Description</span></span>                                          |
|-------|------------------------------------------------------|
| <span data-ttu-id="3c3a0-112">true</span><span class="sxs-lookup"><span data-stu-id="3c3a0-112">true</span></span>  | <span data-ttu-id="3c3a0-113">A visualização é exibida em tela inteira.</span><span class="sxs-lookup"><span data-stu-id="3c3a0-113">Visualization is displayed full-screen.</span></span>              |
| <span data-ttu-id="3c3a0-114">false</span><span class="sxs-lookup"><span data-stu-id="3c3a0-114">false</span></span> | <span data-ttu-id="3c3a0-115">Padrão.</span><span class="sxs-lookup"><span data-stu-id="3c3a0-115">Default.</span></span> <span data-ttu-id="3c3a0-116">A visualização não é exibida em tela inteira.</span><span class="sxs-lookup"><span data-stu-id="3c3a0-116">Visualization is not displayed full-screen.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="3c3a0-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="3c3a0-117">Remarks</span></span>

<span data-ttu-id="3c3a0-118">Uma visualização pode ser colocada no modo de tela inteira somente enquanto a mídia está sendo reproduzida ou pausada.</span><span class="sxs-lookup"><span data-stu-id="3c3a0-118">A visualization can be put into full-screen mode only while media is playing or paused.</span></span> <span data-ttu-id="3c3a0-119">Se *Player*. **currentMedia** é vídeo, um plug-in de vídeo deve estar presente.</span><span class="sxs-lookup"><span data-stu-id="3c3a0-119">If *Player*.**currentMedia** is video, a video plug-in must be present.</span></span> <span data-ttu-id="3c3a0-120">Se for áudio, um plug-in de visualização que dá suporte à exibição de tela inteira deve estar presente.</span><span class="sxs-lookup"><span data-stu-id="3c3a0-120">If it is audio, a visualization plug-in that supports full-screen display must be present.</span></span>

## <a name="requirements"></a><span data-ttu-id="3c3a0-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3c3a0-121">Requirements</span></span>



| <span data-ttu-id="3c3a0-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="3c3a0-122">Requirement</span></span> | <span data-ttu-id="3c3a0-123">Valor</span><span class="sxs-lookup"><span data-stu-id="3c3a0-123">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="3c3a0-124">Versão</span><span class="sxs-lookup"><span data-stu-id="3c3a0-124">Version</span></span><br/> | <span data-ttu-id="3c3a0-125">Windows Media Player versão 7,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="3c3a0-125">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="3c3a0-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="3c3a0-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3c3a0-127">**Elemento EFFECTs**</span><span class="sxs-lookup"><span data-stu-id="3c3a0-127">**EFFECTS Element**</span></span>](effects-element.md)
</dt> </dl>

 

 





