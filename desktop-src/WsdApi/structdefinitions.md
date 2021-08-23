---
description: Gera definições de estrutura C para tipos conhecidos.
ms.assetid: 38ba2e8a-d5b1-47b2-b410-ae161f5039bf
title: Elemento structDefinitions
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c4c8ad894a42bbafd183031849e458ad5f3bf155a9ccba4e704321e875163c4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119611556"
---
# <a name="structdefinitions-element"></a>Elemento structDefinitions

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
| [**Arquivo**](file.md)<br/> | Saída de um arquivo do gerador de código.<br/> <br/> |



## <a name="remarks"></a>Comentários

Estruturas para tipos conhecidos são referenciadas por grande parte do código gerado e pelo código do aplicativo. Esse elemento é usado para gerar arquivos de inclusão. Esse elemento deve ocorrer após um [**elemento structDeclarations**](structdeclarations.md) para que as referências entre estruturas sejam tratadas corretamente.

## <a name="element-information"></a>Informações do elemento



| Rótulo | Valor |
|-------------------------------------|---------------|
| Sistema mínimo com suporte<br/> | Windows Vista |
| Pode estar vazio                        | Sim           |



 

 




