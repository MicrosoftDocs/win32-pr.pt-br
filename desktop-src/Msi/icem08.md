---
description: O ICEM08 garante que um módulo não exclua outro módulo do qual depende.
ms.assetid: 56d115b4-7410-4db2-a9af-bc6716f3358d
title: ICEM08
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43f5d0076de382889e5fd3df8a03dddb51c6a73eb5a4f825068f6cd66ad24d07
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119811006"
---
# <a name="icem08"></a>ICEM08

O ICEM08 garante que um módulo não exclua outro módulo do qual depende.

## <a name="result"></a>Resultado

ICEM08 posta um erro quando um módulo exclui outro módulo do qual ele depende.

## <a name="example"></a>Exemplo

ICEM08 posta a seguinte mensagem de erro para um módulo que contém as entradas de banco de dados mostradas no exemplo.

``` syntax
Error: This module requires module ModuleB.<GUID> (1033v1.0) but also 
lists it as an exclusion.
```

[Tabela ModuleDependency](moduledependency-table.md)



| ModuleID             | ModuleLanguage | Requeridoid           | RequiredLanguage | RequiredVersion |
|----------------------|----------------|----------------------|------------------|-----------------|
| Móduloa.<GUID> | 1046           | ModuleB.<GUID> | 1046             | 1.0             |



 

[Tabela ModuleExclusion](moduleexclusion-table.md)



| ModuleID             | ModuleLanguage | Exclusão excluída           | ExcludedLanguage | ExcludedMinVersion | ExcludedMaxVersion |
|----------------------|----------------|----------------------|------------------|--------------------|--------------------|
| Móduloa.<GUID> | 1046           | ModuleB.<GUID> | 1046             |                    | 1.0                |



 

Para corrigir o erro, remova a dependência ou a exclusão. Se ModuleB for uma dependência (requeridoid) do Móduloa, você não poderá excluí-la (conforme mostrado na coluna ExludedID da tabela ModuleExclusion). Se você precisar excluir ModuleB, deverá remover a dependência do Móduloa nele.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência de ICE do módulo de mesclagem](merge-module-ice-reference.md)
</dt> </dl>

 

 



