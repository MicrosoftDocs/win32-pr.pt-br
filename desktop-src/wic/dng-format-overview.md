---
description: Este tópico fornece informações sobre o codec DNG nativo disponível por meio do WIC (Windows Imaging Component).
ms.assetid: 6F87A47D-E54A-42D9-92DC-2411803278AA
title: Visão geral do formato DNG
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e32719e3fa9f45802058708e83635e52e287524496ae49f13f2168362358a7ea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118204373"
---
# <a name="dng-format-overview"></a>Visão geral do formato DNG

\[Algumas informações estão relacionadas ao produto pré-lançado, que pode ser substancialmente modificado antes de ser lançado comercialmente. A Microsoft não oferece garantias, expressas ou implícitas, das informações aqui fornecidas.\]

Este tópico fornece informações sobre o codec DNG nativo disponível por meio do WIC (Windows Imaging Component).

-   [Identidade do Codec](#codec-identity)
-   [Decodificação](#decoding)

## <a name="codec-identity"></a>Identidade do Codec

A tabela a seguir fornece informações de identificação de codec.



|     Componente          |  Descrição                                         |
|------------------------|------------------------------------------------------|
| Nomes formais         | DNG (Digital Negative)                               |
| Extensões de nome de arquivo | .dng                                                 |
| Tipos MIME           | image/DNG                                            |
| Suporte à especificação  | Especificação DNG (Digital Negative) Versão 1.4.0.0 |



 

A tabela a seguir lista os GUIDs usados para identificar os componentes nativos do codec DNG.



| Componente        | Nome amigável             | GUID                                |
|------------------|---------------------------|-------------------------------------|
| Formato do contêiner | GUID \_ ContainerFormatAdng | f3ff6d0d-38c0-41c4-b1fe1f3824f17b84 |
| Decodificador          | CLSID \_ WICAdngDecoder     | 981d9411-909e-42a7-8f5da747ff052edb |



 

## <a name="decoding"></a>Decodificação

A API de decodificação do WIC foi projetada para ser independente de codec e a decodificação de imagem para codecs habilitados para WIC é essencialmente a mesma. Para obter mais informações sobre decodificação de imagem, consulte Visão [geral de decodificação.](-wic-creating-decoder.md) Para obter mais informações sobre como usar dados de imagem decodificados, consulte Visão geral das [fontes de bitmap](-wic-bitmapsources.md).

O decodificador não dá suporte à decodificação de dados brutos do sensor e dá suporte apenas a arquivos com uma representação de imagem não bruta inserida em um IFD com NewSubFileType igual a 1.

 

 



