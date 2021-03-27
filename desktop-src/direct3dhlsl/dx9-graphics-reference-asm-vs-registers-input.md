---
title: Registro de entrada
description: Registro de entrada
ms.assetid: 7cd8e555-4e69-4905-a541-62e09b41a602
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 983f0520ccc50fa1683d4b8254ac436fff7491a1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103916416"
---
# <a name="input-register"></a>Registro de entrada

Registro de entrada do sombreador de vértice.

Os dados de cada vértice (usando um ou mais fluxos de vértice de entrada) são carregados nos registros de entrada de vértice antes da execução do sombreador de vértice. Os registros de entrada consistem em vetores de ponto flutuante de 16 4 componentes, designados como V0 por meio de v15. Esses registros são somente leitura. Um registro de entrada é associado a dados de vértice por meio de uma declaração de vértice.

As propriedades de registro a seguir controlam como cada registro se comporta:



| Propriedade        | Descrição                                                                                   |
|-----------------|-----------------------------------------------------------------------------------------------|
| Name            | v \[ n \] -n é um número de registro opcional. 0 é o valor padrão usado, se for omitido.     |
| Contagem           | Um máximo de 16 registros, V0-v15.                                                          |
| Permissões de e/s | Somente leitura. Esse registro não pode ser gravado pela API ou dentro do sombreador.                   |
| Portas de leitura      | 1. este é o número de vezes que um registro pode ser lido em uma única instrução. Veja abaixo. |



 

Qualquer instrução única pode acessar apenas um registro de entrada de vértice. No entanto, cada fonte na instrução pode Swizzler e negar de forma independente o vetor conforme ele é lido.

## <a name="example"></a>Exemplo

Aqui está um exemplo que usa uma declaração de vértice para associar dados de posição de vértice 2D para registrar V0.

A declaração de vértice pertence ao aplicativo:


```
D3DVERTEXELEMENT9 decl[] =
{
    { 0, 0, D3DDECLTYPE_FLOAT2, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_POSITION, 0 },
      D3DDECL_END()
};
```



Aqui está a declaração de sombreador de vértice correspondente:


```
dcl_position v0
```





| Versões do sombreador de vértice | 1\_1 | 2 \_ 0 | 2 \_ SW | 2 \_ x | 3 \_ 0 | 3 \_ SW |
|------------------------|------|------|-------|------|------|-------|
| Registro de posição      | x    | x    | x     | x    | x    | x     |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Registros de sombreador de vértice](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 




