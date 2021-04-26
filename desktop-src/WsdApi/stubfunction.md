---
description: Especifica se as referências de função de stub devem ser incluídas nas estruturas de operação nas definições de tipo de porta para operações unidirecionais e bidirecionais.
ms.assetid: 2547f71d-8a30-4df8-ba38-6707c415708e
title: elemento stubFunction
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a77f37aed20dae4f04eea087e3d1eac2d23369af
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107994143"
---
# <a name="stubfunction-element"></a>elemento stubFunction

Especifica se as referências de função de stub devem ser incluídas nas estruturas de operação nas definições de tipo de porta para operações unidirecionais e bidirecionais.

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

As referências de função de stub são usadas em cenários de hospedagem para operações unidirecionais e bidirecionais.

Os valores válidos para esse elemento são 1 (referências de função TRUE/stub incluídas) e 0 (FALSE/nenhuma referência de função de stub incluída).

## <a name="element-information"></a>Informações do elemento



| Label | Valor |
|-------------------------------------|---------------|
| Sistema mínimo com suporte<br/> | Windows Vista |
| Pode estar vazio                        | Sim           |



 

 




