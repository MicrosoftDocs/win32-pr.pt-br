---
description: Este tópico fornece informações sobre o codec BMP nativo disponível por meio do Windows Imaging Component (WIC).
ms.assetid: 85AC5A30-A915-439E-A10F-B2833DDA995C
title: Visão geral do formato BMP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3492189f80b43915bab94a7ea8359f2e5950f7c5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103662292"
---
# <a name="bmp-format-overview"></a>Visão geral do formato BMP

Este tópico fornece informações sobre o codec BMP nativo disponível por meio do Windows Imaging Component (WIC).

## <a name="codec-identity"></a>Identidade do codec

A tabela a seguir fornece informações de identificação do codec.



|                        |                       |
|------------------------|-----------------------|
| Nome (s) formal (es)         | Formato de bitmap do Windows |
| Extensão (s) de nome de arquivo | BMP, DIB              |
| tipo MIME              | image/bmp             |
| Suporte à especificação  | Especificação BMP V5  |



 

A tabela a seguir lista os GUIDs usados para identificar os componentes do codec BMP nativos.



| Componente        | Nome amigável            | GUID                                |
|------------------|--------------------------|-------------------------------------|
| Formato do contêiner | \_CONTAINERFORMATBMP GUID | 0af1d87e-fcfe-4188-bdeba7906471cbe3 |
| Decodificador          | \_WICBMPDECODER CLSID     | 6b462062-7cbf-400d-9fdb813dd10f2778 |
| Codificador          | \_WICBMPENCODER CLSID     | 69be8bb4-d66d-47c8-865aed1589433782 |



 

## <a name="encoding"></a>Codificação

A API de codificação do WIC é projetada para ser independente de codec e, portanto, a codificação de imagem para codecs habilitados para WIC é essencialmente a mesma. Para obter mais informações sobre codificação de imagem usando a API do WIC, consulte [visão geral da codificação](-wic-creating-encoder.md).

### <a name="encoder-options"></a>Opções de codificador

Os codecs habilitados para WIC diferem no nível de opção de codificação. As opções de codificador refletem os recursos de um codificador de imagem e cada codec nativo dá suporte a um conjunto dessas opções de codificador. As opções de codificador podem ser opções básicas compatíveis com o WIC disponíveis para todos os códigos habilitados para WIC (embora não sejam necessariamente suportados) ou opções específicas de codec projetadas pelo codec de formato de imagem. Para gerenciar essas opções de codificação durante o processo de codificação, o WIC usa a interface [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) . Para obter mais informações sobre como usar a interface **IPropertyBag2** para a codificação WIC, consulte [visão geral da codificação](-wic-creating-encoder.md).

A tabela a seguir lista as opções de codificador do WIC com suporte do codec BMP nativo.



| Nome da Propriedade               | VARTYPE      | Intervalo de valores                      | Valor padrão      |
|-----------------------------|--------------|----------------------------------|--------------------|
| **EnableV5Header32bppBGRA** | **BOOL do VT \_** | **VARIANTE \_ true/Variant \_ false** | **VARIANTE \_ falso** |



 

### <a name="enablev5header32bppbgra"></a>EnableV5Header32bppBGRA

Especifica se os dados de codificação devem ser permitidos no \_ formato de pixel WICPIXELFORMAT32BPPBGRA GUID. Se essa opção for definida como **Variant \_ true**, o bmp será gravado com um cabeçalho BITMAPV5HEADER.

O valor padrão é **Variant \_ false**.

Se uma opção de codificador estiver presente na lista de opções de IPropertyBag2 para a qual o codec não dá suporte, ela será ignorada.

Observação para arquivos BMP de 16 bits e de 32 bits do Windows, o codec BMP ignora qualquer canal alfa, pois muitos arquivos de imagem herdados contêm dados inválidos nesse canal extra. A partir do Windows 8, os arquivos BMP de 32 bits do Windows gravados usando o **BITMAPV5HEADER** com conteúdo de canal alfa válido são lidos como WICPixelFormat32bppBGRA

## <a name="decoding"></a>Decodificação

A API de decodificação de WIC é projetada para ser independente de codec e a decodificação de imagem para codecs habilitados para WIC é essencialmente a mesma. Para obter mais informações sobre a decodificação de imagem, consulte a [visão geral da decodificação](-wic-creating-decoder.md). Para obter mais informações sobre como usar dados de imagem decodificados, consulte a [visão geral de fontes de bitmap](-wic-bitmapsources.md).

 

 
