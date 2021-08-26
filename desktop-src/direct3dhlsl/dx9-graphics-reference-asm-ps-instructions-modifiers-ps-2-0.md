---
title: Modificadores para ps_2_0 e superior
description: Modificadores de instrução afetam o resultado da instrução antes de ser gravado no registro de destino. Saiba mais sobre modificadores para ps_2_0 e superior.
ms.assetid: eb2a8a1f-51bc-4516-b679-a8fb25b0dda0
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6875789c40a2f0fab2987927662658a821de5742b2473b7947250cfb11da8155
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119982886"
---
# <a name="modifiers-for-ps_2_0-and-above"></a>Modificadores para ps \_ 2 \_ 0 e superior

Modificadores de instrução afetam o resultado da instrução antes de ser gravado no registro de destino.

Esta seção contém informações de referência para os modificadores de instrução implementados pelo sombreador de pixel versão \_ 2 0 e superior.



| Name                                     | Sintaxe     | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|------------------------------------------|------------|------|------|-------|------|-------|
| [Centróide](#centroid)                    | \_Centróide | x    | x    | x     | x    | x     |
| [Precisão \_ parcial](#partial-precision) | \_Pp       | x    | x    | x     | x    | x     |
| [Saturar](#saturate)                    | \_Sentado      | x    | x    | x     | x    | x     |



 

## <a name="centroid"></a>Centróide

O modificador centroide é um modificador opcional que fixa a interpolação de atributo dentro do intervalo do primitivo quando um centro de pixels multisamplo não é coberto pelo primitivo. Isso pode ser visto em [Amostragem centroide](https://msdn.microsoft.com/library/ee415231(VS.85).aspx).

Você pode aplicar o modificador de centroide a uma instrução de assembly, conforme mostrado aqui:


```
dcl_texcoord0_centroid v0
```



Você também pode aplicar o modificador de centroide a uma semântica, conforme mostrado aqui:


```
float4 TexturePointCentroidPS( float4 TexCoord : TEXCOORD0_centroid ) : COLOR0
{
    return tex2D( PointSampler, TexCoord );
}
```



Além disso, qualquer [Registro de Cor de](dx9-graphics-reference-asm-ps-registers-input-color.md) Entrada (v ) declarado com uma semântica de cor terá \# automaticamente o centroide aplicado. Gradientes computados de atributos que são amostrados por centroide não têm garantia de serem precisos.

## <a name="partial-precision"></a>Precisão parcial

O modificador de instrução de precisão parcial ( pp) indica áreas em que a precisão parcial é aceitável, desde que \_ a implementação subjacente seja compatível com ela. As implementações são sempre livres para ignorar o modificador e executar as operações afetadas com precisão total.

O \_ modificador pp pode ocorrer em dois contextos:

-   Em uma declaração de coordenada de textura para habilitar a passagem de coordenadas de textura para o sombreador de pixel em formato de precisão parcial. Isso permite, por exemplo, o uso de coordenadas de textura para retransmitir dados de cor para o sombreador de pixel, que pode ser mais rápido com precisão parcial do que com precisão total em algumas implementações. Na ausência desse modificador, as coordenadas de textura devem ser passadas com precisão total.
-   Em qualquer instrução, incluindo instruções de carregamento de textura. Isso indica que a implementação tem permissão para executar a instrução com precisão parcial e armazenar um resultado de precisão parcial. Na ausência de um modificador explícito, a instrução deve ser executada com precisão total (independentemente da precisão de entrada).

Exemplos:


```
dcl_texcoord0_pp t1
cmp_pp r0, r1, r2, r3
```



## <a name="saturate"></a>Saturar

O modificador de instrução saturado (sáb) satura (ou fixa) o resultado da instrução para o intervalo 0, 1 antes de \_ escrever no registro de \[ \] destino.

O modificador de instrução sáb pode ser usado com qualquer instrução, exceto \_ [frc - ps](frc---ps.md), [sincos - ps](sincos---ps.md)e qualquer instrução de \* tex.

Para ps \_ 2 \_ 0, ps 2 x e \_ \_ ps \_ 2 \_ sw, \_ [](dx9-graphics-reference-asm-ps-registers-output-color.md) [](dx9-graphics-reference-asm-ps-registers-output-depth.md)o modificador de instrução sáb não pode ser usado com instruções escritas em qualquer registro de saída (Registro de Cor de Saída ou Registro de Profundidade de Saída ). Essa restrição não se aplica a ps \_ 3 \_ 0 e superior.

Exemplo:


```
dp3_sat r0, v0, c1
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Instruções do sombreador de pixel](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




