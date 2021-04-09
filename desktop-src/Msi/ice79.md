---
description: ICE79 valida as referências a componentes e recursos inseridos nos campos de banco de dados usando o tipo de dado Condition.
ms.assetid: f0a8ceac-084a-4693-b27d-f610eec4702a
title: ICE79
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9081297f2bf2f11283380c0f057bd0fbec417975
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090779"
---
# <a name="ice79"></a>ICE79

ICE79 valida as referências a componentes e recursos inseridos nos campos de banco de dados usando o tipo de dado [Condition](condition.md) .

## <a name="result"></a>Resultado

ICE79 posta dois avisos.



| Aviso de ICE79                                                                      | Descrição                                                      |
|------------------------------------------------------------------------------------|------------------------------------------------------------------|
| A tabela de validação está ausente no banco de dados \_ . Não foi possível verificar completamente os nomes das propriedades. | A tabela de [ \_ validação](-validation-table.md)está ausente no banco de dados. |
| Erro ao recuperar valores da coluna \[ 2 \] na tabela \[ 1 \] . Ignorando coluna.         | Erro ao recuperar o valor.                                          |



 

ICE79 posta dois erros.



| Erro de ICE79                                                          | Descrição                               |
|----------------------------------------------------------------------|-------------------------------------------|
| Componente '% ls ' referenciado na coluna '% s'. ' % s' da linha% s é inválido. | Uma referência de componente inválida foi encontrada. |
| Recurso '% ls ' referenciado na coluna '% s'. ' % s' da linha% s é inválido.   | Foi encontrada uma referência de recurso inválida    |



 

## <a name="example"></a>Exemplo

ICE79 relata os seguintes erros para o exemplo:

``` syntax
Component 'NoSuchComponent' referenced in column 
'InstallExecuteSequence'.'Condition' of row Custom2 is invalid.
Feature 'NoSuchFeature' referenced in column 
'InstallExecuteSequence'.'Condition' of row Custom1 is invalid.
```

Neste exemplo, NoSuchComponent está ausente da tabela de [componentes](component-table.md) e NoSuchFeature está ausente da tabela de [recursos](feature-table.md).

[Tabela InstallExecuteSequence](installexecutesequence-table.md) (parcial)



| Ação  | Condição                                |
|---------|------------------------------------------|
| Personalizado1 | TESTaction = 1046 e &NoSuchFeature>2  |
| Custom2 | TESTaction = 146 e $NoSuchComponent>2 |



 

Para corrigir esses erros, insira registros válidos para NoSuchFeature e NoSuchComponent nas tabelas de recursos e componentes.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência de ICE](ice-reference.md)
</dt> </dl>

 

 



