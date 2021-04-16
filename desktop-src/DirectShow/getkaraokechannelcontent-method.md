---
description: O método GetKaraokeChannelContent recupera um valor que indica o tipo de conteúdo no canal do karaokê especificado no fluxo especificado.
ms.assetid: e36a88b8-7184-44a4-8e02-204440f651bc
title: Método GetKaraokeChannelContent
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bd35705f1fba65eaf5c6f7c67ea55078c68e5036
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105768644"
---
# <a name="getkaraokechannelcontent-method"></a><span data-ttu-id="b713d-103">Método GetKaraokeChannelContent</span><span class="sxs-lookup"><span data-stu-id="b713d-103">GetKaraokeChannelContent Method</span></span>

> [!Note]  
> <span data-ttu-id="b713d-104">Esse componente está disponível para uso nos sistemas operacionais Microsoft Windows 2000, Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="b713d-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="b713d-105">Ele poderá ser alterado ou ficar indisponível em versões subsequentes.</span><span class="sxs-lookup"><span data-stu-id="b713d-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="b713d-106">O `GetKaraokeChannelContent` método recupera um valor que indica o tipo de conteúdo no canal do karaokê especificado no fluxo especificado.</span><span class="sxs-lookup"><span data-stu-id="b713d-106">The `GetKaraokeChannelContent` method retrieves a value that indicates the type of content in the specified karaoke channel in the specified stream.</span></span>

``` syntax
[ iContent = ] MSWebDVD.GetKaraokeChannelContent(iStream, iChannel)
```

## <a name="parameters"></a><span data-ttu-id="b713d-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b713d-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b713d-108"><span id="iStream"></span><span id="istream"></span><span id="ISTREAM"></span>*iStream*</span><span class="sxs-lookup"><span data-stu-id="b713d-108"><span id="iStream"></span><span id="istream"></span><span id="ISTREAM"></span>*iStream*</span></span>
</dt> <dd>

<span data-ttu-id="b713d-109">Especifica o fluxo de áudio como um inteiro.</span><span class="sxs-lookup"><span data-stu-id="b713d-109">Specifies the audio stream as an Integer.</span></span>

</dd> <dt>

<span data-ttu-id="b713d-110"><span id="iChannel"></span><span id="ichannel"></span><span id="ICHANNEL"></span>*iChannel*</span><span class="sxs-lookup"><span data-stu-id="b713d-110"><span id="iChannel"></span><span id="ichannel"></span><span id="ICHANNEL"></span>*iChannel*</span></span>
</dt> <dd>

<span data-ttu-id="b713d-111">Especifica o canal como um inteiro.</span><span class="sxs-lookup"><span data-stu-id="b713d-111">Specifies the channel as an Integer.</span></span> <span data-ttu-id="b713d-112">Os valores possíveis para cada canal são:</span><span class="sxs-lookup"><span data-stu-id="b713d-112">The possible values for each channel are:</span></span>



| <span data-ttu-id="b713d-113">Valor</span><span class="sxs-lookup"><span data-stu-id="b713d-113">Value</span></span>  | <span data-ttu-id="b713d-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="b713d-114">Description</span></span>    |
|--------|----------------|
| <span data-ttu-id="b713d-115">0x0001</span><span class="sxs-lookup"><span data-stu-id="b713d-115">0x0001</span></span> | <span data-ttu-id="b713d-116">Guia vocal 1</span><span class="sxs-lookup"><span data-stu-id="b713d-116">Guide Vocal 1</span></span>  |
| <span data-ttu-id="b713d-117">0x0002</span><span class="sxs-lookup"><span data-stu-id="b713d-117">0x0002</span></span> | <span data-ttu-id="b713d-118">Guia vocal 2</span><span class="sxs-lookup"><span data-stu-id="b713d-118">Guide Vocal 2</span></span>  |
| <span data-ttu-id="b713d-119">0x0004</span><span class="sxs-lookup"><span data-stu-id="b713d-119">0x0004</span></span> | <span data-ttu-id="b713d-120">Guia de melodia 1</span><span class="sxs-lookup"><span data-stu-id="b713d-120">Guide Melody 1</span></span> |
| <span data-ttu-id="b713d-121">0x0008</span><span class="sxs-lookup"><span data-stu-id="b713d-121">0x0008</span></span> | <span data-ttu-id="b713d-122">Guia de melodia 2</span><span class="sxs-lookup"><span data-stu-id="b713d-122">Guide Melody 2</span></span> |
| <span data-ttu-id="b713d-123">0x0010</span><span class="sxs-lookup"><span data-stu-id="b713d-123">0x0010</span></span> | <span data-ttu-id="b713d-124">Guia de melodia A</span><span class="sxs-lookup"><span data-stu-id="b713d-124">Guide Melody A</span></span> |
| <span data-ttu-id="b713d-125">0x0020</span><span class="sxs-lookup"><span data-stu-id="b713d-125">0x0020</span></span> | <span data-ttu-id="b713d-126">Guia de melodia B</span><span class="sxs-lookup"><span data-stu-id="b713d-126">Guide Melody B</span></span> |
| <span data-ttu-id="b713d-127">0x0040</span><span class="sxs-lookup"><span data-stu-id="b713d-127">0x0040</span></span> | <span data-ttu-id="b713d-128">Efeito de som A</span><span class="sxs-lookup"><span data-stu-id="b713d-128">Sound Effect A</span></span> |
| <span data-ttu-id="b713d-129">0x0080</span><span class="sxs-lookup"><span data-stu-id="b713d-129">0x0080</span></span> | <span data-ttu-id="b713d-130">Efeito de som B</span><span class="sxs-lookup"><span data-stu-id="b713d-130">Sound Effect B</span></span> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b713d-131">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="b713d-131">Return Value</span></span>

<span data-ttu-id="b713d-132">Retorna um valor inteiro cujos bits individuais especificam o conteúdo do canal do karaokê.</span><span class="sxs-lookup"><span data-stu-id="b713d-132">Returns an integer value whose individual bits specify the contents of the karaoke channel.</span></span>

## <a name="remarks"></a><span data-ttu-id="b713d-133">Comentários</span><span class="sxs-lookup"><span data-stu-id="b713d-133">Remarks</span></span>

<span data-ttu-id="b713d-134">A numeração do canal de áudio de DVD é baseada em zero, portanto, os canais 2, 3 e 4 são os canais auxiliares do karaokê.</span><span class="sxs-lookup"><span data-stu-id="b713d-134">DVD audio channel numbering is zero-based, so channels 2, 3, and 4 are the auxiliary karaoke channels.</span></span> <span data-ttu-id="b713d-135">Depois que o método retornar, execute uma operação AND bit a bit em *iContent* para determinar o conteúdo de cada canal.</span><span class="sxs-lookup"><span data-stu-id="b713d-135">After the method returns, perform a bitwise AND operation on *iContent* to determine the contents of each channel.</span></span> <span data-ttu-id="b713d-136">Como um único canal pode ter mais de um tipo de conteúdo registrado nele, você deve testar todos os valores possíveis mesmo depois que uma correspondência for encontrada.</span><span class="sxs-lookup"><span data-stu-id="b713d-136">Because a single channel might have more than one type of content recorded on it, you should test for all the possible values even after a match is found.</span></span>

<span data-ttu-id="b713d-137">Depois que o usuário conhece o conteúdo de cada canal, ele deve ser capaz de ajustar o volume ou ativar ou desativar os canais individuais, conforme necessário.</span><span class="sxs-lookup"><span data-stu-id="b713d-137">After the user knows the contents of each channel, he or she must be able to adjust the volume or turn the individual channels on or off as needed.</span></span> <span data-ttu-id="b713d-138">Implemente essa funcionalidade em seu aplicativo usando a propriedade [**KaraokeAudioPresentationMode**](karaokeaudiopresentationmode-property.md) .</span><span class="sxs-lookup"><span data-stu-id="b713d-138">Implement this functionality in your application by using the [**KaraokeAudioPresentationMode**](karaokeaudiopresentationmode-property.md) property.</span></span>

> [!Note]  
> <span data-ttu-id="b713d-139">Para reproduzir discos do karaokê, o decodificador de áudio no sistema do usuário deve ser compatível com a implementação do karaokê do DirectShow 8.</span><span class="sxs-lookup"><span data-stu-id="b713d-139">To play karaoke discs, the audio decoder on the user's system must be compatible with the DirectShow 8 karaoke implementation.</span></span>

 

 

 



