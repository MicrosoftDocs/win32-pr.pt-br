---
description: Este tópico fornece informações sobre o codec TIFF nativo disponível por meio Windows Imaging Component (WIC).
ms.assetid: 021AAF33-A89E-4336-AEB1-1A0D79A14C75
title: Visão geral do formato TIFF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81b28dfcc85dac21e95e6c76118d2db57cb74a08
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444417"
---
# <a name="tiff-format-overview"></a>Visão geral do formato TIFF

Este tópico fornece informações sobre o codec TIFF nativo disponível por meio Windows Imaging Component (WIC).

-   [Identidade do Codec](#codec-identity)
-   [Codificação](#encoding)
    -   [Opções do codificador](#encoder-options)
-   [Decodificação](#decoding)

## <a name="codec-identity"></a>Identidade do Codec

A tabela a seguir fornece informações de identificação de codec.



|   Componente            |   Descrição                   |
|------------------------|---------------------------------|
| Nomes formais         | TIFF |
| Extensões de nome de arquivo | tiff, tif                       |
| Tipos MIME           | image/tiff, image/tif           |
| Suporte à especificação  | Especificação TIFF 6.0          |



 

A tabela a seguir lista os GUIDs usados para identificar os componentes de codec TIFF nativos.



| Componente        | Nome amigável             | GUID                                 |
|------------------|---------------------------|--------------------------------------|
| Formato do contêiner | Contêiner \_ GUIDFormatTiff | 163bcc30-e2e9-4f0b-961da3e9fdb788a3  |
| Decodificador          | CLSID \_ WICTiffDecoder     | b54e85d9-fe23-499f-8b886es7137502b |
| Codificador          | CLSID \_ WICTiffEncoder     | 0131be10-2001-4c5f-a9b0cc88fab64ce8  |



 

## <a name="encoding"></a>Codificação

A API de codificação WIC foi projetada para ser independente de codec e a codificação de imagem para codecs habilitados para WIC é essencialmente a mesma. Para obter mais informações sobre a codificação de imagem usando a API WIC, consulte a [Visão geral de codificação](-wic-creating-encoder.md).

### <a name="encoder-options"></a>Opções do codificador

Os codecs habilitados para WIC diferem no nível da opção de codificação. As opções do codificador refletem as funcionalidades de um codificador de imagem e cada codec nativo dá suporte a um conjunto dessas opções de codificador. As opções de codificador podem ser opções básicas com suporte do WIC disponíveis para todos os códigos habilitados para WIC (embora não necessariamente com suporte) ou opções específicas de codec projetadas pelo codec de formato de imagem. Para gerenciar essas opções de codificação durante o processo de codificação, o WIC usa a interface [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) . Para obter mais informações sobre como usar a interface **IPropertyBag2** para codificação WIC, consulte a Visão geral [de codificação](-wic-creating-encoder.md).

O codec TIFF usa opções básicas do WIC. A tabela a seguir lista as opções do codificador WIC com suporte pelo codec TIFF nativo.

| Nome da propriedade         | Vartype | Intervalo de valores | Valor Padrão    |
|-----------------------|---------|-------------|------------------|
| CompressionQuality    | VT \_ R4  | 0 - 1.0     | 0                |
| TiffCompressionMethod | VT \_ UI1 | [**WICTiffCompressionOption**](/windows/desktop/api/Wincodec/ne-wincodec-wictiffcompressionoption) | [**WICTiffCompressionDontCare**](/windows/desktop/api/Wincodec/ne-wincodec-wictiffcompressionoption) |

Se uma opção de codificador estiver presente na lista de opções [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) à qual o codec não dá suporte, ela será ignorada.

### <a name="compressionquality-option"></a>Opção CompressionQuality

Especifica a qualidade de compactação desejada. 0.0 indica o esquema de compactação menos eficiente disponível. Normalmente, esse esquema resulta em uma codificação mais rápida, mas em uma saída maior. Um valor de 1,0 especifica o esquema de compactação mais eficiente disponível. Normalmente, esse esquema resulta em uma codificação mais longa, mas produz uma saída menor.

O valor padrão é 0.

### <a name="tiffcompressionmethod-option"></a>Opção TiffCompressionMethod

Especifica o método de compactação TIFF.

O valor padrão é [**WICTiffCompressionDontCare.**](/windows/desktop/api/Wincodec/ne-wincodec-wictiffcompressionoption)

## <a name="decoding"></a>Decodificação

As APIs de decodificação do WIC foram projetadas para serem independentes de codec e a decodificação de imagem para codecs habilitados para WIC é essencialmente a mesma. Para obter mais informações sobre decodificação de imagem, consulte Visão [geral de decodificação.](-wic-creating-decoder.md) Para obter mais informações sobre como usar dados de imagem decodificados, consulte Visão geral das [fontes de bitmap](-wic-bitmapsources.md).

 

 
