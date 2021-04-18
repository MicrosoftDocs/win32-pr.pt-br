---
description: Este tópico fornece informações sobre o codec TIFF nativo disponível por meio do Windows Imaging Component (WIC).
ms.assetid: 021AAF33-A89E-4336-AEB1-1A0D79A14C75
title: Visão geral do formato TIFF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db603857da892d4b699bb7df7d8b3e2ee5566326
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105781448"
---
# <a name="tiff-format-overview"></a>Visão geral do formato TIFF

Este tópico fornece informações sobre o codec TIFF nativo disponível por meio do Windows Imaging Component (WIC).

-   [Identidade do codec](#codec-identity)
-   [Codificação](#encoding)
    -   [Opções de codificador](#encoder-options)
-   [Decodificação](#decoding)

## <a name="codec-identity"></a>Identidade do codec

A tabela a seguir fornece informações de identificação do codec.



|                        |                                 |
|------------------------|---------------------------------|
| Nome (s) formal (es)         | TIFF |
| Extensão (s) de nome de arquivo | TIFF, TIF                       |
| Tipo (s) MIME           | imagem/TIFF, imagem/TIF           |
| Suporte à especificação  | Especificação TIFF 6,0          |



 

A tabela a seguir lista os GUIDs usados para identificar os componentes do codec TIFF nativo.



| Componente        | Nome amigável             | GUID                                 |
|------------------|---------------------------|--------------------------------------|
| Formato do contêiner | \_CONTAINERFORMATTIFF GUID | 163bcc30-e2e9-4f0b-961da3e9fdb788a3  |
| Decodificador          | \_WICTIFFDECODER CLSID     | b54e85d9-fe23-499f-8b886acea7137502b |
| Codificador          | \_WICTIFFENCODER CLSID     | 0131be10-2001-4c5f-a9b0cc88fab64ce8  |



 

## <a name="encoding"></a>Codificação

A API de codificação do WIC é projetada para ser independente de codec e a codificação de imagem para codecs habilitados para WIC é essencialmente a mesma. Para obter mais informações sobre codificação de imagem usando a API do WIC, consulte [visão geral da codificação](-wic-creating-encoder.md).

### <a name="encoder-options"></a>Opções de codificador

Os codecs habilitados para WIC diferem no nível de opção de codificação. As opções de codificador refletem os recursos de um codificador de imagem e cada codec nativo dá suporte a um conjunto dessas opções de codificador. As opções de codificador podem ser opções básicas compatíveis com o WIC disponíveis para todos os códigos habilitados para WIC (embora não sejam necessariamente suportados) ou opções específicas de codec projetadas pelo codec de formato de imagem. Para gerenciar essas opções de codificação durante o processo de codificação, o WIC usa a interface [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) . Para obter mais informações sobre como usar a interface **IPropertyBag2** para codificação WIC, consulte [visão geral da codificação](-wic-creating-encoder.md).

O codec TIFF usa opções básicas de WIC. A tabela a seguir lista as opções de codificador do WIC com suporte do codec TIFF nativo.

| Nome da Propriedade         | VARTYPE | Intervalo de valores | Valor padrão    |
|-----------------------|---------|-------------|------------------|
| CompressionQuality    | VT \_ R4  | 0-1,0     | 0                |
| TiffCompressionMethod | \_UI1 VT | [**WICTiffCompressionOption**](/windows/desktop/api/Wincodec/ne-wincodec-wictiffcompressionoption) | [**WICTiffCompressionDontCare**](/windows/desktop/api/Wincodec/ne-wincodec-wictiffcompressionoption) |

Se uma opção de codificador estiver presente na lista de opções de [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) para a qual o codec não dá suporte, ela será ignorada.

### <a name="compressionquality-option"></a>Opção CompressionQuality

Especifica a qualidade de compactação desejada. 0,0 indica o esquema de compactação menos eficiente disponível. Normalmente, esse esquema resulta em uma codificação mais rápida, mas uma saída maior. Um valor de 1,0 especifica o esquema de compactação mais eficiente disponível. Normalmente, esse esquema resulta em uma codificação mais longa, mas produz uma saída menor.

O valor padrão é 0.

### <a name="tiffcompressionmethod-option"></a>Opção TiffCompressionMethod

Especifica o método de compactação TIFF.

O valor padrão é [**WICTiffCompressionDontCare**](/windows/desktop/api/Wincodec/ne-wincodec-wictiffcompressionoption).

## <a name="decoding"></a>Decodificação

As APIs de decodificação de WIC são projetadas para serem independentes de codec e a decodificação de imagem para codecs habilitados para WIC é essencialmente a mesma. Para obter mais informações sobre a decodificação de imagem, consulte a [visão geral da decodificação](-wic-creating-decoder.md). Para obter mais informações sobre como usar dados de imagem decodificados, consulte a [visão geral de fontes de bitmap](-wic-bitmapsources.md).

 

 
