---
description: Leia sobre os elementos ParameterRef na estrutura de esquema de impressão. Este tópico não é atual. Para obter as informações mais atuais, consulte a especificação do esquema de impressão.
ms.assetid: 78df6acf-eb4e-46c1-bf1d-c0a99cf49bff
title: Elementos ParameterRef
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2935317bc4107e2071911ab1df826426b2bcec17
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112396521"
---
# <a name="parameterref-elements"></a>Elementos ParameterRef

Este tópico não é atual. Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Os elementos ParameterRef se aplicam especificamente a elementos Option, permitindo que a capacidade desse elemento Option se refira a um determinado elemento ParameterDef. Para esses elementos de opção, um elemento ScoredProperty que caracteriza a opção não é embutido no código no documento PrintCapabilities como um valor, mas em vez disso é variável. Para habilitar essa variabilidade, esses elementos ScoredProperty contêm um elemento ParameterRef. Um elemento ScoredProperty não pode conter um elemento Value e um elemento ParameterRef. Elementos de opção contendo um ou mais elementos ParameterRef são chamados de elementos de opção com parâmetros.

A estrutura de esquema de impressão permite que um elemento de opção contenha qualquer número de elementos ScoredProperty que se referem a elementos de parâmetro, juntamente com qualquer número de elementos ScoredProperty que contêm elementos de valor. A estrutura também permite que qualquer número de elementos de recurso contenha elementos de opção com parâmetros e qualquer número de elementos de opção com parâmetros seja permitido para cada elemento de recurso. Além disso, a mesma construção de parâmetro pode ser referenciada por vários elementos de opção diferentes, elementos de opção que podem pertencer a elementos de recurso iguais ou diferentes.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Especificação de esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



