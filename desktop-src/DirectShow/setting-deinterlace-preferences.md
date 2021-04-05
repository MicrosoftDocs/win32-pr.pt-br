---
description: Definindo preferências de desentrelaçamento
ms.assetid: 31d59f17-552b-46d1-89e4-751216f54280
title: Definindo preferências de desentrelaçamento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be52ae3023c8e4bc83c3305a104c389f423cffd6
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103645626"
---
# <a name="setting-deinterlace-preferences"></a><span data-ttu-id="77fbc-103">Definindo preferências de desentrelaçamento</span><span class="sxs-lookup"><span data-stu-id="77fbc-103">Setting Deinterlace Preferences</span></span>

<span data-ttu-id="77fbc-104">O VMR (Video mixagem Renderer) dá suporte ao desentrelaçamento acelerado por hardware, o que melhora a qualidade de renderização para vídeo entrelaçado.</span><span class="sxs-lookup"><span data-stu-id="77fbc-104">The Video Mixing Renderer (VMR) supports hardware-accelerated deinterlacing, which improves rendering quality for interlaced video.</span></span> <span data-ttu-id="77fbc-105">Os recursos exatos que estão disponíveis dependem do hardware subjacente.</span><span class="sxs-lookup"><span data-stu-id="77fbc-105">The exact features that are available depend on the underlying hardware.</span></span> <span data-ttu-id="77fbc-106">O aplicativo pode consultar os recursos de desentrelaçamento de hardware e definir as preferências de desentrelaçamento por meio da interface [**IVMRDeinterlaceControl**](/windows/desktop/api/Strmif/nn-strmif-ivmrdeinterlacecontrol) (VMR-7) ou da interface [**IVMRDeinterlaceControl9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrdeinterlacecontrol9) (VMR-9).</span><span class="sxs-lookup"><span data-stu-id="77fbc-106">The application can query for the hardware deinterlacing capabilities and set deinterlacing preferences through the [**IVMRDeinterlaceControl**](/windows/desktop/api/Strmif/nn-strmif-ivmrdeinterlacecontrol) interface (VMR-7) or [**IVMRDeinterlaceControl9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrdeinterlacecontrol9) interface (VMR-9).</span></span> <span data-ttu-id="77fbc-107">O desentrelaçamento é realizado em uma base por fluxo.</span><span class="sxs-lookup"><span data-stu-id="77fbc-107">Deinterlacing is performed on a per-stream basis.</span></span>

<span data-ttu-id="77fbc-108">Há uma diferença importante no comportamento de entrelaçamento entre o VMR-7 e o VMR-9.</span><span class="sxs-lookup"><span data-stu-id="77fbc-108">There is one important difference in interlacing behavior between the VMR-7 and the VMR-9.</span></span> <span data-ttu-id="77fbc-109">Em sistemas em que o hardware de gráficos não dá suporte ao Desentrelaçamento avançado, o VMR-7 pode retornar à sobreposição de hardware e instruí-lo a usar um desentrelaçamento de estilo BOB.</span><span class="sxs-lookup"><span data-stu-id="77fbc-109">On systems where the graphics hardware doesn't support advanced deinterlacing, the VMR-7 can fall back to the hardware overlay and instruct it to use a BOB style deinterlace.</span></span> <span data-ttu-id="77fbc-110">Nesse caso, embora o VMR esteja relatando 30fps, o vídeo está realmente sendo renderizado em 60 invertidos por segundo.</span><span class="sxs-lookup"><span data-stu-id="77fbc-110">In this case, although the VMR is reporting 30fps the video is actually being rendered at 60 flips per second.</span></span>

<span data-ttu-id="77fbc-111">Exceto no caso do VMR-7 usando a sobreposição de hardware, o desentrelaçamento é executado pelo mixer do VMR.</span><span class="sxs-lookup"><span data-stu-id="77fbc-111">Except in the case of the VMR-7 using hardware overlay, deinterlacing is performed by the VMR's mixer.</span></span> <span data-ttu-id="77fbc-112">O mixer usa a DDI (interface de driver de dispositivo) de desentrelaçamento do DirectX Video Acceleration (DXVA) para executar o desentrelaçamento.</span><span class="sxs-lookup"><span data-stu-id="77fbc-112">The mixer uses the DirectX Video Acceleration (DXVA) deinterlacing device driver interface (DDI) to perform the deinterlacing.</span></span> <span data-ttu-id="77fbc-113">Essa DDI não pode ser chamada por aplicativos e os aplicativos não podem substituir a funcionalidade de desentrelaçamento do VMR.</span><span class="sxs-lookup"><span data-stu-id="77fbc-113">This DDI is not callable by applications, and applications cannot replace the VMR's deinterlacing functionality.</span></span> <span data-ttu-id="77fbc-114">No entanto, um aplicativo pode selecionar o modo de desentrelaçamento desejado, conforme descrito nesta seção.</span><span class="sxs-lookup"><span data-stu-id="77fbc-114">However, an application can select the desired deinterlacing mode, as described in this section.</span></span>

> [!Note]  
> <span data-ttu-id="77fbc-115">Esta seção descreve os métodos **IVMRDeinterlaceControl9** , mas as versões do VMR-7 são quase idênticas.</span><span class="sxs-lookup"><span data-stu-id="77fbc-115">This section describes the **IVMRDeinterlaceControl9** methods, but the VMR-7 versions are almost identical.</span></span>

 

<span data-ttu-id="77fbc-116">Para obter os recursos de desentrelaçamento de um fluxo de vídeo, faça o seguinte:</span><span class="sxs-lookup"><span data-stu-id="77fbc-116">To get the deinterlacing capabilities for a video stream, do the following:</span></span>

1.  <span data-ttu-id="77fbc-117">Preencha uma estrutura [**VMR9VideoDesc**](/previous-versions/windows/desktop/api/Vmr9/ns-vmr9-vmr9videodesc) com uma descrição do fluxo de vídeo.</span><span class="sxs-lookup"><span data-stu-id="77fbc-117">Fill in a [**VMR9VideoDesc**](/previous-versions/windows/desktop/api/Vmr9/ns-vmr9-vmr9videodesc) structure with a description of the video stream.</span></span> <span data-ttu-id="77fbc-118">Detalhes de como preencher essa estrutura são fornecidos posteriormente.</span><span class="sxs-lookup"><span data-stu-id="77fbc-118">Details of how to fill in this structure are given later.</span></span>
2.  <span data-ttu-id="77fbc-119">Passe a estrutura para o método [**IVMRDeinterlaceControl9:: GetNumberOfDeinterlaceModes**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrdeinterlacecontrol9-getnumberofdeinterlacemodes) .</span><span class="sxs-lookup"><span data-stu-id="77fbc-119">Pass the structure to the [**IVMRDeinterlaceControl9::GetNumberOfDeinterlaceModes**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrdeinterlacecontrol9-getnumberofdeinterlacemodes) method.</span></span> <span data-ttu-id="77fbc-120">Chame o método duas vezes.</span><span class="sxs-lookup"><span data-stu-id="77fbc-120">Call the method twice.</span></span> <span data-ttu-id="77fbc-121">A primeira chamada retorna o número de modos de desentrelaçamento que o hardware suporta para o formato especificado.</span><span class="sxs-lookup"><span data-stu-id="77fbc-121">The first call returns the number of deinterlace modes the hardware supports for the specified format.</span></span> <span data-ttu-id="77fbc-122">Aloque uma matriz de GUIDs desse tamanho e chame o método novamente, passando o endereço da matriz.</span><span class="sxs-lookup"><span data-stu-id="77fbc-122">Allocate an array of GUIDs of this size, and call the method again, passing in the address of the array.</span></span> <span data-ttu-id="77fbc-123">A segunda chamada preenche a matriz com GUIDs.</span><span class="sxs-lookup"><span data-stu-id="77fbc-123">The second call fills the array with GUIDs.</span></span> <span data-ttu-id="77fbc-124">Cada GUID identifica um modo de desentrelaçamento.</span><span class="sxs-lookup"><span data-stu-id="77fbc-124">Each GUID identifies one deinterlacing mode.</span></span>
3.  <span data-ttu-id="77fbc-125">Para obter o recursos de um modo específico, chame o método [**IVMRDeinterlaceControl9:: GetDeinterlaceModeCaps**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrdeinterlacecontrol9-getdeinterlacemodecaps) .</span><span class="sxs-lookup"><span data-stu-id="77fbc-125">To get the capabiltiies of a particular mode, call the [**IVMRDeinterlaceControl9::GetDeinterlaceModeCaps**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrdeinterlacecontrol9-getdeinterlacemodecaps) method.</span></span> <span data-ttu-id="77fbc-126">Passe a mesma estrutura **VMR9VideoDesc** , junto com um dos GUIDs da matriz.</span><span class="sxs-lookup"><span data-stu-id="77fbc-126">Pass in the same **VMR9VideoDesc** structure, along with one of the GUIDs from the array.</span></span> <span data-ttu-id="77fbc-127">O método preenche uma estrutura [**VMR9DeinterlaceCaps**](/previous-versions/windows/desktop/api/Vmr9/ns-vmr9-vmr9deinterlacecaps) com os recursos do modo.</span><span class="sxs-lookup"><span data-stu-id="77fbc-127">The method fills a [**VMR9DeinterlaceCaps**](/previous-versions/windows/desktop/api/Vmr9/ns-vmr9-vmr9deinterlacecaps) structure with the mode capabilities.</span></span>

<span data-ttu-id="77fbc-128">O código a seguir mostra estas etapas:</span><span class="sxs-lookup"><span data-stu-id="77fbc-128">The following code shows these steps:</span></span>


```C++
VMR9VideoDesc VideoDesc; 
DWORD dwNumModes = 0;
// Fill in the VideoDesc structure (not shown).
hr = pDeinterlace->GetNumberOfDeinterlaceModes(&VideoDesc, 
    &dwNumModes, NULL);
if (SUCCEEDED(hr) && (dwNumModes != 0))
{
    // Allocate an array for the GUIDs that identify the modes.
    GUID *pModes = new GUID[dwNumModes];
    if (pModes)
    {
        // Fill the array.
        hr = pDeinterlace->GetNumberOfDeinterlaceModes(&VideoDesc, 
            &dwNumModes, pModes);
        if (SUCCEEDED(hr))
        {
            // Loop through each item and get the capabilities.
            for (int i = 0; i < dwNumModes; i++)
            {
                VMR9DeinterlaceCaps Caps;
                hr = pDeinterlace->GetDeinterlaceModeCaps(pModes + i, 
                    &VideoDesc, &Caps);
                if (SUCCEEDED(hr))
                {
                    // Examine the Caps structure.
                }
            }
        }
        delete [] pModes;
    }
}
```



<span data-ttu-id="77fbc-129">Agora o aplicativo pode definir o modo de desentrelaçamento para o fluxo, usando os seguintes métodos:</span><span class="sxs-lookup"><span data-stu-id="77fbc-129">Now the application can set the deinterlacing mode for the stream, using the following methods:</span></span>

-   <span data-ttu-id="77fbc-130">O método [**SetDeinterlaceMode**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrdeinterlacecontrol9-setdeinterlacemode) define o modo preferencial.</span><span class="sxs-lookup"><span data-stu-id="77fbc-130">The [**SetDeinterlaceMode**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrdeinterlacecontrol9-setdeinterlacemode) method sets the preferred mode.</span></span> <span data-ttu-id="77fbc-131">Use o GUID \_ NULL para desligar o desentrelaçamento.</span><span class="sxs-lookup"><span data-stu-id="77fbc-131">Use GUID\_NULL to turn off deinterlacing.</span></span>
-   <span data-ttu-id="77fbc-132">O método [**SetDeinterlacePrefs**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrdeinterlacecontrol9-setdeinterlaceprefs) especifica o comportamento se o modo solicitado não estiver disponível.</span><span class="sxs-lookup"><span data-stu-id="77fbc-132">The [**SetDeinterlacePrefs**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrdeinterlacecontrol9-setdeinterlaceprefs) method specifies the behavior if the requested mode is not available.</span></span>
-   <span data-ttu-id="77fbc-133">O método [**GetDeinterlaceMode**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrdeinterlacecontrol9-getdeinterlacemode) retorna o modo preferencial que você definiu.</span><span class="sxs-lookup"><span data-stu-id="77fbc-133">The [**GetDeinterlaceMode**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrdeinterlacecontrol9-getdeinterlacemode) method returns the preferred mode that you set.</span></span>
-   <span data-ttu-id="77fbc-134">O método [**GetActualDeinterlaceMode**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrdeinterlacecontrol9-getactualdeinterlacemode) retorna o modo real em uso, que pode ser um modo de fallback, se o modo preferencial não estiver disponível.</span><span class="sxs-lookup"><span data-stu-id="77fbc-134">The [**GetActualDeinterlaceMode**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrdeinterlacecontrol9-getactualdeinterlacemode) method returns the actual mode in use, which might be a fallback mode, if the preferred mode is not available.</span></span>

<span data-ttu-id="77fbc-135">As páginas de referência do método fornecem mais informações.</span><span class="sxs-lookup"><span data-stu-id="77fbc-135">The method reference pages give more information.</span></span>

<span data-ttu-id="77fbc-136">**Usando a estrutura VMR9VideoDesc**</span><span class="sxs-lookup"><span data-stu-id="77fbc-136">**Using the VMR9VideoDesc Structure**</span></span>

<span data-ttu-id="77fbc-137">No procedimento fornecido anteriormente, a primeira etapa é preencher uma estrutura **VMR9VideoDesc** com uma descrição do fluxo de vídeo.</span><span class="sxs-lookup"><span data-stu-id="77fbc-137">In the procedure given previously, the first step is to fill in a **VMR9VideoDesc** structure with a description of the video stream.</span></span> <span data-ttu-id="77fbc-138">Comece obtendo o tipo de mídia do fluxo de vídeo.</span><span class="sxs-lookup"><span data-stu-id="77fbc-138">Start by getting the media type of the video stream.</span></span> <span data-ttu-id="77fbc-139">Você pode fazer isso chamando [**IPin:: ConnectionMediaType**](/windows/desktop/api/Strmif/nf-strmif-ipin-connectionmediatype) no pino de entrada do filtro do VMR.</span><span class="sxs-lookup"><span data-stu-id="77fbc-139">You can do this by calling [**IPin::ConnectionMediaType**](/windows/desktop/api/Strmif/nf-strmif-ipin-connectionmediatype) on the VMR filter's input pin.</span></span> <span data-ttu-id="77fbc-140">Em seguida, confirme se o fluxo de vídeo está entrelaçado.</span><span class="sxs-lookup"><span data-stu-id="77fbc-140">Then confirm whether the video stream is interlaced.</span></span> <span data-ttu-id="77fbc-141">Somente os formatos [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) podem ser entrelaçados.</span><span class="sxs-lookup"><span data-stu-id="77fbc-141">Only [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) formats can be interlaced.</span></span> <span data-ttu-id="77fbc-142">Se o tipo de formato for FORMAT \_ VIDEOINFO, ele deverá ser um quadro progressivo.</span><span class="sxs-lookup"><span data-stu-id="77fbc-142">If the format type is FORMAT\_VideoInfo, it must be a progressive frame.</span></span> <span data-ttu-id="77fbc-143">Se o tipo de formato for FORMAT \_ VideoInfo2, verifique o campo **dwInterlaceFlags** do \_ sinalizador isentrelaçated AMINTERLACE.</span><span class="sxs-lookup"><span data-stu-id="77fbc-143">If the format type is FORMAT\_VideoInfo2, check the **dwInterlaceFlags** field for the AMINTERLACE\_IsInterlaced flag.</span></span> <span data-ttu-id="77fbc-144">A presença desse sinalizador indica que o vídeo está entrelaçado.</span><span class="sxs-lookup"><span data-stu-id="77fbc-144">The presence of this flag indicates the video is interlaced.</span></span>

<span data-ttu-id="77fbc-145">Suponha que a variável **pBMI** seja um ponteiro para a estrutura [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) no bloco de formato.</span><span class="sxs-lookup"><span data-stu-id="77fbc-145">Assume that the variable **pBMI** is a pointer to the [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) structure in the format block.</span></span> <span data-ttu-id="77fbc-146">Defina os seguintes valores na estrutura **VMR9VideoDesc** :</span><span class="sxs-lookup"><span data-stu-id="77fbc-146">Set the following values in the **VMR9VideoDesc** structure:</span></span>

-   <span data-ttu-id="77fbc-147">**dwSize**: defina esse campo como `sizeof(VMR9VideoDesc)` .</span><span class="sxs-lookup"><span data-stu-id="77fbc-147">**dwSize**: Set this field to `sizeof(VMR9VideoDesc)`.</span></span>
-   <span data-ttu-id="77fbc-148">**dwSampleWidth**: defina esse campo como `pBMI->biWidth` .</span><span class="sxs-lookup"><span data-stu-id="77fbc-148">**dwSampleWidth**: Set this field to `pBMI->biWidth`.</span></span>
-   <span data-ttu-id="77fbc-149">**dwSampleHeight**: defina esse campo como `abs(pBMI->biHeight)` .</span><span class="sxs-lookup"><span data-stu-id="77fbc-149">**dwSampleHeight**: Set this field to `abs(pBMI->biHeight)`.</span></span>
-   <span data-ttu-id="77fbc-150">**SampleFormat**: Este campo descreve as características de entrelaçamento do tipo de mídia.</span><span class="sxs-lookup"><span data-stu-id="77fbc-150">**SampleFormat**: This field describes the interlace characteristics of the media type.</span></span> <span data-ttu-id="77fbc-151">Verifique o campo **dwInterlaceFlags** na estrutura **VIDEOINFOHEADER2** e defina **SampleFormat** igual ao sinalizador equivalente [**VMR9 \_ SampleFormat**](/previous-versions/windows/desktop/api/Vmr9/ne-vmr9-vmr9_sampleformat) .</span><span class="sxs-lookup"><span data-stu-id="77fbc-151">Check the **dwInterlaceFlags** field in the **VIDEOINFOHEADER2** structure, and set **SampleFormat** equal to the equivalent [**VMR9\_SampleFormat**](/previous-versions/windows/desktop/api/Vmr9/ne-vmr9-vmr9_sampleformat) flag.</span></span> <span data-ttu-id="77fbc-152">Uma função auxiliar para fazer isso é fornecida abaixo.</span><span class="sxs-lookup"><span data-stu-id="77fbc-152">A helper function to do this is given below.</span></span>
-   <span data-ttu-id="77fbc-153">**InputSampleFreq**: esse campo fornece a frequência de entrada, que pode ser calculada a partir do campo **AvgTimePerFrame** na estrutura **VIDEOINFOHEADER2** .</span><span class="sxs-lookup"><span data-stu-id="77fbc-153">**InputSampleFreq**: This field gives the input frequency, which can be calculated from the **AvgTimePerFrame** field in the **VIDEOINFOHEADER2** structure.</span></span> <span data-ttu-id="77fbc-154">No caso geral, defina **dwNumerator** como 10 milhões e defina **dwDenominator** como **AvgTimePerFrame**.</span><span class="sxs-lookup"><span data-stu-id="77fbc-154">In the general case, set **dwNumerator** to 10000000, and set **dwDenominator** to **AvgTimePerFrame**.</span></span> <span data-ttu-id="77fbc-155">No entanto, você também pode verificar se há algumas taxas de quadros bem conhecidas:</span><span class="sxs-lookup"><span data-stu-id="77fbc-155">However, you can also check for some well-known frame rates:</span></span>

    | <span data-ttu-id="77fbc-156">Tempo médio por quadro</span><span class="sxs-lookup"><span data-stu-id="77fbc-156">Average time per frame</span></span> | <span data-ttu-id="77fbc-157">Taxa de quadros (FPS)</span><span class="sxs-lookup"><span data-stu-id="77fbc-157">Frame rate (fps)</span></span> | <span data-ttu-id="77fbc-158">Numera</span><span class="sxs-lookup"><span data-stu-id="77fbc-158">Numerator</span></span> | <span data-ttu-id="77fbc-159">Denominador</span><span class="sxs-lookup"><span data-stu-id="77fbc-159">Denominator</span></span> |
    |------------------------|------------------|-----------|-------------|
    | <span data-ttu-id="77fbc-160">166833</span><span class="sxs-lookup"><span data-stu-id="77fbc-160">166833</span></span>                 | <span data-ttu-id="77fbc-161">59,94 (NTSC)</span><span class="sxs-lookup"><span data-stu-id="77fbc-161">59.94 (NTSC)</span></span>     | <span data-ttu-id="77fbc-162">60000</span><span class="sxs-lookup"><span data-stu-id="77fbc-162">60000</span></span>     | <span data-ttu-id="77fbc-163">1001</span><span class="sxs-lookup"><span data-stu-id="77fbc-163">1001</span></span>        |
    | <span data-ttu-id="77fbc-164">333667</span><span class="sxs-lookup"><span data-stu-id="77fbc-164">333667</span></span>                 | <span data-ttu-id="77fbc-165">29,97 (NTSC)</span><span class="sxs-lookup"><span data-stu-id="77fbc-165">29.97 (NTSC)</span></span>     | <span data-ttu-id="77fbc-166">30000</span><span class="sxs-lookup"><span data-stu-id="77fbc-166">30000</span></span>     | <span data-ttu-id="77fbc-167">1001</span><span class="sxs-lookup"><span data-stu-id="77fbc-167">1001</span></span>        |
    | <span data-ttu-id="77fbc-168">417188</span><span class="sxs-lookup"><span data-stu-id="77fbc-168">417188</span></span>                 | <span data-ttu-id="77fbc-169">23,97 (NTSC)</span><span class="sxs-lookup"><span data-stu-id="77fbc-169">23.97 (NTSC)</span></span>     | <span data-ttu-id="77fbc-170">24.000</span><span class="sxs-lookup"><span data-stu-id="77fbc-170">24000</span></span>     | <span data-ttu-id="77fbc-171">1001</span><span class="sxs-lookup"><span data-stu-id="77fbc-171">1001</span></span>        |
    | <span data-ttu-id="77fbc-172">200000</span><span class="sxs-lookup"><span data-stu-id="77fbc-172">200000</span></span>                 | <span data-ttu-id="77fbc-173">50, 0 (PAL)</span><span class="sxs-lookup"><span data-stu-id="77fbc-173">50.00 (PAL)</span></span>      | <span data-ttu-id="77fbc-174">50</span><span class="sxs-lookup"><span data-stu-id="77fbc-174">50</span></span>        | <span data-ttu-id="77fbc-175">1</span><span class="sxs-lookup"><span data-stu-id="77fbc-175">1</span></span>           |
    | <span data-ttu-id="77fbc-176">400000</span><span class="sxs-lookup"><span data-stu-id="77fbc-176">400000</span></span>                 | <span data-ttu-id="77fbc-177">25, 0 (PAL)</span><span class="sxs-lookup"><span data-stu-id="77fbc-177">25.00 (PAL)</span></span>      | <span data-ttu-id="77fbc-178">25</span><span class="sxs-lookup"><span data-stu-id="77fbc-178">25</span></span>        | <span data-ttu-id="77fbc-179">1</span><span class="sxs-lookup"><span data-stu-id="77fbc-179">1</span></span>           |
    | <span data-ttu-id="77fbc-180">416667</span><span class="sxs-lookup"><span data-stu-id="77fbc-180">416667</span></span>                 | <span data-ttu-id="77fbc-181">24, 0 (filme)</span><span class="sxs-lookup"><span data-stu-id="77fbc-181">24.00 (Film)</span></span>     | <span data-ttu-id="77fbc-182">24</span><span class="sxs-lookup"><span data-stu-id="77fbc-182">24</span></span>        | <span data-ttu-id="77fbc-183">1</span><span class="sxs-lookup"><span data-stu-id="77fbc-183">1</span></span>           |

    

     

-   <span data-ttu-id="77fbc-184">**OutputFrameFreq**: esse campo fornece a frequência de saída, que pode ser calculada com base no valor de **InputSampleFreq** e nas características de intercalação do fluxo de entrada:</span><span class="sxs-lookup"><span data-stu-id="77fbc-184">**OutputFrameFreq**: This field gives the output frequency, which can be calculated from the **InputSampleFreq** value and the interleaving characteristics of the input stream:</span></span>
    -   <span data-ttu-id="77fbc-185">Defina **OutputFrameFreq. dwDenominator** igual a **InputSampleFreq. dwDenominator**.</span><span class="sxs-lookup"><span data-stu-id="77fbc-185">Set **OutputFrameFreq.dwDenominator** equal to **InputSampleFreq.dwDenominator**.</span></span>
    -   <span data-ttu-id="77fbc-186">Se o vídeo de entrada for intercalado, defina **OutputFrameFreq. dwNumerator** como 2 x **InputSampleFreq. dwNumerator**.</span><span class="sxs-lookup"><span data-stu-id="77fbc-186">If the input video is interleaved, set **OutputFrameFreq.dwNumerator** to 2 x **InputSampleFreq.dwNumerator**.</span></span> <span data-ttu-id="77fbc-187">(Após desentrelaçar, a taxa de quadros é duplicada.) Caso contrário, defina o valor como **InputSampleFreq. dwNumerator**.</span><span class="sxs-lookup"><span data-stu-id="77fbc-187">(After deinterlacing, the frame rate is doubled.) Otherwise, set the value to **InputSampleFreq.dwNumerator**.</span></span>
-   <span data-ttu-id="77fbc-188">**dwFourCC**: defina esse campo como `pBMI->biCompression` .</span><span class="sxs-lookup"><span data-stu-id="77fbc-188">**dwFourCC**: Set this field to `pBMI->biCompression`.</span></span>

<span data-ttu-id="77fbc-189">A função auxiliar a seguir converte os sinalizadores AMINTERLACE \_ *X* em valores [**\_ SampleFormat VMR9**](/previous-versions/windows/desktop/api/Vmr9/ne-vmr9-vmr9_sampleformat) :</span><span class="sxs-lookup"><span data-stu-id="77fbc-189">The following helper function converts AMINTERLACE\_*X* flags to [**VMR9\_SampleFormat**](/previous-versions/windows/desktop/api/Vmr9/ne-vmr9-vmr9_sampleformat) values:</span></span>


```C++
#define IsInterlaced(x) ((x) & AMINTERLACE_IsInterlaced)
#define IsSingleField(x) ((x) & AMINTERLACE_1FieldPerSample)
#define IsField1First(x) ((x) & AMINTERLACE_Field1First)

VMR9_SampleFormat ConvertInterlaceFlags(DWORD dwInterlaceFlags)
{
    if (IsInterlaced(dwInterlaceFlags)) {
        if (IsSingleField(dwInterlaceFlags)) {
            if (IsField1First(dwInterlaceFlags)) {
                return VMR9_SampleFieldSingleEven;
            }
            else {
                return VMR9_SampleFieldSingleOdd;
            }
        }
        else {
            if (IsField1First(dwInterlaceFlags)) {
                return VMR9_SampleFieldInterleavedEvenFirst;
             }
            else {
                return VMR9_SampleFieldInterleavedOddFirst;
            }
        }
    }
    else {
        return VMR9_SampleProgressiveFrame;  // Not interlaced.
    }
}
```



 

 



