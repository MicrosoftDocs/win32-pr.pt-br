---
title: texldb-PS
description: Instrução de carregamento de textura tendenciosa. Essa instrução usa o quarto elemento (. a ou. w) para diferenciar o nível de detalhes de amostragem de textura antes da amostragem.
ms.assetid: cafd72c9-b7bb-4e3f-8a8c-de26a4446864
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 912c4c61f6c1f2b6bef46c7c5b6ea17223df5eb8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104084615"
---
# <a name="texldb---ps"></a>texldb-PS

Instrução de carregamento de textura tendenciosa. Essa instrução usa o quarto elemento (. a ou. w) para diferenciar o nível de detalhes de amostragem de textura antes da amostragem.

## <a name="syntax"></a>Syntax



| texldb DST, src0, src1 |
|------------------------|



 

Em que:

-   DST é o registro de destino.
-   src0 é um registro de origem que fornece as coordenadas de textura para o exemplo de textura. Consulte [registro de coordenadas de textura](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md).
-   src1 identifica a [amostra (Direct3D 9 ASM-PS)](dx9-graphics-reference-asm-ps-registers-sampler.md) (s \# ), em que \# especifica qual número de amostra de textura deve ser amostrado. O classificador foi associado a ele uma textura e um estado de amostra definido por [**D3DSAMPLERSTATETYPE**](/windows/desktop/direct3d9/d3dsamplerstatetype).

Para obter as restrições ao usar texldb, consulte a instrução [texld-PS \_ 2 \_ 0 e up](texld---ps-2-0.md) .

### <a name="ps_2_0-and-ps_2_x"></a>PS \_ 2 \_ 0 e PS \_ 2 \_ x

o horário de verão deve ser um [registro temporário](dx9-graphics-reference-asm-ps-registers-temporary.md) (r \# ) e somente a máscara de xyzw (máscara padrão) é permitida.

src0 deve ser um [registro de coordenadas de textura](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md) (t \# ) ou um [registro temporário](dx9-graphics-reference-asm-ps-registers-temporary.md) (r \# ), sem modificador ou swizzle.

src1 deve ser uma [amostra (Direct3D 9 ASM-PS)](dx9-graphics-reference-asm-ps-registers-sampler.md) (s \# ), sem modificador ou swizzle.

Se o \_ bit D3DD3DPSHADERCAPS2 0 \_ NODEPENDENTREADLIMIT Cap não estiver definido (em D3DPSHADERCAPS2 \_ 0), uma instrução de textura específica (texld, texldp, texldb, texldd) poderá ser dependente, no máximo, terceiro. Uma instrução de textura dependente de primeira ordem é uma instrução de textura na qual:

-   src0 é um [registro temporário](dx9-graphics-reference-asm-ps-registers-temporary.md) (r \# ).
-   o DST foi gravado anteriormente, agora sendo gravado novamente.

Uma instrução de textura dependente de segunda ordem é definida como uma instrução de textura que lê ou grava em um [registro temporário](dx9-graphics-reference-asm-ps-registers-temporary.md) (r \# ) cujo conteúdo, antes de executar a instrução de textura, dependa (talvez indiretamente) no resultado de uma instrução de textura dependente de primeira ordem. Uma instrução de textura dependente de ordem<sup>th</sup>é derivada de uma instrução de textura de ordem (n-<sup>1).</sup>

### <a name="ps_3_0"></a>PS \_ 3 \_ 0

src1 deve ser uma [amostra (Direct3D 9 ASM-PS)](dx9-graphics-reference-asm-ps-registers-sampler.md) (s \# ), sem nenhum modificador. Swizzle é permitido em src1 e, quando aplicado, os resultados da pesquisa de textura são pré-swizzled antes de gravados no DST.

## <a name="remarks"></a>Comentários



| Versões do sombreador de pixel | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| texldb                |      |      |      |      | x    | x    | x     | x    | x     |



 

texldb ajusta o nível de detalhe mipmap, calculado normalmente como parte do processo de exemplo pelo valor (assinado) em src0. w. Valores de tendência positivos resultarão na seleção de mipmaps menor e vice-versa. Para PS \_ 2 \_ 0 e PS \_ 2 \_ x, os valores de tendência podem estar dentro do intervalo \[ de-3,0, + 3,0 \] . Para \_ o PS 3 \_ 0, os valores de tendência podem estar dentro do intervalo \[ de-16,0, + 15,0 \] . Os valores de tendência fora desses intervalos produzem resultados indefinidos. O estado de amostra D3DSAMP \_ MIPMAPLODBIAS ainda é respeitado, e a tendência de texldb é adicionada a isso, mas em uma base por pixel. Depois que o nível de detalhe tendenciosa é calculado, D3DSAMP \_ MAXMIPLEVEL ainda é respeitado e ocorre o exemplo de textura. Após texldb, o conteúdo de src0 não será afetado (a menos que o DST seja o mesmo registro).

O número de coordenadas necessárias para src0 executar o exemplo de textura depende de como src1 foi declarado, além do componente. w. Os tipos de amostra são declarados com o tipo de [ \_ amostra DCL (SM2, SM3-PS ASM)](dcl-samplertype---ps.md). Se src1 for declarado como um classificador 2D, então src0 deverá conter coordenadas. xyw; se src1 for declarado como uma amostra de cubo ou uma amostra de volume, então src0 deverá conter coordenadas. xyzw. A amostragem de uma textura 2D com coordenadas. xyzw é permitida (a coordenada z é ignorada).

Se a textura de origem contiver menos de quatro componentes, os padrões serão colocados nos componentes ausentes. Os padrões dependem do formato de textura, conforme mostrado na tabela a seguir:



| Formato de textura                                                                                          | Valores padrão       |
|---------------------------------------------------------------------------------------------------------|----------------------|
| D3DFMT \_ R5G6B5, D3DFMT \_ R8G8B8, D3DFMT \_ L8, D3DFMT \_ L16, D3DFMT \_ R3G3B2, D3DFMT \_ CxV8U8, D3DFMT \_ L6V5U5 | A = 1,0              |
| D3DFMT \_ V8U8, D3DFMT \_ V16U16, D3DFMT \_ G16R16, D3DFMT G16R16F \_ , D3DFMT \_ G32R32F                          | B = A = 1,0          |
| D3DFMT \_ a8                                                                                              | R = G = B = 0,0      |
| D3DFMT \_ R16F, D3DFMT \_ R32F                                                                              | G = B = A = 1,0      |
| Todos os formatos de profundidade/estêncil                                                                               | R = B = 0,0, A = 1,0 |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Instruções do sombreador de pixel](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 