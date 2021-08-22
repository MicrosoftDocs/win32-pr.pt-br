---
description: O ICE47 verifica as tabelas Feature e FeatureComponents para recursos com 1600 ou mais componentes.
ms.assetid: e3101569-4d0b-48c9-8ba2-6f0de0c39e74
title: ICE47
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1fdcf1f71af9bb8784c15b159836d329a94e7e6f33b34c31cbba72f9b31349a5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119381946"
---
# <a name="ice47"></a>ICE47

O ICE47 verifica [as tabelas Feature](feature-table.md) e [FeatureComponents](featurecomponents-table.md) para recursos com 1600 ou mais componentes.

## <a name="result"></a>Resultado

O ICE47 postará uma mensagem de erro se um recurso exceder o limite máximo de 1600 componentes por recurso.

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

 

 



