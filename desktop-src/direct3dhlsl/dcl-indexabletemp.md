---
title: dcl_indexableTemp (sm4 – asm)
description: dcl \_ indexableTemp (sm4 - asm)
ms.assetid: 32d8e7ce-4b28-48c3-b794-56ace96394f0
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 9f1d6e02b36daef0643910d69404adc0973ebbcf6370ae5f5c11ad2aa7bd3480
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118793439"
---
# <a name="dcl_indexabletemp-sm4---asm"></a>dcl \_ indexableTemp (sm4 - asm)

Declara um registro indexável e temporário.



| dcl \_ indexableTemp x *N size , \[ \] ComponentCount* |
|-------------------------------------------------|



 



| Item                                                                                                                           | Descrição                                                                                 |
|--------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| <span id="N"></span><span id="n"></span>*N*<br/>                                                                         | \[em \] Um inteiro que indica o número do registro.<br/>                              |
| <span id="_size_"></span><span id="_SIZE_"></span>*\[Tamanho\]*<br/>                                                        | \[em \] Um valor inteiro opcional. O número de elementos na matriz de registro.<br/>  |
| <span id="ComponentCount"></span><span id="componentcount"></span><span id="COMPONENTCOUNT"></span>*ComponentCount*<br/> | \[em \] Um valor inteiro opcional. O número de componentes na matriz de registro.<br/> |



 

Um registro contém espaço suficiente para um valor de quatro componentes de 32 bits; O número de elementos na matriz de registros temporários (indexáveis e não [indexáveis](dcl-temps.md)) não pode exceder 4096.

Essa instrução se aplica aos seguintes estágios do sombreador:



| Sombreador de vértice | Sombreador de geometria | Sombreador de pixel |
|---------------|-----------------|--------------|
| x             | x               | x            |



 

Essa instrução é incluída para auxiliar na depuração de um sombreador no assembly; não é possível autor de um sombreador na linguagem de assembly usando o Modelo de Sombreador 4.

## <a name="example"></a>Exemplo

Aqui estão alguns exemplos do código gerado para registros indexáveis.


```
dcl_indexableTemp x0[23], 2 ; // An indexable array of 23, 2-component, 32-bit elements
dcl_indexableTemp x1[16], 4 ; // An indexable array of 16, 4-component, 32-bit elements
```



## <a name="minimum-shader-model"></a>Modelo de sombreador mínimo

Essa função tem suporte nos modelos de sombreador a seguir.



| Modelo de Sombreador                                              | Com suporte |
|-----------------------------------------------------------|-----------|
| [Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)        | sim       |
| [Modelo de sombreador 4.1](dx-graphics-hlsl-sm4.md)              | sim       |
| [Modelo de sombreador 4](dx-graphics-hlsl-sm4.md)                | sim       |
| [Modelo de sombreador 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | não        |
| [Modelo de sombreador 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | não        |
| [Modelo de sombreador 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | não        |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Assembly do modelo de sombreador 4 (DirectX HLSL)](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





