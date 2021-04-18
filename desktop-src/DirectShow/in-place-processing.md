---
description: Processamento de In-Place
ms.assetid: 61e5c12c-e42a-42d8-ac5b-e60afaceda82
title: Processamento de In-Place
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ba0aa5c50fc000eadadc0f121db6f954a57c338
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105766304"
---
# <a name="in-place-processing"></a><span data-ttu-id="83632-103">Processamento de In-Place</span><span class="sxs-lookup"><span data-stu-id="83632-103">In-Place Processing</span></span>

<span data-ttu-id="83632-104">Determinadas transformações de dados podem ser realizadas com a modificação direta dos dados.</span><span class="sxs-lookup"><span data-stu-id="83632-104">Certain data transformations can be accomplished by directly modifying the data.</span></span> <span data-ttu-id="83632-105">Isso é chamado *de* processamento in-loco.</span><span class="sxs-lookup"><span data-stu-id="83632-105">This is called *in-place* processing.</span></span> <span data-ttu-id="83632-106">Muitos efeitos de áudio e vídeo podem ser feitos dessa maneira.</span><span class="sxs-lookup"><span data-stu-id="83632-106">Many audio and video effects can be done in this manner.</span></span> <span data-ttu-id="83632-107">Se um DMO der suporte ao processamento in-loco, ele expõe a interface [**IMediaObjectInPlace**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-imediaobjectinplace) .</span><span class="sxs-lookup"><span data-stu-id="83632-107">If a DMO supports in-place processing, it exposes the [**IMediaObjectInPlace**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-imediaobjectinplace) interface.</span></span> <span data-ttu-id="83632-108">O processamento in-loco é geralmente mais eficiente do que usar buffers separados para a saída.</span><span class="sxs-lookup"><span data-stu-id="83632-108">In-place processing is generally more efficient than using separate buffers for the output.</span></span> <span data-ttu-id="83632-109">(Uma exceção principal é quando o buffer reside na memória de vídeo.</span><span class="sxs-lookup"><span data-stu-id="83632-109">(One major exception is when the buffer resides in video memory.</span></span> <span data-ttu-id="83632-110">Nessa situação, as operações de leitura são muito mais lentas do que as operações de gravação, portanto, o processamento in-loco não é recomendado.)</span><span class="sxs-lookup"><span data-stu-id="83632-110">In that situation, read operations are much slower than write operations, so in-place processing is not recommended.)</span></span>

<span data-ttu-id="83632-111">Para processar dados no local, o cliente faz uma única chamada para o método [**IMediaObjectInPlace::P modelos**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobjectinplace-process) , em vez de chamadas separadas para **ProcessInput** e **ProcessOutput**.</span><span class="sxs-lookup"><span data-stu-id="83632-111">To process data in place, the client makes a single call to the [**IMediaObjectInPlace::Process**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobjectinplace-process) method, rather than separate calls to **ProcessInput** and **ProcessOutput**.</span></span> <span data-ttu-id="83632-112">O método **process** é síncrono; todo o processamento ocorre dentro da chamada.</span><span class="sxs-lookup"><span data-stu-id="83632-112">The **Process** method is synchronous; all processing occurs inside the call.</span></span> <span data-ttu-id="83632-113">Além disso, o processamento in-loco não usa objetos **IMediaBuffer** .</span><span class="sxs-lookup"><span data-stu-id="83632-113">Also, in-place processing does not use **IMediaBuffer** objects.</span></span> <span data-ttu-id="83632-114">O método **process** usa um ponteiro diretamente para o buffer de memória.</span><span class="sxs-lookup"><span data-stu-id="83632-114">The **Process** method takes a pointer directly to the memory buffer.</span></span>

<span data-ttu-id="83632-115">Um DMO que dá suporte ao processamento in-loco ainda deve implementar a interface **IMediaObject** , incluindo os métodos **ProcessInput** e **ProcessOutput** .</span><span class="sxs-lookup"><span data-stu-id="83632-115">A DMO that supports in-place processing still must implement the **IMediaObject** interface, including the **ProcessInput** and **ProcessOutput** methods.</span></span> <span data-ttu-id="83632-116">O cliente pode escolher se deseja usar o processamento in-loco ou usar buffers separados.</span><span class="sxs-lookup"><span data-stu-id="83632-116">The client can choose whether to use in-place processing or use separate buffers.</span></span> <span data-ttu-id="83632-117">No entanto, não misture os dois tipos de processamento.</span><span class="sxs-lookup"><span data-stu-id="83632-117">However, do not mix the two types of processing.</span></span> <span data-ttu-id="83632-118">Se você chamar **process**, não chame **ProcessInput** ou **ProcessOutput**, e vice-versa.</span><span class="sxs-lookup"><span data-stu-id="83632-118">If you call **Process**, do not call **ProcessInput** or **ProcessOutput**, and vice-versa.</span></span>

<span data-ttu-id="83632-119">**Caudas de efeito**</span><span class="sxs-lookup"><span data-stu-id="83632-119">**Effect Tails**</span></span>

<span data-ttu-id="83632-120">Um DMO in-loco pode criar uma saída adicional depois que a entrada é interrompida.</span><span class="sxs-lookup"><span data-stu-id="83632-120">An in-place DMO might create some additional output after the input stops.</span></span> <span data-ttu-id="83632-121">Isso é chamado de *cauda de efeito*.</span><span class="sxs-lookup"><span data-stu-id="83632-121">This is called an *effect tail*.</span></span> <span data-ttu-id="83632-122">Por exemplo, um efeito de reverberação continua depois que a entrada chega a silêncio.</span><span class="sxs-lookup"><span data-stu-id="83632-122">For example, a reverb effect continues after the input reaches silence.</span></span> <span data-ttu-id="83632-123">Se houver um final de efeito, o método **process** retornará S \_ false.</span><span class="sxs-lookup"><span data-stu-id="83632-123">If there is an effect tail, the **Process** method returns S\_FALSE.</span></span> <span data-ttu-id="83632-124">Depois que o aplicativo processa todos os seus dados, ele pode gerar a cauda do efeito enviando buffers vazios para o método **process** .</span><span class="sxs-lookup"><span data-stu-id="83632-124">Once the application has processed all of its data, it can generate the effect tail by sending empty buffers to the **Process** method.</span></span>

## <a name="related-topics"></a><span data-ttu-id="83632-125">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="83632-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="83632-126">Hospedando diretamente um DMO</span><span class="sxs-lookup"><span data-stu-id="83632-126">Directly Hosting a DMO</span></span>](directly-hosting-a-dmo.md)
</dt> </dl>

 

 



