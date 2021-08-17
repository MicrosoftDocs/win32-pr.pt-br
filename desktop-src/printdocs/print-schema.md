---
description: Esta visão geral descreve o esquema de impressão e links para imprimir tópicos de referência de esquema. O esquema de impressão inclui as palavras-chave do esquema de impressão e a estrutura.
ms.assetid: d746bdd1-96c2-41f5-ad99-0b51c8ee8731
title: Referência de esquema de impressão herdado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 540496004534dff3e66ce1c30415ccec14c6d7b31c59ecf2f79905c25d5e7861
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118470853"
---
# <a name="legacy-print-schema-reference"></a>Referência de esquema de impressão herdado

Este tópico não é atual. Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

o esquema de impressão e as tecnologias relacionadas estão disponíveis no microsoft .NET Framework 3,0, microsoft Windows Vista e versões posteriores.

O esquema de impressão fornece um formato baseado em XML para expressar e organizar um grande conjunto de propriedades que descrevem um formato de trabalho ou PrintCapabilities de uma maneira hierarquicamente estruturada.

O esquema de impressão é um termo abrangente que inclui dois componentes, as palavras-chave do esquema de impressão e a estrutura de esquema de impressão. O documento de palavras-chave do esquema de impressão é um esquema público que define um conjunto de instâncias de elemento que pode ser usado para descrever os atributos do dispositivo e a formatação do trabalho de impressão. A estrutura de esquema de impressão é um esquema público que define uma coleção hierarquicamente estruturada de tipos de elemento XML e especifica como os tipos de elemento podem ser usados juntos.

As palavras-chave do esquema de impressão e a estrutura de esquema de impressão formam a base para duas tecnologias de impressão relacionadas ao esquema, o esquema de PrintCapabilities e o esquema PrintTicket.

É importante ter em mente que uma das metas do esquema de impressão é dar suporte a extensões de esquema por provedores. Ou seja, os provedores não estão restritos a usar somente as instâncias de propriedade, recurso, opção ou ParameterInit definidas nas palavras-chave do esquema de impressão nas tecnologias criadas na estrutura de esquema de impressão. As instâncias de elemento específicas do provedor podem estar livremente intercaladas dentro das instâncias de elemento definidas nas palavras-chave do esquema de impressão. O único requisito é que as instâncias de propriedade específicas do provedor (ou seja, privadas) devem pertencer a um namespace que esteja claramente associado ao provedor.

-   [Plano de fundo do esquema de impressão](print-schema-background.md)

-   [Schema-Related tecnologias de impressão](print-schema-related-technologies.md)

-   [Termos usados no esquema de impressão](terms-used-in-the-print-schema.md)

-   [Sintaxe do esquema de impressão](syntax-of-the-print-schema.md)

-   [Resumo dos tipos de elementos](summary-of-element-types.md)

-   [Estrutura de esquema de impressão](print-schema-framework.md)

-   [Imprimir palavras-chave públicas do esquema](print-schema-public-keywords.md)

-   [Construção de esquema e documento de PrintCapabilities](printcapabilities-schema-and-document-construction.md)

-   [Construção de esquema e documento do PrintTicket](printticket-schema-and-document-construction.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Especificação de esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



