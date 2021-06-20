---
description: A Estrutura de Esquema de Impressão define um namespace que inclui os elementos e atributos XML definidos nas Palavras-chave de esquema de impressão.
ms.assetid: 5a07ec21-dc7c-46d5-b1c2-de06f53fe6bf
title: Objetos e nomes definidos nas palavras-chave de esquema de impressão
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73aabdac90de6743388ca1f4d44e1ad52c020dbd
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112408549"
---
# <a name="objects-and-names-defined-in-the-print-schema-keywords"></a>Objetos e nomes definidos nas palavras-chave de esquema de impressão

Este tópico não é atual. Para obter as informações mais atuais, consulte a [Especificação de Esquema de Impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

A Estrutura de Esquema de Impressão define um namespace que inclui os elementos e atributos XML definidos nas Palavras-chave de esquema de impressão. Isso inclui elementos como Feature, Option e ScoredProperty; nomes de atributo, como nome e propagação; e valores para atributos XML, como restritos. Em outras palavras, cada uso de um nome definido nas Palavras-chave de Esquema de Impressão deve ser explicitamente qualificado com esse namespace ou deve ser implicitamente associado a esse namespace pelo uso de um atributo xmlns padrão. O documento Palavras-chave de esquema de impressão define as instâncias de elemento público que podem aparecer em qualquer contexto ou local específico. As instâncias de elemento devem aparecer somente dentro do contexto ou local designado na Estrutura de Esquema de Impressão. Por exemplo, a instância <psf:Option name= "psk:Letter"> que é definida nas Palavras-chave de esquema de impressão deve aparecer dentro da instância do <psf:Feature name = "psk:PageMediaSize"> (também definida nas Palavras-chave de esquema de impressão). Você não tem a liberdade de usar uma determinada instância option fora do contexto especificado.

Instâncias de elemento definidas de forma privada podem aparecer em qualquer lugar, desde que o tipo de elemento apareça em um contexto permitido pela Estrutura de Esquema de Impressão.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Especificação de esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



