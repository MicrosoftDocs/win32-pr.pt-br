---
description: Saiba mais sobre a sintaxe do esquema de impressão, que é expressa na sintaxe XML e é composta por um pequeno número de tipos de elementos.
ms.assetid: d67518e3-c379-4a50-aeda-31afaa7f05dd
title: Sintaxe do esquema de impressão
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ef52dbdbdfacc2d3cc947b46558319577a75b1b
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112405289"
---
# <a name="syntax-of-the-print-schema"></a>Sintaxe do esquema de impressão

Este tópico não é atual. Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

O esquema de impressão é expresso na sintaxe XML. Portanto, os leitores devem estar familiarizados com a sintaxe XML e os termos como elemento, marca do elemento, conteúdo do elemento, atributo e namespace. A estrutura do esquema de impressão é composta por um pequeno número de tipos de elementos; cada tipo de elemento atende a uma finalidade específica nas tecnologias criadas no esquema de impressão.

Os tipos de elementos são diferenciados por sua marca de elemento XML. A estrutura de esquema de impressão define a estrutura geral e a organização das tecnologias dependentes, denotando para cada tipo de elemento quais tipos de elementos são permitidos como elementos filho.

Muitos tipos de elementos são diferenciados de outros do mesmo tipo pelo atributo de nome, que desempenha uma função significativa no esquema. O atributo Name serve para identificar instâncias de cada tipo de elemento. As palavras-chave do esquema de impressão definem um conjunto de valores para o atributo Name para muitos dos tipos de elemento. Na maioria dos casos, os provedores podem atribuir seus próprios valores ao atributo Name. Eles precisam apenas garantir que os valores sejam QName de XML qualificados com um namespace exclusivo para o provedor.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Especificação de esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



