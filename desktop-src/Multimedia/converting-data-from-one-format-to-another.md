---
title: Convertendo dados de um formato para outro
description: Convertendo dados de um formato para outro
ms.assetid: df995b7d-ac45-4964-a1b0-efd079c0c010
keywords:
- Gerenciador de compactação de áudio (ACM), convertendo dados
- ACM (Gerenciador de compactação de áudio), convertendo dados
- Exemplos do ACM, convertendo dados
- convertendo dados
- função acmStreamOpen
- função acmStreamSize
- função acmStreamPrepareHeader
- função acmStreamConvert
- função acmStreamUnprepareHeader
- função acmStreamClose
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9645342aa9f19b2c31de77dc9d1031122ed0b2ac
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292128"
---
# <a name="converting-data-from-one-format-to-another"></a><span data-ttu-id="db762-113">Convertendo dados de um formato para outro</span><span class="sxs-lookup"><span data-stu-id="db762-113">Converting Data from One Format to Another</span></span>

<span data-ttu-id="db762-114">O ACM usa funções de fluxo para dar suporte à conversão de formato de dados.</span><span class="sxs-lookup"><span data-stu-id="db762-114">The ACM uses stream functions to support data format conversion.</span></span> <span data-ttu-id="db762-115">Os conversores no ACM alteram o formato, mas não o tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="db762-115">Converters in the ACM change the format, but not the data type.</span></span> <span data-ttu-id="db762-116">Por exemplo, um módulo conversor pode alterar 44-kHz, dados de 16 bits para 44-kHz, dados de 8 bits.</span><span class="sxs-lookup"><span data-stu-id="db762-116">For example, a converter module can change 44-kHz, 16-bit data to 44-kHz, 8-bit data.</span></span>

<span data-ttu-id="db762-117">As seguintes funções do ACM dão suporte à conversão de formato de dados.</span><span class="sxs-lookup"><span data-stu-id="db762-117">The following ACM functions support data format conversion.</span></span> <span data-ttu-id="db762-118">Eles são listados na ordem em que você normalmente os usaria.</span><span class="sxs-lookup"><span data-stu-id="db762-118">They are listed in the order in which you would typically use them.</span></span>

-   <span data-ttu-id="db762-119">A função [**acmStreamOpen**](/windows/desktop/api/Msacm/nf-msacm-acmstreamopen) abre um fluxo de conversão.</span><span class="sxs-lookup"><span data-stu-id="db762-119">The [**acmStreamOpen**](/windows/desktop/api/Msacm/nf-msacm-acmstreamopen) function opens a conversion stream.</span></span>
-   <span data-ttu-id="db762-120">A função [**acmStreamSize**](/windows/desktop/api/Msacm/nf-msacm-acmstreamsize) calcula o tamanho apropriado do buffer de origem ou de destino.</span><span class="sxs-lookup"><span data-stu-id="db762-120">The [**acmStreamSize**](/windows/desktop/api/Msacm/nf-msacm-acmstreamsize) function calculates the appropriate size of the source or destination buffer.</span></span>
-   <span data-ttu-id="db762-121">A função [**acmStreamPrepareHeader**](/windows/desktop/api/Msacm/nf-msacm-acmstreamprepareheader) prepara os buffers de origem e de destino a serem usados em uma conversão.</span><span class="sxs-lookup"><span data-stu-id="db762-121">The [**acmStreamPrepareHeader**](/windows/desktop/api/Msacm/nf-msacm-acmstreamprepareheader) function prepares source and destination buffers to be used in a conversion.</span></span>
-   <span data-ttu-id="db762-122">A função [**acmStreamConvert**](/windows/desktop/api/Msacm/nf-msacm-acmstreamconvert) converte dados em um buffer de origem no formato de destino, gravando os dados convertidos no buffer de destino.</span><span class="sxs-lookup"><span data-stu-id="db762-122">The [**acmStreamConvert**](/windows/desktop/api/Msacm/nf-msacm-acmstreamconvert) function converts data in a source buffer into the destination format, writing the converted data into the destination buffer.</span></span>
-   <span data-ttu-id="db762-123">A função [**acmStreamUnprepareHeader**](/windows/desktop/api/Msacm/nf-msacm-acmstreamunprepareheader) limpa os buffers de origem e de destino preparados pelo **acmStreamPrepareHeader**.</span><span class="sxs-lookup"><span data-stu-id="db762-123">The [**acmStreamUnprepareHeader**](/windows/desktop/api/Msacm/nf-msacm-acmstreamunprepareheader) function cleans up the source and destination buffers prepared by **acmStreamPrepareHeader**.</span></span> <span data-ttu-id="db762-124">Você deve chamar essa função antes de liberar os buffers de origem e de destino.</span><span class="sxs-lookup"><span data-stu-id="db762-124">You must call this function before freeing the source and destination buffers.</span></span>
-   <span data-ttu-id="db762-125">A função [**acmStreamClose**](/windows/desktop/api/Msacm/nf-msacm-acmstreamclose) fecha um fluxo de conversão.</span><span class="sxs-lookup"><span data-stu-id="db762-125">The [**acmStreamClose**](/windows/desktop/api/Msacm/nf-msacm-acmstreamclose) function closes a conversion stream.</span></span>

<span data-ttu-id="db762-126">Ao converter dados, primeiro identifique o formato de origem e, em seguida, escolha o formato de destino.</span><span class="sxs-lookup"><span data-stu-id="db762-126">When converting data, first identify the source format, then choose the destination format.</span></span> <span data-ttu-id="db762-127">A maneira mais fácil de fazer isso é usando a função [**acmFormatChoose**](/windows/desktop/api/Msacm/nf-msacm-acmformatchoose) , que exibe uma caixa de diálogo de seleção de formato e retorna a opção de formato do usuário.</span><span class="sxs-lookup"><span data-stu-id="db762-127">The easiest way to do this is by using the [**acmFormatChoose**](/windows/desktop/api/Msacm/nf-msacm-acmformatchoose) function, which displays a format-selection dialog box and returns the user's format choice.</span></span>

<span data-ttu-id="db762-128">Quando você conhece os formatos de origem e destino, pode usar [**acmStreamOpen**](/windows/desktop/api/Msacm/nf-msacm-acmstreamopen) para abrir um fluxo de conversão.</span><span class="sxs-lookup"><span data-stu-id="db762-128">When you know the source and destination formats, you can use [**acmStreamOpen**](/windows/desktop/api/Msacm/nf-msacm-acmstreamopen) to open a conversion stream.</span></span> <span data-ttu-id="db762-129">Em seguida, você pode usar a função [**acmStreamSize**](/windows/desktop/api/Msacm/nf-msacm-acmstreamsize) para determinar os tamanhos de buffer apropriados.</span><span class="sxs-lookup"><span data-stu-id="db762-129">Then you can use the [**acmStreamSize**](/windows/desktop/api/Msacm/nf-msacm-acmstreamsize) function to determine the appropriate buffer sizes.</span></span>

<span data-ttu-id="db762-130">A próxima etapa é preparar os buffers a serem usados na conversão usando [**acmStreamPrepareHeader**](/windows/desktop/api/Msacm/nf-msacm-acmstreamprepareheader).</span><span class="sxs-lookup"><span data-stu-id="db762-130">The next step is to prepare the buffers to be used in the conversion by using [**acmStreamPrepareHeader**](/windows/desktop/api/Msacm/nf-msacm-acmstreamprepareheader).</span></span>

<span data-ttu-id="db762-131">Para executar a conversão, use [**acmStreamConvert**](/windows/desktop/api/Msacm/nf-msacm-acmstreamconvert) até que todos os buffers tenham sido processados.</span><span class="sxs-lookup"><span data-stu-id="db762-131">To perform the conversion, use [**acmStreamConvert**](/windows/desktop/api/Msacm/nf-msacm-acmstreamconvert) until all the buffers have been processed.</span></span> <span data-ttu-id="db762-132">Quando a conversão for concluída, use [**acmStreamUnprepareHeader**](/windows/desktop/api/Msacm/nf-msacm-acmstreamunprepareheader) para limpar os buffers e, em seguida, use [**acmStreamClose**](/windows/desktop/api/Msacm/nf-msacm-acmstreamclose) para fechar o fluxo de conversão.</span><span class="sxs-lookup"><span data-stu-id="db762-132">When the conversion is complete, use [**acmStreamUnprepareHeader**](/windows/desktop/api/Msacm/nf-msacm-acmstreamunprepareheader) to clean up the buffers and then use [**acmStreamClose**](/windows/desktop/api/Msacm/nf-msacm-acmstreamclose) to close the conversion stream.</span></span>

 

 




