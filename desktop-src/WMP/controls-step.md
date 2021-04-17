---
title: Método Controls. Step
description: O método Step faz com que o item de mídia de vídeo atual congele a reprodução no próximo quadro ou no quadro anterior.
ms.assetid: f717c583-4073-45a9-b05d-7134d02724a4
keywords:
- método Step Windows Media Player
- método Step Windows Media Player, classe Controls
- Classe Controls do Windows Media Player, método Step
topic_type:
- apiref
api_name:
- Controls.step
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 43fc50ea28bde95efef6e6261788fdcc62df6089
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105811122"
---
# <a name="controlsstep-method"></a><span data-ttu-id="f6b13-106">Método Controls. Step</span><span class="sxs-lookup"><span data-stu-id="f6b13-106">Controls.step method</span></span>

<span data-ttu-id="f6b13-107">O método **Step** faz com que o item de mídia de vídeo atual congele a reprodução no próximo quadro ou no quadro anterior.</span><span class="sxs-lookup"><span data-stu-id="f6b13-107">The **step** method causes the current video media item to freeze playback on the next frame or the previous frame.</span></span>

## <a name="syntax"></a><span data-ttu-id="f6b13-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f6b13-108">Syntax</span></span>


```JScript
Controls.step(
  frameCount
)
```



## <a name="parameters"></a><span data-ttu-id="f6b13-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f6b13-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f6b13-110">*frameCount* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f6b13-110">*frameCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f6b13-111">**Número** (**longo**) indicando quantos quadros passar antes de congelar.</span><span class="sxs-lookup"><span data-stu-id="f6b13-111">**Number** (**long**) indicating how many frames to step before freezing.</span></span> <span data-ttu-id="f6b13-112">Deve ser definido no momento como 1 ou-1.</span><span class="sxs-lookup"><span data-stu-id="f6b13-112">Must currently be set to 1 or -1.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f6b13-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f6b13-113">Return value</span></span>

<span data-ttu-id="f6b13-114">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="f6b13-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f6b13-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="f6b13-115">Remarks</span></span>

<span data-ttu-id="f6b13-116">Esse método atualmente só dá suporte aos parâmetros 1 ou-1, portanto, você só pode passar um quadro por vez.</span><span class="sxs-lookup"><span data-stu-id="f6b13-116">This method currently only supports the parameters 1 or -1, so you can only step one frame at a time.</span></span>

<span data-ttu-id="f6b13-117">**Windows Media Player 10 Mobile:** Não há suporte para esse método.</span><span class="sxs-lookup"><span data-stu-id="f6b13-117">**Windows Media Player 10 Mobile:** This method is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="f6b13-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f6b13-118">Requirements</span></span>



| <span data-ttu-id="f6b13-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="f6b13-119">Requirement</span></span> | <span data-ttu-id="f6b13-120">Valor</span><span class="sxs-lookup"><span data-stu-id="f6b13-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="f6b13-121">Versão</span><span class="sxs-lookup"><span data-stu-id="f6b13-121">Version</span></span><br/> | <span data-ttu-id="f6b13-122">Windows Media Player para Windows XP ou posterior.</span><span class="sxs-lookup"><span data-stu-id="f6b13-122">Windows Media Player for Windows XP or later.</span></span><br/>                           |
| <span data-ttu-id="f6b13-123">DLL</span><span class="sxs-lookup"><span data-stu-id="f6b13-123">DLL</span></span><br/>     | <dl> <span data-ttu-id="f6b13-124"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f6b13-124"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f6b13-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="f6b13-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f6b13-126">**Objeto Controls**</span><span class="sxs-lookup"><span data-stu-id="f6b13-126">**Controls Object**</span></span>](controls-object.md)
</dt> <dt>

[<span data-ttu-id="f6b13-127">**Objeto de DVD**</span><span class="sxs-lookup"><span data-stu-id="f6b13-127">**DVD Object**</span></span>](dvd-object.md)
</dt> </dl>

 

 





