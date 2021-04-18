---
description: Gera definições de estrutura C para tipos conhecidos.
ms.assetid: 38ba2e8a-d5b1-47b2-b410-ae161f5039bf
title: elemento structDefinitions
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e33ca9ac9ce3f9e868646c0bfff260238c30e572
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105780277"
---
# <a name="structdefinitions-element"></a>elemento structDefinitions

Gera definições de estrutura C para tipos conhecidos.

## <a name="usage"></a>Uso

``` syntax
<structDefinitions/>
```

## <a name="attributes"></a>Atributos

Não há atributos.

## <a name="child-elements"></a>Elementos filho

Não há elementos filho.

## <a name="parent-elements"></a>Elementos pai



| Elemento                         | Descrição                                                    |
|---------------------------------|----------------------------------------------------------------|
| [**Grupo**](file.md)<br/> | Gera um arquivo do gerador de código.<br/> <br/> |



## <a name="remarks"></a>Comentários

Estruturas para tipos conhecidos são referenciadas por grande parte do código gerado e pelo código do aplicativo. Esse elemento é usado para gerar arquivos de inclusão. Esse elemento deve ocorrer após um elemento [**structDeclarations**](structdeclarations.md) para que as referências entre as estruturas sejam manipuladas corretamente.

## <a name="element-information"></a>Informações do elemento



|                                     |               |
|-------------------------------------|---------------|
| Sistema mínimo com suporte<br/> | Windows Vista |
| Pode estar vazio                        | Sim           |



 

 




