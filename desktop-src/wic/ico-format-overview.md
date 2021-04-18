---
description: Este tópico fornece informações sobre o codec do Native ICO disponível por meio do Windows Imaging Component (WIC).
ms.assetid: EF28956E-7156-4BAE-8805-C64B8C8ADE50
title: Visão geral do formato ICO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d370497e9231d6deb8d1793a26a53565b5cd99c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105763068"
---
# <a name="ico-format-overview"></a>Visão geral do formato ICO

Este tópico fornece informações sobre o codec do Native ICO disponível por meio do Windows Imaging Component (WIC).

## <a name="codec-identity"></a>Identidade do codec

A tabela a seguir fornece informações de identificação do codec.



|                        |                   |
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

 

 



