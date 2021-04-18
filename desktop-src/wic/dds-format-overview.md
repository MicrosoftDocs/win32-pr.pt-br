---
description: Fornece informações sobre o codec do DDS nativo disponível por meio do Windows Imaging Component (WIC).
ms.assetid: 6CFDD674-C8AE-4F29-B2E5-C9C9431CB85A
title: Visão geral do formato DDS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1c45222a66d5a250caaf46db465d2359e09b3e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105810657"
---
# <a name="dds-format-overview"></a>Visão geral do formato DDS

Este tópico fornece informações sobre o codec do DDS nativo disponível por meio do Windows Imaging Component (WIC).

## <a name="codec-identity"></a>Identidade do codec

A tabela a seguir fornece informações de identificação do codec.



|                        |                    |
|------------------------|--------------------|
| Nome (s) formal (es)         | Superfície do DirectDraw |
| Extensão (s) de nome de arquivo | DDS                |
| tipo MIME              | Image/VND-MS. DDS   |



 

A tabela a seguir lista os GUIDs usados para identificar os componentes do codec DDS nativo.



| Componente        | Nome amigável            | GUID                                |
|------------------|--------------------------|-------------------------------------|
| Formato do contêiner | \_CONTAINERFORMATDDS GUID | 9967cb95-2e85-4ac8-8ca283d7ccd425c9 |
| Decodificador          | \_WICDDSDECODER CLSID     | 9053699f-a341-429d-9e90ee437cf80c73 |
| Codificador          | \_WICDDSENCODER CLSID     | a61dde94-66ce-4ac1-881b71680588895e |



 

## <a name="pixel-format-support"></a>Suporte a formato de pixel

Observe que o formato DDS dá suporte a qualquer valor de [**\_ formato dxgi**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) válido. No entanto, o codec DDS do WIC dá suporte apenas à decodificação e à codificação de arquivos que contêm os seguintes formatos:

-   \_Formato dxgi \_ BC1 \_ UNORM
-   \_Formato dxgi \_ BC2 \_ UNORM
-   \_Formato dxgi \_ BC3 \_ UNORM

## <a name="encoding"></a>Codificação

As APIs de codificação do WIC são projetadas para serem independentes de codec e, portanto, a codificação de imagem para codecs habilitados para WIC é essencialmente a mesma. Para obter mais informações sobre codificação de imagem usando a API do WIC, consulte [visão geral da codificação](-wic-creating-encoder.md).

O formato de arquivo DDS tem requisitos exclusivos que surgem de seu suporte para conceitos como mipmaps e matrizes de textura. Para exercer total controle sobre a codificação de imagem DDS, você deve usar a interface [**IWICDdsEncoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicddsencoder) para definir parâmetros de codificação específicos do DDS.

## <a name="decoding"></a>Decodificação

As APIs de decodificação de WIC são projetadas para serem independentes de codec e a decodificação de imagem para codecs habilitados para WIC é essencialmente a mesma. Para obter mais informações sobre a decodificação de imagem, consulte a [visão geral da decodificação](-wic-creating-decoder.md). Para obter mais informações sobre como usar dados de imagem decodificados, consulte a [visão geral de fontes de bitmap](-wic-bitmapsources.md).

## <a name="block-compressed-data-access"></a>Bloquear acesso a dados compactados

Além de dar suporte às interfaces de codec padrão do WIC, o decodificador DDS fornece acesso direto aos dados compactados do bloco nativo usando as interfaces específicas do DDS, [**IWICDdsDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicddsdecoder) e [**IWICDdsFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicddsframedecode). Para usar essas interfaces, chame QueryInterface fora de [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) e [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode), respectivamente.

 

 
