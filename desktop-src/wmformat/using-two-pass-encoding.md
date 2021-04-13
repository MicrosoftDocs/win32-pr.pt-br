---
title: Usando a codificação Two-Pass (SDK do Windows Media Format 11)
description: Usando a codificação Two-Pass
ms.assetid: 55fc768b-15f0-4236-ad0d-3792ccaa9b4f
keywords:
- ASF (Advanced Systems Format), codificação de duas passagens
- ASF (formato de sistemas avançados), codificação de duas passagens
- codificação de dois passos, sobre
- 2-passar codificação, sobre
- codecs, codificação em duas passagens
- codificação de duas passagens, interface IWMWriterPreprocess
- 2-passar codificação, interface IWMWriterPreprocess
- IWMWriterPreprocess
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c3794856f47c1656cc53006268c41a063cdde96
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104499227"
---
# <a name="using-two-pass-encoding-windows-media-format-11-sdk"></a><span data-ttu-id="63cf4-111">Usando a codificação Two-Pass (SDK do Windows Media Format 11)</span><span class="sxs-lookup"><span data-stu-id="63cf4-111">Using Two-Pass Encoding (Windows Media Format 11 SDK)</span></span>

<span data-ttu-id="63cf4-112">Alguns codecs dão suporte à codificação de duas passagens para determinados formatos.</span><span class="sxs-lookup"><span data-stu-id="63cf4-112">Some codecs support two-pass encoding for certain formats.</span></span> <span data-ttu-id="63cf4-113">Em alguns casos, um codec requer que um formato especificado seja codificado usando duas passagens.</span><span class="sxs-lookup"><span data-stu-id="63cf4-113">In some cases, a codec requires that a specified format be encoded using two passes.</span></span> <span data-ttu-id="63cf4-114">Quando a codificação de duas passagens é usada, você envia os exemplos do fluxo para o codec antes da passagem de codificação.</span><span class="sxs-lookup"><span data-stu-id="63cf4-114">When two-pass encoding is used, you send the samples for the stream to the codec before the encoding pass.</span></span> <span data-ttu-id="63cf4-115">O codec analisa os exemplos e configura a passagem de codificação com base na análise.</span><span class="sxs-lookup"><span data-stu-id="63cf4-115">The codec analyzes the samples and configures the encoding pass based on the analysis.</span></span> <span data-ttu-id="63cf4-116">Isso resulta em um arquivo codificado com mais eficiência.</span><span class="sxs-lookup"><span data-stu-id="63cf4-116">This results in a more efficiently encoded file.</span></span>

<span data-ttu-id="63cf4-117">Para determinar se um codec dá suporte à codificação de uma passagem, ou de duas passagens, ou ambos, para um determinado formato, chame [**IWMCodecInfo3:: SetCodecEnumerationSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmcodecinfo3-setcodecenumerationsetting) com g \_ wszNumPasses e o valor apropriado e, em seguida, enumere os formatos para ver se aquele que você deseja é retornado.</span><span class="sxs-lookup"><span data-stu-id="63cf4-117">To determine whether a codec supports one-pass encoding, or two-pass, or both, for a given format, call [**IWMCodecInfo3::SetCodecEnumerationSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmcodecinfo3-setcodecenumerationsetting) with g\_wszNumPasses and the appropriate value, and then enumerate the formats to see if the one you want is returned.</span></span> <span data-ttu-id="63cf4-118">Para obter mais informações sobre os codecs de mídia do Windows que dão suporte à codificação de duas passagens, consulte [escolhendo um método de codificação](choosing-an-encoding-method.md).</span><span class="sxs-lookup"><span data-stu-id="63cf4-118">For more information about the Windows Media codecs that support two-pass encoding, see [Choosing an Encoding Method](choosing-an-encoding-method.md).</span></span>

<span data-ttu-id="63cf4-119">Você pode usar codificação de duas passagens com o SDK de formato de mídia do Windows chamando métodos da interface [**IWMWriterPreprocess**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterpreprocess) .</span><span class="sxs-lookup"><span data-stu-id="63cf4-119">You can use two-pass encoding with the Windows Media Format SDK by calling methods of the [**IWMWriterPreprocess**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterpreprocess) interface.</span></span>

<span data-ttu-id="63cf4-120">Nos casos em que a codificação de duas passagens é necessária para um determinado formato, mas o aplicativo não executa uma passagem de pré-processamento, a primeira chamada para [**WriteSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-writesample) falhará com o NS \_ E o número de \_ \_ passagens inválido \_ .</span><span class="sxs-lookup"><span data-stu-id="63cf4-120">In cases where two-pass encoding is required for a particular format, but the application fails to perform a preprocessing pass, the first call to [**WriteSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-writesample) will fail with NS\_E\_INVALID\_NUM\_PASSES.</span></span>

<span data-ttu-id="63cf4-121">A função de exemplo a seguir demonstra como executar a codificação de duas passagens.</span><span class="sxs-lookup"><span data-stu-id="63cf4-121">The following example function demonstrates how to perform two-pass encoding.</span></span> <span data-ttu-id="63cf4-122">Essa função é chamada depois que o gravador tiver sido definido com um perfil e iniciado.</span><span class="sxs-lookup"><span data-stu-id="63cf4-122">This function is called after the writer has been set with a profile and started.</span></span> <span data-ttu-id="63cf4-123">Para obter mais informações sobre como usar esse código, consulte [usando os exemplos de código](using-the-code-examples.md).</span><span class="sxs-lookup"><span data-stu-id="63cf4-123">For more information about using this code, see [Using the Code Examples](using-the-code-examples.md).</span></span>


```C++
HRESULT PreProcess(IWMWriter* pWriter, DWORD dwInputNum)
{
    HRESULT hr        = S_OK;
    DWORD   dwMaxPass = 0;

    IWMWriterPreprocess* pPreProc = NULL;

    // Get the writer preprocessor interface.
    hr = pWriter->QueryInterface(IID_IWMWriterPreprocess, 
                                 (void**) &pPreProc);
    GOTO_EXIT_IF_FAILED(hr);

    // Check that the input can be preprocessed.
    hr = pPreProc->GetMaxPreprocessingPasses(dwInputNum,0, &dwMaxPass);
    GOTO_EXIT_IF_FAILED(hr);

    if(dwMaxPass == 0)
    {
        hr = NS_E_INVALID_REQUEST;
        goto Exit;
    }

    // Set the number of preprocessing passes to the maximum.
    hr = pPreProc->SetNumPreprocessingPasses(dwInputNum, 0, dwMaxPass);
    GOTO_EXIT_IF_FAILED(hr);

    // Call BeginWriting before calling BeginPreprocessingPass
    hr = pWriter->BeginWriting();

    // Start preprocessing the first pass.
    hr = pPreProc->BeginPreprocessingPass(dwInputNum, 0);
    GOTO_EXIT_IF_FAILED(hr);

    // TODO: Make repeated calls to pPreProc->PreprocessSample to
    // preprocess all the samples in the stream.

    // End preprocessing.
    hr = pPreProc->EndPreprocessingPass(dwInputNum, 0);
    GOTO_EXIT_IF_FAILED(hr);

    // TODO: If the maximum number of preprocessing passes is greater
    // than one, repeat the preprocessing steps for each pass.

Exit:
    SAFE_RELEASE(pPreProc);
    Return hr;
}

```



## <a name="related-topics"></a><span data-ttu-id="63cf4-124">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="63cf4-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="63cf4-125">**Gravando arquivos ASF**</span><span class="sxs-lookup"><span data-stu-id="63cf4-125">**Writing ASF Files**</span></span>](writing-asf-files.md)
</dt> </dl>

 

 




