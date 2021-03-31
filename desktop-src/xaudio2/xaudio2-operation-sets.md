---
description: Esta visão geral apresenta vários métodos XAudio2 que você pode chamar como parte de um conjunto de operações.
ms.assetid: 5bfd747d-af65-f619-e549-be8130748261
title: Conjuntos de operações XAudio2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90955fc0557f3f84840436c121f768caff4af81b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104172041"
---
# <a name="xaudio2-operation-sets"></a><span data-ttu-id="b2b5c-103">Conjuntos de operações XAudio2</span><span class="sxs-lookup"><span data-stu-id="b2b5c-103">XAudio2 Operation Sets</span></span>

<span data-ttu-id="b2b5c-104">Esta visão geral apresenta vários métodos XAudio2 que você pode chamar como parte de um conjunto de operações.</span><span class="sxs-lookup"><span data-stu-id="b2b5c-104">This overview introduces several XAudio2 methods that you can call as part of an operation set.</span></span>

<span data-ttu-id="b2b5c-105">Vários métodos XAudio2 usam o argumento *operationset* , que permite que eles sejam chamados como parte de um grupo adiado.</span><span class="sxs-lookup"><span data-stu-id="b2b5c-105">Several XAudio2 methods take the *OperationSet* argument, which allows them to be called as part of a deferred group.</span></span> <span data-ttu-id="b2b5c-106">Em um momento específico, você pode aplicar um conjunto inteiro de alterações simultaneamente chamando a função [**IXAudio2:: CommitChanges**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-commitchanges) com o identificador *operationset* para esse grupo.</span><span class="sxs-lookup"><span data-stu-id="b2b5c-106">At a specific time, you can apply an entire set of changes simultaneously by calling the function [**IXAudio2::CommitChanges**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-commitchanges) with the *OperationSet* identifier for that group.</span></span> <span data-ttu-id="b2b5c-107">O identificador é um número arbitrário.</span><span class="sxs-lookup"><span data-stu-id="b2b5c-107">The identifier is an arbitrary number.</span></span> <span data-ttu-id="b2b5c-108">Assim, ele permite que partes separadas do código do cliente apliquem alterações atômicas separadas ao grafo sem qualquer conflito.</span><span class="sxs-lookup"><span data-stu-id="b2b5c-108">Thus, it allows separate parts of the client code to apply separate atomic changes to the graph without any conflict.</span></span> <span data-ttu-id="b2b5c-109">A prática recomendada é para o cliente incrementar um contador global sempre que precisar gerar um novo identificador *operationset* exclusivo.</span><span class="sxs-lookup"><span data-stu-id="b2b5c-109">The recommended practice is for the client to increment a global counter whenever it needs to generate a unique, new *OperationSet* identifier.</span></span> <span data-ttu-id="b2b5c-110">Um conjunto de alterações no grafo, aplicado atomicamente, tem a garantia de ser preciso de exemplo.</span><span class="sxs-lookup"><span data-stu-id="b2b5c-110">A set of changes to the graph, applied atomically, is guaranteed to be sample-accurate.</span></span> <span data-ttu-id="b2b5c-111">Por exemplo, as vozes serão iniciadas em sincronia.</span><span class="sxs-lookup"><span data-stu-id="b2b5c-111">For example, voices will start in sync.</span></span>

<span data-ttu-id="b2b5c-112">Se você definir *operationset* como XAudio2 \_ Commit \_ agora, a alteração se aplicará imediatamente.</span><span class="sxs-lookup"><span data-stu-id="b2b5c-112">If you set *OperationSet* to XAUDIO2\_COMMIT\_NOW, the change applies immediately.</span></span> <span data-ttu-id="b2b5c-113">Ela entra em vigor no primeiro passo de processamento de áudio após a chamada do método.</span><span class="sxs-lookup"><span data-stu-id="b2b5c-113">It takes effect in the first audio processing pass after the method call.</span></span> <span data-ttu-id="b2b5c-114">Se você chamar [**CommitChanges**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-commitchanges) com XAudio2 \_ Commit \_ All, as alterações em todos os conjuntos de operações pendentes serão executadas, independentemente do seu identificador *operationset* .</span><span class="sxs-lookup"><span data-stu-id="b2b5c-114">If you call [**CommitChanges**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-commitchanges) with XAUDIO2\_COMMIT\_ALL, changes to all pending operations sets are performed, regardless of their *OperationSet* identifier.</span></span>

<span data-ttu-id="b2b5c-115">Determinados métodos entram em vigor imediatamente quando são chamados de um retorno de chamada XAudio2 com um *operationset* de XAudio2 \_ Commit \_ Now.</span><span class="sxs-lookup"><span data-stu-id="b2b5c-115">Certain methods take effect immediately when they are called from an XAudio2 callback with an *OperationSet* of XAUDIO2\_COMMIT\_NOW.</span></span> <span data-ttu-id="b2b5c-116">Todos os outros métodos que usam um argumento *operationset* só entrarão em vigor na próxima passagem de processamento depois que o método for chamado (se chamado com XAudio2 \_ Commit \_ Now), ou após [**CommitChanges**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-commitchanges) ser chamado com o mesmo *operationset*.</span><span class="sxs-lookup"><span data-stu-id="b2b5c-116">All other methods that take an *OperationSet* argument only take effect on the next processing pass after the method is called (if called with XAUDIO2\_COMMIT\_NOW), or after [**CommitChanges**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-commitchanges) is called with the same *OperationSet*.</span></span> <span data-ttu-id="b2b5c-117">Por isso, determinadas chamadas de método nem sempre podem ocorrer na mesma ordem em que foram chamadas.</span><span class="sxs-lookup"><span data-stu-id="b2b5c-117">Because of this, certain method calls may not always happen in the same order in which they were called.</span></span>

<span data-ttu-id="b2b5c-118">Todas as operações pendentes são confirmadas atomicamente quando [**IXAudio2:: StopEngine**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-stopengine) é chamado.</span><span class="sxs-lookup"><span data-stu-id="b2b5c-118">All pending operations are committed atomically when [**IXAudio2::StopEngine**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-stopengine) is called.</span></span> <span data-ttu-id="b2b5c-119">Todos os métodos que são chamados enquanto o mecanismo é interrompido entram em vigor imediatamente, independentemente do valor de *operationset* fornecido.</span><span class="sxs-lookup"><span data-stu-id="b2b5c-119">Any methods that are called while the engine is stopped take effect immediately, regardless of the *OperationSet* value provided.</span></span> <span data-ttu-id="b2b5c-120">Quando você reinicia o mecanismo, XAudio2 retorna para o modo assíncrono.</span><span class="sxs-lookup"><span data-stu-id="b2b5c-120">When you restart the engine, XAudio2 returns to asynchronous mode.</span></span>

<span data-ttu-id="b2b5c-121">Cenários simples nos quais os conjuntos de operações são úteis incluem os exemplos a seguir.</span><span class="sxs-lookup"><span data-stu-id="b2b5c-121">Simple scenarios in which operation sets are useful include the following examples.</span></span>

-   <span data-ttu-id="b2b5c-122">Iniciando várias vozes simultaneamente.</span><span class="sxs-lookup"><span data-stu-id="b2b5c-122">Starting multiple voices simultaneously.</span></span>
-   <span data-ttu-id="b2b5c-123">Enviando simultaneamente um buffer para uma voz, definindo os parâmetros de voz e iniciando a voz.</span><span class="sxs-lookup"><span data-stu-id="b2b5c-123">Simultaneously submitting a buffer to a voice, setting the voice parameters, and starting the voice.</span></span>
-   <span data-ttu-id="b2b5c-124">Fazer uma alteração em larga escala no grafo, como conectar todas as vozes de origem a uma nova voz submix.</span><span class="sxs-lookup"><span data-stu-id="b2b5c-124">Making a large-scale change to the graph, such as connecting all source voices to a new submix voice.</span></span>

<span data-ttu-id="b2b5c-125">Consulte [como agrupar métodos de áudio como uma operação definida](how-to--group-audio-methods-as-an-operation-set.md) para obter um exemplo de como usar um conjunto de operações.</span><span class="sxs-lookup"><span data-stu-id="b2b5c-125">See [How to: Group Audio Methods as an Operation Set](how-to--group-audio-methods-as-an-operation-set.md) for an example of using an operation set.</span></span>

## <a name="operation-set-methods"></a><span data-ttu-id="b2b5c-126">Métodos de conjunto de operações</span><span class="sxs-lookup"><span data-stu-id="b2b5c-126">Operation Set Methods</span></span>

<span data-ttu-id="b2b5c-127">Você pode chamar os seguintes métodos como parte de um conjunto de operações.</span><span class="sxs-lookup"><span data-stu-id="b2b5c-127">You can call the following methods as part of an operation set.</span></span>

-   [<span data-ttu-id="b2b5c-128">**IXAudio2SourceVoice:: ExitLoop**</span><span class="sxs-lookup"><span data-stu-id="b2b5c-128">**IXAudio2SourceVoice::ExitLoop**</span></span>](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-exitloop)
-   [<span data-ttu-id="b2b5c-129">**IXAudio2Voice:: setfilterparameters**</span><span class="sxs-lookup"><span data-stu-id="b2b5c-129">**IXAudio2Voice::SetFilterParameters**</span></span>](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setfilterparameters)
-   [<span data-ttu-id="b2b5c-130">**IXAudio2SourceVoice:: SetFrequencyRatio**</span><span class="sxs-lookup"><span data-stu-id="b2b5c-130">**IXAudio2SourceVoice::SetFrequencyRatio**</span></span>](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-setfrequencyratio)
-   [<span data-ttu-id="b2b5c-131">**IXAudio2Voice::D isableEffect**</span><span class="sxs-lookup"><span data-stu-id="b2b5c-131">**IXAudio2Voice::DisableEffect**</span></span>](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-disableeffect)
-   [<span data-ttu-id="b2b5c-132">**IXAudio2Voice::EnableEffect**</span><span class="sxs-lookup"><span data-stu-id="b2b5c-132">**IXAudio2Voice::EnableEffect**</span></span>](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-enableeffect)
-   [<span data-ttu-id="b2b5c-133">**IXAudio2Voice::SetChannelVolumes**</span><span class="sxs-lookup"><span data-stu-id="b2b5c-133">**IXAudio2Voice::SetChannelVolumes**</span></span>](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setchannelvolumes)
-   [<span data-ttu-id="b2b5c-134">**IXAudio2Voice:: seteffectparameters**</span><span class="sxs-lookup"><span data-stu-id="b2b5c-134">**IXAudio2Voice::SetEffectParameters**</span></span>](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectparameters)
-   [<span data-ttu-id="b2b5c-135">**IXAudio2Voice::SetOutputMatrix**</span><span class="sxs-lookup"><span data-stu-id="b2b5c-135">**IXAudio2Voice::SetOutputMatrix**</span></span>](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setoutputmatrix)
-   [<span data-ttu-id="b2b5c-136">**IXAudio2Voice:: SetVolume**</span><span class="sxs-lookup"><span data-stu-id="b2b5c-136">**IXAudio2Voice::SetVolume**</span></span>](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setvolume)
-   [<span data-ttu-id="b2b5c-137">**IXAudio2SourceVoice:: iniciar**</span><span class="sxs-lookup"><span data-stu-id="b2b5c-137">**IXAudio2SourceVoice::Start**</span></span>](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-start)
-   [<span data-ttu-id="b2b5c-138">**IXAudio2SourceVoice:: Stop**</span><span class="sxs-lookup"><span data-stu-id="b2b5c-138">**IXAudio2SourceVoice::Stop**</span></span>](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-stop)

<span data-ttu-id="b2b5c-139">Conforme descrito anteriormente, o código do cliente deve, finalmente, chamar a função [**IXAudio2:: CommitChanges**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-commitchanges) para executar as alterações adiadas.</span><span class="sxs-lookup"><span data-stu-id="b2b5c-139">As described previously, client code must ultimately call the function [**IXAudio2::CommitChanges**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-commitchanges) to execute the deferred changes.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b2b5c-140">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="b2b5c-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b2b5c-141">Conjuntos de operações</span><span class="sxs-lookup"><span data-stu-id="b2b5c-141">Operation Sets</span></span>](operation-sets.md)
</dt> <dt>

[<span data-ttu-id="b2b5c-142">Guia de Programação em XAudio2</span><span class="sxs-lookup"><span data-stu-id="b2b5c-142">XAudio2 Programming Guide</span></span>](programming-guide.md)
</dt> <dt>

[<span data-ttu-id="b2b5c-143">Como: Agrupar métodos de áudio como um conjunto de operações</span><span class="sxs-lookup"><span data-stu-id="b2b5c-143">How to: Group Audio Methods as an Operation Set</span></span>](how-to--group-audio-methods-as-an-operation-set.md)
</dt> </dl>

 

 
