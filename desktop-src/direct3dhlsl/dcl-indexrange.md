---
title: dcl_indexRange (sm4 – asm)
description: dcl \_ indexRange (sm4 – asm)
ms.assetid: 88af30f3-dbf9-4556-b170-a7371680f9b9
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6fe587c3a5cfeae21b5da09a2dd79b67b82bc0c2
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122472062"
---
# <a name="dcl_indexrange-sm4---asm"></a>dcl \_ indexRange (sm4 – asm)

Declara um intervalo de registros que serão acessados por índice (um inteiro computado no sombreador).



| dcl \_ indexRange *minRegisterM*, *maxRegisterN* |
|------------------------------------------------|



 




| Item | Descrição | 
|------|-------------|
| <span id="minRegisterM"></span><span id="minregisterm"></span><span id="MINREGISTERM"></span><em>minRegisterM</em><br /> | [in] O primeiro registro para acessar por índice. <br /><ul><li><em>minRegister</em> é v para <strong>um registro</strong> de entrada de sombreador de vértice ou pixel ou <strong>o</strong> para um registro de saída do sombreador de vértice.</li><li><em>M</em> é um inteiro que indica o número do registro.</li></ul> | 
| <span id="maxRegisterN"></span><span id="maxregistern"></span><span id="MAXREGISTERN"></span><em>maxRegisterN</em><br /> | [in] O último registro para acessar por índice. O mesmo formato que <em>minRegister,</em> exceto <em>N,</em> é o número do registro.<br /> | 




 

As seguintes restrições se aplicam a todos os registros:

-   Os registros mínimo e máximo devem ser do mesmo tipo e ter as mesmas máscaras de componente (se as máscaras são declaradas).
-   Um registro pode ter vários intervalos de índice, desde que eles não se sobreponham.
-   O número mínimo do registro deve ser menor que o número máximo do registro.
-   Um registro de índice não pode conter [um valor do sistema.](dx-graphics-hlsl-semantics.md)
-   Indexar um registro fora da declaração de índice máximo produz resultados indefinido.

Os registros de entrada do sombreador de pixel devem usar o mesmo modo de interpolação; Os registros de saída do sombreador de pixel não são indexáveis.

Um registro de entrada do sombreador de geometria tem duas dimensões (eixo de vértice, eixo de atributo); o intervalo de índice se aplica somente ao eixo de atributo porque o eixo de vértice é sempre totalmente indexável.

Essa instrução se aplica aos seguintes estágios do sombreador:



| Sombreador de vértice | Sombreador de geometria | Sombreador de pixel |
|---------------|-----------------|--------------|
| x             | x               | x            |



 

Essa instrução é incluída para auxiliar na depuração de um sombreador no assembly; não é possível autor de um sombreador na linguagem de assembly usando o Modelo de Sombreador 4.

## <a name="example"></a>Exemplo

Veja um exemplo.


```
dcl_indexRange v1, v3
dcl_indexRange v4, v9
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

 

 





