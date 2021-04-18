---
description: A propriedade KaraokeAudioPresentationMode define ou recupera a combinação de alto-falantes à esquerda para os canais auxiliares do karaokê.
ms.assetid: f32706eb-7f97-433d-854a-17d57cc60190
title: Propriedade KaraokeAudioPresentationMode
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 429f15c99d58136d4c423c4f66b19d12c93802a9
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105810935"
---
# <a name="karaokeaudiopresentationmode-property"></a><span data-ttu-id="c35de-103">Propriedade KaraokeAudioPresentationMode</span><span class="sxs-lookup"><span data-stu-id="c35de-103">KaraokeAudioPresentationMode Property</span></span>

> [!Note]  
> <span data-ttu-id="c35de-104">Esse componente está disponível para uso nos sistemas operacionais Microsoft Windows 2000, Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="c35de-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="c35de-105">Ele poderá ser alterado ou ficar indisponível em versões subsequentes.</span><span class="sxs-lookup"><span data-stu-id="c35de-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="c35de-106">A `KaraokeAudioPresentationMode` propriedade define ou recupera a combinação de alto-falantes à direita para os canais do karaokê auxiliar.</span><span class="sxs-lookup"><span data-stu-id="c35de-106">The `KaraokeAudioPresentationMode` property sets or retrieves the right-left speaker mix for the auxiliary karaoke channels.</span></span>

``` syntax
[iMode ] = MSWebDVD.KaraokeAudioPresentationMode
```

## <a name="return-value"></a><span data-ttu-id="c35de-107">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="c35de-107">Return Value</span></span>

<span data-ttu-id="c35de-108">Retorna um valor inteiro que contém um conjunto de sinalizadores de bit indicando como os canais auxiliares do karaokê são downmixeds aos alto-falantes esquerdo e direito.</span><span class="sxs-lookup"><span data-stu-id="c35de-108">Returns an integer value containing a set of bit flags indicating how the auxiliary karaoke channels are downmixed to the left and right speakers.</span></span>

## <a name="remarks"></a><span data-ttu-id="c35de-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="c35de-109">Remarks</span></span>

<span data-ttu-id="c35de-110">Essa propriedade é de leitura/gravação com um valor padrão de zero.</span><span class="sxs-lookup"><span data-stu-id="c35de-110">This property is read/write with a default value of zero.</span></span>

<span data-ttu-id="c35de-111">Os canais de áudio são baseados em zero, de modo que os canais 0 e 1 geralmente representam os canais do alto-falante direito e esquerdo e os canais 2 a 4 são os três canais auxiliares do karaokê.</span><span class="sxs-lookup"><span data-stu-id="c35de-111">Audio channels are zero-based, so channels 0 and 1 generally represent the right and left speaker channels and channels 2 through 4 are the three auxiliary karaoke channels.</span></span> <span data-ttu-id="c35de-112">Quando o objeto MSWebDVD entra no modo karaokê, ele automaticamente desativa os canais 2 e superiores.</span><span class="sxs-lookup"><span data-stu-id="c35de-112">When the MSWebDVD object enters karaoke mode, it automatically mutes channels 2 and higher.</span></span> <span data-ttu-id="c35de-113">Use operações **or bits para** definir o bit apropriado para enviar um canal auxiliar para o palestrante esquerdo, o orador direito, ambos os alto-falantes (ambos os bits) ou para nenhum alto-falante (ambos bits desativados).</span><span class="sxs-lookup"><span data-stu-id="c35de-113">Use bitwise **OR** operations to set the appropriate bit in order to send an auxiliary channel to the left speaker, right speaker, both speakers (both bits on), or to no speakers (both bits off).</span></span> <span data-ttu-id="c35de-114">Esses bits são todos desativados por padrão sempre que o navegador de DVD entra no modo de karaokê.</span><span class="sxs-lookup"><span data-stu-id="c35de-114">These bits are all off by default whenever the DVD Navigator enters karaoke mode.</span></span> <span data-ttu-id="c35de-115">O valor dos bits e sua ação correspondente são fornecidos na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="c35de-115">The value of the bits and their corresponding action is given in the following table.</span></span>



| <span data-ttu-id="c35de-116">Valor</span><span class="sxs-lookup"><span data-stu-id="c35de-116">Value</span></span>  | <span data-ttu-id="c35de-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="c35de-117">Description</span></span>                            |
|--------|----------------------------------------|
| <span data-ttu-id="c35de-118">0x0004</span><span class="sxs-lookup"><span data-stu-id="c35de-118">0x0004</span></span> | <span data-ttu-id="c35de-119">Canal 2 do downmix para o alto-falante esquerdo</span><span class="sxs-lookup"><span data-stu-id="c35de-119">Downmix Channel 2 to the left speaker</span></span>  |
| <span data-ttu-id="c35de-120">0x0008</span><span class="sxs-lookup"><span data-stu-id="c35de-120">0x0008</span></span> | <span data-ttu-id="c35de-121">Downmix canal 3 para o alto-falante esquerdo</span><span class="sxs-lookup"><span data-stu-id="c35de-121">Downmix Channel 3 to the left speaker</span></span>  |
| <span data-ttu-id="c35de-122">0x0010</span><span class="sxs-lookup"><span data-stu-id="c35de-122">0x0010</span></span> | <span data-ttu-id="c35de-123">Canal 4 do downmix para o alto-falante esquerdo</span><span class="sxs-lookup"><span data-stu-id="c35de-123">Downmix Channel 4 to the left speaker</span></span>  |
| <span data-ttu-id="c35de-124">0x0400</span><span class="sxs-lookup"><span data-stu-id="c35de-124">0x0400</span></span> | <span data-ttu-id="c35de-125">Downmix canal 2 para o alto-falante direito</span><span class="sxs-lookup"><span data-stu-id="c35de-125">Downmix Channel 2 to the right speaker</span></span> |
| <span data-ttu-id="c35de-126">0x0800</span><span class="sxs-lookup"><span data-stu-id="c35de-126">0x0800</span></span> | <span data-ttu-id="c35de-127">Downmix Channel 3 para o alto-falante direito</span><span class="sxs-lookup"><span data-stu-id="c35de-127">Downmix Channel 3 to the right speaker</span></span> |
| <span data-ttu-id="c35de-128">0x1000</span><span class="sxs-lookup"><span data-stu-id="c35de-128">0x1000</span></span> | <span data-ttu-id="c35de-129">Canal 4 do downmix para o alto-falante direito</span><span class="sxs-lookup"><span data-stu-id="c35de-129">Downmix Channel 4 to the right speaker</span></span> |



 

 

 



