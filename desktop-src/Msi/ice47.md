---
description: ICE47 verifica o recurso e as tabelas FeatureComponents para obter recursos com 1600 ou mais componentes.
ms.assetid: e3101569-4d0b-48c9-8ba2-6f0de0c39e74
title: ICE47
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: baa04c2df52571f56612242d2dc7da8b5a91647c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104169400"
---
# <a name="ice47"></a>ICE47

ICE47 verifica o [recurso](feature-table.md) e as tabelas [FeatureComponents](featurecomponents-table.md) para obter recursos com 1600 ou mais componentes.

## <a name="result"></a>Resultado

ICE47 posta uma mensagem de erro se um recurso exceder o limite máximo de 1600 componentes por recurso.

## <a name="example"></a>Exemplo

ICE47 relataria o seguinte aviso:

``` syntax
Feature 'Feature1' has 1600 components. This could cause 
    problems on Win9X systems. You should try to have less 
    than 800 components per feature."
```

[Tabela de recursos](feature-table.md) (parcial)



| Recurso  |
|----------|
| Feature1 |



 

[Tabela FeatureComponents](featurecomponents-table.md) (parcial)



| Ação   | Condição     |
|----------|---------------|
| Feature1 | Component1    |
| Feature1 | Component1600 |



 

Para corrigir esse aviso, tente dividir o recurso em vários recursos

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência de ICE](ice-reference.md)
</dt> </dl>

 

 



