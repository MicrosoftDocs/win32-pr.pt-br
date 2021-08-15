---
title: Usando Two-Pass codificação (SDK Windows Media Format 11)
description: Usando Two-Pass codificação
ms.assetid: 55fc768b-15f0-4236-ad0d-3792ccaa9b4f
keywords:
- ASF (Advanced Systems Format), codificação de duas passs
- ASF (Formato de Sistemas Avançados), codificação de duas passs
- codificação de duas passs, sobre
- Codificação de duas passs, sobre
- codecs, codificação de duas passs
- codificação de duas passs, interface IWMWriterPreprocess
- Codificação de duas passs, interface IWMWriterPreprocess
- IWMWriterPreprocess
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd0683af636197b3f8116fca4dea85ce15609d2c99b0d9e0c11dfe0a2662a424
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117653831"
---
# <a name="using-two-pass-encoding-windows-media-format-11-sdk"></a>Usando Two-Pass codificação (SDK Windows Media Format 11)

Alguns codecs são suportados com codificação de duas passs para determinados formatos. Em alguns casos, um codec requer que um formato especificado seja codificado usando duas passagens. Quando a codificação de duas passs é usada, você envia os exemplos do fluxo para o codec antes da passagem da codificação. O codec analisa os exemplos e configura a passagem de codificação com base na análise. Isso resulta em um arquivo codificado com mais eficiência.

Para determinar se um codec dá suporte à codificação de uma passagem ou duas passagens ou ambos, para um determinado formato, chame [**IWMCodecInfo3::SetCodecEnumerationSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmcodecinfo3-setcodecenumerationsetting) com g wszNumPasses e o valor apropriado e, em seguida, enumere os formatos para ver se o que você deseja é \_ retornado. Para obter mais informações sobre Windows codecs de mídia que suportam codificação de duas passs, consulte Escolhendo um método [de codificação](choosing-an-encoding-method.md).

Você pode usar a codificação de duas passões com o SDK Windows Media Format chamando métodos da interface [**IWMWriterPreprocess.**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterpreprocess)

Nos casos em que a codificação de duas passagens é necessária para um formato específico, mas o aplicativo não executa uma passagem de pré-processamento, a primeira chamada para [**WriteSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-writesample) falhará com NS \_ E INVALID NUM \_ \_ \_ PASSES.

A função de exemplo a seguir demonstra como executar a codificação de duas passões. Essa função é chamada depois que o autor é definido com um perfil e iniciado. Para obter mais informações sobre como usar esse código, [consulte Usando os exemplos de código](using-the-code-examples.md).


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

[**Escrevendo arquivos ASF**](writing-asf-files.md)
</dt> </dl>

 

 




