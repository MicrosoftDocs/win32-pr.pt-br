---
title: VÍDEO. tela inteira
description: O atributo fullScreen especifica ou recupera um valor que indica se o vídeo é exibido no modo de tela inteira.
ms.assetid: de74d95a-31a2-4f65-811c-4e8018ee484a
keywords:
- VÍDEO. tela inteira do Windows Media Player
topic_type:
- apiref
api_name:
- VIDEO.fullScreen
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c27fa1bde6437b55689494751410145995862d8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105765781"
---
# <a name="videofullscreen"></a><span data-ttu-id="684ad-104">VÍDEO. tela inteira</span><span class="sxs-lookup"><span data-stu-id="684ad-104">VIDEO.fullScreen</span></span>

<span data-ttu-id="684ad-105">O atributo **fullscreen** especifica ou recupera um valor que indica se o vídeo é exibido no modo de tela inteira.</span><span class="sxs-lookup"><span data-stu-id="684ad-105">The **fullScreen** attribute specifies or retrieves a value indicating whether the video is displayed in full-screen mode.</span></span>

``` syntax
        elementID.fullScreen
```

## <a name="possible-values"></a><span data-ttu-id="684ad-106">Valores possíveis</span><span class="sxs-lookup"><span data-stu-id="684ad-106">Possible Values</span></span>

<span data-ttu-id="684ad-107">Esse atributo é um **booliano** de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="684ad-107">This attribute is a read/write **Boolean**.</span></span>



| <span data-ttu-id="684ad-108">Valor</span><span class="sxs-lookup"><span data-stu-id="684ad-108">Value</span></span> | <span data-ttu-id="684ad-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="684ad-109">Description</span></span>                                          |
|-------|------------------------------------------------------|
| <span data-ttu-id="684ad-110">true</span><span class="sxs-lookup"><span data-stu-id="684ad-110">true</span></span>  | <span data-ttu-id="684ad-111">O vídeo é exibido no modo de tela inteira.</span><span class="sxs-lookup"><span data-stu-id="684ad-111">Video displays in full-screen mode.</span></span>                  |
| <span data-ttu-id="684ad-112">false</span><span class="sxs-lookup"><span data-stu-id="684ad-112">false</span></span> | <span data-ttu-id="684ad-113">Padrão.</span><span class="sxs-lookup"><span data-stu-id="684ad-113">Default.</span></span> <span data-ttu-id="684ad-114">O vídeo não é exibido no modo de tela inteira.</span><span class="sxs-lookup"><span data-stu-id="684ad-114">Video does not display in full-screen mode.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="684ad-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="684ad-115">Remarks</span></span>

<span data-ttu-id="684ad-116">Essa propriedade pode ser especificada somente em tempo de execução, após o carregamento de um arquivo.</span><span class="sxs-lookup"><span data-stu-id="684ad-116">This property can be specified only at run time, after a file has been loaded.</span></span> <span data-ttu-id="684ad-117">Portanto, ele deve ser definido dentro de um manipulador de eventos de script.</span><span class="sxs-lookup"><span data-stu-id="684ad-117">It must therefore be set within a script event handler.</span></span> <span data-ttu-id="684ad-118">O botão de escape é usado para retornar à exibição normal.</span><span class="sxs-lookup"><span data-stu-id="684ad-118">The escape button is used to return to normal viewing.</span></span>

## <a name="requirements"></a><span data-ttu-id="684ad-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="684ad-119">Requirements</span></span>



| <span data-ttu-id="684ad-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="684ad-120">Requirement</span></span> | <span data-ttu-id="684ad-121">Valor</span><span class="sxs-lookup"><span data-stu-id="684ad-121">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="684ad-122">Versão</span><span class="sxs-lookup"><span data-stu-id="684ad-122">Version</span></span><br/> | <span data-ttu-id="684ad-123">Windows Media Player versão 7,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="684ad-123">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="684ad-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="684ad-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="684ad-125">**Elemento VIDEO**</span><span class="sxs-lookup"><span data-stu-id="684ad-125">**VIDEO Element**</span></span>](video-element.md)
</dt> <dt>

[<span data-ttu-id="684ad-126">**VÍDEO. maintainAspectRatio**</span><span class="sxs-lookup"><span data-stu-id="684ad-126">**VIDEO.maintainAspectRatio**</span></span>](video-maintainaspectratio.md)
</dt> <dt>

[<span data-ttu-id="684ad-127">**VÍDEO. shrinkToFit**</span><span class="sxs-lookup"><span data-stu-id="684ad-127">**VIDEO.shrinkToFit**</span></span>](video-shrinktofit.md)
</dt> <dt>

[<span data-ttu-id="684ad-128">**VÍDEO. stretchToFit**</span><span class="sxs-lookup"><span data-stu-id="684ad-128">**VIDEO.stretchToFit**</span></span>](video-stretchtofit.md)
</dt> </dl>

 

 





