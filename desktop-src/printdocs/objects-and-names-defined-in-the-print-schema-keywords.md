---
description: A estrutura de esquema de impressão define um namespace que inclui os elementos e atributos XML definidos nas palavras-chave do esquema de impressão.
ms.assetid: 5a07ec21-dc7c-46d5-b1c2-de06f53fe6bf
title: Objetos e nomes definidos nas palavras-chave do esquema de impressão
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be119d7931210bbc0aea82a4a59534b135ef8655e3aad1ef2c2afaf275d31833
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119718976"
---
# <a name="objects-and-names-defined-in-the-print-schema-keywords"></a>Objetos e nomes definidos nas palavras-chave do esquema de impressão

Este tópico não é atual. Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

A estrutura de esquema de impressão define um namespace que inclui os elementos e atributos XML definidos nas palavras-chave do esquema de impressão. Isso inclui elementos como recurso, opção e ScoredProperty; nomes de atributos como Name e propagar; e valores para atributos XML, como restritos. Em outras palavras, cada uso de um nome definido nas palavras-chave do esquema de impressão deve ser explicitamente qualificado com esse namespace ou deve ser implicitamente associado a esse namespace pelo uso de um atributo xmlns padrão. O documento de palavras-chave do esquema de impressão define as instâncias do elemento público que podem aparecer em qualquer contexto ou local específico. As instâncias de elemento devem aparecer somente dentro do contexto ou local designado na estrutura de esquema de impressão. Por exemplo, a <PSF: Option Name = "PSK: letter" > instância definida nas palavras-chave do esquema de impressão deve aparecer dentro da instância do <PSF: Feature Name = "PSK: PageMediaSize >" (também definida nas palavras-chave do esquema de impressão). Você não tem a liberdade de usar uma determinada instância de opção fora de seu contexto especificado.

As instâncias de elemento definidas de modo privado podem aparecer em qualquer lugar, desde que o tipo de elemento apareça em um contexto permitido pela estrutura de esquema de impressão.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Especificação de esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



