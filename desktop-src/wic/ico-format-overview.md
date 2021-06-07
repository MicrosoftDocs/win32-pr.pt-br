---
description: Este tópico fornece informações sobre o codec de ICO nativo disponível por meio Windows Imaging Component (WIC).
ms.assetid: EF28956E-7156-4BAE-8805-C64B8C8ADE50
title: Visão geral do formato ICO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 329a53a3b5d386c5e5386141162c608dc9db1ec0
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444459"
---
# <a name="ico-format-overview"></a>Visão geral do formato ICO

Este tópico fornece informações sobre o codec de ICO nativo disponível por meio Windows Imaging Component (WIC).

## <a name="codec-identity"></a>Identidade do Codec

A tabela a seguir fornece informações de identificação de codec.



|   Componente            | Descrição       |
|------------------------|-------------------|
| Nomes formais         | Formato de ícone (ICO) |
| Extensões de nome de arquivo | Ico               |
| tipo MIME              | image/ico         |
| Suporte à especificação  |                   |



 

A tabela a seguir lista os GUIDs usados para identificar os componentes de codec de ICO nativos.



| Componente        | Nome amigável            | GUID                                |
|------------------|--------------------------|-------------------------------------|
| Formato do contêiner | Contêiner \_ GUIDFormatIco | a3a860c4-338f-4c17-919afba4b5628f21 |
| Decodificador          | CLSID \_ WICIcoDecoder     | c61bfcdf-2e0f-4aad-a8d7e06bafebcdfe |
| Codificador          | NÃO DISPONÍVEL            | NÃO DISPONÍVEL                       |



 

## <a name="encoding"></a>Codificação

O WIC não fornece um codificador de imagem de ICO nativo.

## <a name="decoding"></a>Decodificação

A API de decodificação do WIC foi projetada para ser independente de codec e a decodificação de imagem para codecs habilitados para WIC é essencialmente a mesma. Para obter mais informações sobre decodificação de imagem, consulte Visão [geral de decodificação.](-wic-creating-decoder.md) Para obter mais informações sobre como usar dados de imagem decodificados, consulte Visão geral das [fontes de bitmap](-wic-bitmapsources.md).

 

 



