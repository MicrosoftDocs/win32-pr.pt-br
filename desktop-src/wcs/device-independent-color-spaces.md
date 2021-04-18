---
title: Espaços de cores independentes do dispositivo
description: Reconhecendo a necessidade de medidas de cores padrão, independentes de dispositivo, a Comissão International de l'Eclairage (Comissão Internacional na iluminação) ou CIE, criou um espaço de cores baseado em \ 0034; imaginário \ 0034; cores primárias.
ms.assetid: 8597dad3-1eb8-49f9-9843-1f9068a65925
keywords:
- WCS (sistema de cores do Windows), espaços de cores independentes de dispositivo
- WCS (sistema de cores do Windows), espaços de cores independentes de dispositivo
- gerenciamento de cores de imagem, espaços de cores independentes de dispositivo
- gerenciamento de cores, espaços de cores independentes de dispositivo
- cores, espaços de cores independentes de dispositivo
- espaços de cores, independentes de dispositivo
- espaços de cores independentes de dispositivo
- Commission International de l'Eclairage (CIE)
- CIE (Comissão Internacional de iluminação)
- CIE (Commission International de l'Eclairage)
- CIE (Comissão Internacional sobre iluminação)
- Espaço de cores CIEXYZ
- Espaço de cores XYZ
- espaço de cores sRGB
- espaços de cores, CIEXYZ
- espaços de cores, sRGB
- espaços de cores, XYZ
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d044379f8f04467f7be94f09d1eb1fa41816d3e
ms.sourcegitcommit: 38954f8f0d70f44bff4a943784f468ebd7ef691a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "105795514"
---
# <a name="device-independent-color-spaces"></a><span data-ttu-id="f0843-120">Espaços de cores independentes do dispositivo</span><span class="sxs-lookup"><span data-stu-id="f0843-120">Device-Independent Color Spaces</span></span>

<span data-ttu-id="f0843-121">Reconhecendo a necessidade de medidas de cores padrão, independentes de dispositivo, a Comissão International de l'Eclairage (Comissão Internacional na iluminação) ou CIE, criou um [espaço de cores](c.md) com base em [cores primárias](p.md)"imaginários".</span><span class="sxs-lookup"><span data-stu-id="f0843-121">Recognizing the need for standard, device-independent color measurements, the Commission International de l'Eclairage (International Commission on Illumination), or CIE, created a [color space](c.md) based on "imaginary" [primary colors](p.md).</span></span> <span data-ttu-id="f0843-122">Nenhum dispositivo real é esperado para produzir cores nesse espaço de cores.</span><span class="sxs-lookup"><span data-stu-id="f0843-122">No actual device is expected to produce colors in this color space.</span></span> <span data-ttu-id="f0843-123">Ele é usado como um meio de converter cores de um espaço de cor para outro.</span><span class="sxs-lookup"><span data-stu-id="f0843-123">It is used as a means of converting colors from one color space to another.</span></span> <span data-ttu-id="f0843-124">As cores primárias nesse espaço de cores são as cores abstratas X, Y e Z.</span><span class="sxs-lookup"><span data-stu-id="f0843-124">The primary colors in this color space are the abstract colors X, Y, and Z.</span></span>

<span data-ttu-id="f0843-125">O espaço de cores de 1931 CIEXYZ é amplamente usado como a base para conversão de espaço de cor.</span><span class="sxs-lookup"><span data-stu-id="f0843-125">The 1931 CIEXYZ color space is widely used as the basis for color space conversion.</span></span> <span data-ttu-id="f0843-126">No entanto, com o crescimento da Internet, as considerações sobre largura de banda tornaram o espaço de cores XYZ incômodo.</span><span class="sxs-lookup"><span data-stu-id="f0843-126">With the rise of the Internet, however, bandwidth considerations have made the XYZ color space unwieldy.</span></span> <span data-ttu-id="f0843-127">A troca de imagens sobre a largura de banda limitada da Internet exige um modelo de [cores](c.md)mais compacto.</span><span class="sxs-lookup"><span data-stu-id="f0843-127">The exchange of images over the limited bandwidth of the Internet necessitates a more compact [color model](c.md).</span></span>

<span data-ttu-id="f0843-128">Como resultado, a Hewlett-Packard e a Microsoft propuseram a adoção de um espaço de cores RGB predefinido padrão conhecido como sRGB, para permitir o gerenciamento preciso de cores com muito pouca sobrecarga de dados.</span><span class="sxs-lookup"><span data-stu-id="f0843-128">As a result, Hewlett-Packard and Microsoft have proposed the adoption of a standard predefined RGB color space known as sRGB, so as to allow accurate color management with very little data overhead.</span></span> <span data-ttu-id="f0843-129">Esse padrão foi aprovado como um padrão internacional formal pelo International Electrotechnical Commission (IEC) como IEC 61966-2-1: sistemas de multimídia e medição de EquipmentColour e ManagementPart 2-1: cor ManagementDefault o espaço de cores RGB.</span><span class="sxs-lookup"><span data-stu-id="f0843-129">This standard has been approved as a formal international standard by the International Electrotechnical Commission (IEC) as IEC 61966-2-1: Multimedia Systems and EquipmentColour Measurement and ManagementPart 2-1: Colour ManagementDefault RGB Colour Space.</span></span> <span data-ttu-id="f0843-130">Ele está disponível diretamente do IEC em <https://www.iec.ch/> .</span><span class="sxs-lookup"><span data-stu-id="f0843-130">It is available directly from the IEC at <https://www.iec.ch/>.</span></span> <span data-ttu-id="f0843-131">As informações que abordam os problemas técnicos envolvidos no sRGB estão disponíveis na Internet em:</span><span class="sxs-lookup"><span data-stu-id="f0843-131">Information discussing the technical issues involved in sRGB is available on the Internet at:</span></span>

[<span data-ttu-id="f0843-132">Um espaço de cores padrão para a Internet-sRGB</span><span class="sxs-lookup"><span data-stu-id="f0843-132">A Standard Default Color Space for the Internet - sRGB</span></span>](https://www.w3.org/Graphics/Color/sRGB.html)

<span data-ttu-id="f0843-133">Uma versão de arquivo de ajuda de um white paper discutindo os problemas técnicos envolvidos em sRGB, sRGB. HLP, está disponível na \\ pasta de ajuda da referência do programador do WCS 1,0 no SDK da plataforma.</span><span class="sxs-lookup"><span data-stu-id="f0843-133">A help-file version of a white paper discussing the technical issues involved in sRGB, sRGB.HLP, is available in the \\Help folder of the WCS 1.0 Programmer's Reference in the Platform SDK.</span></span>

<span data-ttu-id="f0843-134">Formatos de arquivo diferentes podem usar ou adicionar um sinalizador para especificar que a imagem está no espaço de cores sRGB.</span><span class="sxs-lookup"><span data-stu-id="f0843-134">Different file formats may use or add a flag to specify that the image is in sRGB color space.</span></span> <span data-ttu-id="f0843-135">No formato DIB (bitmap independente de dispositivo) do Windows, definir o membro **bV5CSType** da estrutura [BITMAPV5HEADER](using-structures-in-wcs-1-0.md) para LCS \_ sRGB especifica que as cores de DIB estão no espaço de cores sRGB.</span><span class="sxs-lookup"><span data-stu-id="f0843-135">In the Windows device-independent bitmap (DIB) format, setting the **bV5CSType** member of the [BITMAPV5HEADER](using-structures-in-wcs-1-0.md) structure to LCS\_sRGB specifies that the DIB colors are in the sRGB color space.</span></span>

 

 




