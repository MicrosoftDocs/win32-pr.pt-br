---
description: ICEM08 garante que um módulo não exclua outro módulo do que ele depende.
ms.assetid: 56d115b4-7410-4db2-a9af-bc6716f3358d
title: ICEM08
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c953c40d29458613b0fc2027dd691adb672eb15
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122884219"
---
# <a name="icem08"></a>ICEM08

ICEM08 garante que um módulo não exclua outro módulo do que ele depende.

## <a name="result"></a>Result

ICEM08 posta um erro quando um módulo exclui outro módulo do que ele depende.

## <a name="example"></a>Exemplo

ICEM08 posta a seguinte mensagem de erro para um módulo que contém as entradas de banco de dados mostradas no exemplo.

``` syntax
Error: This module requires module ModuleB.<GUID> (1033v1.0) but also 
lists it as an exclusion.
```

[Tabela ModuleDependency](moduledependency-table.md)



| ModuleID             | ModuleLanguage | RequiredID           | RequiredLanguage | RequiredVersion |
|----------------------|----------------|----------------------|------------------|-----------------|
| ModuleA. &lt; GUID&gt; | 1046           | ModuleB. &lt; GUID&gt; | 1046             | 1.0             |



 

[Tabela ModuleExclusion](moduleexclusion-table.md)



| ModuleID             | ModuleLanguage | ExcludedID           | ExcludedLanguage | ExcludedMinVersion | ExcludedMaxVersion |
|----------------------|----------------|----------------------|------------------|--------------------|--------------------|
| ModuleA. &lt; GUID&gt; | 1046           | ModuleB. &lt; GUID&gt; | 1046             |                    | 1.0                |



 

Para corrigir o erro, remova a dependência ou a exclusão. Se ModuleB for uma dependência (RequiredID) de ModuleA, você não poderá exclui-la (conforme mostrado na coluna ExludedID da tabela ModuleExclusion). Se for necessário excluir o ModuleB, você deverá remover a dependência do ModuleA nele.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência ice do módulo de mesclagem](merge-module-ice-reference.md)
</dt> </dl>

 

 



