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
# <a name="using-two-pass-encoding-windows-media-format-11-sdk"></a>Usando a codificação Two-Pass (SDK do Windows Media Format 11)

Alguns codecs dão suporte à codificação de duas passagens para determinados formatos. Em alguns casos, um codec requer que um formato especificado seja codificado usando duas passagens. Quando a codificação de duas passagens é usada, você envia os exemplos do fluxo para o codec antes da passagem de codificação. O codec analisa os exemplos e configura a passagem de codificação com base na análise. Isso resulta em um arquivo codificado com mais eficiência.

Para determinar se um codec dá suporte à codificação de uma passagem, ou de duas passagens, ou ambos, para um determinado formato, chame [**IWMCodecInfo3:: SetCodecEnumerationSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmcodecinfo3-setcodecenumerationsetting) com g \_ wszNumPasses e o valor apropriado e, em seguida, enumere os formatos para ver se aquele que você deseja é retornado. Para obter mais informações sobre os codecs de mídia do Windows que dão suporte à codificação de duas passagens, consulte [escolhendo um método de codificação](choosing-an-encoding-method.md).

Você pode usar codificação de duas passagens com o SDK de formato de mídia do Windows chamando métodos da interface [**IWMWriterPreprocess**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterpreprocess) .

Nos casos em que a codificação de duas passagens é necessária para um determinado formato, mas o aplicativo não executa uma passagem de pré-processamento, a primeira chamada para [**WriteSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-writesample) falhará com o NS \_ E o número de \_ \_ passagens inválido \_ .

A função de exemplo a seguir demonstra como executar a codificação de duas passagens. Essa função é chamada depois que o gravador tiver sido definido com um perfil e iniciado. Para obter mais informações sobre como usar esse código, consulte [usando os exemplos de código](using-the-code-examples.md).


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



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Gravando arquivos ASF**](writing-asf-files.md)
</dt> </dl>

 

 




