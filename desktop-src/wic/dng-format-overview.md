---
description: Este tópico fornece informações sobre o codec DNG nativo disponível por meio do Windows Imaging Component (WIC).
ms.assetid: 6F87A47D-E54A-42D9-92DC-2411803278AA
title: Visão geral do formato DNG
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63f766356f7c13d7b2bb25adab5411ae55c2735f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104296812"
---
# <a name="dng-format-overview"></a>Visão geral do formato DNG

\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente. A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]

Este tópico fornece informações sobre o codec DNG nativo disponível por meio do Windows Imaging Component (WIC).

-   [Identidade do codec](#codec-identity)
-   [Decodificação](#decoding)

## <a name="codec-identity"></a>Identidade do codec

A tabela a seguir fornece informações de identificação do codec.



|                        |                                                      |
|------------------------|------------------------------------------------------|
| Nome (s) formal (es)         | Negativo digital (DNG)                               |
| Extensão (s) de nome de arquivo | .dng                                                 |
| Tipo (s) MIME           | imagem/DNG                                            |
| Suporte à especificação  | Especificação de DNG (digital negativo) versão 1.4.0.0 |



 

A tabela a seguir lista os GUIDs usados para identificar os componentes nativos do codec DNG.



| Componente        | Nome amigável             | GUID                                |
|------------------|---------------------------|-------------------------------------|
| Formato do contêiner | \_CONTAINERFORMATADNG GUID | f3ff6d0d-38c0-41c4-b1fe1f3824f17b84 |
| Decodificador          | \_WICADNGDECODER CLSID     | 981d9411-909e-42a7-8f5da747ff052edb |



 

## <a name="decoding"></a>Decodificação

A API de decodificação de WIC é projetada para ser independente de codec e a decodificação de imagem para codecs habilitados para WIC é essencialmente a mesma. Para obter mais informações sobre a decodificação de imagem, consulte a [visão geral da decodificação](-wic-creating-decoder.md). Para obter mais informações sobre como usar dados de imagem decodificados, consulte a [visão geral de fontes de bitmap](-wic-bitmapsources.md).

O decodificador não dá suporte à decodificação de dados de sensor bruto e só dá suporte a arquivos com uma representação de imagem não bruta inserida em uma IFD com NewSubFileType igual a 1.

 

 



