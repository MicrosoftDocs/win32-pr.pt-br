---
description: Transformações de Media Foundation
ms.assetid: cb23fe0a-c42c-4912-a0bf-1f0b18a6f4e0
title: Transformações de Media Foundation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa0518ced06169f6d998bdad1747878d109e0676
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "105764550"
---
# <a name="media-foundation-transforms"></a><span data-ttu-id="faf4e-103">Transformações de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="faf4e-103">Media Foundation Transforms</span></span>

<span data-ttu-id="faf4e-104">Transformações de Media Foundation (MFTs) fornecem um modelo genérico para o processamento de dados de mídia.</span><span class="sxs-lookup"><span data-stu-id="faf4e-104">Media Foundation transforms (MFTs) provide a generic model for processing media data.</span></span> <span data-ttu-id="faf4e-105">MFTs são usados para decodificadores, codificadores e processadores de sinais digitais (DSPs).</span><span class="sxs-lookup"><span data-stu-id="faf4e-105">MFTs are used for decoders, encoders, and digital signal processors (DSPs).</span></span> <span data-ttu-id="faf4e-106">Em suma, tudo que fica no pipeline de mídia entre a origem da mídia e o coletor de mídia é uma MFT.</span><span class="sxs-lookup"><span data-stu-id="faf4e-106">In short, anything that sits in the media pipeline between the media source and the media sink is an MFT.</span></span>

<span data-ttu-id="faf4e-107">Esta seção descreve o modelo de programação MFT e como implementar um MFT, com recomendações para tipos específicos de MFTs, como decodificadores.</span><span class="sxs-lookup"><span data-stu-id="faf4e-107">This section describes the MFT programming model and how to implement an MFT, with recommendations for specific types of MFTs, such as decoders.</span></span>



| <span data-ttu-id="faf4e-108">Tópico</span><span class="sxs-lookup"><span data-stu-id="faf4e-108">Topic</span></span>                                                                    | <span data-ttu-id="faf4e-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="faf4e-109">Description</span></span>                                                                                                                                                                                         |
|--------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="faf4e-110">Sobre o MFTs</span><span class="sxs-lookup"><span data-stu-id="faf4e-110">About MFTs</span></span>](about-mfts.md)                                             | <span data-ttu-id="faf4e-111">Fornece uma breve visão geral do MFTs</span><span class="sxs-lookup"><span data-stu-id="faf4e-111">Provides a brief overview of MFTs</span></span>                                                                                                                                                                   |
| [<span data-ttu-id="faf4e-112">Modelo de processamento de MFT básico</span><span class="sxs-lookup"><span data-stu-id="faf4e-112">Basic MFT Processing Model</span></span>](basic-mft-processing-model.md)             | <span data-ttu-id="faf4e-113">Descreve em mais detalhes o modelo básico para processamento de dados com um MFT.</span><span class="sxs-lookup"><span data-stu-id="faf4e-113">Describes in more detail the basic model for processing data with an MFT.</span></span>                                                                                                                           |
| [<span data-ttu-id="faf4e-114">MFTs assíncrona</span><span class="sxs-lookup"><span data-stu-id="faf4e-114">Asynchronous MFTs</span></span>](asynchronous-mfts.md)                               | <span data-ttu-id="faf4e-115">Descreve um modelo de processamento assíncrono que é uma alternativa ao modelo básico.</span><span class="sxs-lookup"><span data-stu-id="faf4e-115">Describes an asynchronous processing model that is an alternative to the basic model.</span></span><br/> <span data-ttu-id="faf4e-116">O processamento assíncrono foi introduzido no Windows 7.</span><span class="sxs-lookup"><span data-stu-id="faf4e-116">Asynchronous processing was introduced in Windows 7.</span></span> <span data-ttu-id="faf4e-117">Nem todo MFT dá suporte a esse modelo.</span><span class="sxs-lookup"><span data-stu-id="faf4e-117">Not every MFT supports this model.</span></span><br/> |
| [<span data-ttu-id="faf4e-118">Registrando e enumerando MFTs</span><span class="sxs-lookup"><span data-stu-id="faf4e-118">Registering and Enumerating MFTs</span></span>](registering-and-enumerating-mfts.md) | <span data-ttu-id="faf4e-119">Como registrar um MFT e como enumerar MFTs no registro.</span><span class="sxs-lookup"><span data-stu-id="faf4e-119">How to register an MFT and how to enumerate MFTs in the registry.</span></span>                                                                                                                                   |
| [<span data-ttu-id="faf4e-120">Campo de restrições de uso</span><span class="sxs-lookup"><span data-stu-id="faf4e-120">Field of Use Restrictions</span></span>](field-of-use-restrictions.md)               | <span data-ttu-id="faf4e-121">Descreve o mecanismo para desbloquear um MFT que tem restrições de campo de uso.</span><span class="sxs-lookup"><span data-stu-id="faf4e-121">Describes the mechanism for unlocking an MFT that has field-of-use restrictions.</span></span>                                                                                                                    |
| [<span data-ttu-id="faf4e-122">Comparação de MFTs e DMOs</span><span class="sxs-lookup"><span data-stu-id="faf4e-122">Comparison of MFTs and DMOs</span></span>](comparison-of-mfts-and-dmos.md)           | <span data-ttu-id="faf4e-123">Resume as diferenças entre MFTs e DMOs.</span><span class="sxs-lookup"><span data-stu-id="faf4e-123">Summarizes the differences between MFTs and DMOs.</span></span>                                                                                                                                                   |
| [<span data-ttu-id="faf4e-124">Gravando uma MFT personalizada</span><span class="sxs-lookup"><span data-stu-id="faf4e-124">Writing a Custom MFT</span></span>](writing-a-custom-mft.md)                         | <span data-ttu-id="faf4e-125">Diretrizes para gravar um MFT personalizado.</span><span class="sxs-lookup"><span data-stu-id="faf4e-125">Guidelines for writing a custom MFT.</span></span>                                                                                                                                                                |



 

## <a name="related-topics"></a><span data-ttu-id="faf4e-126">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="faf4e-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="faf4e-127">Pipeline de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="faf4e-127">Media Foundation Pipeline</span></span>](media-foundation-pipeline.md)
</dt> <dt>

[<span data-ttu-id="faf4e-128">Arquitetura Media Foundation</span><span class="sxs-lookup"><span data-stu-id="faf4e-128">Media Foundation Architecture</span></span>](media-foundation-architecture.md)
</dt> <dt>

[<span data-ttu-id="faf4e-129">**IMFTransform**</span><span class="sxs-lookup"><span data-stu-id="faf4e-129">**IMFTransform**</span></span>](/windows/desktop/api/mftransform/nn-mftransform-imftransform)
</dt> </dl>

 

 




