---
title: dcl_input (sm4 – asm)
description: entrada dcl \_ (sm4 – asm)
ms.assetid: 13456f2a-ee6c-42da-a9fe-670ab0fcbddf
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 8214287a4afb4c683a94e213cdfed133c03219e2
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122467003"
---
# <a name="dcl_input-sm4---asm"></a>entrada dcl \_ (sm4 – asm)

Declara um registro de entrada do sombreador.



| dcl \_ input v N *\[ .mask , \] \[ interpolationMode \]* |
|-------------------------------------------------|



 




| Item | Descrição | 
|------|-------------|
| <span id="vN_.mask_"></span><span id="vn_.mask_"></span><span id="VN_.MASK_"></span>v<em>N[.mask]</em><br /> | [in] Um registro de dados de vértice. <br /><ul><li><em>N</em> é um inteiro que identifica o número do registro.</li><li><em>[.mask] é</em> uma máscara de componente opcional (.xyzw) que especifica quais dos componentes de registro usar.</li></ul> | 
| <span id="interpolationMode"></span><span id="interpolationmode"></span><span id="INTERPOLATIONMODE"></span><em>Interpolationmode</em><br /> | [in] Opcional. O modo de interpolação, que só é honorado nos registros de entrada do sombreador de pixel. Pode ser um dos seguintes valores: <br /><ul><li>constante – não interpolar entre valores de registro.</li><li>linear – interpolar linearmente entre valores de registro.</li><li>linearCentoid - o mesmo que linear, mas centroide fixado ao multisampling.</li><li>linearNoperspective – o mesmo que linear, mas sem correção de perspectiva.</li><li>linearNoperspectiveCentoid - o mesmo que linear, centroide fixado quando multisampling, sem correção de perspectiva.</li></ul> | 




 

### <a name="interpolation-notes"></a>Notas de interpolação

Por padrão, os atributos de vértice são interpolados de um centro de pixels ao executar a antialiação multisample. Se um centro de pixels não for coberto, um atributo será extrapolado para um centro de pixels antes da interpolação.

Para um pixel que não é totalmente coberto ou um atributo que não abrange um centro de pixels, você pode especificar a amostragem de centroide que força a amostragem a ocorrer em algum lugar dentro da área coberta do pixel. Como uma máscara de exemplo (se usada) é aplicada antes que o centroide seja calculado, qualquer local de exemplo mascarado pela máscara de exemplo não pode ser escolhido como um local centroide.

Essa instrução se aplica aos seguintes estágios do sombreador:



| Sombreador de vértice | Sombreador de geometria | Sombreador de pixel |
|---------------|-----------------|--------------|
| x             | x               | x            |



 

Para identificar a entrada como um valor do sistema, use [dcl \_ input \_ sv (sm4 - asm)](dcl-input-sv.md).

Essa instrução é incluída para auxiliar na depuração de um sombreador no assembly; não é possível autor de um sombreador na linguagem de assembly usando o Modelo de Sombreador 4.

## <a name="example"></a>Exemplo

Veja alguns exemplos.


```
dcl_input v3.xyz

dcl_input v0.x, linearCentroid
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

 

 





