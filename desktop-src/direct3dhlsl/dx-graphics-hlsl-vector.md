---
title: Tipo de vetor (HLSL)
description: Um vetor contém entre um e quatro componentes escalares; cada componente de um vetor deve ser do mesmo tipo.
ms.assetid: 16e66f3c-c513-4d03-8adf-463dc8d83e12
keywords:
- Tipo de vetor HLSL
topic_type:
- apiref
api_name:
- Vector Type
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 76d07da5d22dfb44215f70a7620d6519b5c8a802
ms.sourcegitcommit: 3d9dce1bd6c84e2b51759e940aa95aa9b459cd20
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "104989128"
---
# <a name="vector-type"></a>Tipo de vetor

Um vetor contém entre um e quatro componentes escalares; cada componente de um vetor deve ser do mesmo tipo.



|                     |
|---------------------|
| **Nome do TypeNumber** |



 


```
TypeComponents Name
```



## <a name="components"></a>Componentes



| Item                                                                                                                             | Descrição                                                                                                                                                                                                           |
|----------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TypeComponents"></span><span id="typecomponents"></span><span id="TYPECOMPONENTS"></span>**TypeComponents**<br/> | Um único nome que contém duas partes. A primeira parte é um dos tipos [escalares](dx-graphics-hlsl-data-types.md) . A segunda parte é o número de componentes, que deve estar entre 1 e 4, inclusive.<br/> |
| <span id="Name"></span><span id="name"></span><span id="NAME"></span>**Nomes**<br/>                                         | Uma cadeia de caracteres ASCII que identifica exclusivamente o nome da variável.<br/>                                                                                                                                                |



 

## <a name="examples"></a>Exemplos

Estes são alguns exemplos:


```
bool    bVector;   // scalar containing 1 Boolean
int1    iVector = 1;
float3  fVector = { 0.2f, 0.3f, 0.4f };
```



Um vetor pode ser declarado usando essa sintaxe também:


```
vector <Type, Number> VariableName
```



Estes são alguns exemplos:


```
vector <int,    1> iVector = 1;
vector <double, 4> dVector = { 0.2, 0.3, 0.4, 0.5 };
```

## <a name="see-also"></a>Confira também

<dl> <dt>

[Tipos de dados (DirectX HLSL)](dx-graphics-hlsl-data-types.md)
</dt> </dl>

 

 





