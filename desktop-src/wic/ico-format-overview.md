---
description: este tópico fornece informações sobre o codec da ICO nativa disponível por meio do componente de Windows Imaging (WIC).
ms.assetid: EF28956E-7156-4BAE-8805-C64B8C8ADE50
title: Visão geral do formato ICO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: caf90f0a31beb2d004dcb43e08cb0b6b1539021071ff2cb3302b3076033bc833
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118204066"
---
# <a name="ico-format-overview"></a>Visão geral do formato ICO

este tópico fornece informações sobre o codec da ICO nativa disponível por meio do componente de Windows Imaging (WIC).

## <a name="codec-identity"></a>Identidade do codec

A tabela a seguir fornece informações de identificação do codec.



|   Componente            | Descrição       |
|------------------------|-------------------|
| Nome (s) formal (es)         | Formato de ícone (ICO) |
| Extensão (s) de nome de arquivo | ico               |
| tipo MIME              | imagem/ico         |
| Suporte à especificação  |                   |



 

A tabela a seguir lista os GUIDs usados para identificar os componentes do codec do Native ICO.



| Componente        | Nome amigável            | GUID                                |
|------------------|--------------------------|-------------------------------------|
| Formato do contêiner | \_CONTAINERFORMATICO GUID | a3a860c4-338f-4c17-919afba4b5628f21 |
| Decodificador          | \_WICICODECODER CLSID     | c61bfcdf-2e0f-4aad-a8d7e06bafebcdfe |
| Codificador          | NÃO DISPONÍVEL            | NÃO DISPONÍVEL                       |



 

## <a name="encoding"></a>Codificação

O WIC não fornece um codificador de imagem ICO nativo.

## <a name="decoding"></a>Decodificação

A API de decodificação de WIC é projetada para ser independente de codec e a decodificação de imagem para codecs habilitados para WIC é essencialmente a mesma. Para obter mais informações sobre a decodificação de imagem, consulte a [visão geral da decodificação](-wic-creating-decoder.md). Para obter mais informações sobre como usar dados de imagem decodificados, consulte a [visão geral de fontes de bitmap](-wic-bitmapsources.md).

 

 



