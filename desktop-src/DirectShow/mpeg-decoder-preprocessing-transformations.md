---
description: Transformações de pré-processamento do decodificador MPEG
ms.assetid: c7ae0137-0d02-46da-9532-738d805e327d
title: Transformações de pré-processamento do decodificador MPEG
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82d7bcf8eeda8062606ce0046a55e34d3c2d90fe
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/22/2021
ms.locfileid: "107908894"
---
# <a name="mpeg-decoder-preprocessing-transformations"></a><span data-ttu-id="84583-103">Transformações de pré-processamento do decodificador MPEG</span><span class="sxs-lookup"><span data-stu-id="84583-103">MPEG Decoder Preprocessing Transformations</span></span>

<span data-ttu-id="84583-104">**Letterbox e PanScan**</span><span class="sxs-lookup"><span data-stu-id="84583-104">**Letterbox and PanScan**</span></span>

<span data-ttu-id="84583-105">A imagem 4x3 pode ser formada preenchendo a parte superior e inferior da imagem (chamada de imagem Letterbox) ou extraindo uma parte 4x3 da imagem (chamada de imagem PanScan).</span><span class="sxs-lookup"><span data-stu-id="84583-105">The 4x3 image can be formed by either padding the top and bottom of the image (referred to as a Letterbox image) or by extracting a 4x3 portion of the image (referred to as a PanScan image).</span></span> <span data-ttu-id="84583-106">Os fluxos de menus e subimagem são sobrepostos sobre a imagem de vídeo final.</span><span class="sxs-lookup"><span data-stu-id="84583-106">The menus and subpicture streams are overlaid on top of the final video image.</span></span> <span data-ttu-id="84583-107">As imagens de taxa de 16x9 são armazenadas em um formato 4x3 Anamorphic.</span><span class="sxs-lookup"><span data-stu-id="84583-107">The 16x9 ratio images are stored in a 4x3 anamorphic format.</span></span> <span data-ttu-id="84583-108">Esticar o vídeo de origem 720x480 de proporção de 4x3 de Anamorphic para uma taxa de proporção 16x9 forma a imagem de aspecto do 16x9 original.</span><span class="sxs-lookup"><span data-stu-id="84583-108">Stretching the anamorphic 4x3 aspect ratio 720x480 source video to a 16x9 aspect ratio forms the original 16x9 aspect image.</span></span>

<span data-ttu-id="84583-109">Veja abaixo uma descrição de como exibir corretamente cada um dos modos e seus destaques:</span><span class="sxs-lookup"><span data-stu-id="84583-109">Below is a description of how to correctly display each of the modes and their highlights:</span></span>

-   <span data-ttu-id="84583-110">**Tela widescreen:** O vídeo de origem ampliado para a maior área de 16x9 da janela de saída.</span><span class="sxs-lookup"><span data-stu-id="84583-110">**Widescreen:** The source video stretched into the largest 16x9 area of the output window.</span></span> <span data-ttu-id="84583-111">Os destaques são relativos ao interior da área 16x9.</span><span class="sxs-lookup"><span data-stu-id="84583-111">The highlights are relative to the inside of the 16x9 area.</span></span> <span data-ttu-id="84583-112">As barras pretas devem ser adicionadas à parte superior e inferior ou aos lados para manter uma área 16x9.</span><span class="sxs-lookup"><span data-stu-id="84583-112">Black bars should be added to either the top and bottom or to the sides to maintain a 16x9 area.</span></span>
-   <span data-ttu-id="84583-113">**Verificação de Pan:** No vídeo do 16x9, use o deslocamento horizontal fornecido no fluxo MPEG2 para extrair uma subjanela 4x3.</span><span class="sxs-lookup"><span data-stu-id="84583-113">**Pan Scan:** From the 16x9 video, use the horizontal offset provided in the MPEG2 stream to extract a 4x3 subwindow.</span></span> <span data-ttu-id="84583-114">Coloque a subjanela 4x3 na área de maior 4x3 da janela do cliente de saída.</span><span class="sxs-lookup"><span data-stu-id="84583-114">Place the 4x3 subwindow into the largest 4x3 area of the output client window.</span></span> <span data-ttu-id="84583-115">As coordenadas do realce são relativas à janela de saída 4x3 e não têm relação com o vídeo 16x9 de origem.</span><span class="sxs-lookup"><span data-stu-id="84583-115">The highlight's coordinates are relative to the 4x3 output window and have no relationship to the source 16x9 video.</span></span> <span data-ttu-id="84583-116">As barras pretas devem ser adicionadas à parte superior e inferior ou aos lados para manter uma área 4x3.</span><span class="sxs-lookup"><span data-stu-id="84583-116">Black bars should be added to either the top and bottom or to the sides to maintain a 4x3 area.</span></span>
-   <span data-ttu-id="84583-117">**Letterbox:** Calcule a maior área de 4x3 da janela de saída.</span><span class="sxs-lookup"><span data-stu-id="84583-117">**Letterbox:** Compute the largest 4x3 area of the output window.</span></span> <span data-ttu-id="84583-118">As barras pretas devem ser adicionadas à parte superior e inferior ou aos lados para manter uma área 4x3.</span><span class="sxs-lookup"><span data-stu-id="84583-118">Black bars should be added to either the top and bottom or to the sides to maintain a 4x3 area.</span></span> <span data-ttu-id="84583-119">O vídeo Anamorphic de origem 4x3 (representando uma imagem 16x9) é colocado na maior subjanela 16x9 dentro da área 4x3.</span><span class="sxs-lookup"><span data-stu-id="84583-119">The source anamorphic 4x3 video (representing a 16x9 image) is placed in the largest 16x9 subwindow inside of the 4x3 area.</span></span> <span data-ttu-id="84583-120">As barras pretas devem ser adicionadas à parte superior e inferior da subjanela para manter uma área 16x9.</span><span class="sxs-lookup"><span data-stu-id="84583-120">Black bars should be added to the top and bottom of the subwindow to maintain a 16x9 area.</span></span> <span data-ttu-id="84583-121">As coordenadas do realce são relativas à área 4x3 e não têm relação com o vídeo 16x9 de origem.</span><span class="sxs-lookup"><span data-stu-id="84583-121">The highlight's coordinates are relative to the 4x3 area and have no relationship to the source 16x9 video.</span></span> <span data-ttu-id="84583-122">É possível que um disco especifique um realce que está fora da área 16x9 (mas ainda na janela 4x3).</span><span class="sxs-lookup"><span data-stu-id="84583-122">It is possible for a disk to specify a highlight that lies outside of the 16x9 area (but still in the 4x3 window).</span></span> <span data-ttu-id="84583-123">Para vídeo 4x3, o vídeo é colocado na área de saída maior 4x3 da janela do cliente de saída.</span><span class="sxs-lookup"><span data-stu-id="84583-123">For 4x3 video, the video is placed in the largest 4x3 output area of the output client window.</span></span> <span data-ttu-id="84583-124">As barras pretas devem ser adicionadas à parte superior e inferior ou aos lados para manter uma área 4x3.</span><span class="sxs-lookup"><span data-stu-id="84583-124">Black bars should be added to either the top and bottom or to the sides to maintain a 4x3 area.</span></span>

<span data-ttu-id="84583-125">**Pré-processamento de MPEG com o navegador de DVD e o VMR**</span><span class="sxs-lookup"><span data-stu-id="84583-125">**MPEG preprocessing with the DVD Navigator and VMR**</span></span>

<span data-ttu-id="84583-126">Atualmente, o decodificador é passado \_ como um tipo de mídia de vídeo MPEG2 de formato \_ (cujo bloco de formato aponta para uma estrutura [**MPEG2VIDEOINFO**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo) ).</span><span class="sxs-lookup"><span data-stu-id="84583-126">Currently, the decoder is passed a FORMAT\_MPEG2\_VIDEO media type (whose format block points to a [**MPEG2VIDEOINFO**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo) structure).</span></span> <span data-ttu-id="84583-127">Nos Pins de saída, o decodificador produz um tipo de mídia de formato \_ VideoInfo2, cujo bloco de formato aponta para uma estrutura [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) .</span><span class="sxs-lookup"><span data-stu-id="84583-127">On the output pins, the decoder produces a FORMAT\_VideoInfo2 media type, whose format block points to a [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) structure.</span></span> <span data-ttu-id="84583-128">O campo **dwReserved** da estrutura foi renomeado para sinalizadores **dwControls** .</span><span class="sxs-lookup"><span data-stu-id="84583-128">The structure's **dwReserved** field has been renamed to **dwControls** flags.</span></span>

<span data-ttu-id="84583-129">O membro **dwControlFlags** agora conterá os novos bits.</span><span class="sxs-lookup"><span data-stu-id="84583-129">The **dwControlFlags** member will now contain the new bits.</span></span>



| <span data-ttu-id="84583-130">Label</span><span class="sxs-lookup"><span data-stu-id="84583-130">Label</span></span> | <span data-ttu-id="84583-131">Valor</span><span class="sxs-lookup"><span data-stu-id="84583-131">Value</span></span> |
|--------------------------|------------|
| <span data-ttu-id="84583-132">AMCONTROL \_ usado</span><span class="sxs-lookup"><span data-stu-id="84583-132">AMCONTROL\_USED</span></span>          | <span data-ttu-id="84583-133">0x00000001</span><span class="sxs-lookup"><span data-stu-id="84583-133">0x00000001</span></span> |
| <span data-ttu-id="84583-134">AMCONTROL \_ pad \_ para \_ 4x3</span><span class="sxs-lookup"><span data-stu-id="84583-134">AMCONTROL\_PAD\_TO\_4x3</span></span>  | <span data-ttu-id="84583-135">0x00000002</span><span class="sxs-lookup"><span data-stu-id="84583-135">0x00000002</span></span> |
| <span data-ttu-id="84583-136">AMCONTROL \_ pad \_ para \_ 16x9</span><span class="sxs-lookup"><span data-stu-id="84583-136">AMCONTROL\_PAD\_TO\_16x9</span></span> | <span data-ttu-id="84583-137">0x00000004</span><span class="sxs-lookup"><span data-stu-id="84583-137">0x00000004</span></span> |



 

<span data-ttu-id="84583-138">O AMCONTROL \_ usado é usado para testar se há suporte para esses novos sinalizadores.</span><span class="sxs-lookup"><span data-stu-id="84583-138">AMCONTROL\_USED is used to test whether these new flags are supported.</span></span> <span data-ttu-id="84583-139">Um filtro de origem deve definir o \_ sinalizador AMCONTROL usado e ver se o QueryAccept (MediaType) foi bem sucedido no PIN do downstream.</span><span class="sxs-lookup"><span data-stu-id="84583-139">A source filter should set the AMCONTROL\_USED flag and see if QueryAccept(MediaType) succeeds on the downstream pin.</span></span> <span data-ttu-id="84583-140">Se ele for rejeitado, os sinalizadores AMCONTROL não poderão ser usados e dwReserved1 deverá ser definido como 0.</span><span class="sxs-lookup"><span data-stu-id="84583-140">If it is rejected, then the AMCONTROL flags cannot be used and dwReserved1 must be set to 0.</span></span>

<span data-ttu-id="84583-141">AMCONTROL \_ pad \_ para \_ 4x3 indica que a imagem deve ser preenchida e exibida em uma área de 4x3.</span><span class="sxs-lookup"><span data-stu-id="84583-141">AMCONTROL\_PAD\_TO\_4x3 indicates that the image should be padded and displayed in a 4x3 area.</span></span>

<span data-ttu-id="84583-142">AMCONTROL \_ pad \_ para \_ 16x9 indica que a imagem deve ser preenchida e exibida em uma área de 16x9.</span><span class="sxs-lookup"><span data-stu-id="84583-142">AMCONTROL\_PAD\_TO\_16x9 indicates that the image should be padded and displayed in a 16x9 area.</span></span>

<span data-ttu-id="84583-143">O decodificador deve copiar ou processar os bits de forma oculta.</span><span class="sxs-lookup"><span data-stu-id="84583-143">The decoder should either blindly copy or process the bits.</span></span> <span data-ttu-id="84583-144">Se o decodificador executar o formato Letterbox em si, ele deverá alterar a taxa de proporção de pixel, preencher a imagem e remover os bits AMCONTROL correspondentes \_ \* .</span><span class="sxs-lookup"><span data-stu-id="84583-144">If the decoder performs letterboxing itself, then it must alter the pixel aspect ratio, pad the image and remove the corresponding AMCONTROL\_\* bits.</span></span>

<span data-ttu-id="84583-145">O MPEG2VIDEOINFO. dwFlags agora contém três sinalizadores para controlar como o conteúdo deve ser exibido:</span><span class="sxs-lookup"><span data-stu-id="84583-145">The MPEG2VIDEOINFO.dwFlags now contains three flags for controlling for controlling how the content should be displayed:</span></span>

-   <span data-ttu-id="84583-146">`AMMPEG2_DoPanScan (0x00000001)`: Se esse sinalizador for definido, o decodificador de vídeo MPEG-2 deverá cortar a imagem de saída com base nos vetores de digitalização de Pan na extensão de exibição de imagem \_ \_ e alterar a taxa de proporção da imagem para 4x3.</span><span class="sxs-lookup"><span data-stu-id="84583-146">`AMMPEG2_DoPanScan (0x00000001)`: If this flag is set, the MPEG-2 video decoder should crop the output image based on pan-scan vectors in picture\_display\_extension and change the picture aspect ratio to 4x3.</span></span> <span data-ttu-id="84583-147">O VMR não deve receber um exemplo de 16x9 com esse sinalizador.</span><span class="sxs-lookup"><span data-stu-id="84583-147">The VMR should not receive a 16x9 sample with this flag.</span></span> <span data-ttu-id="84583-148">Uma implementação simples pode alterar o retângulo de origem para indicar uma região de origem de 540 largo com uma borda esquerda igual ao deslocamento de exibição na extensão de exibição de imagem \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="84583-148">A simple implementation might alter the source rectangle to indicate a 540 wide source region with a left edge equal to the display offset in the picture\_display\_extension.</span></span>
-   <span data-ttu-id="84583-149">`AMMPEG2_LetterboxAnalogOut (0x00000020)`: Quando um decodificador de hardware exibe esse fluxo para uma saída de vídeo (geralmente um conector SVIDEO no cartão), ele deve aplicar as regras para exibir um exemplo de 16x9 em uma exibição de 4x3.</span><span class="sxs-lookup"><span data-stu-id="84583-149">`AMMPEG2_LetterboxAnalogOut (0x00000020)`: When a hardware decoder displays this stream to a video output (usually an SVIDEO connector on the card), it should apply the rules for displaying a 16x9 sample on a 4x3 display.</span></span>

    <span data-ttu-id="84583-150">Um decodificador de software (ou um decodificador de hardware produzindo saída enviada para o VMR) tem duas opções ao processar imagens:</span><span class="sxs-lookup"><span data-stu-id="84583-150">A software decoder (or a hardware decoder producing output sent to the VMR) has two options when processing images:</span></span>

    1.  <span data-ttu-id="84583-151">Ignore esse sinalizador e passe o conteúdo do VideoInfoHeader2 para o VMR (o AMCONTROL \_ pad \_ para \_ 4x3 Flag já será definido pelo [navegador de DVD](dvd-navigator-filter.md) no exemplo).</span><span class="sxs-lookup"><span data-stu-id="84583-151">Ignore this flag and pass the VideoInfoHeader2 contents to the VMR (the AMCONTROL\_PAD\_TO\_4x3 flag will already be set by the [DVD Navigator](dvd-navigator-filter.md) on the sample).</span></span> <span data-ttu-id="84583-152">O VMR encontrará um exemplo de vídeo 16x9 com o AMCONTROL \_ pad \_ para \_ 4x3 conjunto de sinalizadores e um fluxo de subimagem 4x3.</span><span class="sxs-lookup"><span data-stu-id="84583-152">The VMR will encounter a 16x9 video sample with the AMCONTROL\_PAD\_TO\_4x3 flag set and a 4x3 subpicture stream.</span></span> <span data-ttu-id="84583-153">O aplicativo deve definir os retângulos de destino normalizados dos dois fluxos para ter a mesma largura.</span><span class="sxs-lookup"><span data-stu-id="84583-153">The application must set the output normalized destination rectangles of the two streams to be the same width.</span></span>
    2.  <span data-ttu-id="84583-154">Converta o fluxo Anamorphic em uma imagem 4x3 preenchendo a parte superior e inferior da imagem e definindo a taxa de proporção da imagem como 4x3 (consulte Letterbox acima) e removendo o \_ bloco AMCONTROL \_ para \_ 4x3 bit do VIDEOINFOHEADER2.</span><span class="sxs-lookup"><span data-stu-id="84583-154">Convert the anamorphic stream to a 4x3 image by padding the top and bottom of the image and setting the image aspect ratio to 4x3 (see Letterbox above) and removing the AMCONTROL\_PAD\_TO\_4x3 bit from the VIDEOINFOHEADER2.</span></span>

    <span data-ttu-id="84583-155">Os decodificadores DirectXVA que mesclam os fluxos de vídeo e subimagem terão que processar esse sinalizador.</span><span class="sxs-lookup"><span data-stu-id="84583-155">DirectXVA decoders that blend the video and subpicture streams will have to process this flag.</span></span> <span data-ttu-id="84583-156">Se o hardware não puder dimensionar a subimagem mesclada, o decodificador deverá produzir um fluxo de subimagem separado para o VMR para misturar com o vídeo.</span><span class="sxs-lookup"><span data-stu-id="84583-156">If the hardware cannot scale the blended subpicture, then the decoder should produce a separate subpicture stream for the VMR to blend with the video.</span></span>

-   <span data-ttu-id="84583-157">`AMMPEG2_WidescreenAnalogOut (0x00000200)`: Quando um decodificador de hardware exibe esse fluxo para uma saída de vídeo (geralmente um conector SVIDEO no cartão), ele deve assumir uma exibição de 16x9 (Anamorphic).</span><span class="sxs-lookup"><span data-stu-id="84583-157">`AMMPEG2_WidescreenAnalogOut (0x00000200)`: When a hardware decoder displays this stream to a video output (usually an SVIDEO connector on the card), it should assume a 16x9 (anamorphic) display.</span></span>

    <span data-ttu-id="84583-158">Um decodificador de software (ou um decodificador de hardware produzindo saída enviada para o VMR) tem duas opções ao processar uma imagem Anamorphic:</span><span class="sxs-lookup"><span data-stu-id="84583-158">A software decoder (or a hardware decoder producing output sent to the VMR) has two options when processing an anamorphic image:</span></span>

    1.  <span data-ttu-id="84583-159">Ignore esse sinalizador e copie o conteúdo do VideoInfoHeader2 para o VMR.</span><span class="sxs-lookup"><span data-stu-id="84583-159">Ignore this flag and copy the VideoInfoHeader2 contents to the VMR.</span></span> <span data-ttu-id="84583-160">O VMR irá preencher as imagens de 4x3 para 16x9 se elas tiverem o AMCONTROL \_ pad \_ para \_ 16x9 definido.</span><span class="sxs-lookup"><span data-stu-id="84583-160">The VMR will pad 4x3 images to 16x9 if they have the AMCONTROL\_PAD\_TO\_16x9 set.</span></span>
    2.  <span data-ttu-id="84583-161">Preencha a imagem de saída para uma imagem 16x9 e remova o AMCONTROL \_ pad \_ para \_ 16x9 bit.</span><span class="sxs-lookup"><span data-stu-id="84583-161">Pad the output image to a 16x9 image and remove the AMCONTROL\_PAD\_TO\_16x9 bit.</span></span>

<span data-ttu-id="84583-162">A maioria dos decodificadores deve usar **GetMediaType** para detectar uma alteração de mídia no pino de entrada e copiar o conteúdo de **VIDEOINFOHEADER2** (contido no **MPEG2INFOHEADER**) para o pino de saída.</span><span class="sxs-lookup"><span data-stu-id="84583-162">Most decoders should use **GetMediaType** to detect a media change on the input pin and copy the **VIDEOINFOHEADER2** contents (contained in the **MPEG2INFOHEADER**) to the output pin.</span></span> <span data-ttu-id="84583-163">Provavelmente, eles só processarão o bit PanScan.</span><span class="sxs-lookup"><span data-stu-id="84583-163">They will probably only process the PanScan bit.</span></span>

<span data-ttu-id="84583-164">O código de exemplo a seguir mostra como copiar o conteúdo do **VIDEOINFOHEADER2** de um PIN de entrada para um pino de saída.</span><span class="sxs-lookup"><span data-stu-id="84583-164">The following example code shows how to copy the **VIDEOINFOHEADER2** contents from an input pin to an output pin.</span></span>


```C++
#include <dvdmedia.h>
HRESULT CopyMPeg2ToVideoInfoHeader2(CMediaSample* pInSample, CMediaSample* pOutSample)
{
    HRESULT hr = S_OK;
    // Check for a media type on the input sample.
    AM_MEDIA_TYPE* pInType;
    if (pInSample->GetMediaType(&pInType) == S_OK) 
    {
        // Make sure it's an MPEG2 Video format.
        if ((pInType->formattype == FORMAT_MPEG2_VIDEO) &&
            (pInType->cbFormat >= sizeof(MPEG2VIDEOINFO)))
        {
            hr = S_OK; // Initialize hr for the CMediaType constructor.
            CMediaType outType(*pInType, &hr);
            if (FAILED(hr))
            {
                DeleteMediaType( pInType );
                return hr;
            }

            // Set the format type GUID.
            outType.SetFormatType(&FORMAT_VideoInfo2);
                
            // Truncate the format block to include just the VIDEOINFOHEADER part.
            MPEG2VIDEOINFO *pMPeg2Header = (MPEG2VIDEOINFO*)pInType->pbFormat;
            BYTE *pVIH = (BYTE*)&pMPeg2Header->hdr;
            hr = (outType.SetFormat(pVIH, sizeof(VIDEOINFOHEADER2)) ? S_OK : E_OUTOFMEMORY);
            if (SUCCEEDED(hr))
            {
                hr = pOutSample->SetMediaType(&outType);
            }
        } 
        else 
        {
            ASSERT(FALSE); // Not a MPEG2 header.
            hr = VFW_E_INVALIDMEDIATYPE;
        }
        DeleteMediaType( pInType );
    } 

    return hr;
}
```



 

 



