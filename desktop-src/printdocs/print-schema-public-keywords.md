---
description: Este artigo especifica as palavras-chave públicas que são definidas para o esquema de impressão e seu uso para PrintCapabilities e PrintTicket.
ms.assetid: ff966475-626d-4a48-9349-e60454d47c57
title: Imprimir palavras-chave públicas do esquema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0878ced6b011393479657a4fcdd4b7b7f9a2b62a
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112407139"
---
# <a name="print-schema-public-keywords"></a>Imprimir palavras-chave públicas do esquema

Este tópico não é atual. Para obter as informações mais atuais, consulte a [Especificação de Esquema de Impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

A seção a seguir especifica as palavras-chave públicas que são definidas para o esquema de impressão.

## <a name="print-schema-public-keywords-usage-for-print-capabilities"></a>Uso de palavras-chave públicas de esquema de impressão para funcionalidades de impressão

Palavras-chave especificadas em Palavras-chave públicas PrintCapabilities PODEM aparecer em um documento Funcionalidades de Impressão. Para obter mais informações sobre como essas palavras-chave interagem com a tecnologia PrintCapabilities, consulte Visão geral [da seção PrintCapabilities.](overview-of-the-printcapabilities.md)

Palavras-chave públicas específicas para PrintTicket SHOULD NÃO devem aparecer em um documento PrintCapabilities.

## <a name="print-schema-public-keywords-usage-for-printticket"></a>Uso de palavras-chave públicas de esquema de impressão para PrintTicket

Palavras-chave especificadas em Palavras-chave públicas printTicket PODEM aparecer em um PrintTicket. As palavras-chave PrintTicket são implementadas como um tipo de elemento Property. Para obter mais informações sobre como essas palavras-chave interagem com a tecnologia PrintTicket, consulte a seção Informações de configuração não relacionadas [a PrintCapabilities.](configuration-information-not-related-to-printcapabilities.md)

Palavras-chave especificadas em Palavras-chave públicas PrintCapabilities PODEM aparecer em um PrintTicket dependendo da implementação do PrintTicket em um aplicativo e/ou driver. Isso fornece seleções para atributos de dispositivo definidos no documento PrintCapabilities. Para obter mais informações sobre a interação entre palavras-chave PrintCapabilities e PrintTicket, consulte a seção Finalidade da [PrintTicket.](purpose-of-the-printticket.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Especificação de esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



