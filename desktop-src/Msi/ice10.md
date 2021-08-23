---
description: ICE10 valida que o estado de anúncio de recursos filho corresponde ao do seu recurso pai.
ms.assetid: b0e0d837-245e-4c38-a7c4-06dda0eea25c
title: ICE10
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80071bdb7f219904c03d7c6b5b947a1bd818af2c3ebc270b0bfb17f2cf185280
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119581206"
---
# <a name="ice10"></a>ICE10

ICE10 valida que o estado de anúncio de recursos filho corresponde ao do seu recurso pai.

Um recurso filho não pode cancelar o anúncio enquanto seu recurso pai permite anúncio. A seguinte combinação de atributos pai e filho é, portanto, inválida.

``` syntax
parent = msidbFeatureAttributesFavorAdvertise 
child = msidbFeatureAttributesDisallowAdvertise
```

Essa combinação é inválida porque desligaria o pai sempre que o pai deveria ser anunciado. No entanto, o inverso é permitido. Um filho pode ser marcado para favorecer o anúncio enquanto o pai está marcado para não permitir anúncio.

A ação personalizada ICE10 determina o estado dos recursos pai e filho da coluna atributos da tabela de [recursos](feature-table.md) . Observe que é válido definir o estado de um recurso como 0 e ter seu pai ou filho definido como favorecer ou não permitir anúncio.

## <a name="result"></a>Resultado

ICE10 posta um erro se a coluna Attributes da tabela [Feature](feature-table.md) contiver uma incompatibilidade no estado Advertise.

## <a name="example"></a>Exemplo

ICE10 posta a seguinte mensagem de erro para o exemplo mostrado.

``` syntax
Conflicting states, one favors, one disallows. Child: Word differs in advertise state 
from Parent: Office.
```

observação para este exemplo que Microsoft Excel e Microsoft Word são recursos filho de Microsoft Office.

Tabela de [recursos](feature-table.md) (parcial)



| Recurso | Pai do recurso \_ | Atributos |
|---------|-----------------|------------|
| Office  | Nulo            | 4          |
| Excel   | Office          | 4          |
| Word    | Office          | 8          |



 

No exemplo, o Word está definido como não permitir anúncio, que está em conflito com o estado de anúncio de permissão de seu pai, Office.

Em alguns casos, o ICE10 envia o seguinte erro:

``` syntax
Parent feature: 'Parent' not found for child feature: 'Child'. This error means 
that for the child feature 'Child', the feature 'Parent' is not listed in the 
Feature table.
```

Refere-se a uma referência de chave estrangeira inválida. A correção é ter o ponto ' filho ' em seu recurso pai correto ou adicionar uma entrada para o recurso pai ' pai ' à tabela de [recursos](feature-table.md) .

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência de ICE](ice-reference.md)
</dt> </dl>

 

 



