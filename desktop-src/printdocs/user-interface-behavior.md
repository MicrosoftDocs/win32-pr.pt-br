---
description: Este tópico não é atual. Para obter as informações mais atuais, consulte a especificação do esquema de impressão.
ms.assetid: dc19a568-3673-4061-b19a-50d5df0485d0
title: Comportamento da interface do usuário
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0d475472330c8e3ba2ceb06d0cbde9f3a7fb0be
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/05/2021
ms.locfileid: "105763188"
---
# <a name="user-interface-behavior"></a>Comportamento da interface do usuário

Este tópico não é atual. Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Suponha que você está criando um cliente PrintCapabilities que lê em um documento PrintCapabilities e seleciona uma ou mais opções de cada recurso e usa-os para construir um PrintTicket que especifica a configuração a ser usada para processar o trabalho. Para cada recurso de interesse, o cliente deve examinar cada opção e decidir se essa opção é apropriada para a tarefa em questão. Para uma opção que não é parametrizada, ela pode ser avaliada acessando o valor de cada ScoredProperty. No caso de uma opção de tamanho de mídia não parametrizada, o cliente determina se as dimensões de largura e altura da mídia relatadas em cada opção correspondem às dimensões necessárias.

No caso da opção parametrizada, o cliente deve acessar a instância ParameterDef que é indicada na instância ParameterRef contida em uma das instâncias de ScoredProperty. O ParameterDef normalmente define o intervalo de valores permitido para o parâmetro, bem como as unidades (polegadas, mm e assim por diante) representadas pelo valor. Se as dimensões necessárias estiverem dentro do intervalo de valores permitido para cada um dos parâmetros, o cliente terá a tarefa adicional de inicializar os parâmetros (por meio de uma instância de ParameterInit) no PrintTicket. Essa é uma tarefa particularmente importante. Por exemplo, um PrintTicket não deve especificar um tamanho de mídia personalizado sem especificar as dimensões da mídia, porque o PrintTicket resultante será ambíguo e mal definido.

Um conjunto semelhante de circunstâncias deve ser tratado se o cliente for uma interface do usuário. A interface do usuário normalmente exibe os valores das instâncias ScoredProperty definidas para cada opção. Para maior clareza, é essencial exibir o intervalo e as unidades permitidas para os parâmetros em uma opção com parâmetros. Além disso, se o usuário selecionar a opção parametrizada, a interface do usuário deverá solicitar que o usuário insira o valor a ser usado para inicializar cada parâmetro. Finalmente, a interface do usuário deve compor um PrintTicket que reflita todas as seleções do usuário.

Para obter detalhes da construção de PrintTicket e da especificação de inicialização de parâmetro, consulte [criando um Device-Specific PrintTicket](creating-a-device-specific-printticket.md). Para obter informações sobre como desreferenciar instâncias de ParameterRef e interpretar instâncias de ParameterDef, consulte [usando parâmetros](using-parameters.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Especificação de esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



