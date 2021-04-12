---
title: Selecionando taxas de bits
description: Selecionando taxas de bits
ms.assetid: 466524a6-2473-4768-8ae3-0ac18807f88c
keywords:
- perfis, escolhendo taxas de bits
- perfis, taxas de bits
- codecs, escolhendo taxas de bits
- codecs, taxas de bits
- perfis, selecionando taxas de bits
- codecs, selecionando taxas de bits
- taxas de bits, selecionando
- taxas de bits, perfis
- taxas de bits, codecs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3cd8c125aacc5add255962ca37e6060af20d66f8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104291749"
---
# <a name="selecting-bit-rates"></a><span data-ttu-id="866aa-112">Selecionando taxas de bits</span><span class="sxs-lookup"><span data-stu-id="866aa-112">Selecting Bit Rates</span></span>

<span data-ttu-id="866aa-113">Para arquivos que serão transmitidos em uma rede, você deve considerar cuidadosamente quais taxas de bits devem ser usadas.</span><span class="sxs-lookup"><span data-stu-id="866aa-113">For files that will be streamed over a network, you must consider carefully what bit rates you should use.</span></span> <span data-ttu-id="866aa-114">Na maioria das circunstâncias, você pode adicionar as taxas de bits de todos os fluxos em um arquivo em conjunto para obter uma ideia geral da largura de banda disponível necessária para transmitir o arquivo.</span><span class="sxs-lookup"><span data-stu-id="866aa-114">Under most circumstances you can add the bit rates of all of the streams in a file together to get a general idea of the available bandwidth required to stream the file.</span></span> <span data-ttu-id="866aa-115">No entanto, uma determinada quantidade de sobrecarga também é necessária para cada fluxo.</span><span class="sxs-lookup"><span data-stu-id="866aa-115">However, a certain amount of overhead is also required for each stream.</span></span> <span data-ttu-id="866aa-116">Essa sobrecarga é resumida na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="866aa-116">This overhead is summarized in the following table.</span></span>



| <span data-ttu-id="866aa-117">Intervalo de taxa de bits (Kbps)</span><span class="sxs-lookup"><span data-stu-id="866aa-117">Bit-rate range (Kbps)</span></span> | <span data-ttu-id="866aa-118">Largura de banda adicional necessária para sobrecarga (Kbps)</span><span class="sxs-lookup"><span data-stu-id="866aa-118">Additional bandwidth required for overhead (Kbps)</span></span> |
|-----------------------|---------------------------------------------------|
| <span data-ttu-id="866aa-119">10 a 16</span><span class="sxs-lookup"><span data-stu-id="866aa-119">10 – 16</span></span>               | <span data-ttu-id="866aa-120">3</span><span class="sxs-lookup"><span data-stu-id="866aa-120">3</span></span>                                                 |
| <span data-ttu-id="866aa-121">17 a 30</span><span class="sxs-lookup"><span data-stu-id="866aa-121">17 – 30</span></span>               | <span data-ttu-id="866aa-122">4</span><span class="sxs-lookup"><span data-stu-id="866aa-122">4</span></span>                                                 |
| <span data-ttu-id="866aa-123">31 a 45</span><span class="sxs-lookup"><span data-stu-id="866aa-123">31 – 45</span></span>               | <span data-ttu-id="866aa-124">5</span><span class="sxs-lookup"><span data-stu-id="866aa-124">5</span></span>                                                 |
| <span data-ttu-id="866aa-125">46 – 70</span><span class="sxs-lookup"><span data-stu-id="866aa-125">46 – 70</span></span>               | <span data-ttu-id="866aa-126">6</span><span class="sxs-lookup"><span data-stu-id="866aa-126">6</span></span>                                                 |
| <span data-ttu-id="866aa-127">71 – 225</span><span class="sxs-lookup"><span data-stu-id="866aa-127">71 – 225</span></span>              | <span data-ttu-id="866aa-128">7</span><span class="sxs-lookup"><span data-stu-id="866aa-128">7</span></span>                                                 |
| <span data-ttu-id="866aa-129">>225</span><span class="sxs-lookup"><span data-stu-id="866aa-129">>225</span></span>               | <span data-ttu-id="866aa-130">9</span><span class="sxs-lookup"><span data-stu-id="866aa-130">9</span></span>                                                 |



 

<span data-ttu-id="866aa-131">A sobrecarga normal necessária para um fluxo não leva em conta as extensões de unidade de dados.</span><span class="sxs-lookup"><span data-stu-id="866aa-131">The normal overhead required for a stream does not take data unit extensions into account.</span></span> <span data-ttu-id="866aa-132">Cada extensão de unidade de dados adiciona ao tamanho do exemplo ao qual está anexada.</span><span class="sxs-lookup"><span data-stu-id="866aa-132">Every data unit extension adds to the size of the sample to which it is attached.</span></span> <span data-ttu-id="866aa-133">Dependendo do tipo de extensão de unidade de dados, isso pode aumentar muito a taxa de bits para o fluxo.</span><span class="sxs-lookup"><span data-stu-id="866aa-133">Depending upon the type of data unit extension, this can greatly increase the bit rate for the stream.</span></span>

<span data-ttu-id="866aa-134">Você também deve considerar que a máxima largura de banda teórica disponível em uma conexão de rede não é uma taxa de bits de destino prática.</span><span class="sxs-lookup"><span data-stu-id="866aa-134">You must also consider that the theoretical maximum bandwidth available over a network connection is not a practical target bit rate.</span></span> <span data-ttu-id="866aa-135">A largura de banda média disponível para qualquer conexão fornecida é bem curta da capacidade de largura de banda da conexão, devido ao tráfego de rede e a muitos outros fatores.</span><span class="sxs-lookup"><span data-stu-id="866aa-135">The average available bandwidth for any given connection falls well short of the bandwidth capacity of the connection, because of network traffic and many other factors.</span></span>

## <a name="related-topics"></a><span data-ttu-id="866aa-136">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="866aa-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="866aa-137">**Criando perfis**</span><span class="sxs-lookup"><span data-stu-id="866aa-137">**Designing Profiles**</span></span>](designing-profiles.md)
</dt> </dl>

 

 




