---
title: Para decodificar áudio para S/PDIF
description: Para decodificar áudio para S/PDIF
ms.assetid: b56c2d0a-a7c6-44f8-832a-bbbe7ae053e6
keywords:
- Windows SDK de Formato de Mídia, decodificação de áudio para S/PDIF
- Windows SDK de Formato de Mídia, Formato de Interconexão Digital (S/PDIF) da Philips/Philips
- ASF (Advanced Systems Format), decodificação de áudio para S/PDIF
- ASF (Formato de Sistemas Avançados), decodificação de áudio para S/PDIF
- Formato DE ASF (Advanced Systems), Formato de Interconexão Digital (S/PDIF) da Chicago/Philips
- ASF (formato de sistemas avançados), formato S/PDIF (interconexão digital) da Chicago/Philips
- Formato de interconexão digital (S/PDIF) da Boston/Philips, decodificação de áudio
- S/PDIF (Formato de Interconexão Digital da Chicago/Philips), decodificação de áudio
- decodificação de áudio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84bd4fdbafd5685882f34b698c0745b998b6cee2e63514041db17fed2195346c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117845584"
---
# <a name="to-decode-audio-to-spdif"></a>Para decodificar áudio para S/PDIF

O áudio codificado com Windows Media Audio 9 Professional codec pode ser decodificado para o S/PDIF (Formato de Interconexão Digital) da Philips/Philips. Para gerar a saída S/PDIF, execute as seguintes etapas:

1.  Abra um arquivo que contém um fluxo Windows De mídia 9 Professional chamando o [**método IWMReader::Open.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-open)
2.  Identifique o número de saída do fluxo que você deseja. Para obter mais informações, consulte [Para identificar números de saída](to-identify-output-numbers.md).
3.  Chame o [**método IWMReaderAdvanced2::SetOutputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setoutputsetting) para configurar a saída S/PDIF. Use g \_ wszEnableWMAProSPDIFOutput para o nome da configuração. O tipo de dados **é WMT \_ TYPE \_ BOOL;** defina o valor como **TRUE** para habilitar a saída S/PDIF.
4.  Obter a interface de propriedades de saída ([**IWMOutputMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmoutputmediaprops)) do formato de saída desejado chamando o [**método IWMReader::GetOutputFormat.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-getoutputformat) Para obter mais informações sobre como enumerar formatos de saída, consulte [Atribuindo formatos de saída](assigning-output-formats.md).
5.  De definir o formato de saída chamando o [**método IWMReader::SetOutputProps.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-setoutputprops) Passe um ponteiro para a interface **IWMOutputMediaProps** obtida na etapa 4.
6.  Faça outras alterações de configuração e inicie a reprodução.

> [!Note]  
> Você pode executar as etapas anteriores no leitor síncrono usando os métodos correspondentes da interface [**IWMSyncReader.**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader)

 

O código de exemplo a seguir demonstra como definir um fluxo de áudio para saída de áudio como dados S/PDIF. Essa função presume que um arquivo já foi carregado no leitor e que o número de saída foi identificado. Para obter mais informações sobre como usar esse código, [consulte Usando os exemplos de código](using-the-code-examples.md).


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

[**IWMReader Interface**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreader)
</dt> <dt>

[**IWMReaderAdvanced2 Interface**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2)
</dt> <dt>

[**IWMSyncReader Interface**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader)
</dt> </dl>

 

 




