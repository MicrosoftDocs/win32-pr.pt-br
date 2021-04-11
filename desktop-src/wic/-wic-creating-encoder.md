---
description: Um codificador grava dados de imagem em um fluxo. Os codificadores podem compactar, criptografar e alterar os pixels da imagem de várias maneiras antes de gravá-los no fluxo.
ms.assetid: e1e3a9d9-209b-46a6-92da-5570476507cf
title: Visão geral da codificação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3be46aa73082071deb69fdd402f42866b18ef0aa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171526"
---
# <a name="encoding-overview"></a>Visão geral da codificação

Um codificador grava dados de imagem em um fluxo. Os codificadores podem compactar, criptografar e alterar os pixels da imagem de várias maneiras antes de gravá-los no fluxo. O uso de alguns codificadores resulta em compensações — por exemplo, JPEG, que compensa informações de cores para uma melhor compactação. Outros codificadores não resultam em tais perdas — por exemplo, bitmap (BMP). Como muitos codecs usam tecnologia proprietária para obter melhor compactação e fidelidade de imagem, os detalhes sobre como uma imagem é codificada são até o desenvolvedor do codec.

Este tópico inclui as seções a seguir.

-   [IWICBitmapEncoder](#iwicbitmapencoder)
-   [IWICBitmapFrameEncode](#iwicbitmapframeencode)
-   [Exemplo de codificação TIFF](#tiff-encoding-example)
-   [Uso de opções de codificador](#encoder-options-usage)
-   [Opções de codificador](#encoder-options-usage)
-   [Exemplos de opções de codificador](#encoder-options-examples)
-   [Tópicos relacionados](#related-topics)

## <a name="iwicbitmapencoder"></a>IWICBitmapEncoder

[**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) é a interface principal para codificar uma imagem para o formato de destino e usada para serializar os componentes de uma imagem, como miniatura ([**SetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setthumbnail)) e frames ([**CreateNewFrame**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-createnewframe)), para o arquivo de imagem.

Como e quando a serialização ocorre é deixada para o desenvolvedor do codec. Cada bloco de dados individual no formato de arquivo de destino deve ser capaz de definir independentemente da ordem, mas novamente, essa é a decisão do desenvolvedor do codec. Quando o método [**Commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-commit) é chamado no entanto, as alterações na imagem não devem ser permitidas e o fluxo deve ser fechado.

## <a name="iwicbitmapframeencode"></a>IWICBitmapFrameEncode

[**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) é a interface para codificar os quadros individuais de uma imagem. Ele fornece métodos para definir componentes individuais de imagem de quadro, como miniaturas e quadros, bem como dimensões de imagem, DPI e formatos de pixel.

Quadros individuais podem ser codificados com metadados específicos do quadro para que o [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) forneça acesso a um gravador de metadados por meio do método [**GetMetadataQueryWriter**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-getmetadataquerywriter) .

O método [**Commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-commit) do quadro confirma todas as alterações no quadro individual e indica que as alterações feitas nesse quadro não devem mais ser aceitas.

## <a name="tiff-encoding-example"></a>Exemplo de codificação TIFF

No exemplo a seguir, uma imagem TIFF (Tagged Image File Format) é codificada usando [**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) e um [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode). A saída TIFF é personalizada usando o [**WICTiffCompressionOption**](/windows/desktop/api/Wincodec/ne-wincodec-wictiffcompressionoption) e o quadro de bitmap é inicializado usando as opções fornecidas. Depois que a imagem tiver sido criada usando [**WritePixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-writepixels), o quadro será confirmado por meio de [**Commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-commit) e a imagem será salva usando [**Commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-commit).


```C++
IWICImagingFactory *piFactory = NULL;
IWICBitmapEncoder *piEncoder = NULL;
IWICBitmapFrameEncode *piBitmapFrame = NULL;
IPropertyBag2 *pPropertybag = NULL;

IWICStream *piStream = NULL;
UINT uiWidth = 640;
UINT uiHeight = 480;

HRESULT hr = CoCreateInstance(
                CLSID_WICImagingFactory,
                NULL,
                CLSCTX_INPROC_SERVER,
                IID_IWICImagingFactory,
                (LPVOID*) &piFactory);

if (SUCCEEDED(hr))
{
    hr = piFactory->CreateStream(&piStream);
}

if (SUCCEEDED(hr))
{
    hr = piStream->InitializeFromFilename(L"output.tif", GENERIC_WRITE);
}

if (SUCCEEDED(hr))
{
   hr = piFactory->CreateEncoder(GUID_ContainerFormatTiff, NULL, &piEncoder);
}

if (SUCCEEDED(hr))
{
    hr = piEncoder->Initialize(piStream, WICBitmapEncoderNoCache);
}

if (SUCCEEDED(hr))
{
    hr = piEncoder->CreateNewFrame(&piBitmapFrame, &pPropertybag);
}

if (SUCCEEDED(hr))
{        
    // This is how you customize the TIFF output.
    PROPBAG2 option = { 0 };
    option.pstrName = L"TiffCompressionMethod";
    VARIANT varValue;    
    VariantInit(&varValue);
    varValue.vt = VT_UI1;
    varValue.bVal = WICTiffCompressionZIP;      
    hr = pPropertybag->Write(1, &option, &varValue);        
    if (SUCCEEDED(hr))
    {
        hr = piBitmapFrame->Initialize(pPropertybag);
    }
}

if (SUCCEEDED(hr))
{
    hr = piBitmapFrame->SetSize(uiWidth, uiHeight);
}

WICPixelFormatGUID formatGUID = GUID_WICPixelFormat24bppBGR;
if (SUCCEEDED(hr))
{
    hr = piBitmapFrame->SetPixelFormat(&formatGUID);
}

if (SUCCEEDED(hr))
{
    // We're expecting to write out 24bppRGB. Fail if the encoder cannot do it.
    hr = IsEqualGUID(formatGUID, GUID_WICPixelFormat24bppBGR) ? S_OK : E_FAIL;
}

if (SUCCEEDED(hr))
{
    UINT cbStride = (uiWidth * 24 + 7)/8/***WICGetStride**_/;
    UINT cbBufferSize = uiHeight _ cbStride;

    BYTE *pbBuffer = new BYTE[cbBufferSize];

    if (pbBuffer != NULL)
    {
        for (UINT i = 0; i < cbBufferSize; i++)
        {
            pbBuffer[i] = static_cast<BYTE>(rand());
        }

        hr = piBitmapFrame->WritePixels(uiHeight, cbStride, cbBufferSize, pbBuffer);

        delete[] pbBuffer;
    }
    else
    {
        hr = E_OUTOFMEMORY;
    }
}

if (SUCCEEDED(hr))
{
    hr = piBitmapFrame->Commit();
}    

if (SUCCEEDED(hr))
{
    hr = piEncoder->Commit();
}

if (piFactory)
    piFactory->Release();

if (piEncoder)
    piEncoder->Release();

if (piBitmapFrame)
    piBitmapFrame->Release();

if (pPropertybag)
    pPropertybag->Release();

if (piStream)
    piStream->Release();

return hr;
```



## <a name="encoder-options-usage"></a>Uso de opções de codificador

Codificadores diferentes para formatos diferentes precisam expor opções diferentes para a forma como uma imagem é codificado. O Windows Imaging Component (WIC) fornece um mecanismo consistente para expressar se as opções de codificação são necessárias e, ao mesmo tempo, permitir que os aplicativos funcionem com vários codificadores sem a necessidade de conhecimento de um formato específico. Isso é feito fornecendo um parâmetro [IPropertyBag](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768196(v=vs.85)) no método [**CreateNewFrame**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-createnewframe) e o método [**Initialize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-initialize) .

A fábrica de componentes fornece um ponto de criação fácil para a criação de um recipiente de propriedades de opções de codificador. Os codecs podem usar esse serviço se precisarem fornecer um conjunto simples, intuitivo e não conflitante de opções de codificador. O recipiente de propriedades de geração de imagens deve ser inicializado durante a criação com todas as opções de codificador relevantes para esse codec. Para as opções de codificador do conjunto canônico, o intervalo de valores será imposto na gravação. Para necessidades mais avançadas, os codecs devem gravar sua própria implementação do recipiente de propriedades.

Um aplicativo recebe o recipiente de opções do codificador durante a criação do quadro e deve configurar quaisquer valores antes de inicializar o quadro do codificador. Para um aplicativo controlado por interface do usuário, ele pode oferecer uma interface do usuário fixa para as opções canônicas de codificador e uma exibição avançada para as opções restantes. As alterações podem ser feitas uma de cada vez por meio do método Write e qualquer erro será relatado por meio de IErrorLog. O aplicativo de interface do usuário sempre deve ler novamente e exibir todas as opções depois de fazer uma alteração caso a alteração tenha causado um efeito em cascata. Um aplicativo deve estar preparado para manipular a inicialização de quadro com falha para codecs que fornecem apenas relatórios de erros mínimos por meio de seu recipiente de propriedades.

## <a name="encoder-options"></a>Opções de codificador

Um aplicativo pode esperar encontrar o seguinte conjunto de opções de codificador. As opções de codificador refletem os recursos de um codificador e o formato de contêiner subjacente e, portanto, por sua natureza não é realmente independente de codec. Quando possível, as novas opções devem ser normalizadas para que possam ser aplicadas a novos codecs que surgirem.



| Nome da Propriedade      | VARTYPE  | Valor                                                                     | Codecs aplicáveis |
|--------------------|----------|---------------------------------------------------------------------------|-------------------|
| ImageQuality       | VT \_ R4   | 0-1,0                                                                     | JPEG, HDPhoto     |
| CompressionQuality | VT \_ R4   | 0-1,0                                                                     | TIFF              |
| Lossless           | BOOL do VT \_ | **verdadeiro**, **falso**                                                       | HDPhoto           |
| BitmapTransform    | \_UI1 VT  | [**WICBitmapTransformOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions) | JPEG              |



 

ImageQualty de 0,0 significa a menor rendição de fidelidade possível e 1,0 significa a maior fidelidade, que também pode significar sem perdas dependendo do codec.

CompressionQuality de 0,0 significa o esquema de compactação menos eficiente disponível, normalmente resultando em uma codificação rápida, mas uma saída maior. Um valor de 1,0 significa o esquema mais eficiente disponível, normalmente demorando mais tempo para codificar, mas produzindo saída menor. Dependendo dos recursos do codec, esse intervalo pode ser mapeado para um conjunto discreto de métodos de compactação disponíveis.

Sem perdas significa que o codec codifica a imagem como sem perdas, sem perda de dados de imagem. Se o Lossless estiver habilitado, o ImageQuality será ignorado.

Além das opções de codificador genérico acima, os codecs fornecidos com o WIC dão suporte às seguintes opções. Se um codec tiver a necessidade de oferecer suporte a uma opção consistente com o uso nesses codecs fornecidos, é recomendável fazer isso.



| Nome da Propriedade           | VARTYPE           | Valor                                                                             | Codecs aplicáveis |
|-------------------------|-------------------|-----------------------------------------------------------------------------------|-------------------|
| InterlaceOption         | BOOL do VT \_          | Ativar/desativar                                                                            | PNG               |
| FilterOption            | \_UI1 VT           | [**WICPngFilterOption**](/windows/desktop/api/Wincodec/ne-wincodec-wicpngfilteroption)                       | PNG               |
| TiffCompressionMethod   | \_UI1 VT           | [**WICTiffCompressionOption**](/windows/desktop/api/Wincodec/ne-wincodec-wictiffcompressionoption)           | TIFF              |
| Luminância               | \_Matriz VT UI4/VT \_ | 64 entradas (DCT)                                                                  | JPEG              |
| Crominância             | \_Matriz VT UI4/VT \_ | 64 entradas (DCT)                                                                  | JPEG              |
| JpegYCrCbSubsampling    | \_UI1 VT           | [**WICJpegYCrCbSubsamplingOption**](/windows/desktop/api/Wincodec/ne-wincodec-wicjpegycrcbsubsamplingoption) | JPEG              |
| SuppressApp0            | BOOL do VT \_          |                                                                                   | JPEG              |
| EnableV5Header32bppBGRA | BOOL do VT \_          | Ativar/desativar                                                                            | BMP               |



 

Use **VT \_ vazio** para indicar que **\* não \* está definido** como o padrão. Se propriedades adicionais forem definidas, mas sem suporte, o codificador deverá ignorá-las; Isso permite que os aplicativos codifiquem menos lógica se desejam uma funcionalidade que pode ou não estar presente.

## <a name="encoder-options-examples"></a>Exemplos de opções de codificador

No [exemplo de codificação TIFF](#tiff-encoding-example) acima, uma opção de codificador específico é definida. O membro *pstrName* da estrutura PROPBAG2 é definido como o nome de propriedade apropriado e a variante é definida como o VarType correspondente e o valor desejado — nesse caso, um membro da enumeração [**WICTiffCompressionOption**](/windows/desktop/api/Wincodec/ne-wincodec-wictiffcompressionoption) .


```C++
if (SUCCEEDED(hr))
{
    hr = piEncoder->CreateNewFrame(&piBitmapFrame, &pPropertybag);
}

if (SUCCEEDED(hr))
{        
    // This is how you customize the TIFF output.
    PROPBAG2 option = { 0 };
    option.pstrName = L"TiffCompressionMethod";
    VARIANT varValue;    
    VariantInit(&varValue);
    varValue.vt = VT_UI1;
    varValue.bVal = WICTiffCompressionZIP;      
    hr = pPropertybag->Write(1, &option, &varValue);        
    if (SUCCEEDED(hr))
    {
        hr = piBitmapFrame->Initialize(pPropertybag);
    }
}
```



Para usar as opções de codificador padrão, basta inicializar o quadro de bitmap com o recipiente de propriedades retornado quando o quadro foi criado.


```C++
if (SUCCEEDED(hr))
{
    hr = piEncoder->CreateNewFrame(&piBitmapFrame, &pPropertybag);
}

if (SUCCEEDED(hr))
{        
    // Accept the default encoder options.
    if (SUCCEEDED(hr))
    {
        hr = piBitmapFrame->Initialize(pPropertybag);
    }
}
```



Também é possível eliminar o recipiente de propriedades quando não há nenhuma opção de codificador sendo considerada.


```C++
if (SUCCEEDED(hr))
{
    hr = piEncoder->CreateNewFrame(&piBitmapFrame, 0);
}

if (SUCCEEDED(hr))
{        
    // No encoder options.
    if (SUCCEEDED(hr))
    {
        hr = piBitmapFrame->Initialize(0);
    }
}
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

**Conceitua**
</dt> <dt>

[Visão geral do Windows Imaging Component](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[Visão geral da decodificação](-wic-creating-decoder.md)
</dt> <dt>

**Outros recursos**
</dt> <dt>

[Como escrever um CODEC de WIC-Enabled](-wic-howtowriteacodec.md)
</dt> </dl>

 

 
