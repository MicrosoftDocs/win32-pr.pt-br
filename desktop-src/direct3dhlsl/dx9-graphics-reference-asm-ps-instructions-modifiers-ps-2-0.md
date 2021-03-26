---
title: Modificadores para ps_2_0 e acima
description: Os modificadores de instrução afetam o resultado da instrução antes de serem gravados no registro de destino.
ms.assetid: eb2a8a1f-51bc-4516-b679-a8fb25b0dda0
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 7141576b80b7a05a3e61ee9a98fa36958b1d5530
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103823052"
---
# <a name="modifiers-for-ps_2_0-and-above"></a>Modificadores para PS \_ 2 \_ 0 e acima

Os modificadores de instrução afetam o resultado da instrução antes de serem gravados no registro de destino.

Esta seção contém informações de referência para os modificadores de instrução implementados pelo pixel shader versão 2 \_ 0 e superior.



| Name                                     | Sintaxe     | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|------------------------------------------|------------|------|------|-------|------|-------|
| [Centróide](#centroid)                    | \_centróide | x    | x    | x     | x    | x     |
| [\_Precisão parcial](#partial-precision) | \_PP       | x    | x    | x     | x    | x     |
| [Saturar](#saturate)                    | \_saturação      | x    | x    | x     | x    | x     |



 

## <a name="centroid"></a>Centróide

O modificador de centróide é um modificador opcional que coloca a interpolação de atributo dentro do intervalo do primitivo quando um centro de pixel com várias amostras não é coberto pelo primitivo. Isso pode ser visto em [amostragem de centróide](https://msdn.microsoft.com/library/ee415231(VS.85).aspx).

Você pode aplicar o modificador de centróide a uma instrução de assembly, conforme mostrado aqui:


```
dcl_texcoord0_centroid v0
```



Você também pode aplicar o modificador de centróide a uma semântica, conforme mostrado aqui:


```
float4 TexturePointCentroidPS( float4 TexCoord : TEXCOORD0_centroid ) : COLOR0
{
    return tex2D( PointSampler, TexCoord );
}
```



Além disso, qualquer [registro de cor de entrada](dx9-graphics-reference-asm-ps-registers-input-color.md) (v \# ) declarado com uma semântica de cor terá automaticamente a centróide aplicada. Gradientes computados de atributos que são de exemplo de centróide não têm garantia de serem precisas.

## <a name="partial-precision"></a>Precisão parcial

O modificador de instrução de precisão parcial ( \_ PP) indica áreas em que a precisão parcial é aceitável, desde que a implementação subjacente ofereça suporte a ela. As implementações sempre são gratuitas para ignorar o modificador e executar as operações afetadas com precisão total.

O \_ modificador PP pode ocorrer em dois contextos:

-   Em uma declaração de coordenada de textura para habilitar a passagem de coordenadas de textura para o sombreador de pixel em formato de precisão parcial. Isso permite, por exemplo, o uso de coordenadas de textura para retransmitir dados de cores para o sombreador de pixel, que pode ser mais rápido com precisão parcial do que com precisão total em algumas implementações. Na ausência desse modificador, as coordenadas de textura devem ser passadas com precisão total.
-   Em qualquer instrução, incluindo instruções de carga de textura. Isso indica que a implementação tem permissão para executar a instrução com precisão parcial e armazenar um resultado de precisão parcial. Na ausência de um modificador explícito, a instrução deve ser executada com precisão total (independentemente da precisão de entrada).

Exemplos:


```
dcl_texcoord0_pp t1
cmp_pp r0, r1, r2, r3
```



## <a name="saturate"></a>Saturar

O modificador de instrução saturação ( \_ SAT) satura (ou coloca) o resultado da instrução para o intervalo de \[ 0, 1 \] antes de gravar no registro de destino.

O \_ modificador de instrução SAT pode ser usado com qualquer instrução, exceto [FRC-PS](frc---ps.md), [Sincos-PS](sincos---ps.md)e quaisquer \* instruções Tex.

Para \_ \_ o software PS 2 0, PS \_ 2 \_ x e PS \_ 2 \_ SW, o \_ modificador de instrução SAT não pode ser usado com instruções de gravação em qualquer registro de saída (registro de cor de[saída](dx9-graphics-reference-asm-ps-registers-output-color.md) ou registro de profundidade de [saída](dx9-graphics-reference-asm-ps-registers-output-depth.md)). Essa restrição não se aplica ao PS \_ 3 \_ 0 e acima.

Exemplo:


```
dp3_sat r0, v0, c1
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Instruções do sombreador de pixel](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




