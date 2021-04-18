---
description: O Windows Imaging Component (WIC) foi atualizado com novas versões do Windows. Este tópico fornece uma breve introdução a esses novos recursos.
ms.assetid: 710B71CE-6FCC-46DA-A65C-6E4FC6A04275
title: Novidades no WIC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84b8b3783ac2fd8ef6a971f785cec80f868a6b80
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105813634"
---
# <a name="whats-new-in-wic"></a>Novidades no WIC

O Windows Imaging Component (WIC) foi atualizado com novas versões do Windows. Este tópico fornece uma breve introdução a esses novos recursos.

## <a name="whats-new-for-windows-10-version-1507"></a>O que há de novo para o Windows 10, versão 1507

### <a name="access-to-low-level-jpeg-data-for-wic-decoding-and-encoding"></a>Acesso a dados JPEG de baixo nível para decodificação e codificação de WIC

A partir do Windows 10, versão 1507, o WIC fornece acesso a estruturas de dados JPEG de baixo nível, incluindo tabelas Huffman e quantização. Para mais informações, consulte os seguintes tópicos:

-   Interface [**IWICJpegFrameDecode**](/windows/win32/api/Wincodec/nn-wincodec-iwicjpegframedecode)
-   Interface [**IWICJpegFrameEncode**](/windows/win32/api/Wincodec/nn-wincodec-iwicjpegframeencode)

### <a name="jpeg-indexing"></a>Indexação JPEG

A indexação JPEG é uma técnica que melhora significativamente o desempenho de acessar aleatoriamente pequenas subregiãos de uma imagem JPEG grande, ao custo de algum uso de memória adicional. A indexação JPEG pode ser utilizada por qualquer chamador do WIC.

A interface [**ID2D1ImageSourceFromWic**](/windows/win32/api/d2d1_3/nn-d2d1_3-id2d1imagesourcefromwic) foi projetada para aproveitar a indexação JPEG se ela estiver ativada. Por exemplo, a API ID2D1ImageSource solicitará apenas as seções necessárias da imagem em um cenário, como panorâmica e zoom para uma imagem de grande resolução. Para mais informações, consulte os seguintes tópicos:

-   Método [**IWICJpegFrameDecode:: Setindexing**](/windows/win32/api/Wincodec/nf-wincodec-iwicjpegframedecode-setindexing)
-   Interface [**ID2D1ImageSourceFromWic**](/windows/win32/api/d2d1_3/nn-d2d1_3-id2d1imagesourcefromwic)

## <a name="whats-new-for-windows-81"></a>O que há de novo para Windows 8.1

### <a name="support-for-jpeg-ycbcr-images"></a>Suporte para imagens JPEG YCbCr

A partir do Windows 8.1, o WIC fornece suporte para decodificação, transformação e codificação de dados de imagem JPEG Y'CbCr em seu formato nativo. Isso permite que os aplicativos diminuam significativamente o tempo de processamento e o consumo de memória para determinadas operações de geração de imagens ao trabalhar com JPEGs codificados em Y'CbCr. Para mais informações, consulte os seguintes tópicos:

-   [Direct2D](-wic-sample-d2d-viewer.md)[YCbCr Effect](../direct2d/ycbcr-effect.md)
-   Interface [**IWICPlanarBitmapSourceTransform**](/windows/win32/api/Wincodec/nn-wincodec-iwicplanarbitmapsourcetransform)
-   Interface [**IWICPlanarBitmapFrameEncode**](/windows/win32/api/Wincodec/nn-wincodec-iwicplanarbitmapframeencode)

### <a name="support-for-block-compressed-formats-dds-files"></a>Suporte para formatos compactados de bloco (arquivos DDS)

A partir do Windows 8.1, o WIC adiciona um novo codec que dá suporte a imagens DDS codificadas nos seguintes formatos: \_ formato dxgi \_ BC1 \_ UNORM, \_ formato dxgi \_ BC2 \_ UNORM e \_ formato dxgi \_ BC3 \_ UNORM. Os dados compactados por bloco DDS podem ser acessados em um formulário decodificado usando interfaces WIC padrão ou acessados diretamente usando novas interfaces específicas do DDS. Para mais informações, consulte os seguintes tópicos:

-   Interface [**IWICDdsDecoder**](/windows/win32/api/Wincodec/nn-wincodec-iwicddsdecoder)
-   Interface [**IWICDdsEncoder**](/windows/win32/api/Wincodec/nn-wincodec-iwicddsencoder)

## <a name="whats-new-for-windows-8"></a>O que há de novo no Windows 8

No Windows 8, o WIC foi atualizado com vários recursos novos. A versão atualizada do WIC também está disponível no Windows 7 e no Windows Server 2008 R2 por meio da [atualização da plataforma para o Windows 7](../direct3darticles/platform-update-for-windows-7.md), que está disponível por meio da [atualização da plataforma para o Windows 7](https://support.microsoft.com/kb/2670838).

### <a name="improved-direct2d-integration"></a>Integração do Direct2D aprimorada

O WIC no Windows 8 fornece essas APIs para melhorar a integração do Direct2D com o WIC:

-   [**IWICImageEncoder**](/windows/win32/api/Wincodec/nn-wincodec-iwicimageencoder) -uma nova interface que pode codificar o conteúdo do Direct2D [**ID2D1Image**](/windows/win32/api/d2d1/nn-d2d1-id2d1image) para um [IWICBitmapFrameEncode](-wic-imp-iwicbitmapframeencode.md). Os métodos dessa interface usam um ponteiro para [**WICImageParameters**](/windows/win32/api/Wincodec/ns-wincodec-wicimageparameters), que são parâmetros para controlar a codificação.
-   [**IWICImagingFactory2**](/windows/win32/api/Wincodec/nn-wincodec-iwicimagingfactory2) – nova fábrica de WIC com o método [**CreateImageEncoder**](/windows/win32/api/Wincodec/nf-wincodec-iwicimagingfactory2-createimageencoder) . Essa interface herda da fábrica de WIC original, [**IWICImagingFactory**](/windows/win32/api/Wincodec/nn-wincodec-iwicimagingfactory), e é criada da mesma maneira.

### <a name="changes-to-bmp-codec-alpha-support"></a>Alterações no suporte a BMP codec Alpha

O WIC no Windows 8 dá suporte ao carregamento de arquivos de imagem [**BITMAPV5HEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapv5header) como imagens formatadas por [WICPixelFormat32bppBGRA](-wic-codec-native-pixel-formats.md). Além disso, o codificador BMP dá suporte a um novo booliano, opção de codificador "EnableV5Header32bppBGRA", que instrui o codificador a gravar um **BITMAPV5HEADER** com os dados da imagem 32bppBGRA.

Para obter mais informações sobre formatos BMP, consulte [visão geral do formato BMP](bmp-format-overview.md).

### <a name="new-pixel-formats"></a>Novos formatos de pixel

O WIC no Windows 8 define esses novos formatos de pixel:

-   \_WICPIXELFORMAT32BPPRGB GUID
-   \_WICPIXELFORMAT64BPPRGB GUID
-   \_WICPIXELFORMAT96BPPRGBFLOAT GUID
-   \_WICPIXELFORMAT64BPPPRGBAHALF GUID

> [!Note]  
> O codec interno TIFF retornará \_ dados GUID WICPixelFormat96bppRGBFloat. Os outros três formatos não são usados por codecs internos.

 

### <a name="restrictions-to-component-extensibility-in-appcontainer"></a>Restrições à extensibilidade de componentes no AppContainer

Ao executar em um processo do AppContainer, que inclui todos os aplicativos da Windows Store, o WIC usará apenas componentes fornecidos pelo Windows, independentemente de os componentes adicionais estarem instalados no sistema. O aplicativo que não está em execução no AppContainer não é afetado.

Os aplicativos não precisam fazer alterações de código para serem executados em um AppContainger, mas o sinalizador [**WICComponentEnumerateOptions**](/windows/win32/api/Wincodec/ne-wincodec-wiccomponentenumerateoptions) e os parâmetros GUID do fornecedor não terão nenhum efeito. O WIC não carregará uma imagem se ela não puder ser decodificada por um codec fornecido pelo Windows e chamar o método [**CreateComponentEnumerator**](/windows/win32/api/Wincodec/nf-wincodec-iwicimagingfactory-createcomponentenumerator) retornará apenas os componentes fornecidos do Windows.

### <a name="changes-to-clsid_wicpngdecoder-and-png-decoder-color-context-support"></a>Alterações em CLSID \_ WICPngDecoder e suporte a contexto de cor do decodificador png

**CLSID \_ do WICPngDecoder1** foi adicionado com o mesmo GUID que **CLSID \_ WICPngDecoder** e **CLSID \_ WICPngDecoder2** foi adicionado.

Quando compilado no SDK do Windows 8, **CLSID \_ WICPngDecoder** é \# definido como **CLSID \_ WICPngDecoder2** para promover aplicativos compilados recentemente usando o novo comportamento de decodificador de png. Os aplicativos devem continuar a especificar **CLSID \_ WICPngDecoder**.

A especificação do **CLSID \_ WICPngDecoder2** criará uma versão do DEcodificador png do WIC que gerará um [**IWICColorContext**](/windows/win32/api/Wincodec/nn-wincodec-iwiccolorcontext) de blocos cHRM e gama. Isso permite que esses metadados de espaço de cores sejam usados com outras APIs do Windows para o gerenciamento de cores da imagem de origem. Um **IWICColorContext** não será gerado a partir das partes gama e cHRM se uma parte iCCP estiver presente, se uma parte do sRGB estiver presente ou se as partes gama e cHRM indicarem um espaço de cores sRGB.

Um aplicativo pode especificar **CLSID \_ WICPngDecoder1** para criar uma versão do DEcodificador png do WIC que não gera um [**IWICColorContext**](/windows/win32/api/Wincodec/nn-wincodec-iwiccolorcontext) a partir das partes gama e cHRM. Isso corresponde ao comportamento do decodificador PNG nas versões anteriores do Windows.

### <a name="changes-to-wincodec_sdk_version"></a>Alterações na \_ versão do SDK do WINCODEC \_

Quando compilado no SDK do Windows 8, **a \_ \_ versão do SDK do WINCODEC** é \# definida como **WINCODEC \_ SDK \_ VERSION2** para promover aplicativos compilados recentemente usando o novo comportamento de decodificador de png. Caso contrário, ele será \# definido como **WINCODEC \_ SDK \_ versão**. Os aplicativos devem continuar a especificar a **\_ \_ versão do SDK do WINCODEC**.

Especificar **a \_ \_ versão do SDK do WINCODEC** ao chamar o [**\_ proxy WICCreateImagingFactory**](-wic-codec-wiccreateimagingfactory-proxy.md) para criar o Imaging Factory faz com que **CLSID \_ WICPngDecoder2** seja criado em vez de **CLSID \_ WICPngDecoder1** do método [**CreateDecoder**](/windows/win32/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoder) e suas variantes. Além disso, um enumerador de informações de componente de decodificador retornará informações de componente **\_ WICPngDecoder2 CLSID** , mas não informações de **CLSID \_ WICPngDecoder1** .

Especificar **WINCODEC \_ SDK \_ versão** fará com que o **CLSID \_ WICPngDecoder1** seja usado em vez do **CLSID \_ WICPngDecoder2** nos casos acima.

### <a name="changes-to-clsid_wicimagingfactory"></a>Alterações em CLSID \_ WICImagingFactory

**CLSID \_ do WICImagingFactory1** foi adicionado com o mesmo GUID que **CLSID \_ WICImagingFactory** e **CLSID \_ WICImagingFactory2** foi adicionado.

Quando compilado no SDK do Windows 8, **CLSID \_ WICImagingFactory** é \# definido como **CLSID \_ WICImagingFactory2** para promover aplicativos compilados recentemente usando o novo comportamento de decodificador de png. Os aplicativos devem continuar a especificar **CLSID \_ WICImagingFactory**.

Especificar **CLSID \_ WICImagingFactory2** ao chamar [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) para criar o Imaging Factory faz com que **CLSID \_ WICPngDecoder2** seja criado em vez de **CLSID \_ WICPngDecoder1** do método [**CreateDecoder**](/windows/win32/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoder) e suas variantes. Além disso, um enumerador de informações de componente de decodificador retornará informações de componente **\_ WICPngDecoder2 CLSID** , mas não informações de **CLSID \_ WICPngDecoder1** .

Especificar **CLSID \_ WICImagingFactory1** fará com que **CLSID \_ WICPngDecoder1** seja usado em vez de **CLSID \_ WICPngDecoder2** nos casos acima.

## <a name="whats-new-for-windows-7"></a>O que há de novo no Windows 7

No Windows 7, o WIC foi atualizado com vários recursos novos. Este tópico fornece uma breve introdução a esses novos recursos.

### <a name="updates-to-the-tiff-codec"></a>Atualizações para o codec TIFF

O codec TIFF do WIC foi atualizado para o Windows 7 para dar suporte a vários recursos que não têm suporte da versão anterior do WIC.

-   Suporte para arquivos TIFF grandes.
-   Decodificar imagens TIFF em ladrilhos.
-   Decodificar imagens TIFF planas (Planar).
-   Decodificar imagens TIFF codificadas em JPEG.

### <a name="progressive-decoding"></a>Decodificação progressiva

A decodificação progressiva fornece a capacidade de decodificar e renderizar de forma incremental partes de uma imagem antes de concluir o download da imagem inteira. Esse recurso melhora muito a experiência do usuário ao exibir imagens da Internet, pois o usuário não precisa aguardar que toda a imagem seja baixada antes que a decodificação possa começar. Com a decodificação progressiva, os usuários podem ver uma visualização de imagem com os dados disponíveis por muito tempo antes de a imagem inteira ser baixada. Esse recurso é essencial para qualquer aplicativo usado para exibir imagens da Internet ou de fontes de dados com largura de banda limitada.

Para obter mais informações, consulte a [visão geral da decodificação progressiva](-wic-progressive-decoding.md).

### <a name="extended-metadata-support-for-jpeg-png-and-gif"></a>Suporte a metadados estendidos para JPEG, PNG e GIF

No Windows 7, o WIC estendeu seu suporte de metadados para imagens JPEG, PNG e GIF.

-   Adicionado suporte para propriedades GIF e GIF animadas.
-   Manipuladores de metadados do JPG expandidos para dar suporte a metadados de crominância, luminância e comentário.
-   Manipuladores de metadados PNG expandidos para dar suporte aos metadados tIME, sRGB, iCCP, sua, cHRM, iTXt, bKGD e gAMA.
-   Adicionados novos manipuladores de metadados 8BIM para metadados ResolutionInfo e metadados de síntese de IPTC.
-   Novos manipuladores de metadados adicionados para o descritor de tela lógica (LSD), descritor de imagem (IMD), GCE (extensões de controle de gráficos) e metadados de extensões de aplicativo (APE has).
-   Suporte para metadados que abrangem blocos de APPn.

### <a name="multi-threaded-apartment-support"></a>Suporte a multi-threaded apartment

Os objetos dentro de um apartamento multithread (MTA) podem ser chamados simultaneamente por qualquer número de threads no MTA, permitindo melhor desempenho em sistemas de vários núcleos e em certos cenários de servidor. Além disso, os codecs do WIC que residem em um MTA podem chamar outros objetos que residem no MTA sem o custo de marshaling associado à chamada entre threads que residem em apartments STA diferentes. No Windows 7, todos os codecs de WIC na caixa foram atualizados para dar suporte a MTA, incluindo JPEG, TIFF, PNG, GIF, ICO e BMP. É altamente recomendável que os codecs sejam gravados para dar suporte ao MTA. Os codecs que não dão suporte a MTA causarão percebido de desempenho significativas em aplicativos multithread devido ao marshaling. Habilitar o suporte ao MTA requer que a sincronização adequada seja implementada no codec. A implementação exata dessas técnicas de sincronização está além do escopo deste documento. Uma referência geral para a sincronização de objetos COM Component Object Model (COM) é fornecida abaixo.

### <a name="metadata-working-group-implementations"></a>Implementações do grupo de trabalho de metadados

Atualmente, há uma variedade de formatos de armazenamento de metadados que contêm propriedades sobrepostas, sem nenhum padrão industrial claro ou orientação sobre métodos consistentes para ler e gravar esses formatos de metadados. Para ajudar com essa variedade de formatos e propriedades, o grupo de trabalho de metadados (MWG) foi formado. O objetivo do MWG é fornecer diretrizes que garantam a interoperabilidade entre uma ampla variedade de plataformas, aplicativos e dispositivos. As diretrizes estabelecidas pelo MWG se aplicam aos campos de metadados XMP, EXIF e IPTC e aos formatos de imagem JPEG, TIFF e PSD.

No Windows 7, o manipulador de metadados de fotos e a camada de política de metadados foram atualizados para ler e gravar metadados de imagem de acordo com as diretrizes estabelecidas pelo MWG. Para obter mais informações sobre o grupo de trabalho de metadados (MWG), veja as [diretrizes de metadados estabelecidas](https://s3.amazonaws.com/software.tagthatphoto.com/docs/mwg_guidance.pdf).

### <a name="windows-7-features-supported-on-windows-vista-and-windows-server-2008"></a>Recursos do Windows 7 com suporte no Windows Vista e no Windows Server 2008

A [atualização de plataforma para o Windows Vista](../win7ip/platform-update-for-windows-vista-portal.md) é um conjunto de bibliotecas de tempo de execução que permite aos desenvolvedores direcionar aplicativos para o Windows 7 e o Windows Vista. A atualização de plataforma para o Windows Server 2008 é um conjunto de bibliotecas de tempo de execução que permite aos desenvolvedores direcionar aplicativos para o Windows Server 2008 R2 e o Windows Server 2008. A atualização da plataforma para Windows Vista e a atualização da plataforma para Windows Server 2008 estarão disponíveis para todos os clientes do Windows Vista e do Windows Server 2008 por meio de Windows Update. Aplicativos de terceiros que exigem atualização de plataforma para Windows Vista ou atualização de plataforma para Windows Server 2008 podem ter Windows Update detectar se a atualização necessária está instalada; Se não estiver, Windows Update será baixado e instalado em segundo plano. Para obter mais informações sobre as duas atualizações, consulte Atualização de plataforma para Windows Vista

 

 
