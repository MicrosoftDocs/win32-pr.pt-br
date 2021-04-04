---
description: ICE25 valida que um arquivo. msi satisfaz todas as suas dependências e exclusões do módulo de mesclagem interna.
ms.assetid: e6e3ea44-a1d4-451a-b326-e8fb7ed4adeb
title: ICE25
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0d966c4c374d6e61e30b44a41ad88bed8bf907f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103828977"
---
# <a name="ice25"></a>ICE25

ICE25 valida que um arquivo. msi satisfaz todas as suas dependências e exclusões do [módulo de mesclagem](merge-modules.md) interna. O ICE valida o seguinte:

-   Todas as dependências do módulo de mesclagem indicadas na [tabela ModuleDependency](moduledependency-table.md) do arquivo. msi são satisfeitas por pelo menos um módulo de mesclagem listado na [tabela ModuleSignature](modulesignature-table.md).
-   Nenhum dos módulos de mesclagem excluídos na [tabela ModuleExclusion](moduleexclusion-table.md) é incompatível com os módulos de mesclagem listados na [tabela ModuleSignature](modulesignature-table.md).

## <a name="result"></a>Resultado

O ICE25 posta uma mensagem de erro se o arquivo. msi tiver sido mesclado anteriormente com um módulo de mesclagem incompatível ou se ele não tiver sido mesclado com um módulo de mesclagem necessário.

## <a name="example"></a>Exemplo

ICE25 posta os erros a seguir para o exemplo mostrado.

``` syntax
Dependency failure: Need ModuleX@0 v2.0 
Module ModuleB@1033 v1.0 is excluded.
```

[Tabela ModuleSignature](modulesignature-table.md)



| ModuleID | Idioma | Versão |
|----------|----------|---------|
| Móduloa  | 0        | 1.0     |
| ModuleB  | 1046     | 1.0     |



 

[Tabela ModuleDependency](moduledependency-table.md)



| ModuleID | ModuleLanguage | Requeridoid | RequiredLanguage | RequiredVersion |
|----------|----------------|------------|------------------|-----------------|
| Móduloa  | 0              | ModuleX    | 0                | 2,0             |



 

[Tabela ModuleExclusion](moduleexclusion-table.md)



| ModuleID | ModuleLanguage | Exclusão excluída | ExcludedLanguage | ExcludedMinVersion | ExcludedMaxVersion |
|----------|----------------|------------|------------------|--------------------|--------------------|
| Móduloa  | 0              | ModuleB    | 1046             |                    |                    |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência de ICE](ice-reference.md)
</dt> </dl>

 

 



