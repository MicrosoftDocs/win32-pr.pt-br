---
description: ICE72 verifica se as ações personalizadas não internas não são usadas na tabela AdvtExecuteSequence.
ms.assetid: b04227d5-5bd6-434a-860c-498d787a1f0a
title: ICE72
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d9d8e1859ffd8123cc7aa3dc801c5484d28ccb2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105753445"
---
# <a name="ice72"></a>ICE72

ICE72 verifica se as ações personalizadas não internas não são usadas na [tabela AdvtExecuteSequence](advtexecutesequence-table.md). Especificamente, apenas o tipo 19, o tipo 35, e as ações personalizadas de tipo 51 são permitidas na tabela AdvtExecuteSequence. Se outras ações personalizadas forem usadas, o anúncio poderá não se comportar conforme o esperado.

## <a name="result"></a>Resultado

ICE72 retornará um erro se a tabela AdvExecuteSequence usar ações personalizadas que não sejam do tipo 35, digite 51 e digite 19.

## <a name="example"></a>Exemplo

ICE72 relata o seguinte erro para o exemplo mostrado:

``` syntax
Custom Action 'CA1' in the AdvtExecuteSequence table is not allowed. Only built-in custom actions are allowed.
```

Para corrigir o erro, remova ' CA1 ' da tabela AdvtExecuteSequence.

[Tabela AdvtExecuteSequence](advtexecutesequence-table.md) (parcial)



| Ação |
|--------|
| CA1    |
| CA35   |



 

[Tabela CustomAction](customaction-table.md) (parcial)



| Ação | Tipo |
|--------|------|
| CA1    | 1    |
| CA35   | 35   |



 

## <a name="tables-used-during-execution"></a>Tabelas usadas durante a execução

[Tabela AdvtExecuteSequence](advtexecutesequence-table.md)

[Tabela CustomAction](customaction-table.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Tipo de ação personalizada 19](custom-action-type-19.md)
</dt> <dt>

[Tipo de ação personalizada 35](custom-action-type-35.md)
</dt> <dt>

[Tipo de ação personalizada 51](custom-action-type-51.md)
</dt> <dt>

[Referência de ICE](ice-reference.md)
</dt> </dl>

 

 



