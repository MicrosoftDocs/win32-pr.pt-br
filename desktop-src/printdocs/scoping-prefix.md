---
description: Este tópico não é atual. Para obter as informações mais atuais, consulte a especificação do esquema de impressão.
ms.assetid: 4bad85d7-a933-43fe-9d79-4835d92c82d6
title: Prefixo de escopo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef74be192671124872e19e87973a266da4a09226
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/05/2021
ms.locfileid: "103837692"
---
# <a name="scoping-prefix"></a>Prefixo de escopo

Este tópico não é atual. Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Um prefixo de escopo é um rótulo textual acrescentado previamente a uma palavra-chave de esquema para fornecer um escopo contextual. Isso permite a contratação de um contexto específico e bem compreendido para palavras-chave de maneira predefinida. O recurso de esquema de impressão, o ParameterDef, o ParameterInit e o ParameterRef e os elementos de palavra-chave de propriedade de nível raiz devem ter um dos seguintes prefixos de escopo: "trabalho", "documento" ou "página".

## <a name="interpretation-of-the-scoping-prefix-with-printticket-content"></a>Interpretação do prefixo de escopo com conteúdo PrintTicket

O PrintTicket pode ser dividido em três níveis de conteúdo que representam o trabalho de alto nível, os documentos no trabalho e as páginas de cada documento. Esses níveis são classificados de acordo com a especificidade; o nível do trabalho é mais geral, o nível do documento e, em seguida, o nível da página é mais específico. Um trabalho consiste em um ou mais documentos e um documento consiste em uma ou mais páginas.

## <a name="job-level-prefix"></a>Prefixo de nível de trabalho

Um tíquete de nível de trabalho contém todas as configurações de formatação de trabalho destinadas a aplicar a um trabalho inteiro. Todos os elementos com prefixos de escopo de "trabalho", "documento" ou "página" são permitidos em um tíquete de nível de trabalho.

As configurações prefixadas de "documento" e "página" especificadas em um tíquete de nível de trabalho serão aplicadas automaticamente aos tíquetes de nível de documento e de página.

## <a name="document-level-prefix"></a>Prefixo de nível de documento

O tíquete de nível de documento incorpora qualquer configuração de formatação de trabalho destinada a aplicar a um ou mais documentos em um trabalho. Isso pode incluir as configurações especificadas anteriormente no tíquete de nível de trabalho. Somente elementos com prefixos de escopo de "Document" ou "Page" são permitidos em um tíquete de nível de documento.

Um tíquete de nível de documento pode conter configurações prefixadas de documento especificadas anteriormente pelo tíquete de nível de trabalho.

## <a name="page-level-prefix"></a>Prefixo de nível de página

O tíquete de nível de página incorpora qualquer configuração de formatação de trabalho destinada a se aplicar a uma ou mais páginas de um trabalho (não limitado a um único documento). Isso pode incluir as configurações especificadas anteriormente no tíquete de nível de trabalho ou de documento. Somente elementos com prefixos de escopo de "Page" são permitidos em um tíquete de nível de página.

Um tíquete de nível de página pode conter configurações prefixadas de "página" especificadas anteriormente pelo tíquete de nível de trabalho e/ou pelo tíquete de nível de documento.

## <a name="prefix-usage-within-a-printticket-or-print-capabilities-document"></a>Uso de prefixo em um documento de PrintTicket ou recursos de impressão

Os documentos PrintTicket e PrintCapabilities não devem conter várias palavras-chave que diferem apenas no prefixo de escopo.? Por exemplo, um documento PrintCapabilities não deve ter JobInputBin e PageInputBin especificados.? No entanto, um documento de recursos de impressão pode ter JobDuplexAllDocumentsContiguously e DocumentDuplex especificados porque eles são considerados diferentes recursos, pois apresentam comportamento diferente.? Este exemplo também é verdadeiro para um único PrintTicket.

## <a name="prefix-conflict-management"></a>Gerenciamento de conflitos de prefixo

Um conflito de palavra-chave entre as configurações é definido como, o mesmo elemento de esquema de impressão de nível raiz indicado pelo atributo XML "Name", que aparece em Tíquetes de vários níveis. Se não houver conflito, um elemento com escopo de prefixo poderá ser empurrado para baixo ou herdado de um tíquete mais geral para um tíquete mais específico. Se houver um conflito, a configuração do tíquete mais específico terá precedência. Ou seja, as configurações por página em um tíquete de nível de página substituem as configurações idênticas por página em um tíquete de nível de documento ou de trabalho. Da mesma forma, as configurações de documento no tíquete de nível de documento têm precedência sobre as configurações de documento no tíquete de nível de trabalho.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Especificação de esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



