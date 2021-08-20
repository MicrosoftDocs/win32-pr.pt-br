---
title: Registro de coordenadas de textura (referência do HLSL PS)
description: Registro de entrada do sombreador de pixel contendo coordenadas de textura.
ms.assetid: 423f249d-fa9f-41f2-adbf-d97ceace06f5
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 42ef86bba7ca3c31f6158a6aee8d3228cd696fa500f4066b2ef7492558c307c9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118090021"
---
# <a name="texture-coordinate-register-hlsl-ps-reference"></a>Registro de coordenadas de textura (referência do HLSL PS)

Registro de entrada do sombreador de pixel contendo coordenadas de textura.



| Versões do sombreador de pixel       | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ SW | 2 \_ x | 3 \_ 0 | 3 \_ SW |
|-----------------------------|------|------|------|------|------|-------|------|------|-------|
| Registro de coordenadas de textura |      |      |      |      | x    | x     | x    | x    | x     |



 

Um registro de coordenadas de textura contém dados de coordenadas de textura. Antes que um registro de coordenadas de textura seja usado, ele deve ser declarado por uma declaração de sombreador de pixel. Para obter detalhes sobre como declarar um registro de textura, consulte [DCL-(SM2, SM3-PS ASM)](dcl---ps.md).

Além disso, aqui estão algumas outras propriedades de registros de coordenadas de textura.

-   Há oito registros de coordenadas de textura de sombreador de pixel, T0 a T7.
-   Esses são registros somente leitura.
-   Eles contêm valores RGBA de quatro componentes iterados a partir de vértices de entrada.
-   Eles contêm alta precisão, altos valores de dados de intervalo dinâmico interpolados dos dados de vértice. Os valores são gerados com a interpolação de perspectiva correta. Os dados são precisão de ponto flutuante e são assinados.
-   Há um máximo de uma em uma única instrução.
-   Várias leituras de um registro de coordenadas de textura em um sombreador devem usar [máscara de gravação de registro de destino](dx9-graphics-reference-asm-ps-registers-modifiers-write-mask.md)idêntica.
-   O modificador de precisão parcial opcional \[ \_ PP \] se aplica às leituras dependentes. Isso ocorre porque a precisão parcial afeta as operações aritméticas que envolvem o registro de coordenadas de textura. Ele não afetará a precisão das instruções de endereço de textura porque não afeta os iteradores de coordenadas de textura.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Register](dx9-graphics-reference-asm-ps-registers.md)
</dt> </dl>

 

 




