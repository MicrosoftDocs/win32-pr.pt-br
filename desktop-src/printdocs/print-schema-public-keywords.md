---
description: Este artigo especifica as palavras-chave públicas que são definidas para o esquema de impressão e seu uso para PrintCapabilities e PrintTicket.
ms.assetid: ff966475-626d-4a48-9349-e60454d47c57
title: Imprimir palavras-chave públicas do esquema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fbcab9ce943b7f344ce12c378252bc07c69260f75c607b36f7af54c107d3f84a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119886356"
---
# <a name="print-schema-public-keywords"></a>Imprimir palavras-chave públicas do esquema

Este tópico não é atual. Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

A seção a seguir especifica as palavras-chave públicas que são definidas para o esquema de impressão.

## <a name="print-schema-public-keywords-usage-for-print-capabilities"></a>Imprimir o uso de palavras-chave públicas do esquema para recursos de impressão

Palavras-chave especificadas em palavras-chave públicas de PrintCapabilities podem aparecer em um documento de recursos de impressão. Para obter mais informações sobre como essas palavras-chave interagem com a tecnologia PrintCapabilities, consulte [visão geral da seção PrintCapabilities](overview-of-the-printcapabilities.md) .

Palavras-chave públicas específicas do PrintTicket não devem aparecer em um documento de PrintCapabilities.

## <a name="print-schema-public-keywords-usage-for-printticket"></a>Imprimir o uso de palavras-chave públicas do esquema para PrintTicket

Palavras-chave especificadas em palavras-chave públicas PrintTicket podem aparecer em um PrintTicket. As palavras-chave PrintTicket são implementadas como um tipo de elemento de propriedade. Para obter mais informações sobre como essas palavras-chave interagem com a tecnologia PrintTicket, consulte [informações de configuração não relacionadas à seção PrintCapabilities](configuration-information-not-related-to-printcapabilities.md) .

Palavras-chave especificadas em palavras-chave públicas de PrintCapabilities podem aparecer em um PrintTicket, dependendo da implementação do PrintTicket em um aplicativo e/ou driver. Isso fornece seleções para atributos de dispositivo definidos no documento PrintCapabilities. Para obter mais informações sobre a interação entre as palavras-chave de PrintCapabilities e o PrintTicket, consulte a [finalidade da seção PrintTicket](purpose-of-the-printticket.md) .

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Especificação de esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



