---
description: Trabalhando com exemplos e buffers de mídia de MFT
ms.assetid: dda4048e-bc4c-40ac-a6bd-34984f3717e0
title: Trabalhando com exemplos e buffers de mídia de MFT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6373f6d75b4122409b54649eed6f90e95c2f50c7
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "104297916"
---
# <a name="working-with-mft-media-buffers-and-samples"></a><span data-ttu-id="1b7cd-103">Trabalhando com exemplos e buffers de mídia de MFT</span><span class="sxs-lookup"><span data-stu-id="1b7cd-103">Working with MFT Media Buffers and Samples</span></span>

<span data-ttu-id="1b7cd-104">O codec MFTs passa dados de mídia para frente e para trás usando os buffers de mídia e exemplos.</span><span class="sxs-lookup"><span data-stu-id="1b7cd-104">Codec MFTs pass media data back and forth by using media buffers and samples.</span></span>

<span data-ttu-id="1b7cd-105">Um buffer de mídia é um objeto COM que gerencia um bloco de memória, normalmente, para manter os dados de mídia.</span><span class="sxs-lookup"><span data-stu-id="1b7cd-105">A media buffer is a COM object that manages a block of memory, typically to hold media data.</span></span> <span data-ttu-id="1b7cd-106">Quando os dados são passados para ou de um MFT, eles são sempre passados na forma de um buffer de mídia.</span><span class="sxs-lookup"><span data-stu-id="1b7cd-106">When data is passed to or from an MFT, it is always passed in the form of a media buffer.</span></span>

<span data-ttu-id="1b7cd-107">Todos os buffers de mídia expõem a interface **IMFMediaBuffer** .</span><span class="sxs-lookup"><span data-stu-id="1b7cd-107">All media buffers expose the **IMFMediaBuffer** interface.</span></span> <span data-ttu-id="1b7cd-108">Essa interface é projetada para qualquer tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="1b7cd-108">This interface is designed for any type of data.</span></span> <span data-ttu-id="1b7cd-109">Os buffers que contêm dados de vídeo geralmente também expõem **IMF2DBuffer**.</span><span class="sxs-lookup"><span data-stu-id="1b7cd-109">Buffers containing video data often also expose **IMF2DBuffer**.</span></span>

<span data-ttu-id="1b7cd-110">Um buffer de mídia tem um tamanho máximo, que é a quantidade de memória alocada para o buffer.</span><span class="sxs-lookup"><span data-stu-id="1b7cd-110">A media buffer has a maximum size, which is the amount of memory allocated for the buffer.</span></span> <span data-ttu-id="1b7cd-111">Para localizar o tamanho máximo, chame **IMFMediaBuffer:: GetMaxLength**.</span><span class="sxs-lookup"><span data-stu-id="1b7cd-111">To find the maximum size, call **IMFMediaBuffer::GetMaxLength**.</span></span> <span data-ttu-id="1b7cd-112">Em qualquer ponto no tempo, um buffer de mídia também tem um comprimento atual, que é a quantidade de dados válidos no buffer, variando de zero bytes até o tamanho máximo.</span><span class="sxs-lookup"><span data-stu-id="1b7cd-112">At any point in time, a media buffer also has a current length, which is the amount of valid data in the buffer, ranging from zero bytes up to the maximum size.</span></span> <span data-ttu-id="1b7cd-113">Para obter o comprimento atual, chame **IMFMediaBuffer:: GetCurrentLength**.</span><span class="sxs-lookup"><span data-stu-id="1b7cd-113">To get the current length, call **IMFMediaBuffer::GetCurrentLength**.</span></span> <span data-ttu-id="1b7cd-114">Quando o buffer é criado, o comprimento atual é zero.</span><span class="sxs-lookup"><span data-stu-id="1b7cd-114">When the buffer is created, the current length is zero.</span></span> <span data-ttu-id="1b7cd-115">Se você gravar dados no buffer, chame **IMFMediaBuffer:: SetCurrentLength** para atualizar o comprimento atual.</span><span class="sxs-lookup"><span data-stu-id="1b7cd-115">If you write data to the buffer, call **IMFMediaBuffer::SetCurrentLength** to update the current length.</span></span>

<span data-ttu-id="1b7cd-116">Para acessar a memória no buffer, chame **IMFMediaBuffer:: Lock**.</span><span class="sxs-lookup"><span data-stu-id="1b7cd-116">To access the memory in the buffer, call **IMFMediaBuffer::Lock**.</span></span> <span data-ttu-id="1b7cd-117">Esse método retorna um ponteiro para o início do bloco de memória.</span><span class="sxs-lookup"><span data-stu-id="1b7cd-117">This method returns a pointer to the start of the memory block.</span></span> <span data-ttu-id="1b7cd-118">Quando terminar de usar o ponteiro, chame **IMFMediaBuffer:: Unlock**.</span><span class="sxs-lookup"><span data-stu-id="1b7cd-118">When you are done using the pointer, call **IMFMediaBuffer::Unlock**.</span></span> <span data-ttu-id="1b7cd-119">O método **Lock** não é um mecanismo de sincronização de threads; Ele não garante que outros threads não possam acessar o buffer.</span><span class="sxs-lookup"><span data-stu-id="1b7cd-119">The **Lock** method is not a thread synchronization mechanism; it does not guarantee that other threads cannot access the buffer.</span></span> <span data-ttu-id="1b7cd-120">O método **Lock** é usado para garantir que a memória acessada permaneça válida até que você chame o método **Unlock** .</span><span class="sxs-lookup"><span data-stu-id="1b7cd-120">The **Lock** method is used to assure that the memory accessed will remain valid until you call the **Unlock** method.</span></span>

<span data-ttu-id="1b7cd-121">Um objeto de exemplo de mídia (no contexto do SDK do Media Foundation) é um objeto que contém uma lista ordenada de zero ou mais buffers.</span><span class="sxs-lookup"><span data-stu-id="1b7cd-121">A media sample object (in the context of the Media Foundation SDK) is an object that contains an ordered list of zero or more buffers.</span></span> <span data-ttu-id="1b7cd-122">Amostras de mídia expõem a interface **IMFSample** .</span><span class="sxs-lookup"><span data-stu-id="1b7cd-122">Media samples expose the **IMFSample** interface.</span></span>

<span data-ttu-id="1b7cd-123">Para criar um novo exemplo, chame a função **MFCreateSample** .</span><span class="sxs-lookup"><span data-stu-id="1b7cd-123">To create a new sample, call the **MFCreateSample** function.</span></span> <span data-ttu-id="1b7cd-124">Inicialmente, a lista de buffers do exemplo está vazia.</span><span class="sxs-lookup"><span data-stu-id="1b7cd-124">Initially, the sample's buffer list is empty.</span></span> <span data-ttu-id="1b7cd-125">Para adicionar um buffer ao final da lista, chame **IMFSample:: addbuffer**.</span><span class="sxs-lookup"><span data-stu-id="1b7cd-125">To add a buffer to the end of the list, call **IMFSample::AddBuffer**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1b7cd-126">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="1b7cd-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1b7cd-127">Trabalhando com codec DMOs</span><span class="sxs-lookup"><span data-stu-id="1b7cd-127">Working with Codec DMOs</span></span>](workingwithcodecdmos.md)
</dt> <dt>

[<span data-ttu-id="1b7cd-128">Trabalhando com codec MFTs</span><span class="sxs-lookup"><span data-stu-id="1b7cd-128">Working with Codec MFTs</span></span>](workingwithcodecmfts.md)
</dt> </dl>

 

 



