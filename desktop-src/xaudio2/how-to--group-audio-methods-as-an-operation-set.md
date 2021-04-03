---
description: Este tópico mostra como você pode agrupar os métodos XAudio2 para que eles entrem em vigor ao mesmo tempo.
ms.assetid: 1b50acc5-a6b2-e010-9e7e-0080a5ee4a58
title: 'Como: Agrupar métodos de áudio como um conjunto de operações'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5146c650ae6f89331c40f3e0db896f49484a6f0e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829072"
---
# <a name="how-to-group-audio-methods-as-an-operation-set"></a><span data-ttu-id="fd7cc-103">Como: Agrupar métodos de áudio como um conjunto de operações</span><span class="sxs-lookup"><span data-stu-id="fd7cc-103">How to: Group Audio Methods as an Operation Set</span></span>

<span data-ttu-id="fd7cc-104">Este tópico mostra como você pode agrupar os métodos XAudio2 para que eles entrem em vigor ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="fd7cc-104">This topic shows you how you can group together XAudio2 methods so they take effect at the same time.</span></span>

## <a name="to-group-audio-methods-as-an-operation-set"></a><span data-ttu-id="fd7cc-105">Para agrupar métodos de áudio como um conjunto de operações</span><span class="sxs-lookup"><span data-stu-id="fd7cc-105">To group audio methods as an operation set</span></span>

1.  <span data-ttu-id="fd7cc-106">Declare um contador de conjunto de operações globais.</span><span class="sxs-lookup"><span data-stu-id="fd7cc-106">Declare a global operation set counter.</span></span>

    <span data-ttu-id="fd7cc-107">O contador de [conjunto de operações](operation-sets.md) garante que cada conjunto de operações seja exclusivo.</span><span class="sxs-lookup"><span data-stu-id="fd7cc-107">The [operation set](operation-sets.md) counter ensures that each operation set is unique.</span></span>

    ```
    UINT32 OperationSetCounter = 0;
    ```

    

2.  <span data-ttu-id="fd7cc-108">Incrementar o contador global.</span><span class="sxs-lookup"><span data-stu-id="fd7cc-108">Increment the global counter.</span></span>

    <span data-ttu-id="fd7cc-109">Cada vez que você envia um novo [conjunto de operações](operation-sets.md), o contador global deve ser incrementado para garantir que cada conjunto seja exclusivo.</span><span class="sxs-lookup"><span data-stu-id="fd7cc-109">Each time you submit a new [operation set](operation-sets.md), the global counter should increment to ensure each set is unique.</span></span>

    ```
    UINT32 OperationID = UINT32(InterlockedIncrement(LPLONG(&OperationSetCounter)));
    ```

    

3.  <span data-ttu-id="fd7cc-110">Agrupe as chamadas de método definindo seus parâmetros de [conjunto de operações](operation-sets.md) .</span><span class="sxs-lookup"><span data-stu-id="fd7cc-110">Group the method calls by setting their [operation set](operation-sets.md) parameters.</span></span>

4.  <span data-ttu-id="fd7cc-111">Defina os parâmetros do [conjunto de operações](operation-sets.md) como o valor atual do contador global.</span><span class="sxs-lookup"><span data-stu-id="fd7cc-111">Set the [operation set](operation-sets.md) parameters to the current value of the global counter.</span></span>

    <span data-ttu-id="fd7cc-112">Nesse caso, quatro chamadas para [**IXAudio2SourceVoice:: Start**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-start) são agrupadas como uma [operação definida](operation-sets.md).</span><span class="sxs-lookup"><span data-stu-id="fd7cc-112">In this case, four calls to [**IXAudio2SourceVoice::Start**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-start) are grouped as one [operation set](operation-sets.md).</span></span> <span data-ttu-id="fd7cc-113">O agrupamento das chamadas faz com que todos os quatro sons sejam iniciados exatamente ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="fd7cc-113">Grouping the calls causes all four of the sounds to start at exactly the same time.</span></span>

    ```
    hr = pSFXSourceVoice1->Start( 0, OperationID );
    hr = pSFXSourceVoice2->Start( 0, OperationID );
    hr = pSFXSourceVoice3->Start( 0, OperationID );
    hr = pSFXSourceVoice4->Start( 0, OperationID );
    ```

    

5.  <span data-ttu-id="fd7cc-114">Inicie o [conjunto de operações](operation-sets.md).</span><span class="sxs-lookup"><span data-stu-id="fd7cc-114">Start the [operation set](operation-sets.md).</span></span>

    <span data-ttu-id="fd7cc-115">Depois de chamar todos os métodos no conjunto, inicie o conjunto chamando [**IXAudio2:: CommitChanges**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-commitchanges) com o valor atual do contador global.</span><span class="sxs-lookup"><span data-stu-id="fd7cc-115">After you call all the methods in the set, start the set by calling [**IXAudio2::CommitChanges**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-commitchanges) with the current value of the global counter.</span></span>

    ```
    pXAudio2->CommitChanges(OperationID);
    ```

    

## <a name="related-topics"></a><span data-ttu-id="fd7cc-116">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="fd7cc-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fd7cc-117">Conjuntos de operações</span><span class="sxs-lookup"><span data-stu-id="fd7cc-117">Operation Sets</span></span>](operation-sets.md)
</dt> <dt>

[<span data-ttu-id="fd7cc-118">Guia de Programação em XAudio2</span><span class="sxs-lookup"><span data-stu-id="fd7cc-118">XAudio2 Programming Guide</span></span>](programming-guide.md)
</dt> <dt>

[<span data-ttu-id="fd7cc-119">Conjuntos de operações XAudio2</span><span class="sxs-lookup"><span data-stu-id="fd7cc-119">XAudio2 Operation Sets</span></span>](xaudio2-operation-sets.md)
</dt> </dl>

 

 
