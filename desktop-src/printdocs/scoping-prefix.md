---
description: Um prefixo de escopo é um rótulo textual pré-anexado a uma palavra-chave de esquema para fornecer um escopo contextual, incluindo Trabalho, Documento e Página.
ms.assetid: 4bad85d7-a933-43fe-9d79-4835d92c82d6
title: Prefixo de definição de scoping
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06ad23369d2b2c60c00752e4f5be31f6ad605e2814d0b7502d42ff79baa10977
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118234089"
---
# <a name="scoping-prefix"></a>Prefixo de definição de scoping

Este tópico não é atual. Para obter as informações mais atuais, consulte a [Especificação de Esquema de Impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Um prefixo de escopo é um rótulo textual pré-anexado a uma palavra-chave de esquema para fornecer um escopo contextual. Isso permite a acreção de um contexto específico e bem compreendido para palavras-chave de maneira predefinida. Recurso de esquema de impressão, ParameterDef, ParameterInit e ParameterRef e a palavra-chave Property de nível raiz Elements DEVEM ter um dos seguintes prefixos de escopo: "Job", "Document" ou "Page".

## <a name="interpretation-of-the-scoping-prefix-with-printticket-content"></a>Interpretação do prefixo de definição de tela com o conteúdo printTicket

O PrintTicket pode ser dividido em três níveis de conteúdo que representam o trabalho de alto nível, os documentos no trabalho e as páginas em cada documento. Esses níveis são classificados de acordo com a especificidade; o Nível de Trabalho é mais geral, em seguida, o Nível do Documento e, em seguida, o Nível da Página é mais específico. Um trabalho consiste em um ou mais documentos e um documento consiste em uma ou mais páginas.

## <a name="job-level-prefix"></a>Prefixo de nível de trabalho

Um tíquete de Nível de Trabalho contém todas as configurações de formatação de trabalho destinadas a aplicar a um trabalho inteiro. Todos os Elementos com prefixos de escopo de "Trabalho", "Documento" ou "Página" são permitidos em um tíquete de Nível de Trabalho.

As configurações prefixadas "Documento" e "Página" especificadas em um tíquete de Nível de Trabalho serão aplicadas automaticamente aos tíquetes de Nível de Documento e Página.

## <a name="document-level-prefix"></a>Prefixo no nível do documento

O tíquete Nível do Documento incorpora as configurações de formatação de trabalho destinadas a aplicar a um ou mais documentos em um trabalho. Isso pode incluir configurações especificadas anteriormente no tíquete nível de trabalho. Somente elementos com prefixos de escopo de "Documento" ou "Página" são permitidos em um tíquete de Nível de Documento.

Um Tíquete de Nível de Documento pode conter configurações prefixadas por documento especificadas anteriormente pelo Tíquete de nível de trabalho.

## <a name="page-level-prefix"></a>Prefixo no nível da página

O tíquete nível de página incorpora as configurações de formatação de trabalho destinadas a aplicar a uma ou mais páginas um trabalho (não limitado a um único documento). Isso pode incluir as configurações especificadas anteriormente no tíquete Nível de Trabalho ou Documento. Somente Elementos com prefixos de escopo de "Page" são permitidos em um tíquete de Nível de Página.

Um Tíquete de Nível de Página pode conter as configurações prefixadas de "Página" especificadas anteriormente pelo tíquete de nível de trabalho e/ou o tíquete de nível de documento.

## <a name="prefix-usage-within-a-printticket-or-print-capabilities-document"></a>Uso de prefixo em um documento de funcionalidades printTicket ou de impressão

Os documentos PrintTicket e PrintCapabilities NÃO DEVEM conter várias palavras-chave que diferem apenas no prefixo de definição de tela.? Por exemplo, um documento PrintCapabilities NÃO DEVE ter JobInputBin e PageInputBin especificados.? No entanto, um documento Funcionalidades de Impressão PODE ter JobDuplexAllDocumentsContiguously e DocumentDuplex especificados porque eles são considerados recursos diferentes, pois apresentam um comportamento diferente.? Este exemplo também é verdadeiro para um único PrintTicket.

## <a name="prefix-conflict-management"></a>Gerenciamento de conflitos de prefixo

Um conflito de palavra-chave entre as configurações é definido como o mesmo elemento de esquema de impressão de nível raiz anotado pelo atributo XML "name", que aparece em vários tíquetes de nível. Se não houver conflito, um elemento com escopo de prefixo poderá ser pressionado ou herdado de um tíquete mais geral para um tíquete mais específico. Se houver um conflito, a configuração do tíquete mais específico tem precedência. Ou seja, as configurações de cada página em um tíquete de Nível de Página substituem as configurações idênticas por página em um tíquete de Nível de Trabalho ou Documento. Da mesma forma, as configurações de documento no tíquete nível do documento têm precedência sobre as configurações do documento no tíquete nível de trabalho.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Especificação de esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



