---
description: Este tópico não é atual. Para obter as informações mais atuais, consulte a especificação do esquema de impressão.
ms.assetid: 055e502d-631f-49d2-8577-65396373d478
title: Representando atributos como construções de recurso/opção ou como parâmetros
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2c24843a175337f40a84dcdacc41e1a2ab1e15e
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/05/2021
ms.locfileid: "104011970"
---
# <a name="representing-attributes-as-featureoption-constructs-or-as-parameters"></a>Representando atributos como construções de recurso/opção ou como parâmetros

Este tópico não é atual. Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

O autor de um documento de PrintCapabilities define os atributos de dispositivo que compõem a configuração. No documento PrintCapabilities, o autor pode optar por representar um atributo de dispositivo como um constructo de recurso/opção ou como uma construção de parâmetro.

Se um atributo de dispositivo tiver um número relativamente pequeno de Estados possíveis que não se enquadram em nenhum tipo de padrão óbvio, um constructo de recurso/opção será geralmente a melhor opção. Por exemplo, se os valores permitidos para o atributo de dispositivo PageMediaSize forem os valores letra, ofício, A4ISO, tablóide e Envelope10, um constructo de recurso/opção seria a melhor opção para representação. Devido à dificuldade e à ambiguidade associada à expressar os valores permitidos sem Enumeração explícita, a construção do parâmetro não é apropriada para o atributo PageMediaSize.

Se um atributo de dispositivo puder ser representado por um intervalo de inteiros, a representação de parâmetro geralmente é a melhor opção, especialmente para intervalos que incluem muitos valores. Por exemplo, se o atributo de dispositivo CopyCount para um modelo específico de impressora puder variar de 1 a 99.999, esse atributo deverá ser Categorizado como um parâmetro, definindo uma instância de ParameterDef. Atribua valores às instâncias de propriedade padrão MinValue e MaxValue do elemento ParameterDef para definir o intervalo de valores para o atributo JobCopyCount. Devido ao grande número de valores que devem ser explicitamente listados como elementos de opção, a representação de recurso/opção não é apropriada para o atributo de dispositivo JobCopyCount.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Especificação de esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



