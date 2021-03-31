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
# <a name="to-decode-audio-to-spdif"></a>Para decodificar áudio para S/PDIF

O áudio codificado com o codec Windows Media Audio 9 Professional pode ser decodificado para o S/PDIF (formato de interconexão digital) da Sony/Philips. Para gerar a saída de S/PDIF, execute as seguintes etapas:

1.  Abra um arquivo que contenha um fluxo do Windows Media Audio 9 Professional chamando o método [**IWMReader:: Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-open) .
2.  Identifique o número de saída do fluxo desejado. Para obter mais informações, consulte [para identificar números de saída](to-identify-output-numbers.md).
3.  Chame o método [**IWMReaderAdvanced2:: SetOutputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setoutputsetting) para configurar a saída de S/PDIF. Use g \_ wszEnableWMAProSPDIFOutput para o nome da configuração. O tipo de dados é **WMT \_ tipo \_ bool**; defina o valor como **true** para habilitar a saída S/PDIF.
4.  Obtenha a interface de propriedades de saída ([**IWMOutputMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmoutputmediaprops)) do formato de saída desejado chamando o método [**IWMReader:: GetOutputFormat**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-getoutputformat) . Para obter mais informações sobre como enumerar formatos de saída, consulte [atribuindo formatos de saída](assigning-output-formats.md).
5.  Defina o formato de saída chamando o método [**IWMReader:: SetOutputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-setoutputprops) . Passe um ponteiro para a interface **IWMOutputMediaProps** obtida na etapa 4.
6.  Faça outras alterações de configuração e comece a reprodução.

> [!Note]  
> Você pode executar as etapas anteriores no leitor síncrono usando os métodos correspondentes da interface [**IWMSyncReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader) .

 

O código de exemplo a seguir demonstra como definir um fluxo de áudio para saída de áudio como dados S/PDIF. Essa função pressupõe que um arquivo já foi carregado no leitor e que o número de saída foi identificado. Para obter mais informações sobre como usar esse código, consulte [usando os exemplos de código](using-the-code-examples.md).


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



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Tópicos avançados**](advanced-topics.md)
</dt> <dt>

[**Lendo arquivos ASF**](reading-asf-files.md)
</dt> <dt>

[**Interface IWMReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreader)
</dt> <dt>

[**Interface IWMReaderAdvanced2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2)
</dt> <dt>

[**Interface IWMSyncReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader)
</dt> </dl>

 

 




