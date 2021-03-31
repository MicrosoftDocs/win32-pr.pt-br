---
description: O SAMI (Synchronized Media Interchange) é um formato para adicionar legendas à mídia digital.
ms.assetid: 007c8181-089e-4e56-a31d-9d1942f90b07
title: Fonte de mídia SAMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9340b51815b130cb41061478358b2ab9dcf68f60
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "104011938"
---
# <a name="sami-media-source"></a>Fonte de mídia SAMI

O SAMI (Synchronized Media Interchange) é um formato para adicionar legendas à mídia digital. As legendas são armazenadas em um arquivo de texto separado com a extensão de nome de arquivo. SMI ou. Sami.

No Media Foundation, os arquivos de legenda SAMI têm suporte por meio da fonte de mídia SAMI. Use o [resolvedor de origem](source-resolver.md) para criar uma instância da fonte de mídia Sami de um fluxo de URL ou de bytes. Media Foundation não fornece um componente que exibe legendas SAMI. O aplicativo deve interpretar os dados de legenda que ele recebe da fonte de mídia SAMI.

Veja a seguir um exemplo de arquivo SAMI.

``` syntax
<SAMI>
<HEAD>
    <STYLE TYPE="text/css">
    <!--
    P {
        font-family: Arial;
        background: #000000;
        text-align: center;
        }

#standard {Name: Standard; color: #FFFFFF; font-size: 14pt; } 
#hilite {Name: Youth; color: greenyellow; font-size: 18pt;}

    .ENUSCC { Name: English; lang: EN-US-CC; }
    .FRFRCC { Name: French; lang: fr-FR; } 

    -->
    </STYLE>
</HEAD>
<BODY>
    <SYNC Start="0">
        <P Class="ENUSCC">The <I>first</I> caption.</P>
        <P Class="FRFRCC">Un</P>
    </SYNC>
    <SYNC Start="3000">
        <P Class="ENUSCC">The <I>second</I> caption.</P>
        <P Class="FRFRCC">Deux</P>
    </SYNC>
    <SYNC Start="5000">
        <P Class="ENUSCC">The <I>third</I> caption.</P>
        <P Class="FRFRCC">Trois</P>
    </SYNC>
</BODY>
</SAMI>
```

O `<STYLE>` elemento contém informações de estilo. Este exemplo contém um estilo base para `<P>` elementos, juntamente com dois estilos nomeados, "Standard" e "hilite". Os estilos nomeados são usados para modificar o estilo base. As legendas são colocadas dentro dos `<SYNC>` elementos. O atributo Start fornece o tempo de apresentação em milissegundos para essa legenda. As legendas neste exemplo são dadas em dois idiomas, especificados por suas marcas de idioma RFC-1766, "en-US" e "fr-FR". Dentro das legendas, os idiomas são identificados por seus nomes de classe; Nesse caso, "ENUSCC" e "FRFRCC".

A fonte de mídia SAMI cria um fluxo de mídia para cada idioma. Por padrão, o primeiro fluxo é selecionado e os fluxos restantes são desmarcados. O aplicativo pode alterar a seleção de fluxo chamando [**IMFPresentationDescriptor:: SelectStream**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-selectstream) e [**IMFPresentationDescriptor::D eselectstream**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-deselectstream). Cada descritor de fluxo contém os atributos a seguir.



| Atributo                                                       | Descrição                                      |
|-----------------------------------------------------------------|--------------------------------------------------|
| [**\_linguagem SD \_ MF**](mf-sd-language-attribute.md)            | Marca de idioma, conforme fornecido pelo `lang` atributo.  |
| [**\_linguagem de \_ Sami \_ SD MF**](mf-sd-sami-language-attribute.md) | Nome do idioma, conforme fornecido pelo `Name` atributo. |



 

Cada fluxo tem o seguinte tipo de mídia:



| Atributo                                                                            | Valor                 |
|--------------------------------------------------------------------------------------|-----------------------|
| [**\_ \_ tipo principal MF \_ MT**](mf-mt-major-type-attribute.md)                            | **Sami de MFMediaType \_** |
| [**\_ \_ todos os exemplos do MF MT são \_ \_ independentes**](mf-mt-all-samples-independent-attribute.md) | **TRUE**              |



 

A fonte SAMI entrega cada legenda em um exemplo de mídia separado. O carimbo de data/hora de exemplo e a duração são derivados do `<SYNC>` elemento. O buffer de mídia contido no exemplo mantém a legenda como texto ASCII. O estilo de legenda é inserido na legenda como um atributo embutido `STYLE` . Por exemplo, considerando o arquivo SAMI anterior e usando o fluxo de idioma inglês com os estilos padrão, o primeiro buffer de mídia conterá os dados a seguir. (As quebras de linha podem ser diferentes das mostradas aqui.)

``` syntax
<P STYLE="
    font-family: Arial;
    background: #000000;
    text-align: center;
    Name: English; lang: EN-US-CC;  
    Name: Standard; color: #FFFFFF; 
    font-size: 14pt; ">The<I>first</I> caption.
```

## <a name="sami-styles"></a>Estilos SAMI

Para alterar o estilo atual, use a interface [**IMFSAMIStyle**](/windows/desktop/api/mfidl/nn-mfidl-imfsamistyle) . Essa interface é obtida chamando [**IMFGetService:: GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) na fonte de mídia Sami. (Se você estiver usando a fonte de mídia SAMI com a sessão de mídia, chame **GetService** na sessão de mídia.) O identificador de serviço é o **\_ \_ serviço MF Sami**.

O exemplo a seguir define o estilo SAMI atual, especificado pelo índice.


```C++
HRESULT SetSAMIStyleByIndex(IMFMediaSource *pSource, DWORD index)
{
    IMFSAMIStyle *pSami = NULL;

    DWORD cStyles;
    PROPVARIANT varStyles;

    HRESULT hr = MFGetService(pSource, MF_SAMI_SERVICE, IID_PPV_ARGS(&pSami));
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pSami->GetStyleCount(&cStyles);
    if (FAILED(hr))
    {
        goto done;
    }

    if (index >= cStyles)
    {
        hr = E_INVALIDARG;
        goto done;
    }

    hr = pSami->GetStyles(&varStyles);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pSami->SetSelectedStyle(varStyles.calpwstr.pElems[index]);

done:
    PropVariantClear(&varStyles);
    SafeRelease(&pSami);
    return hr;
}
```



Este exemplo chama os seguintes métodos na fonte de mídia SAMI:

-   [**IMFSAMIStyle:: GetStyleCount**](/windows/desktop/api/mfidl/nf-mfidl-imfsamistyle-getstylecount) Obtém o número de estilos.
-   [**IMFSAMIStyle:: Getstyles**](/windows/desktop/api/mfidl/nf-mfidl-imfsamistyle-getstyles) Obtém uma lista dos nomes de estilo, armazenados em um **PROPVARIANT**.
-   [**IMFSAMIStyle:: Setselecionadostyle**](/windows/desktop/api/mfidl/nf-mfidl-imfsamistyle-setselectedstyle) define um estilo por nome.

A lista de nomes de estilo também é armazenada no descritor de apresentação, no atributo [**MF \_ PD \_ Sami de \_ estilo**](mf-pd-sami-stylelist-attribute.md) .

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Fontes de mídia e coletores](media-sources-and-sinks.md)
</dt> <dt>

[Formatos de mídia compatíveis com o Media Foundation](supported-media-formats-in-media-foundation.md)
</dt> </dl>

 

 



