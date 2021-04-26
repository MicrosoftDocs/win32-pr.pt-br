---
description: Define o prefixo a ser usado no código gerado para nomes de macros no namespace.
ms.assetid: ead82070-5546-4036-bff2-8da2714d4264
title: elemento macroPrefix
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c9590092d78ea4700715a868bb7e50f15833011
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107998743"
---
# <a name="macroprefix-element"></a>elemento macroPrefix

Define o prefixo a ser usado no código gerado para nomes de macros no namespace.

## <a name="usage"></a>Uso

``` syntax
<macroPrefix/>
```

## <a name="attributes"></a>Atributos

Não há atributos.

## <a name="child-elements"></a>Elementos filho

Não há elementos filho.

## <a name="parent-elements"></a>Elementos pai



| Elemento                                   | Descrição                                                        |
|-------------------------------------------|--------------------------------------------------------------------|
| [**nameSpace**](namespace.md)<br/> | Um namespace a ser usado para geração de código.<br/> <br/> |



## <a name="remarks"></a>Comentários

Esse elemento substitui o prefixo de URI padrão usado para macros geradas. Por exemplo, se o prefixo da macro for "AV \_ " e o nome for "TUNER", a macro gerada para o nome qualificado será " \_ sintonizador de AV".

Por padrão, o código gerado cria um prefixo de macro preferencial a partir do URI.

## <a name="element-information"></a>Informações do elemento



| Label | Valor |
|-------------------------------------|---------------|
| Sistema mínimo com suporte<br/> | Windows Vista |
| Pode estar vazio                        | Sim           |



 

 




