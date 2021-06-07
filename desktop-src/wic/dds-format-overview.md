---
description: Fornece informações sobre o codec DDS nativo disponível por meio do WIC (Windows Imaging Component).
ms.assetid: 6CFDD674-C8AE-4F29-B2E5-C9C9431CB85A
title: Visão geral do formato DDS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f860a5759218575acb53be5f2142e71aa34e9554
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444947"
---
# <a name="dds-format-overview"></a>Visão geral do formato DDS

Este tópico fornece informações sobre o codec DDS nativo disponível por meio do WIC (Windows Imaging Component).

## <a name="codec-identity"></a>Identidade do Codec

A tabela a seguir fornece informações de identificação de codec.



| Componente              | Descrição        |
|------------------------|--------------------|
| Nomes formais         | DirectDraw Surface |
| Extensões de nome de arquivo | Dds                |
| tipo MIME              | image/vnd-ms.dds   |



 

A tabela a seguir lista os GUIDs usados para identificar os componentes nativos do codec do DDS.



| Componente        | Nome amigável            | GUID                                |
|------------------|--------------------------|-------------------------------------|
| Formato do contêiner | Contêiner \_ GUIDFormatDds | 9967cb95-2e85-4ac8-8ca283d7ccd425c9 |
| Decodificador          | CLSID \_ WICDdsDecoder     | 9053699f-a341-429d-9e90ee437cf80c73 |
| Codificador          | CLSID \_ WICDdsEncoder     | a61dde94-66ce-4ac1-881b71680588895e |



 

## <a name="pixel-format-support"></a>Suporte ao formato de pixel

Observe que o formato DDS dá suporte a qualquer [**valor DXGI \_ FORMAT válido.**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) No entanto, o codec DDS do WIC dá suporte apenas a arquivos de decodificação e codificação que contêm os seguintes formatos:

-   FORMATO DXGI \_ \_ BC1 \_ UNORM
-   FORMATO DXGI \_ \_ BC2 \_ UNORM
-   FORMATO DXGI \_ \_ BC3 \_ UNORM

## <a name="encoding"></a>Codificação

As APIs de codificação WIC são projetadas para serem independentes de codec e, portanto, a codificação de imagem para codecs habilitados para WIC é essencialmente a mesma. Para obter mais informações sobre a codificação de imagem usando a API WIC, consulte a [Visão geral de codificação](-wic-creating-encoder.md).

O formato de arquivo DDS tem requisitos exclusivos que surgem de seu suporte para conceitos como mipmaps e matrizes de textura. Para controlar totalmente a codificação de imagem DDS, você deve usar a interface [**IWICDdsEncoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicddsencoder) para definir parâmetros de codificação específicos do DDS.

## <a name="decoding"></a>Decodificação

As APIs de decodificação do WIC foram projetadas para serem independentes de codec e a decodificação de imagem para codecs habilitados para WIC é essencialmente a mesma. Para obter mais informações sobre decodificação de imagem, consulte Visão [geral de decodificação.](-wic-creating-decoder.md) Para obter mais informações sobre como usar dados de imagem decodificados, consulte Visão geral das [fontes de bitmap](-wic-bitmapsources.md).

## <a name="block-compressed-data-access"></a>Bloquear o acesso a dados compactados

Além de dar suporte às interfaces de codec padrão do WIC, o decodificador DDS fornece acesso direto aos dados compactados de bloco nativo usando as interfaces específicas de DDS, [**IWICDdsDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicddsdecoder) e [**IWICDdsFrameDecode.**](/windows/desktop/api/Wincodec/nn-wincodec-iwicddsframedecode) Para usar essas interfaces, chame QueryInterface de [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) e [**IWICBitmapFrameDecode,**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)respectivamente.

 

 
