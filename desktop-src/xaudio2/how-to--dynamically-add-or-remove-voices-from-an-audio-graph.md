---
description: Você pode alterar grafos de áudio a qualquer momento para adicionar ou remover vozes ou subgrafos inteiros.
ms.assetid: b2f9ec6a-4b5b-e618-759b-d7dbc0d97ac4
title: 'Como: Adicionar ou remover dinamicamente vozes de um gráfico de áudio'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fdb26150b5614ec53e4cc4de5af74e9a14ee2a94
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090680"
---
# <a name="how-to-dynamically-add-or-remove-voices-from-an-audio-graph"></a><span data-ttu-id="6317b-103">Como: Adicionar ou remover dinamicamente vozes de um gráfico de áudio</span><span class="sxs-lookup"><span data-stu-id="6317b-103">How to: Dynamically Add or Remove Voices From an Audio Graph</span></span>

<span data-ttu-id="6317b-104">Você pode alterar grafos de áudio a qualquer momento para adicionar ou remover vozes ou subgrafos inteiros.</span><span class="sxs-lookup"><span data-stu-id="6317b-104">You can change audio graphs at any time to add or remove voices or entire subgraphs.</span></span> <span data-ttu-id="6317b-105">Este tópico mostra como adicionar ou remover vozes submix de um grafo criado seguindo as etapas em [como compilar um grafo básico de processamento de áudio](how-to--build-a-basic-audio-processing-graph.md).</span><span class="sxs-lookup"><span data-stu-id="6317b-105">This topic shows you how to add or remove submix voices from a graph that has been created following the steps in [How to: Build a Basic Audio Processing Graph](how-to--build-a-basic-audio-processing-graph.md).</span></span> <span data-ttu-id="6317b-106">Uma única voz pode enviar sua saída para várias vozes ou para uma cadeia de vozes longa.</span><span class="sxs-lookup"><span data-stu-id="6317b-106">A single voice can send its output to several voices or to a long chain of voices.</span></span> <span data-ttu-id="6317b-107">Remover ou adicionar uma única voz pode ter um grande efeito em um grafo de áudio.</span><span class="sxs-lookup"><span data-stu-id="6317b-107">Removing or adding a single voice can have a large effect on an audio graph.</span></span>

## <a name="to-dynamically-change-an-audio-graph"></a><span data-ttu-id="6317b-108">Para alterar dinamicamente um grafo de áudio</span><span class="sxs-lookup"><span data-stu-id="6317b-108">To dynamically change an audio graph</span></span>

<span data-ttu-id="6317b-109">Adicionar e remover vozes de um grafo de áudio é muito semelhante a adicionar ou remover nós de uma única lista ou grafo vinculado.</span><span class="sxs-lookup"><span data-stu-id="6317b-109">Adding and removing voices from an audio graph is very similar to adding or removing nodes from a single-linked list or graph.</span></span>

-   <span data-ttu-id="6317b-110">Para adicionar uma voz ou um subgrafo a um grafo de áudio</span><span class="sxs-lookup"><span data-stu-id="6317b-110">To add a voice or subgraph to an audio graph</span></span>

    <span data-ttu-id="6317b-111">Defina a saída de uma voz no grafo, a voz pai, para a voz a ser adicionada usando a função [**SetOutputVoices**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setoutputvoices) .</span><span class="sxs-lookup"><span data-stu-id="6317b-111">Set the output of a voice in the graph, the parent voice, to the voice to be added using the [**SetOutputVoices**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setoutputvoices) function.</span></span> <span data-ttu-id="6317b-112">Defina a saída da nova voz para o filho original da voz pai.</span><span class="sxs-lookup"><span data-stu-id="6317b-112">Set the output of the new voice to the original child of the parent voice.</span></span>

    ```
    XAUDIO2_SEND_DESCRIPTOR send = {0, pNewVoice};
    XAUDIO2_VOICE_SENDS sendlist = {1, &send};
    pParentVoice->SetOutputVoices(&sendlist);
    send.pOutputVoice = pChildVoice;
    pNewVoice->SetOutputVoices(&sendlist);
    ```

    

-   <span data-ttu-id="6317b-113">Para remover uma voz ou um subgrafo de um grafo de áudio</span><span class="sxs-lookup"><span data-stu-id="6317b-113">To remove a voice or subgraph from an audio graph</span></span>

    <span data-ttu-id="6317b-114">Defina a voz de saída do pai da voz que está sendo removida para o filho da voz que está sendo removida.</span><span class="sxs-lookup"><span data-stu-id="6317b-114">Set the output voice of the parent of the voice being removed to the child of the voice being removed.</span></span> <span data-ttu-id="6317b-115">Se a voz que está sendo removida estiver no final do grafo, a voz pai deverá ser alterada para apontar para a voz mestra.</span><span class="sxs-lookup"><span data-stu-id="6317b-115">If the voice being removed is at the end of the graph, the parent voice should be changed to point to the master voice.</span></span>

    ```
    XAUDIO2_SEND_DESCRIPTOR send = {0, pChildVoice};
    XAUDIO2_VOICE_SENDS sendlist = {1, &send};
    pParentVoice->SetOutputVoices(&sendlist);
    ```

    

<span data-ttu-id="6317b-116">Observe que, para maior clareza, cada pai tem apenas um filho nesses exemplos.</span><span class="sxs-lookup"><span data-stu-id="6317b-116">Note that for clarity each parent only has one child in these examples.</span></span> <span data-ttu-id="6317b-117">Se um nó pai tiver vários filhos, sua caixa de envio conterá uma matriz de vozes em vez de um ponteiro para apenas uma voz.</span><span class="sxs-lookup"><span data-stu-id="6317b-117">If a parent node has multiple children, its sendlist will contain an array of voices instead of a pointer to just one voice.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6317b-118">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="6317b-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6317b-119">Gráficos de áudio</span><span class="sxs-lookup"><span data-stu-id="6317b-119">Audio Graphs</span></span>](audio-graphs.md)
</dt> <dt>

[<span data-ttu-id="6317b-120">Guia de Programação em XAudio2</span><span class="sxs-lookup"><span data-stu-id="6317b-120">XAudio2 Programming Guide</span></span>](programming-guide.md)
</dt> <dt>

[<span data-ttu-id="6317b-121">Como: Compilar um gráfico de processamento de áudio básico</span><span class="sxs-lookup"><span data-stu-id="6317b-121">How to: Build a Basic Audio Processing Graph</span></span>](how-to--build-a-basic-audio-processing-graph.md)
</dt> <dt>

[<span data-ttu-id="6317b-122">Como: Usar vozes de submixagem</span><span class="sxs-lookup"><span data-stu-id="6317b-122">How to: Use Submix Voices</span></span>](how-to--use-submix-voices.md)
</dt> <dt>

[<span data-ttu-id="6317b-123">Como: Criar uma cadeia de efeitos</span><span class="sxs-lookup"><span data-stu-id="6317b-123">How to: Create an Effect Chain</span></span>](how-to--create-an-effect-chain.md)
</dt> </dl>

 

 
