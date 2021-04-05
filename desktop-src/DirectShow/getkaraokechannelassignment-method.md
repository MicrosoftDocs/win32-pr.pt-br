---
description: O método GetKaraokeChannelAssignment recupera um valor que indica como os canais do karaokê são atribuídos aos alto-falantes.
ms.assetid: 08e35fa6-fa1b-4f9f-8f56-d953c4422226
title: Método GetKaraokeChannelAssignment
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dafe1217e08f3dc4f55aeec42424b1ebf9d86d22
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103826060"
---
# <a name="getkaraokechannelassignment-method"></a><span data-ttu-id="90e09-103">Método GetKaraokeChannelAssignment</span><span class="sxs-lookup"><span data-stu-id="90e09-103">GetKaraokeChannelAssignment Method</span></span>

> [!Note]  
> <span data-ttu-id="90e09-104">Esse componente está disponível para uso nos sistemas operacionais Microsoft Windows 2000, Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="90e09-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="90e09-105">Ele poderá ser alterado ou ficar indisponível em versões subsequentes.</span><span class="sxs-lookup"><span data-stu-id="90e09-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="90e09-106">O `GetKaraokeChannelAssignment` método recupera um valor que indica como os canais do karaokê são atribuídos aos alto-falantes.</span><span class="sxs-lookup"><span data-stu-id="90e09-106">The `GetKaraokeChannelAssignment` method retrieves a value that indicates how the karaoke channels are assigned to the speakers.</span></span>

``` syntax
[ iAssignment = ] MSWebDVD.GetKaraokeChannelAssignment(iStream)
```

## <a name="parameters"></a><span data-ttu-id="90e09-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="90e09-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="90e09-108"><span id="iStream"></span><span id="istream"></span><span id="ISTREAM"></span>*iStream*</span><span class="sxs-lookup"><span data-stu-id="90e09-108"><span id="iStream"></span><span id="istream"></span><span id="ISTREAM"></span>*iStream*</span></span>
</dt> <dd>

<span data-ttu-id="90e09-109">Especifica o fluxo de áudio como um inteiro.</span><span class="sxs-lookup"><span data-stu-id="90e09-109">Specifies the audio stream as an Integer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="90e09-110">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="90e09-110">Return Value</span></span>

<span data-ttu-id="90e09-111">Retorna um inteiro que indica a atribuição de viva-voz para o fluxo especificado.</span><span class="sxs-lookup"><span data-stu-id="90e09-111">Returns an integer indicating the speaker assignment for the specified stream.</span></span>



| <span data-ttu-id="90e09-112">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="90e09-112">Return code</span></span> | <span data-ttu-id="90e09-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="90e09-113">Description</span></span>                                                             |
|-------------|-------------------------------------------------------------------------|
| <span data-ttu-id="90e09-114">2</span><span class="sxs-lookup"><span data-stu-id="90e09-114">2</span></span>           | <span data-ttu-id="90e09-115">O fluxo é atribuído aos alto-falantes esquerdo e direito.</span><span class="sxs-lookup"><span data-stu-id="90e09-115">The stream is assigned to the left and right speakers.</span></span>                  |
| <span data-ttu-id="90e09-116">3</span><span class="sxs-lookup"><span data-stu-id="90e09-116">3</span></span>           | <span data-ttu-id="90e09-117">O fluxo é atribuído aos alto-falantes esquerdo, direito e intermediário.</span><span class="sxs-lookup"><span data-stu-id="90e09-117">The stream is assigned to the left, right, and middle speakers.</span></span>         |
| <span data-ttu-id="90e09-118">4</span><span class="sxs-lookup"><span data-stu-id="90e09-118">4</span></span>           | <span data-ttu-id="90e09-119">O fluxo é atribuído aos alto-falantes esquerdo, direito e Audio1.</span><span class="sxs-lookup"><span data-stu-id="90e09-119">The stream is assigned to the left, right, and audio1 speakers.</span></span>         |
| <span data-ttu-id="90e09-120">5</span><span class="sxs-lookup"><span data-stu-id="90e09-120">5</span></span>           | <span data-ttu-id="90e09-121">O fluxo é atribuído aos alto-falantes esquerdo, direito, médio e Audio1.</span><span class="sxs-lookup"><span data-stu-id="90e09-121">The stream is assigned to the left, right, middle, and audio1 speakers.</span></span> |
| <span data-ttu-id="90e09-122">6</span><span class="sxs-lookup"><span data-stu-id="90e09-122">6</span></span>           | <span data-ttu-id="90e09-123">O fluxo é atribuído aos alto-falantes esquerdo, direito e Audio2.</span><span class="sxs-lookup"><span data-stu-id="90e09-123">The stream is assigned to the left, right, and audio2 speakers.</span></span>         |
| <span data-ttu-id="90e09-124">7</span><span class="sxs-lookup"><span data-stu-id="90e09-124">7</span></span>           | <span data-ttu-id="90e09-125">O fluxo é atribuído aos alto-falantes esquerdo, direito, médio e Audio2.</span><span class="sxs-lookup"><span data-stu-id="90e09-125">The stream is assigned to the left, right, middle, and audio2 speakers.</span></span> |



 

## <a name="see-also"></a><span data-ttu-id="90e09-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="90e09-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="90e09-127">**KaraokeAudioPresentationMode**</span><span class="sxs-lookup"><span data-stu-id="90e09-127">**KaraokeAudioPresentationMode**</span></span>](karaokeaudiopresentationmode-property.md)
</dt> </dl>

 

 



