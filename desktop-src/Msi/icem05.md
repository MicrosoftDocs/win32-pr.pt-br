---
description: ICEM05 verifica se o módulo de mesclagem está corretamente associado aos componentes no módulo. A associação incorreta de um componente a um módulo faz com que o componente seja associado incorretamente ao banco de dados de destino.
ms.assetid: 1bf4041e-b198-4897-8719-8505fd8180ec
title: ICEM05
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ee34dbc16b9cf3aeaa16aec9b5d62671cd51036c563bfb8561815ad3c21d0ec
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119996776"
---
# <a name="icem05"></a>ICEM05

ICEM05 verifica se o módulo de mesclagem está corretamente associado aos componentes no módulo. A associação incorreta de um componente a um módulo faz com que o componente seja associado incorretamente ao banco de dados de destino.

O módulo de mesclagem ICEs é armazenado em um arquivo. Cub do módulo de mesclagem chamado Mergemod. Cub e não no arquivo. Cub que contém a ICEs usada para a validação do pacote.

## <a name="result"></a>Resultado

ICEM05 posta um erro se o banco de dados do módulo associa incorretamente componentes e o módulo.

## <a name="example"></a>Exemplo

ICEM05 posta as seguintes mensagens de erro para um módulo que contém as entradas de banco de dados mostradas abaixo.

``` syntax
The component Component2.OtherModule.GUID2.1033 in the 
ModuleComponents table does not belong to this Merge Module.
The component Component1.MyModule.GUID1.1033 in the ModuleComponents 
table is not listed in the Component table.
The component 'Component3' in the Component table is not listed in the 
ModuleComponents table.
```

[Tabela ModuleSignature](modulesignature-table.md)



| ModuleID         | Idioma | Versão |
|------------------|----------|---------|
| MyModule. *GUID1* | 1046     | 1.0     |



 

[**Tabela ModuleComponents**](modulecomponents-table.md)



| Componente  | ModuleID            | Idioma |
|------------|---------------------|----------|
| Component1 | MyModule. *GUID1*    | 1046     |
| Component2 | OtherModule. *GUID2* | 1046     |



 

[Tabela de componentes](component-table.md) (parcial)



| Componente  | ComponentID |
|------------|-------------|
| Component3 | *GUID4*     |
| Component2 | *GUID5*     |



 

O ICE do módulo de mesclagem relata o primeiro erro porque a tabela ModuleComponents tenta associar um componente a outro módulo que não é o módulo atual especificado na tabela ModuleSignature. Para corrigir isso, altere as colunas ModuleID e Language do registro ModuleComponents para Component2 para o módulo atual, MyModule. *GUID1*.

A ICE do módulo de mesclagem relata o segundo erro porque o primeiro registro na tabela ModuleComponents tenta associar Component1 ao módulo. Este componente não existe na tabela de componentes do módulo de mesclagem. Um módulo só pode ser associado a um componente existente no módulo. Para corrigir isso, remova o registro do componente não existente.

O ICE do módulo de mesclagem relata o terceiro erro porque o módulo tenta adicionar Component3 ao banco de dados de destino. Este componente não foi associado ao módulo na tabela ModuleComponents. Para corrigir esse erro, adicione um registro para Component3 à tabela ModuleComponents.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência de ICE do módulo de mesclagem](merge-module-ice-reference.md)
</dt> </dl>

 

 



