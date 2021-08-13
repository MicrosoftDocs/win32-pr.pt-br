---
description: Especifica se as referências de função stub devem ser incluídas nas estruturas de operação nas definições de tipo de porta para operações de uso único e de duas vias.
ms.assetid: 2547f71d-8a30-4df8-ba38-6707c415708e
title: Elemento stubFunction
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc9304aa33bd193edc631949a93e1d770a1fade3d0c5726a9f2d897ea1862476
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118552407"
---
# <a name="stubfunction-element"></a>Elemento stubFunction

Especifica se as referências de função stub devem ser incluídas nas estruturas de operação nas definições de tipo de porta para operações de uso único e de duas vias.

## <a name="usage"></a>Uso

``` syntax
<stubFunction/>
```

## <a name="attributes"></a>Atributos

Não há atributos.

## <a name="child-elements"></a>Elementos filho

Não há elementos filho.

## <a name="parent-elements"></a>Elementos pai



| Elemento                                                       | Descrição                                                  |
|---------------------------------------------------------------|--------------------------------------------------------------|
| [**portTypeDefinitions**](porttypedefinitions.md)<br/> | Gera constantes C para tipos de porta.<br/> <br/> |



## <a name="remarks"></a>Comentários

As referências de função stub são usadas em cenários de hospedagem para operações de uso único e de duas vias.

Os valores válidos para esse elemento são 1 (referências de função TRUE/stub incluídas) e 0 (referências de função false/sem stub incluídas).

## <a name="element-information"></a>Informações do elemento



| Rótulo | Valor |
|-------------------------------------|---------------|
| Sistema mínimo com suporte<br/> | Windows Vista |
| Pode estar vazio                        | Sim           |



 

 




