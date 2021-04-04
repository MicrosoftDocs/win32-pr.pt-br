---
title: Dados de entrada e saída
description: Dados de entrada e saída
ms.assetid: a03b5327-65df-4cb9-a639-1e943ac28bfc
keywords:
- Plug-ins do Windows Media Player, entrada e saída de dados
- plug-ins, entrada e saída de dados
- plug-ins de processamento de sinal digital, entrada e saída de dados
- Plug-ins do DSP, entrada e saída de dados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39f66946dc796337d1f1e638cfe3828b3cbfbb6e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104084083"
---
# <a name="data-input-and-output"></a><span data-ttu-id="07a27-107">Dados de entrada e saída</span><span class="sxs-lookup"><span data-stu-id="07a27-107">Data Input and Output</span></span>

<span data-ttu-id="07a27-108">O Windows Media Player fornece dados de áudio ou vídeo para plug-ins DSP por meio de um buffer de entrada alocado pelo Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="07a27-108">Windows Media Player provides audio or video data to DSP plug-ins through an input buffer allocated by Windows Media Player.</span></span> <span data-ttu-id="07a27-109">Plug-ins do DSP retornam dados processados para o Windows Media Player por meio de um buffer de saída que também é alocado pelo Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="07a27-109">DSP plug-ins return processed data to Windows Media Player through an output buffer that is also allocated by Windows Media Player.</span></span> <span data-ttu-id="07a27-110">O Windows Media Player gerencia o processo de passagem de dados entre si mesmo e o plug-in DSP chamando métodos implementados pelo plug-in.</span><span class="sxs-lookup"><span data-stu-id="07a27-110">Windows Media Player manages the process of passing data between itself and the DSP plug-in by calling methods implemented by the plug-in.</span></span> <span data-ttu-id="07a27-111">Para que um plug-in atue como um DMO (objeto de mídia do DirectX), o processo funciona da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="07a27-111">For a plug-in acting as a DirectX Media Object (DMO), the process works as follows:</span></span>

1.  <span data-ttu-id="07a27-112">O Windows Media Player chama **IMediaObject::P rocessinput**, passando um ponteiro para um objeto **IMediaBuffer** para o plug-in do DSP.</span><span class="sxs-lookup"><span data-stu-id="07a27-112">Windows Media Player calls **IMediaObject::ProcessInput**, passing a pointer to an **IMediaBuffer** object to the DSP plug-in.</span></span>
2.  <span data-ttu-id="07a27-113">O plug-in do DSP mantém uma contagem de referência no objeto de buffer de entrada.</span><span class="sxs-lookup"><span data-stu-id="07a27-113">The DSP plug-in keeps a reference count on the input buffer object.</span></span> <span data-ttu-id="07a27-114">O plug-in do DSP retorna um **HRESULT** de êxito ou falha apropriado.</span><span class="sxs-lookup"><span data-stu-id="07a27-114">The DSP plug-in returns an appropriate success or failure **HRESULT**.</span></span>
3.  <span data-ttu-id="07a27-115">O Windows Media Player chama **IMediaObject::P rocessoutput**, passando um ponteiro para uma matriz de estruturas de buffer de dados de saída do DMO (que contêm buffers de saída) para o plug-in do DSP. **\_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="07a27-115">Windows Media Player calls **IMediaObject::ProcessOutput**, passing a pointer to an array of **DMO\_OUTPUT\_DATA\_BUFFER** structures (which contain output buffers) to the DSP plug-in.</span></span>
4.  <span data-ttu-id="07a27-116">O plug-in do DSP processa os dados no buffer de entrada e, em seguida, copia os dados para o buffer de saída apropriado.</span><span class="sxs-lookup"><span data-stu-id="07a27-116">The DSP plug-in processes the data in the input buffer and then copies the data to the appropriate output buffer.</span></span> <span data-ttu-id="07a27-117">O plug-in do DSP libera a contagem de referência no objeto de buffer de entrada quando todos os dados no buffer são processados.</span><span class="sxs-lookup"><span data-stu-id="07a27-117">The DSP plug-in releases the reference count on the input buffer object when all the data in the buffer has been processed.</span></span> <span data-ttu-id="07a27-118">Em seguida, o plug-in do DSP retorna um **HRESULT** de êxito ou falha apropriado.</span><span class="sxs-lookup"><span data-stu-id="07a27-118">The DSP plug-in then returns an appropriate success or failure **HRESULT**.</span></span>
5.  <span data-ttu-id="07a27-119">O Windows Media Player renderiza o conteúdo no buffer de saída.</span><span class="sxs-lookup"><span data-stu-id="07a27-119">Windows Media Player renders the content in the output buffer.</span></span>

<span data-ttu-id="07a27-120">Para que um plug-in atue como uma Media Foundation transformação (MFT), o processo funciona da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="07a27-120">For a plug-in acting as a Media Foundation Transform (MFT), the process works as follows:</span></span>

-   <span data-ttu-id="07a27-121">O Windows Media Player chama **IMFTransform::P rocessinput**, passando um ponteiro para um objeto de interface **IMFSample** para o plug-in do DSP.</span><span class="sxs-lookup"><span data-stu-id="07a27-121">Windows Media Player calls **IMFTransform::ProcessInput**, passing a pointer to an **IMFSample** interface object to the DSP plug-in.</span></span>
    1.  <span data-ttu-id="07a27-122">O plug-in do DSP mantém uma contagem de referência na interface **IMFSample** .</span><span class="sxs-lookup"><span data-stu-id="07a27-122">The DSP plug-in keeps a reference count on the **IMFSample** interface.</span></span> <span data-ttu-id="07a27-123">O plug-in do DSP retorna um **HRESULT** de êxito ou falha apropriado.</span><span class="sxs-lookup"><span data-stu-id="07a27-123">The DSP plug-in returns an appropriate success or failure **HRESULT**.</span></span>
    2.  <span data-ttu-id="07a27-124">O Windows Media Player chama **IMFTransform::P rocessoutput**, passando um ponteiro para uma matriz de estruturas de buffer de dados de saída da MFT (que contêm buffers de saída) para o plug-in do DSP. **\_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="07a27-124">Windows Media Player calls **IMFTransform::ProcessOutput**, passing a pointer to an array of **MFT\_OUTPUT\_DATA\_BUFFER** structures (which contain output buffers) to the DSP plug-in.</span></span>
    3.  <span data-ttu-id="07a27-125">O plug-in do DSP processa os dados no buffer de entrada e, em seguida, copia os dados para o buffer de saída apropriado.</span><span class="sxs-lookup"><span data-stu-id="07a27-125">The DSP plug-in processes the data in the input buffer and then copies the data to the appropriate output buffer.</span></span> <span data-ttu-id="07a27-126">O plug-in do DSP libera a contagem de referência no objeto de buffer de entrada quando todos os dados no buffer são processados.</span><span class="sxs-lookup"><span data-stu-id="07a27-126">The DSP plug-in releases the reference count on the input buffer object when all the data in the buffer has been processed.</span></span> <span data-ttu-id="07a27-127">Em seguida, o plug-in do DSP retorna um **HRESULT** de êxito ou falha apropriado.</span><span class="sxs-lookup"><span data-stu-id="07a27-127">The DSP plug-in then returns an appropriate success or failure **HRESULT**.</span></span>
    4.  <span data-ttu-id="07a27-128">O Windows Media Player renderiza o conteúdo no buffer de saída.</span><span class="sxs-lookup"><span data-stu-id="07a27-128">Windows Media Player renders the content in the output buffer.</span></span>

<span data-ttu-id="07a27-129">Esse processo se repete continuamente enquanto o plug-in está habilitado e o Windows Media Player tem conteúdo a ser renderizado.</span><span class="sxs-lookup"><span data-stu-id="07a27-129">This process repeats continuously while the plug-in is enabled and Windows Media Player has content to render.</span></span>

> [!Note]  
> <span data-ttu-id="07a27-130">Não escreva código que grave dados no buffer de entrada ou leia dados do buffer de saída.</span><span class="sxs-lookup"><span data-stu-id="07a27-130">Do not write code that writes data to the input buffer or reads data from the output buffer.</span></span> <span data-ttu-id="07a27-131">O acesso incorreto aos buffers de dados pode gerar resultados inesperados.</span><span class="sxs-lookup"><span data-stu-id="07a27-131">Incorrectly accessing data buffers may yield unexpected results.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="07a27-132">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="07a27-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="07a27-133">**Visão geral do desenvolvedor de plug-in do DSP**</span><span class="sxs-lookup"><span data-stu-id="07a27-133">**DSP Plug-in Developer Overview**</span></span>](dsp-plug-in-developer-overview.md)
</dt> </dl>

 

 




