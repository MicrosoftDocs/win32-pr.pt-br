---
title: Objeto de buffer
description: Objeto de buffer
ms.assetid: 0812261c-698c-4071-929c-4363a16dd5a8
keywords:
- SDK do Windows Media Format, objetos de buffer
- Formato de sistema avançado (ASF), objetos de buffer
- ASF (formato de sistemas avançados), objetos de buffer
- objetos, objetos de buffer
- objetos de buffer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a8a9a3c6acfa0b0780b07f2853f60fdd68d0eaf
ms.sourcegitcommit: b04e152a7f51618fc174ffa872654623fe088db2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/21/2020
ms.locfileid: "105782691"
---
# <a name="buffer-object"></a><span data-ttu-id="8aa51-108">Objeto de buffer</span><span class="sxs-lookup"><span data-stu-id="8aa51-108">Buffer Object</span></span>

<span data-ttu-id="8aa51-109">Um objeto buffer é usado para manter amostras e fornecê-los entre os objetos do Windows Media Format SDK e seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="8aa51-109">A buffer object is used to hold samples and deliver them between the objects of the Windows Media Format SDK and your application.</span></span> <span data-ttu-id="8aa51-110">Ao gravar um arquivo, você passa seus exemplos de entrada para o gravador usando objetos de buffer.</span><span class="sxs-lookup"><span data-stu-id="8aa51-110">When you write a file, you pass your input samples to the writer using buffer objects.</span></span> <span data-ttu-id="8aa51-111">Quando você lê um arquivo, o objeto leitor ou o objeto leitor síncrono fornece amostras para seu aplicativo em objetos de buffer.</span><span class="sxs-lookup"><span data-stu-id="8aa51-111">When you read a file, the reader object or synchronous reader object provides samples to your application in buffer objects.</span></span>

<span data-ttu-id="8aa51-112">Para escrever exemplos em um arquivo, você pode criar um objeto de buffer usando o método [**IWMWriter:: AllocateSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-allocatesample) .</span><span class="sxs-lookup"><span data-stu-id="8aa51-112">For writing samples to a file, you can create a buffer object using the [**IWMWriter::AllocateSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-allocatesample) method.</span></span> <span data-ttu-id="8aa51-113">Para exemplos de leitura, o objeto leitor e o objeto leitor síncrono criam objetos de buffer internamente.</span><span class="sxs-lookup"><span data-stu-id="8aa51-113">For reading samples, the reader object and synchronous reader object both create buffer objects internally.</span></span> <span data-ttu-id="8aa51-114">Se você optar pelo, poderá alocar seus próprios objetos de buffer para leitura de arquivo usando [**IWMReaderAllocatorEx:: AllocateForOutputEx**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderallocatorex-allocateforoutputex) ou [**IWMReaderAllocatorEx:: AllocateForStreamEx**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderallocatorex-allocateforstreamex).</span><span class="sxs-lookup"><span data-stu-id="8aa51-114">If you choose to, you can allocate your own buffer objects for file reading by using [**IWMReaderAllocatorEx::AllocateForOutputEx**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderallocatorex-allocateforoutputex) or [**IWMReaderAllocatorEx::AllocateForStreamEx**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderallocatorex-allocateforstreamex).</span></span>

<span data-ttu-id="8aa51-115">As interfaces a seguir têm suporte em cada objeto de buffer.</span><span class="sxs-lookup"><span data-stu-id="8aa51-115">The following interfaces are supported by every buffer object.</span></span>



| <span data-ttu-id="8aa51-116">Interface</span><span class="sxs-lookup"><span data-stu-id="8aa51-116">Interface</span></span>                          | <span data-ttu-id="8aa51-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="8aa51-117">Description</span></span>                                                          |
|------------------------------------|----------------------------------------------------------------------|
| [<span data-ttu-id="8aa51-118">**INSSBuffer**</span><span class="sxs-lookup"><span data-stu-id="8aa51-118">**INSSBuffer**</span></span>](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer)   | <span data-ttu-id="8aa51-119">Controla e fornece acesso ao buffer.</span><span class="sxs-lookup"><span data-stu-id="8aa51-119">Controls and provides access to the buffer.</span></span>                          |
| [<span data-ttu-id="8aa51-120">**INSSBuffer2**</span><span class="sxs-lookup"><span data-stu-id="8aa51-120">**INSSBuffer2**</span></span>](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer2) | <span data-ttu-id="8aa51-121">Não implementado.</span><span class="sxs-lookup"><span data-stu-id="8aa51-121">Not implemented.</span></span>                                                     |
| [<span data-ttu-id="8aa51-122">**INSSBuffer3**</span><span class="sxs-lookup"><span data-stu-id="8aa51-122">**INSSBuffer3**</span></span>](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer3) | <span data-ttu-id="8aa51-123">Dá suporte a propriedades de buffer, que são usadas para extensões de unidade de dados.</span><span class="sxs-lookup"><span data-stu-id="8aa51-123">Supports buffer properties, which are used for data unit extensions.</span></span> |
| [<span data-ttu-id="8aa51-124">**INSSBuffer4**</span><span class="sxs-lookup"><span data-stu-id="8aa51-124">**INSSBuffer4**</span></span>](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer4) | <span data-ttu-id="8aa51-125">Enumera as propriedades do buffer.</span><span class="sxs-lookup"><span data-stu-id="8aa51-125">Enumerates buffer properties.</span></span>                                        |



 

## <a name="related-topics"></a><span data-ttu-id="8aa51-126">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="8aa51-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8aa51-127">**Objetos**</span><span class="sxs-lookup"><span data-stu-id="8aa51-127">**Objects**</span></span>](objects.md)
</dt> </dl>

 

 




