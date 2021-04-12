---
description: Este tópico fornece informações sobre o codec de GIF nativo disponível por meio do Windows Imaging Component (WIC).
ms.assetid: CAEC8F92-8971-42B4-BED8-A6A93522D11E
title: Visão geral do formato GIF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6f592b50300edf79c71ff4050a2c0d5aeba8b23
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170452"
---
# <a name="gif-format-overview"></a>Visão geral do formato GIF

Este tópico fornece informações sobre o codec de GIF nativo disponível por meio do Windows Imaging Component (WIC).

## <a name="codec-identity"></a>Identidade do codec

A tabela a seguir fornece informações de identificação do codec.



|                        |                                       |
|------------------------|---------------------------------------|
| Nome (s) formal (es)         | Graphics Interchange Format 89A (GIF) |
| Extensão (s) de nome de arquivo | GIF                                   |
| tipo MIME              | image/gif                             |
| Suporte à especificação  | Especificação de GIF 89A/89m             |



 

A tabela a seguir lista os GUIDs usados para identificar os componentes do codec GIF nativo.



| Componente        | Nome amigável            | GUID                                |
|------------------|--------------------------|-------------------------------------|
| Formato do contêiner | \_CONTAINERFORMATGIF GUID | 1f8a5601-7d4d-4cbd-9c821bc8d4eeb9a5 |
| Decodificador          | \_WICGIFDECODER CLSID     | 381dda3c-9ce9-4834-a23e1f98f8fc52be |
| Codificador          | \_WICGIFENCODER CLSID     | 114f5598-0b22-40a0-86a1c83ea495adbd |



 

## <a name="encoding"></a>Codificação

A API de codificação do WIC é projetada para ser independente de codec e a codificação de imagem para codecs habilitados para WIC é essencialmente a mesma. Para obter mais informações sobre codificação de imagem usando a API do WIC, consulte [visão geral da codificação](-wic-creating-encoder.md).

### <a name="encoder-options"></a>Opções de codificador

Os codecs habilitados para WIC diferem no nível de opção de codificação. As opções de codificador refletem os recursos de um codificador de imagem e cada codec nativo dá suporte a um conjunto dessas opções de codificador. As opções de codificador podem ser opções básicas compatíveis com o WIC disponíveis para todos os códigos habilitados para WIC (embora não sejam necessariamente suportados) ou opções específicas de codec projetadas pelo codec de formato de imagem. Para gerenciar essas opções de codificação durante o processo de codificação, o WIC usa a interface [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) . Para obter mais informações sobre como usar a interface **IPropertyBag2** para codificação WIC, consulte [visão geral da codificação](-wic-creating-encoder.md).

O codificador GIF não oferece suporte a nenhuma opção básica de WIC e não fornece opções de codificador personalizadas. Se uma opção de codificador estiver na lista de opções [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) , ela será ignorada.

## <a name="decoding"></a>Decodificação

A API de decodificação de WIC é projetada para ser independente de codec e a decodificação de imagem para codecs habilitados para WIC é essencialmente a mesma. Para obter mais informações sobre a decodificação de imagem, consulte a [visão geral da decodificação](-wic-creating-decoder.md). Para obter mais informações sobre como usar dados de imagem decodificados, consulte a [visão geral de fontes de bitmap](-wic-bitmapsources.md).

 

 
