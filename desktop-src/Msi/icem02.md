---
description: ICEM02 verifica se todas as dependências e exclusões do módulo estão relacionadas ao módulo atual.
ms.assetid: c7d77cb6-0ee6-4857-a749-7908e1c5fcda
title: ICEM02
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9a976132dbfad42e95f4141bc00adb48a544c1b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164831"
---
# <a name="icem02"></a>ICEM02

ICEM02 verifica se todas as dependências e exclusões do módulo estão relacionadas ao módulo atual.

O módulo de mesclagem ICEs é armazenado em um arquivo. Cub do módulo de mesclagem chamado Mergemod. Cub e não no arquivo. Cub que contém a ICEs usada para a validação do pacote.

## <a name="result"></a>Resultado

O ICEM02 posta mensagens de erro se o banco de dados do módulo tentar especificar dependências ou exclusões que não estão relacionadas ao módulo atual. ICEM02 posta uma mensagem de erro se o banco de dados do módulo tentar especificar o módulo atual como dependente ou excluído por si só.

## <a name="example"></a>Exemplo

ICEM02 postaria as seguintes mensagens de erro para um módulo que contém as entradas de banco de dados mostradas abaixo.

``` syntax
The dependency OtherModule.GUID2.1033.OtherModule.GUID3.0 in the 
ModuleDependency table creates a dependency for an unrelated module. A 
module can only define dependencies for itself

This module is listed as depending on itself!

The exclusion OtherModule.GUID2.1033.OtherModule.GUID3.0 in the 
ModuleExclusion table creates an excluded module for an unrelated 
module. A module can only define exclusions for itself.

This module excludes itself from the target database!
```

[Tabela ModuleSignature](modulesignature-table.md)



| ModuleID         | Idioma | Versão |
|------------------|----------|---------|
| MyModule. *GUID1* | 1046     | 1.0     |



 

[Tabela ModuleDependency](moduledependency-table.md)



| ModuleID            | ModuleLanguage | Requeridoid          | RequiredLanguage | RequiredVersion |
|---------------------|----------------|---------------------|------------------|-----------------|
| OtherModule. *GUID2* | 1046           | OtherModule. *GUID3* | 0                | 1.0             |
| MyModule. *GUID1*    | 1046           | MyModule. *GUID1*    | 1046             | 1.2             |



 

[Tabela ModuleExclusion](moduleexclusion-table.md) (parcial)



| ModuleID            | ModuleLanguage | Exclusão excluída          | ExcludedLanguage |
|---------------------|----------------|---------------------|------------------|
| OtherModule. *GUID2* | 1046           | OtherModule. *GUID3* | 0                |
| MyModule. *GUID1*    | 1046           | MyModule. *GUID1*    | 1046             |



 

O ICE do módulo de mesclagem lança o primeiro erro porque a da primeira linha na tabela ModuleDependency, que não especifica uma dependência necessária para o módulo atual especificado na tabela ModuleSignature. As dependências de um módulo só podem ser especificadas em sua própria tabela ModuleDependency. Se OtherModule. *GUID3* é exigido pelo módulo atual, substitua as duas primeiras colunas da linha pelos dados da tabela ModuleSignature. Se OtherModule. *GUID3* não é exigido por este módulo, exclua esta linha.

O ICE do módulo de mesclagem lança o segundo erro porque um módulo não pode especificar uma dependência em si mesmo.

O ICE do módulo de mesclagem posta o terceiro erro devido à primeira linha na tabela ModuleExclusion, que não especifica uma exclusão necessária para o módulo atual especificado na tabela ModuleSignature. As exclusões de um módulo só podem ser especificadas em sua própria tabela ModuleExclusion. Se o módulo atual excluir OtherModule. *GUID3*, substitua as duas primeiras colunas da linha pelos dados da tabela ModuleSignature. Se o módulo atual não excluir OtherModule. *GUID3*, exclua esta linha.

O ICE do módulo de mesclagem posta o quarto erro, pois um módulo não pode especificar que ele seja excluído.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência de ICE do módulo de mesclagem](merge-module-ice-reference.md)
</dt> </dl>

 

 



