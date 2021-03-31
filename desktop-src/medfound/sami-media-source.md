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
# <a name="sami-media-source"></a><span data-ttu-id="26d3c-103">Fonte de mídia SAMI</span><span class="sxs-lookup"><span data-stu-id="26d3c-103">SAMI Media Source</span></span>

<span data-ttu-id="26d3c-104">O SAMI (Synchronized Media Interchange) é um formato para adicionar legendas à mídia digital.</span><span class="sxs-lookup"><span data-stu-id="26d3c-104">Synchronized Accessible Media Interchange (SAMI) is a format for adding captions to digital media.</span></span> <span data-ttu-id="26d3c-105">As legendas são armazenadas em um arquivo de texto separado com a extensão de nome de arquivo. SMI ou. Sami.</span><span class="sxs-lookup"><span data-stu-id="26d3c-105">The captions are stored in a separate text file with the file name extension .smi or .sami.</span></span>

<span data-ttu-id="26d3c-106">No Media Foundation, os arquivos de legenda SAMI têm suporte por meio da fonte de mídia SAMI.</span><span class="sxs-lookup"><span data-stu-id="26d3c-106">In Media Foundation, SAMI caption files are supported through the SAMI media source.</span></span> <span data-ttu-id="26d3c-107">Use o [resolvedor de origem](source-resolver.md) para criar uma instância da fonte de mídia Sami de um fluxo de URL ou de bytes.</span><span class="sxs-lookup"><span data-stu-id="26d3c-107">Use the [Source Resolver](source-resolver.md) to create an instance of the SAMI media source from a URL or byte stream.</span></span> <span data-ttu-id="26d3c-108">Media Foundation não fornece um componente que exibe legendas SAMI.</span><span class="sxs-lookup"><span data-stu-id="26d3c-108">Media Foundation does not provide a component that displays SAMI captions.</span></span> <span data-ttu-id="26d3c-109">O aplicativo deve interpretar os dados de legenda que ele recebe da fonte de mídia SAMI.</span><span class="sxs-lookup"><span data-stu-id="26d3c-109">The application must interpret the caption data that it receives from the SAMI media source.</span></span>

<span data-ttu-id="26d3c-110">Veja a seguir um exemplo de arquivo SAMI.</span><span class="sxs-lookup"><span data-stu-id="26d3c-110">The following shows an example SAMI file.</span></span>

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

<span data-ttu-id="26d3c-111">O `<STYLE>` elemento contém informações de estilo.</span><span class="sxs-lookup"><span data-stu-id="26d3c-111">The `<STYLE>` element contains style information.</span></span> <span data-ttu-id="26d3c-112">Este exemplo contém um estilo base para `<P>` elementos, juntamente com dois estilos nomeados, "Standard" e "hilite".</span><span class="sxs-lookup"><span data-stu-id="26d3c-112">This example contains a base style for `<P>` elements, along with two named styles, "standard" and "hilite".</span></span> <span data-ttu-id="26d3c-113">Os estilos nomeados são usados para modificar o estilo base.</span><span class="sxs-lookup"><span data-stu-id="26d3c-113">The named styles are used to modify the base style.</span></span> <span data-ttu-id="26d3c-114">As legendas são colocadas dentro dos `<SYNC>` elementos.</span><span class="sxs-lookup"><span data-stu-id="26d3c-114">Captions are placed within `<SYNC>` elements.</span></span> <span data-ttu-id="26d3c-115">O atributo Start fornece o tempo de apresentação em milissegundos para essa legenda.</span><span class="sxs-lookup"><span data-stu-id="26d3c-115">The start attribute gives the presentation time in milliseconds for that caption.</span></span> <span data-ttu-id="26d3c-116">As legendas neste exemplo são dadas em dois idiomas, especificados por suas marcas de idioma RFC-1766, "en-US" e "fr-FR".</span><span class="sxs-lookup"><span data-stu-id="26d3c-116">The captions in this example are given in two languages, specified by their RFC-1766 language tags, "en-US" and "fr -FR".</span></span> <span data-ttu-id="26d3c-117">Dentro das legendas, os idiomas são identificados por seus nomes de classe; Nesse caso, "ENUSCC" e "FRFRCC".</span><span class="sxs-lookup"><span data-stu-id="26d3c-117">Within the captions, languages are identified by their class names; in this case, "ENUSCC" and "FRFRCC".</span></span>

<span data-ttu-id="26d3c-118">A fonte de mídia SAMI cria um fluxo de mídia para cada idioma.</span><span class="sxs-lookup"><span data-stu-id="26d3c-118">The SAMI media source creates one media stream for each language.</span></span> <span data-ttu-id="26d3c-119">Por padrão, o primeiro fluxo é selecionado e os fluxos restantes são desmarcados.</span><span class="sxs-lookup"><span data-stu-id="26d3c-119">By default, the first stream is selected and the remaining streams are deselected.</span></span> <span data-ttu-id="26d3c-120">O aplicativo pode alterar a seleção de fluxo chamando [**IMFPresentationDescriptor:: SelectStream**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-selectstream) e [**IMFPresentationDescriptor::D eselectstream**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-deselectstream).</span><span class="sxs-lookup"><span data-stu-id="26d3c-120">The application can change the stream selection by calling [**IMFPresentationDescriptor::SelectStream**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-selectstream) and [**IMFPresentationDescriptor::DeselectStream**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-deselectstream).</span></span> <span data-ttu-id="26d3c-121">Cada descritor de fluxo contém os atributos a seguir.</span><span class="sxs-lookup"><span data-stu-id="26d3c-121">Each stream descriptor contains the following attributes.</span></span>



| <span data-ttu-id="26d3c-122">Atributo</span><span class="sxs-lookup"><span data-stu-id="26d3c-122">Attribute</span></span>                                                       | <span data-ttu-id="26d3c-123">Descrição</span><span class="sxs-lookup"><span data-stu-id="26d3c-123">Description</span></span>                                      |
|-----------------------------------------------------------------|--------------------------------------------------|
| [<span data-ttu-id="26d3c-124">**\_linguagem SD \_ MF**</span><span class="sxs-lookup"><span data-stu-id="26d3c-124">**MF\_SD\_LANGUAGE**</span></span>](mf-sd-language-attribute.md)            | <span data-ttu-id="26d3c-125">Marca de idioma, conforme fornecido pelo `lang` atributo.</span><span class="sxs-lookup"><span data-stu-id="26d3c-125">Language tag, as given by the `lang` attribute.</span></span>  |
| [<span data-ttu-id="26d3c-126">**\_linguagem de \_ Sami \_ SD MF**</span><span class="sxs-lookup"><span data-stu-id="26d3c-126">**MF\_SD\_SAMI\_LANGUAGE**</span></span>](mf-sd-sami-language-attribute.md) | <span data-ttu-id="26d3c-127">Nome do idioma, conforme fornecido pelo `Name` atributo.</span><span class="sxs-lookup"><span data-stu-id="26d3c-127">Language name, as given by the `Name` attribute.</span></span> |



 

<span data-ttu-id="26d3c-128">Cada fluxo tem o seguinte tipo de mídia:</span><span class="sxs-lookup"><span data-stu-id="26d3c-128">Each stream has the following media type:</span></span>



| <span data-ttu-id="26d3c-129">Atributo</span><span class="sxs-lookup"><span data-stu-id="26d3c-129">Attribute</span></span>                                                                            | <span data-ttu-id="26d3c-130">Valor</span><span class="sxs-lookup"><span data-stu-id="26d3c-130">Value</span></span>                 |
|--------------------------------------------------------------------------------------|-----------------------|
| [<span data-ttu-id="26d3c-131">**\_ \_ tipo principal MF \_ MT**</span><span class="sxs-lookup"><span data-stu-id="26d3c-131">**MF\_MT\_MAJOR\_TYPE**</span></span>](mf-mt-major-type-attribute.md)                            | <span data-ttu-id="26d3c-132">**Sami de MFMediaType \_**</span><span class="sxs-lookup"><span data-stu-id="26d3c-132">**MFMediaType\_SAMI**</span></span> |
| [<span data-ttu-id="26d3c-133">**\_ \_ todos os exemplos do MF MT são \_ \_ independentes**</span><span class="sxs-lookup"><span data-stu-id="26d3c-133">**MF\_MT\_ALL\_SAMPLES\_INDEPENDENT**</span></span>](mf-mt-all-samples-independent-attribute.md) | <span data-ttu-id="26d3c-134">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="26d3c-134">**TRUE**</span></span>              |



 

<span data-ttu-id="26d3c-135">A fonte SAMI entrega cada legenda em um exemplo de mídia separado.</span><span class="sxs-lookup"><span data-stu-id="26d3c-135">The SAMI source delivers each caption in a separate media sample.</span></span> <span data-ttu-id="26d3c-136">O carimbo de data/hora de exemplo e a duração são derivados do `<SYNC>` elemento.</span><span class="sxs-lookup"><span data-stu-id="26d3c-136">The sample time stamp and duration are derived from the `<SYNC>` element.</span></span> <span data-ttu-id="26d3c-137">O buffer de mídia contido no exemplo mantém a legenda como texto ASCII.</span><span class="sxs-lookup"><span data-stu-id="26d3c-137">The media buffer contained in the sample holds the caption as ASCII text.</span></span> <span data-ttu-id="26d3c-138">O estilo de legenda é inserido na legenda como um atributo embutido `STYLE` .</span><span class="sxs-lookup"><span data-stu-id="26d3c-138">The caption style is embedded in the caption as an inline `STYLE` attribute.</span></span> <span data-ttu-id="26d3c-139">Por exemplo, considerando o arquivo SAMI anterior e usando o fluxo de idioma inglês com os estilos padrão, o primeiro buffer de mídia conterá os dados a seguir.</span><span class="sxs-lookup"><span data-stu-id="26d3c-139">For example, given the previous SAMI file, and using the English-language stream with the default styles, the first media buffer would contain the following data.</span></span> <span data-ttu-id="26d3c-140">(As quebras de linha podem ser diferentes das mostradas aqui.)</span><span class="sxs-lookup"><span data-stu-id="26d3c-140">(The line breaks might differ from what is shown here.)</span></span>

``` syntax
<P STYLE="
    font-family: Arial;
    background: #000000;
    text-align: center;
    Name: English; lang: EN-US-CC;  
    Name: Standard; color: #FFFFFF; 
    font-size: 14pt; ">The<I>first</I> caption.
```

## <a name="sami-styles"></a><span data-ttu-id="26d3c-141">Estilos SAMI</span><span class="sxs-lookup"><span data-stu-id="26d3c-141">SAMI Styles</span></span>

<span data-ttu-id="26d3c-142">Para alterar o estilo atual, use a interface [**IMFSAMIStyle**](/windows/desktop/api/mfidl/nn-mfidl-imfsamistyle) .</span><span class="sxs-lookup"><span data-stu-id="26d3c-142">To change the current style, use the [**IMFSAMIStyle**](/windows/desktop/api/mfidl/nn-mfidl-imfsamistyle) interface.</span></span> <span data-ttu-id="26d3c-143">Essa interface é obtida chamando [**IMFGetService:: GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) na fonte de mídia Sami.</span><span class="sxs-lookup"><span data-stu-id="26d3c-143">This interface is obtained by calling [**IMFGetService::GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) on the SAMI media source.</span></span> <span data-ttu-id="26d3c-144">(Se você estiver usando a fonte de mídia SAMI com a sessão de mídia, chame **GetService** na sessão de mídia.) O identificador de serviço é o **\_ \_ serviço MF Sami**.</span><span class="sxs-lookup"><span data-stu-id="26d3c-144">(If you are using the SAMI media source with the Media Session, call **GetService** on the Media Session.) The service identifier is **MF\_SAMI\_SERVICE**.</span></span>

<span data-ttu-id="26d3c-145">O exemplo a seguir define o estilo SAMI atual, especificado pelo índice.</span><span class="sxs-lookup"><span data-stu-id="26d3c-145">The following example sets the current SAMI style, specified by index.</span></span>


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



<span data-ttu-id="26d3c-146">Este exemplo chama os seguintes métodos na fonte de mídia SAMI:</span><span class="sxs-lookup"><span data-stu-id="26d3c-146">This example calls the following methods on the SAMI media source:</span></span>

-   <span data-ttu-id="26d3c-147">[**IMFSAMIStyle:: GetStyleCount**](/windows/desktop/api/mfidl/nf-mfidl-imfsamistyle-getstylecount) Obtém o número de estilos.</span><span class="sxs-lookup"><span data-stu-id="26d3c-147">[**IMFSAMIStyle::GetStyleCount**](/windows/desktop/api/mfidl/nf-mfidl-imfsamistyle-getstylecount) gets the number of styles.</span></span>
-   <span data-ttu-id="26d3c-148">[**IMFSAMIStyle:: Getstyles**](/windows/desktop/api/mfidl/nf-mfidl-imfsamistyle-getstyles) Obtém uma lista dos nomes de estilo, armazenados em um **PROPVARIANT**.</span><span class="sxs-lookup"><span data-stu-id="26d3c-148">[**IMFSAMIStyle::GetStyles**](/windows/desktop/api/mfidl/nf-mfidl-imfsamistyle-getstyles) gets a list of the style names, stored in a **PROPVARIANT**.</span></span>
-   <span data-ttu-id="26d3c-149">[**IMFSAMIStyle:: Setselecionadostyle**](/windows/desktop/api/mfidl/nf-mfidl-imfsamistyle-setselectedstyle) define um estilo por nome.</span><span class="sxs-lookup"><span data-stu-id="26d3c-149">[**IMFSAMIStyle::SetSelectedStyle**](/windows/desktop/api/mfidl/nf-mfidl-imfsamistyle-setselectedstyle) sets a style by name.</span></span>

<span data-ttu-id="26d3c-150">A lista de nomes de estilo também é armazenada no descritor de apresentação, no atributo [**MF \_ PD \_ Sami de \_ estilo**](mf-pd-sami-stylelist-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="26d3c-150">The list of style names is also stored on the presentation descriptor, in the [**MF\_PD\_SAMI\_STYLELIST**](mf-pd-sami-stylelist-attribute.md) attribute.</span></span>

## <a name="related-topics"></a><span data-ttu-id="26d3c-151">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="26d3c-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="26d3c-152">Fontes de mídia e coletores</span><span class="sxs-lookup"><span data-stu-id="26d3c-152">Media Sources and Sinks</span></span>](media-sources-and-sinks.md)
</dt> <dt>

[<span data-ttu-id="26d3c-153">Formatos de mídia compatíveis com o Media Foundation</span><span class="sxs-lookup"><span data-stu-id="26d3c-153">Supported Media Formats in Media Foundation</span></span>](supported-media-formats-in-media-foundation.md)
</dt> </dl>

 

 



