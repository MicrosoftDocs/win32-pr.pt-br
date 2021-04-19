---
title: Escolhendo um método de codificação
description: Escolhendo um método de codificação
ms.assetid: 095245a6-39eb-4228-86ac-ade94dde3695
keywords:
- perfis, escolhendo métodos de codificação
- perfis, métodos de codificação
- codecs, escolhendo métodos de codificação
- codecs, métodos de codificação
- perfis, selecionando métodos de codificação
- codecs, selecionando métodos de codificação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f54c5bd099e5aaf8b3a735594c8b87a335fc2594
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105763475"
---
# <a name="choosing-an-encoding-method"></a><span data-ttu-id="77ee0-109">Escolhendo um método de codificação</span><span class="sxs-lookup"><span data-stu-id="77ee0-109">Choosing an Encoding Method</span></span>

<span data-ttu-id="77ee0-110">Alguns codecs, como o codec do Windows Media Video 9, dão suporte a vários métodos de codificação.</span><span class="sxs-lookup"><span data-stu-id="77ee0-110">Some codecs, like the Windows Media Video 9 codec, support multiple encoding methods.</span></span> <span data-ttu-id="77ee0-111">O método de codificação que você escolher para um fluxo dependerá de como o fluxo será entregue.</span><span class="sxs-lookup"><span data-stu-id="77ee0-111">The encoding method that you choose for a stream will depend upon how the stream is to be delivered.</span></span> <span data-ttu-id="77ee0-112">A tabela a seguir descreve quando usar os vários métodos de codificação.</span><span class="sxs-lookup"><span data-stu-id="77ee0-112">The following table describes when to use the various encoding methods.</span></span>



| <span data-ttu-id="77ee0-113">Método de codificação</span><span class="sxs-lookup"><span data-stu-id="77ee0-113">Encoding method</span></span>                | <span data-ttu-id="77ee0-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="77ee0-114">Description</span></span>                                                                                                                                                                                       |
|--------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="77ee0-115">1 – passar taxa de bits constante (CBR)</span><span class="sxs-lookup"><span data-stu-id="77ee0-115">1-pass Constant Bit Rate (CBR)</span></span> | <span data-ttu-id="77ee0-116">A única opção para transmissão ao vivo.</span><span class="sxs-lookup"><span data-stu-id="77ee0-116">The only option for live streaming.</span></span> <span data-ttu-id="77ee0-117">Codifica para uma taxa de bits previsível e fornece a qualidade mais baixa de todos os métodos de codificação.</span><span class="sxs-lookup"><span data-stu-id="77ee0-117">Encodes to a predictable bit rate and delivers the lowest quality of all encoding methods.</span></span>                                                                    |
| <span data-ttu-id="77ee0-118">2-passar CBR</span><span class="sxs-lookup"><span data-stu-id="77ee0-118">2-pass CBR</span></span>                     | <span data-ttu-id="77ee0-119">Use para arquivos que serão transmitidos em uma rede para um leitor de cliente, mas que não são transmitidos de uma fonte dinâmica.</span><span class="sxs-lookup"><span data-stu-id="77ee0-119">Use for files that will be streamed over a network to a client reader, but that are not broadcast from a live source.</span></span> <span data-ttu-id="77ee0-120">Codifica para uma taxa de bits previsível, mas com qualidade melhor do que 1-passar CBR.</span><span class="sxs-lookup"><span data-stu-id="77ee0-120">Encodes to a predictable bit rate, but with better quality than 1-pass CBR.</span></span> |
| <span data-ttu-id="77ee0-121">1 – passar taxa de bits variável (VBR)</span><span class="sxs-lookup"><span data-stu-id="77ee0-121">1-pass Variable Bit Rate (VBR)</span></span> | <span data-ttu-id="77ee0-122">Use quando precisar especificar a qualidade da saída codificada.</span><span class="sxs-lookup"><span data-stu-id="77ee0-122">Use when you need to specify the quality of the encoded output.</span></span> <span data-ttu-id="77ee0-123">Fornece a qualidade mais consistente de todos os métodos de codificação.</span><span class="sxs-lookup"><span data-stu-id="77ee0-123">Delivers the most consistent quality of all encoding methods.</span></span> <span data-ttu-id="77ee0-124">Use somente para arquivos locais ou para download.</span><span class="sxs-lookup"><span data-stu-id="77ee0-124">Use only for local files or for downloading.</span></span>                        |
| <span data-ttu-id="77ee0-125">2-passar VBR – irrestrito</span><span class="sxs-lookup"><span data-stu-id="77ee0-125">2-pass VBR – unconstrained</span></span>     | <span data-ttu-id="77ee0-126">Use quando precisar especificar uma largura de banda, mas flutuações em volta da largura de banda especificada são aceitáveis.</span><span class="sxs-lookup"><span data-stu-id="77ee0-126">Use when you need to specify a bandwidth, but fluctuations around the specified bandwidth are acceptable.</span></span> <span data-ttu-id="77ee0-127">Somente para arquivos locais ou somente para download.</span><span class="sxs-lookup"><span data-stu-id="77ee0-127">For local files or downloading only.</span></span>                                                    |
| <span data-ttu-id="77ee0-128">2-passar VBR – restrito</span><span class="sxs-lookup"><span data-stu-id="77ee0-128">2-pass VBR – constrained</span></span>       | <span data-ttu-id="77ee0-129">Use sob as mesmas circunstâncias sem restrição, mas quando você precisar especificar uma taxa de bits de tempo máxima.</span><span class="sxs-lookup"><span data-stu-id="77ee0-129">Use under the same circumstances as unconstrained, but when you need to specify a maximum momentary bit rate.</span></span> <span data-ttu-id="77ee0-130">Somente para arquivos locais ou somente para download.</span><span class="sxs-lookup"><span data-stu-id="77ee0-130">For local files or downloading only.</span></span>                                                |



 

<span data-ttu-id="77ee0-131">A tabela a seguir lista os métodos de codificação que são suportados pelos codecs fornecidos com o Windows Media Format SDK.</span><span class="sxs-lookup"><span data-stu-id="77ee0-131">The following table lists the encoding methods that are supported by the codecs that ship with the Windows Media Format SDK.</span></span>



| <span data-ttu-id="77ee0-132">Codec</span><span class="sxs-lookup"><span data-stu-id="77ee0-132">Codec</span></span>                                  | <span data-ttu-id="77ee0-133">CBR</span><span class="sxs-lookup"><span data-stu-id="77ee0-133">CBR</span></span> | <span data-ttu-id="77ee0-134">2-passar CBR</span><span class="sxs-lookup"><span data-stu-id="77ee0-134">2-pass CBR</span></span> | <span data-ttu-id="77ee0-135">BITS</span><span class="sxs-lookup"><span data-stu-id="77ee0-135">VBR</span></span> | <span data-ttu-id="77ee0-136">2-passar VBR</span><span class="sxs-lookup"><span data-stu-id="77ee0-136">2-pass VBR</span></span> |
|----------------------------------------|-----|------------|-----|------------|
| <span data-ttu-id="77ee0-137">Vídeo do Windows Media 9</span><span class="sxs-lookup"><span data-stu-id="77ee0-137">Windows Media Video 9</span></span>                  | <span data-ttu-id="77ee0-138">X</span><span class="sxs-lookup"><span data-stu-id="77ee0-138">X</span></span>   | <span data-ttu-id="77ee0-139">X</span><span class="sxs-lookup"><span data-stu-id="77ee0-139">X</span></span>          | <span data-ttu-id="77ee0-140">X</span><span class="sxs-lookup"><span data-stu-id="77ee0-140">X</span></span>   | <span data-ttu-id="77ee0-141">X</span><span class="sxs-lookup"><span data-stu-id="77ee0-141">X</span></span>          |
| <span data-ttu-id="77ee0-142">Windows Media Audio 9 e posterior</span><span class="sxs-lookup"><span data-stu-id="77ee0-142">Windows Media Audio 9 and later</span></span>        | <span data-ttu-id="77ee0-143">X</span><span class="sxs-lookup"><span data-stu-id="77ee0-143">X</span></span>   | <span data-ttu-id="77ee0-144">X</span><span class="sxs-lookup"><span data-stu-id="77ee0-144">X</span></span>          | <span data-ttu-id="77ee0-145">X</span><span class="sxs-lookup"><span data-stu-id="77ee0-145">X</span></span>   | <span data-ttu-id="77ee0-146">X</span><span class="sxs-lookup"><span data-stu-id="77ee0-146">X</span></span>          |
| <span data-ttu-id="77ee0-147">Tela do Windows Media Video 9</span><span class="sxs-lookup"><span data-stu-id="77ee0-147">Windows Media Video 9 Screen</span></span>           | <span data-ttu-id="77ee0-148">X</span><span class="sxs-lookup"><span data-stu-id="77ee0-148">X</span></span>   |            | <span data-ttu-id="77ee0-149">X</span><span class="sxs-lookup"><span data-stu-id="77ee0-149">X</span></span>   |            |
| <span data-ttu-id="77ee0-150">Voz do Windows Media Audio 9</span><span class="sxs-lookup"><span data-stu-id="77ee0-150">Windows Media Audio 9 Voice</span></span>            | <span data-ttu-id="77ee0-151">X</span><span class="sxs-lookup"><span data-stu-id="77ee0-151">X</span></span>   |            |     |            |
| <span data-ttu-id="77ee0-152">Windows Media Audio Professional</span><span class="sxs-lookup"><span data-stu-id="77ee0-152">Windows Media Audio Professional</span></span>       | <span data-ttu-id="77ee0-153">X</span><span class="sxs-lookup"><span data-stu-id="77ee0-153">X</span></span>   | <span data-ttu-id="77ee0-154">X</span><span class="sxs-lookup"><span data-stu-id="77ee0-154">X</span></span>          | <span data-ttu-id="77ee0-155">X</span><span class="sxs-lookup"><span data-stu-id="77ee0-155">X</span></span>   | <span data-ttu-id="77ee0-156">X</span><span class="sxs-lookup"><span data-stu-id="77ee0-156">X</span></span>          |
| <span data-ttu-id="77ee0-157">Windows Media Audio sem perdas</span><span class="sxs-lookup"><span data-stu-id="77ee0-157">Windows Media Audio Lossless</span></span>           |     |            | <span data-ttu-id="77ee0-158">X</span><span class="sxs-lookup"><span data-stu-id="77ee0-158">X</span></span>   |            |
| <span data-ttu-id="77ee0-159">Imagem do Windows Media Video 9 e posterior</span><span class="sxs-lookup"><span data-stu-id="77ee0-159">Windows Media Video 9 Image and later</span></span>  | <span data-ttu-id="77ee0-160">X</span><span class="sxs-lookup"><span data-stu-id="77ee0-160">X</span></span>   |            | <span data-ttu-id="77ee0-161">X</span><span class="sxs-lookup"><span data-stu-id="77ee0-161">X</span></span>   |            |
| <span data-ttu-id="77ee0-162">Perfil avançado do Windows Media Video 9</span><span class="sxs-lookup"><span data-stu-id="77ee0-162">Windows Media Video 9 Advanced Profile</span></span> | <span data-ttu-id="77ee0-163">X</span><span class="sxs-lookup"><span data-stu-id="77ee0-163">X</span></span>   | <span data-ttu-id="77ee0-164">X</span><span class="sxs-lookup"><span data-stu-id="77ee0-164">X</span></span>          | <span data-ttu-id="77ee0-165">X</span><span class="sxs-lookup"><span data-stu-id="77ee0-165">X</span></span>   | <span data-ttu-id="77ee0-166">X</span><span class="sxs-lookup"><span data-stu-id="77ee0-166">X</span></span>          |



 

## <a name="related-topics"></a><span data-ttu-id="77ee0-167">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="77ee0-167">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="77ee0-168">**Criando perfis**</span><span class="sxs-lookup"><span data-stu-id="77ee0-168">**Designing Profiles**</span></span>](designing-profiles.md)
</dt> <dt>

[<span data-ttu-id="77ee0-169">**Codificação de taxa de bits constante (CBR)**</span><span class="sxs-lookup"><span data-stu-id="77ee0-169">**Constant Bit Rate (CBR) Encoding**</span></span>](constant-bit-rate--cbr--encoding.md)
</dt> <dt>

[<span data-ttu-id="77ee0-170">**Codificação de duas passagens**</span><span class="sxs-lookup"><span data-stu-id="77ee0-170">**Two-Pass Encoding**</span></span>](two-pass-encoding.md)
</dt> <dt>

[<span data-ttu-id="77ee0-171">**Codificação de taxa de bits variável (VBR)**</span><span class="sxs-lookup"><span data-stu-id="77ee0-171">**Variable Bit Rate (VBR) Encoding**</span></span>](variable-bit-rate--vbr--encoding.md)
</dt> </dl>

 

 




