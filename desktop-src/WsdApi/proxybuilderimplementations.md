---
description: Gera funções para criar proxies tipados.
ms.assetid: 75a686ba-8112-4093-8a1b-13419018aa3a
title: elemento proxyBuilderImplementations
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ad22348b33c60689adf60c029e3a08c2f4d417c
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107996463"
---
# <a name="proxybuilderimplementations-element"></a>elemento proxyBuilderImplementations

Gera funções para criar proxies tipados.

## <a name="usage"></a>Uso

``` syntax
<proxyBuilderImplementations>
  child elements
</proxyBuilderImplementations>
```

## <a name="attributes"></a>Atributos

Não há atributos.

## <a name="child-elements"></a>Elementos filho



| Elemento                                     | Descrição                                                                                                                                                     |
|---------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Codinome**](codename.md)<br/>     | O nome a ser usado para o tipo de porta no código gerado. Por padrão, o nome do código é gerado a partir do nome qualificado do tipo de porta.<br/> <br/> |
| [**portType**](porttype.md)<br/>     | Tipo de porta para o qual o código deve ser gerado.<br/> <br/>                                                                                             |
| [**proxyClass**](proxyclass.md)<br/> | Nome da classe a ser gerada a partir da função do construtor de proxy.<br/> <br/>                                                                                  |



### <a name="child-element-sequence"></a>Sequência de elementos filho

``` syntax
(
  proxyClass, 
  portType+, 
  codeName
)
```

## <a name="parent-elements"></a>Elementos pai



| Elemento                         | Descrição                                                    |
|---------------------------------|----------------------------------------------------------------|
| [**Grupo**](file.md)<br/> | Gera um arquivo do gerador de código.<br/> <br/> |



## <a name="element-information"></a>Informações do elemento



| Label | Valor |
|-------------------------------------|---------------|
| Sistema mínimo com suporte<br/> | Windows Vista |
| Pode estar vazio                        | Não            |



 

 




