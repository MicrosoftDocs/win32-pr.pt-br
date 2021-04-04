---
description: ICE28 é normalmente usado para validar que a ação ForceReboot é colocada antes ou depois, e nunca em um grupo específico de ações nas tabelas de sequência de ação. Consulte o tópico de ação ForceReboot para determinar as ações que compõem esse grupo.
ms.assetid: 746d907a-33e1-479a-bcb0-93e7fd5dd975
title: ICE28
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc65878bdc3db4f9b79ba95b4a170b694a4728ff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646807"
---
# <a name="ice28"></a>ICE28

ICE28 é normalmente usado para validar que a ação ForceReboot é colocada antes ou depois, e nunca em um grupo específico de ações nas tabelas de sequência de ação. Consulte o tópico de [ação ForceReboot](forcereboot-action.md) para determinar as ações que compõem esse grupo.

ICE28 valida ações nas seguintes tabelas de sequência:

[Tabela AdminUISequence](adminuisequence-table.md)

[Tabela AdminExecuteSequence](adminexecutesequence-table.md)

[Tabela InstallUISequence](installuisequence-table.md)

[Tabela InstallExecuteSequence](installexecutesequence-table.md)

## <a name="result"></a>Resultado

ICE28 posta uma mensagem de erro se ForceReboot for sequenciado dentro do grupo de ações especificado.

## <a name="example"></a>Exemplo

Para o exemplo mostrado, ICE28 posta a seguinte mensagem de erro:

``` syntax
Action: 'ForceReboot' of table InstallExecuteSequence is not permitted in the range 5 to 15 because it cannot separate a set of actions contained in this range.
```

[Tabela InstallExecuteSequence](installexecutesequence-table.md)



| Ação             | Sequência |
|--------------------|----------|
| ForceReboot        | 10       |
| RegisterMIMEInfo   |   5      |
| RegisterProgIdInfo | 15       |



 

O número de sequência de 10 fornecido para quebras de ForceReboot gera o erro, pois ele vem entre os números de sequência de RegisterMIMEInfo e RegisterProgIdInfo.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência de ICE](ice-reference.md)
</dt> </dl>

 

 



