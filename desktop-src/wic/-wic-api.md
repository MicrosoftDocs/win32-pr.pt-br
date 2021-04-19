---
description: O Windows Imaging Component (WIC) fornece uma API baseada em Component Object Model (COM) para uso em C e C++.
ms.assetid: 74b14b5e-70e9-410f-a6e6-d8873a5f4fa4
title: Visão geral da API do WIC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f86e5a876010e52489adac9baa7ce57fdfdf80f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105802135"
---
# <a name="wic-api-overview"></a>Visão geral da API do WIC

O Windows Imaging Component (WIC) fornece uma API baseada em Component Object Model (COM) para uso em C e C++. A API do WIC expõe uma variedade de funcionalidades relacionadas a imagens, incluindo:

-   Codecs internos para os formatos de imagem da Web padrão.
-   Suporte interno para formatos de metadados padrão.
-   Ampla gama de suporte a formato de pixel.
-   Suporte de alta cor; incluindo um intervalo estendido de 30 bits, alta precisão de 30 bits e formatos de pixel de grande precisão de 48 bits e de gama ampla.
-   Estrutura extensível para codecs de imagem, formatos de pixel e formatos de metadados.

Este tópico contém os tópicos a seguir.

-   [Arquivos de cabeçalho do WIC](#wic-header-files)
-   [Arquivos de biblioteca](#library-files)
-   [Fábricas de classe](#class-factories)
-   [Componentes de geração de imagens](#imaging-components)
-   [Consulte também](#see-also)

## <a name="wic-header-files"></a>Arquivos de cabeçalho do WIC

As APIs do WIC são definidas nos seguintes arquivos de cabeçalho e IDL (linguagem de definição de interface):



| Arquivo              | Descrição                                          |
|-------------------|------------------------------------------------------|
| wincodec. h        | Define as versões C e C++ das APIs primárias do WIC.  |
| wincodec. idl      | Define as interfaces WIC primárias.                  |
| wincodecsdk. h     | Define as versões C e C++ das APIs de WIC de metadados. |
| wincodecsdk. idl   | Define as interfaces de metadados do WIC.                 |
| wincodec \_ proxy. h | Define as exportações de proxy do WIC.                       |



 

Para usar o WIC, seus aplicativos devem incluir wincodec. h e/ou wincodecsdk. h, dependendo da API de que seu aplicativo precisa.

## <a name="library-files"></a>Arquivos de biblioteca

Os arquivos de biblioteca do WIC:



| Arquivo              | Descrição                                                            |
|-------------------|------------------------------------------------------------------------|
| WindowsCodecs. lib | Biblioteca de importação fornecida pelo SDK (Software Development Kit) do Windows. |
| windowscodecs.dll | Biblioteca de implementação de estoque fornecida pelo sistema operacional.         |



 

Para vincular as APIs do WIC, seu aplicativo deve incluir windowscodec. lib como uma dependência de vinculador adicional.

## <a name="class-factories"></a>Fábricas de classe

A tabela a seguir descreve as duas fábricas de classes COM que as APIs do WIC fornecem para a criação de componentes do WIC.



| Interface de fábrica                                               | Descrição                                                                                                                                             |
|-----------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)     | Fábrica de classes primária para desenvolvimento de aplicativos usando componentes de WIC. Essa fábrica cria componentes como decodificadores de imagem, codificadores e fluxos.   |
| [**IWICComponentFactory**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwiccomponentfactory) | Fábrica de classes direcionada para desenvolvedores de componentes do WIC. Os componentes criados a partir dessa fábrica são usados principalmente no desenvolvimento de manipulador de metadados e de codec. |



 

Para criar uma fábrica de classes, use a função com [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) . O exemplo a seguir demonstra a criação da fábrica de imagens do WIC.


```C++
// Initialize COM
CoInitialize(NULL);

// The factory pointer
IWICImagingFactory *pFactory = NULL;

// Create the COM imaging factory
HRESULT hr = CoCreateInstance(
    CLSID_WICImagingFactory,
    NULL,
    CLSCTX_INPROC_SERVER,
    IID_PPV_ARGS(&pFactory)
);
```



## <a name="imaging-components"></a>Componentes de geração de imagens

As APIs do WIC fornecem vários tipos de componentes de geração de imagens. A tabela a seguir descreve alguns dos componentes do WIC comuns. Para obter uma lista completa dos componentes disponíveis, consulte [interfaces WIC](-wic-codec-ifaces.md).



| Tipo de componente                                                      | Descrição                                                                                                   |
|---------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| [**Bitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap)                             | Representa uma representação na memória gravável de um [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource). |
| [**Decodificador**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)                     | Usado para decodificar dados de imagem de um fluxo em um formato útil para processamento de imagem.                    |
| [**Fita**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)                     | Grava dados de imagem em um fluxo.                                                                                |
| [**Stream**](/windows/desktop/api/Wincodec/nn-wincodec-iwicstream)                             | Usado para ler e gravar dados de um arquivo, recurso de rede, um bloco de memória e assim por diante.                      |
| [**Conversor de formato**](/windows/desktop/api/Wincodec/nn-wincodec-iwicformatconverter)          | Usado para converter de um formato de pixel para outro.                                                             |
| [**Leitor de consulta de metadados**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) | Usado para ler metadados de uma imagem ou quadro de imagem.                                                             |
| [**Gravador de consulta de metadados**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter) | Usado para gravar metadados em um quadro de imagem ou imagem.                                                            |



 

## <a name="see-also"></a>Consulte Também

[Referências](-wic-codec-reference.md)


[Amostras e exemplos de código](-wic-samples.md)


 

 
