---
description: Filtro do analisador SAMI (CC)
ms.assetid: 9b09dd86-3c22-4565-82a0-106d5ca2e42d
title: Filtro do analisador SAMI (CC)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e0449bccd41a09fca952b5d84552ef919055526
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104500547"
---
# <a name="sami-cc-parser-filter"></a>Filtro do analisador SAMI (CC)

Analisa dados de legendas de arquivos de SAMI (intercâmbio de mídia acessível) sincronizados.

SAMI é um formato de texto semelhante a HTML e é usado para codificar legendas baseadas em tempo. Esse filtro converte dados SAMI em um fluxo de texto. Cada exemplo no fluxo contém uma entrada de legenda, juntamente com informações de formato. Os carimbos de data/hora nos exemplos são gerados a partir das informações de hora no arquivo SAMI.

Esse filtro foi projetado para ser usado com o filtro de [processador de comandos de script interno](internal-script-command-renderer-filter.md) . O renderizador de comando de script interno recebe exemplos de texto e os envia para o aplicativo, na forma de notificações de eventos. Para obter mais informações, consulte a seção Comentários.



|                                          |                                                                                                          |
|------------------------------------------|----------------------------------------------------------------------------------------------------------|
| Filtrar interfaces                        | [**IAMStreamSelect**](/windows/desktop/api/Strmif/nn-strmif-iamstreamselect), [ **IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)                           |
| Tipos de mídia de pino de entrada                    | Fluxo de MEDIATYPE \_                                                                                        |
| Interfaces de pino de entrada                     | [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [ **IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)                                         |
| Tipos de mídia do pino de saída                   | \_Texto de MediaType, MEDIASUBTYPE \_ nulo                                                                      |
| Interfaces de pino de saída                    | [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) |
| CLSID do filtro                             | {33FACFE0-A9BE-11D0-A520-00A0D10129C0}                                                                   |
| CLSID de página de propriedades                      | Nenhuma página de propriedades                                                                                         |
| Executável                               | quartz.dll                                                                                               |
| [Núcleo](merit.md)                       | MÉRITO \_ improvável                                                                                          |
| [Categoria do filtro](filter-categories.md) | \_LEGACYAMFILTERCATEGORY CLSID                                                                            |



 

## <a name="remarks"></a>Comentários

Este é um arquivo SAMI simples:


```C++
<SAMI>
<Head>
<STYLE TYPE="text/css"> <!--
    .ENCC {Name: English; lang:en-US; SAMI_TYPE: CC;}
    .FRCC {Name: French; lang:fr-FR; SAMI_TYPE: CC;}
    #NORMAL {Name: Normal; font-family: arial;}
    #GREENTEXT {Name: GreenText; color:green; font-family: verdana;}
-->
</STYLE>
</Head>
<BODY>
<Sync Start=1000>
    <P CLASS="ENCC">One
    <P CLASS="FRCC">Un

<Sync Start=2000>
    <P CLASS="ENCC">Two
    <P CLASS="FRCC">Deux

<Sync Start=3000>
    <P CLASS="ENCC">Three
    <P CLASS="FRCC">Trois
</BODY>
</SAMI>
```



A marca de **estilo** define duas configurações de idioma, inglês (. ENCC) e francês (. FRCC). Ele também define dois estilos, \# normal e \# GREENTEXT. Cada marca de **sincronização** define a hora de início de uma legenda, em milissegundos. As marcas **P** contêm o texto de legenda, enquanto o atributo de **classe** especifica a configuração de idioma à qual a legenda se aplica.

Para cada idioma e estilo, o filtro cria um fluxo lógico. A qualquer momento, exatamente uma transmissão de fluxo de idioma e um estilo são habilitados. Quando o filtro gera um exemplo, ele seleciona a legenda para o idioma atual e aplica o estilo atual. Por padrão, o primeiro idioma e estilo declarados no arquivo são habilitados. Um aplicativo pode usar o método [**IAMStreamSelect:: Enable**](/windows/desktop/api/Strmif/nf-strmif-iamstreamselect-enable) para habilitar um fluxo diferente.

Com as configurações padrão, a primeira legenda no arquivo de exemplo produz a seguinte saída:


```C++
<P STYLE=" Name: English; lang:en-US; SAMI_TYPE: CC; Name: Normal; font-family: arial;">One
```



Se a saída for para o processador de comandos de script interno, esse filtro enviará uma notificação de evento de [**\_ \_ evento OLE do EC**](ec-ole-event.md) . O segundo parâmetro de evento é um BSTR com o texto de legenda. O aplicativo pode recuperar o evento e exibir a legenda.

O exemplo a seguir mostra como renderizar um arquivo SAMI, recuperar informações de fluxo, habilitar fluxos e exibir texto de legenda. O exemplo supõe que o arquivo SAMI anterior seja salvo como C: \\ Sami \_ test \_ File. Sami.

Para resumir, este exemplo usou índices de fluxo embutidos em código quando chama o método **IAMStreamSelect:: Enable** . Ele também executa a verificação mínima de erros.


```C++
void __cdecl main()
{
    HRESULT hr;
    IGraphBuilder *pGraph;
    IMediaControl *pMediaControl;
    IMediaEventEx *pEv;
    IBaseFilter   *pSAMI;

    CoInitialize(NULL);
    
    // Create the filter graph manager.
    CoCreateInstance(CLSID_FilterGraph, NULL, CLSCTX_INPROC, 
                        IID_IGraphBuilder, (void **)&pGraph);
    pGraph->QueryInterface(IID_IMediaControl, (void **)&pMediaControl);
    pGraph->QueryInterface(IID_IMediaEventEx, (void**)&pEv);

    // Create the graph and find the SAMI parser.
    pGraph->RenderFile(L"C:\\Sami_test_file.sami", NULL);
    hr = pGraph->FindFilterByName(L"SAMI (CC) Parser", &pSAMI);
    if (SUCCEEDED(hr)) 
    {
        IAMStreamSelect *pStrm = NULL;
        hr = pSAMI->QueryInterface(IID_IAMStreamSelect, (void**)&pStrm);
        if (SUCCEEDED(hr)) 
        {
            DWORD dwStreams = 0;
            pStrm->Count(&dwStreams);
            printf("Stream count: %d\n", dwStreams);

            // Select French and "GreenText"
            hr = pStrm->Enable(1, AMSTREAMSELECTENABLE_ENABLE);
            hr = pStrm->Enable(3, AMSTREAMSELECTENABLE_ENABLE);

            // Print the name of each logical stream.
            for (DWORD index = 0; index < dwStreams; index++)
            {
                DWORD dwFlags;
                WCHAR *wszName;
                hr = pStrm->Info(index, NULL, &dwFlags, NULL, NULL,
                    &wszName, NULL, NULL);
                if (hr == S_OK)
                {
                    wprintf(L"Stream %d: %s [%s]\n", index, wszName, 
                        (dwFlags ?  L"ENABLED" : L"DISABLED"));
                    CoTaskMemFree(wszName);
                }
            }
            pStrm->Release();
        }
        pSAMI->Release();
    }

    // Run the graph and display the captions.
    pMediaControl->Run();
    while (1)
    {
        long evCode, lParam1, lParam2;
        pEv->GetEvent(&evCode, &lParam1, &lParam2, 100);
        
        if (evCode == EC_OLE_EVENT) {
            wprintf(L"%s\n", (BSTR)lParam2);
        }
        pEv->FreeEventParams(evCode, lParam1, lParam2);

        if (evCode == EC_USERABORT || evCode == EC_COMPLETE || evCode == EC_ERRORABORT)
            break;
    }

    // Clean up.
    pMediaControl->Release();
    pEv->Release();
    pGraph->Release();
    CoUninitialize();
}
```



Esse filtro usa a interface [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) para extrair amostras do filtro de origem. Portanto, ele não dá suporte à interface [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) em seu pino de entrada.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Filtros do DirectShow](directshow-filters.md)
</dt> </dl>

 

 



