---
description: Esta visão geral descreve os tópicos Esquema de Impressão e links para Referência de Esquema de Impressão. O esquema de impressão inclui as Palavras-chave de esquema de impressão e a Estrutura.
ms.assetid: d746bdd1-96c2-41f5-ad99-0b51c8ee8731
title: Referência de esquema de impressão herdado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81a8f417d20913563cfd4a52ba51d21b516e73f0
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112407129"
---
# <a name="legacy-print-schema-reference"></a>Referência de esquema de impressão herdado

Este tópico não é atual. Para obter as informações mais atuais, consulte a [Especificação de Esquema de Impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

O Esquema de Impressão e as tecnologias relacionadas estão disponíveis no Microsoft .NET Framework 3.0, Microsoft Windows Vista e versões posteriores.

O Esquema de Impressão fornece um formato baseado em XML para expressar e organizar um grande conjunto de propriedades que descrevem um formato de trabalho ou PrintCapabilities de maneira hierárquica.

O Esquema de Impressão é um termo que inclui dois componentes, As Palavras-chave de esquema de impressão e a Estrutura de Esquema de Impressão. O documento Palavras-chave de esquema de impressão é um esquema público que define um conjunto de instâncias de elemento que podem ser usadas para descrever atributos de dispositivo e formatação de trabalho de impressão. A Estrutura de Esquema de Impressão é um esquema público que define uma coleção hierarquicamente estruturada de tipos de elemento XML e especifica como os tipos de elemento podem ser usados juntos.

As palavras-chave de esquema de impressão e a Estrutura de Esquema de Impressão formam a base para duas tecnologias relacionadas ao esquema de impressão, o esquema PrintCapabilities e o esquema PrintTicket.

É importante ter em mente que uma das metas do Esquema de Impressão é dar suporte a extensões de esquema por provedores. Ou seja, os provedores não estão restritos a usar apenas as instâncias Property, Feature, Option ou ParameterInit definidas nas Palavras-chave de esquema de impressão nas tecnologias criadas na Estrutura de Esquema de Impressão. Instâncias de elemento específicas do provedor podem ser intercaladas livremente em instâncias de elemento definidas nas Palavras-chave de esquema de impressão. O único requisito é que as instâncias de propriedade específicas do provedor (ou seja, privadas) devem pertencer a um namespace claramente associado ao provedor.

-   [Tela de fundo do esquema de impressão](print-schema-background.md)

-   [Tecnologias de Schema-Related impressão](print-schema-related-technologies.md)

-   [Termos usados no esquema de impressão](terms-used-in-the-print-schema.md)

-   [Sintaxe do esquema de impressão](syntax-of-the-print-schema.md)

-   [Resumo dos tipos de elemento](summary-of-element-types.md)

-   [Estrutura de esquema de impressão](print-schema-framework.md)

-   [Imprimir palavras-chave públicas do esquema](print-schema-public-keywords.md)

-   [Esquema PrintCapabilities e construção de documentos](printcapabilities-schema-and-document-construction.md)

-   [Esquema PrintTicket e construção de documento](printticket-schema-and-document-construction.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Especificação de esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



