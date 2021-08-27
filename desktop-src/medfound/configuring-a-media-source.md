---
description: Configurando uma origem de mídia
ms.assetid: 1378bbe6-be94-4be1-b428-5ec58dabd1fa
title: Configurando uma origem de mídia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 809d215cf282dba1e65c21316fafda47684a2151
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122481702"
---
# <a name="configuring-a-media-source"></a>Configurando uma origem de mídia

Ao usar o [resolvedor de origem](source-resolver.md) para criar uma fonte de mídia, você pode especificar um repositório de propriedades que contém propriedades de configuração. Essas propriedades serão usadas para inicializar a origem da mídia. O conjunto de propriedades com suporte depende da implementação da origem da mídia. Nem toda fonte de mídia define as propriedades de configuração.

A tabela a seguir lista as propriedades de configuração para as fontes de mídia fornecidas no Media Foundation. As fontes de mídia de terceiros podem definir suas próprias propriedades personalizadas.




| Origem da mídia | Propriedades | 
|--------------|------------|
| Origem da rede | Consulte <a href="network-source-features.md">recursos de origem da rede</a>. | 
| Fonte de mídia ASF | <ul><li><a href="mfpkey-asfmediasource-approxseek-property.md"><strong>MFPKEY_ASFMediaSource_ApproxSeek</strong></a></li><li><a href="mfpkey-asfmediasource-iterativeseekifnoindex.md">MFPKEY_ASFMediaSource_IterativeSeekIfNoIndex</a></li><li><a href="mfpkey-asfmediasource-iterativeseek-max-count.md">MFPKEY_ASFMediaSource_IterativeSeek_Max_Count</a></li><li><a href="mfpkey-asfmediasource-iterativeseek-tolerance-in-millisecond.md">MFPKEY_ASFMediaSource_IterativeSeek_Tolerance_In_MilliSecond</a></li></ul> | 




 

Para configurar uma origem, execute as etapas a seguir.

1.  Chame **PSCreateMemoryPropertyStore** para criar um novo repositório de propriedades. Essa função retorna um ponteiro **IPropertyStore** .
2.  Chame **IPropertyStore:: SetValue** para definir uma ou mais propriedades de configuração.
3.  Chame uma das funções de criação do resolvedor de origem, como [**IMFSourceResolver:: CreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfromurl), e passe o ponteiro **IPropertyStore** no parâmetro *pProps* .


```C++
// Creates a media source from a URL.

HRESULT CreateMediaSource(
    PCWSTR pszURL, 
    IPropertyStore *pConfig,    // Optional, can be NULL
    IMFMediaSource **ppSource
    )
{
    IMFSourceResolver* pSourceResolver = NULL;
    IUnknown* pSource = NULL;

    // Create the source resolver.
    HRESULT hr = MFCreateSourceResolver(&pSourceResolver);

    // Use the source resolver to create the media source.
    if (SUCCEEDED(hr))
    {
        MF_OBJECT_TYPE ObjectType;

        DbgLog(L"CreateObjectFromURL");

        hr = pSourceResolver->CreateObjectFromURL(
            pszURL,                     
            MF_RESOLUTION_MEDIASOURCE,  // Create a media source.
            pConfig,                    // Configuration properties.
            &ObjectType,                // Receives the object type. 
            &pSource            
            );

        DbgLog(L"CreateObjectFromURL - FINISHED");

    }

    if (SUCCEEDED(hr))
    {
        hr = pSource->QueryInterface(IID_PPV_ARGS(ppSource));
    }

    SafeRelease(&pSourceResolver);
    SafeRelease(&pSource);
    return hr;
}
```



O resolvedor de origem passa o ponteiro **IPropertyStore** diretamente para o manipulador de esquema ou o manipulador de fluxo de bytes que cria a origem. O resolvedor de origem não faz nenhuma tentativa de validar as propriedades.

Em geral, essas propriedades são usadas para configurações avançadas. Se você não fornecer um repositório de propriedades, a origem da mídia ainda deverá funcionar corretamente com as configurações padrão.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Resolvedor de origem](source-resolver.md)
</dt> </dl>

 

 



