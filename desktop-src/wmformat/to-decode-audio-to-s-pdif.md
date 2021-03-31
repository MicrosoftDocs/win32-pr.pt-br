---
title: Para decodificar áudio para S/PDIF
description: Para decodificar áudio para S/PDIF
ms.assetid: b56c2d0a-a7c6-44f8-832a-bbbe7ae053e6
keywords:
- SDK do Windows Media Format, decodificando áudio para S/PDIF
- SDK do Windows Media Format, formato de interconexão digital Sony/Philips (S/PDIF)
- Formato de sistema avançado (ASF), decodificando áudio para S/PDIF
- ASF (formato de sistemas avançados), decodificando áudio para S/PDIF
- Formato de sistema avançado (ASF), formato de interconexão digital Sony/Philips (S/PDIF)
- ASF (formato de sistemas avançados), formato de interconexão digital Sony/Philips (S/PDIF)
- Formato de interconexão digital Sony/Philips (S/PDIF), decodificando áudio
- S/PDIF (formato de interconexão digital Sony/Philips), decodificando áudio
- decodificando áudio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33fa063baa8e9a88c2fb7a4d9c67375965282167
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/25/2020
ms.locfileid: "103640299"
---
# <a name="to-decode-audio-to-spdif"></a><span data-ttu-id="3c148-112">Para decodificar áudio para S/PDIF</span><span class="sxs-lookup"><span data-stu-id="3c148-112">To Decode Audio to S/PDIF</span></span>

<span data-ttu-id="3c148-113">O áudio codificado com o codec Windows Media Audio 9 Professional pode ser decodificado para o S/PDIF (formato de interconexão digital) da Sony/Philips.</span><span class="sxs-lookup"><span data-stu-id="3c148-113">Audio encoded with the Windows Media Audio 9 Professional codec can be decoded to Sony/Philips Digital Interconnect Format (S/PDIF).</span></span> <span data-ttu-id="3c148-114">Para gerar a saída de S/PDIF, execute as seguintes etapas:</span><span class="sxs-lookup"><span data-stu-id="3c148-114">To generate S/PDIF output, perform the following steps:</span></span>

1.  <span data-ttu-id="3c148-115">Abra um arquivo que contenha um fluxo do Windows Media Audio 9 Professional chamando o método [**IWMReader:: Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-open) .</span><span class="sxs-lookup"><span data-stu-id="3c148-115">Open a file that contains a Windows Media Audio 9 Professional stream by calling the [**IWMReader::Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-open) method.</span></span>
2.  <span data-ttu-id="3c148-116">Identifique o número de saída do fluxo desejado.</span><span class="sxs-lookup"><span data-stu-id="3c148-116">Identify the output number of the stream that you want.</span></span> <span data-ttu-id="3c148-117">Para obter mais informações, consulte [para identificar números de saída](to-identify-output-numbers.md).</span><span class="sxs-lookup"><span data-stu-id="3c148-117">For more information, see [To Identify Output Numbers](to-identify-output-numbers.md).</span></span>
3.  <span data-ttu-id="3c148-118">Chame o método [**IWMReaderAdvanced2:: SetOutputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setoutputsetting) para configurar a saída de S/PDIF.</span><span class="sxs-lookup"><span data-stu-id="3c148-118">Call the [**IWMReaderAdvanced2::SetOutputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setoutputsetting) method to configure S/PDIF output.</span></span> <span data-ttu-id="3c148-119">Use g \_ wszEnableWMAProSPDIFOutput para o nome da configuração.</span><span class="sxs-lookup"><span data-stu-id="3c148-119">Use g\_wszEnableWMAProSPDIFOutput for the setting name.</span></span> <span data-ttu-id="3c148-120">O tipo de dados é **WMT \_ tipo \_ bool**; defina o valor como **true** para habilitar a saída S/PDIF.</span><span class="sxs-lookup"><span data-stu-id="3c148-120">The data type is **WMT\_TYPE\_BOOL**; set the value to **TRUE** to enable S/PDIF output.</span></span>
4.  <span data-ttu-id="3c148-121">Obtenha a interface de propriedades de saída ([**IWMOutputMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmoutputmediaprops)) do formato de saída desejado chamando o método [**IWMReader:: GetOutputFormat**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-getoutputformat) .</span><span class="sxs-lookup"><span data-stu-id="3c148-121">Get the output properties interface ([**IWMOutputMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmoutputmediaprops)) of the desired output format by calling the [**IWMReader::GetOutputFormat**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-getoutputformat) method.</span></span> <span data-ttu-id="3c148-122">Para obter mais informações sobre como enumerar formatos de saída, consulte [atribuindo formatos de saída](assigning-output-formats.md).</span><span class="sxs-lookup"><span data-stu-id="3c148-122">For more information about enumerating output formats, see [Assigning Output Formats](assigning-output-formats.md).</span></span>
5.  <span data-ttu-id="3c148-123">Defina o formato de saída chamando o método [**IWMReader:: SetOutputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-setoutputprops) .</span><span class="sxs-lookup"><span data-stu-id="3c148-123">Set the output format by calling the [**IWMReader::SetOutputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-setoutputprops) method.</span></span> <span data-ttu-id="3c148-124">Passe um ponteiro para a interface **IWMOutputMediaProps** obtida na etapa 4.</span><span class="sxs-lookup"><span data-stu-id="3c148-124">Pass in a pointer to the **IWMOutputMediaProps** interface obtained in step 4.</span></span>
6.  <span data-ttu-id="3c148-125">Faça outras alterações de configuração e comece a reprodução.</span><span class="sxs-lookup"><span data-stu-id="3c148-125">Make any other configuration changes and begin playback.</span></span>

> [!Note]  
> <span data-ttu-id="3c148-126">Você pode executar as etapas anteriores no leitor síncrono usando os métodos correspondentes da interface [**IWMSyncReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader) .</span><span class="sxs-lookup"><span data-stu-id="3c148-126">You can perform the preceding steps on the synchronous reader by using the corresponding methods of the [**IWMSyncReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader) interface.</span></span>

 

<span data-ttu-id="3c148-127">O código de exemplo a seguir demonstra como definir um fluxo de áudio para saída de áudio como dados S/PDIF.</span><span class="sxs-lookup"><span data-stu-id="3c148-127">The following example code demonstrates how to set an audio stream to output audio as S/PDIF data.</span></span> <span data-ttu-id="3c148-128">Essa função pressupõe que um arquivo já foi carregado no leitor e que o número de saída foi identificado.</span><span class="sxs-lookup"><span data-stu-id="3c148-128">This function assumes that a file has already been loaded in the reader and that the output number has been identified.</span></span> <span data-ttu-id="3c148-129">Para obter mais informações sobre como usar esse código, consulte [usando os exemplos de código](using-the-code-examples.md).</span><span class="sxs-lookup"><span data-stu-id="3c148-129">For more information about using this code, see [Using the Code Examples](using-the-code-examples.md).</span></span>


```C++
HRESULT SetSPDIF(DWORD dwOutputNum, IWMReader* pReader)
{
    HRESULT hr = S_OK;

    IWMReaderAdvanced2*  pReaderAdv   = NULL;
    IWMOutputMediaProps* pOutputProps = NULL; 

    BOOL fValue = TRUE;

    // Get the advanced reader interface.
    hr = pReader->QueryInterface(IID_IWMReaderAdvanced2,
                                 (void**)&pReaderAdv);
    GOTO_EXIT_IF_FAILED(hr);

    // Set S/PDIF output.
    hr = pReaderAdv->SetOutputSetting(dwOutputNum, 
                                      g_wszEnableWMAProSPDIFOutput, 
                                      WMT_TYPE_BOOL, 
                                      (BYTE*)&fValue, 
                                      sizeof(BOOL));
    GOTO_EXIT_IF_FAILED(hr);

    // Get the first output format for the stream.
    // NOTE: You could also enumerate the available output formats
    // and pick one to use.

    hr = pReader->GetOutputFormat(dwOutputNum, 0, &pOutputProps);
    GOTO_EXIT_IF_FAILED(hr);

    // Set the output properties back on the reader.
    hr = pReader->SetOutputProps(dwOutputNum, pOutputProps);

Exit:
    SAFE_RELEASE(pReaderAdv);
    SAFE_RELEASE(pOutputProps);

    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="3c148-130">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="3c148-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3c148-131">**Tópicos avançados**</span><span class="sxs-lookup"><span data-stu-id="3c148-131">**Advanced Topics**</span></span>](advanced-topics.md)
</dt> <dt>

[<span data-ttu-id="3c148-132">**Lendo arquivos ASF**</span><span class="sxs-lookup"><span data-stu-id="3c148-132">**Reading ASF Files**</span></span>](reading-asf-files.md)
</dt> <dt>

[<span data-ttu-id="3c148-133">**Interface IWMReader**</span><span class="sxs-lookup"><span data-stu-id="3c148-133">**IWMReader Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreader)
</dt> <dt>

[<span data-ttu-id="3c148-134">**Interface IWMReaderAdvanced2**</span><span class="sxs-lookup"><span data-stu-id="3c148-134">**IWMReaderAdvanced2 Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2)
</dt> <dt>

[<span data-ttu-id="3c148-135">**Interface IWMSyncReader**</span><span class="sxs-lookup"><span data-stu-id="3c148-135">**IWMSyncReader Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader)
</dt> </dl>

 

 




