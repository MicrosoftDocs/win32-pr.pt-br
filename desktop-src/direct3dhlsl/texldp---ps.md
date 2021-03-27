---
title: texldp-PS
description: Instrução de carregamento de textura projetada. Essa instrução divide a coordenada de textura de entrada pelo quarto elemento (. a ou. w) logo antes da amostragem.
ms.assetid: 82e62ba3-a9f5-4afb-8dca-4c54a00843eb
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 045caf6ec922183893df252488946546602d2459
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104294479"
---
# <a name="texldp---ps"></a>texldp-PS

Instrução de carregamento de textura projetada. Essa instrução divide a coordenada de textura de entrada pelo quarto elemento (. a ou. w) logo antes da amostragem.

## <a name="syntax"></a>Syntax



| texldp DST, src0, src1 |
|------------------------|



 

onde

-   DST é o registro de destino.
-   src0 é um registro de origem que fornece as coordenadas de textura para o exemplo de textura. Consulte [registro de coordenadas de textura](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md).
-   src1 identifica a [amostra (Direct3D 9 ASM-PS)](dx9-graphics-reference-asm-ps-registers-sampler.md) (s \# ), em que \# especifica qual número de amostra de textura deve ser amostrado. O classificador foi associado a ele uma textura e um estado de amostra definido por [**D3DSAMPLERSTATETYPE**](/windows/desktop/direct3d9/d3dsamplerstatetype).

Para obter o conjunto de restrições ao usar texldp, consulte [texld](texld---ps-2-0.md).

## <a name="remarks"></a>Comentários

texldp executa projeção nas coordenadas lidas de src0 antes de executar o exemplo. Cada coordenada de textura é dividida por src0. w; em seguida, a textura é amostrada. Quando o texldp é concluído, o conteúdo de src0 não é afetado (a menos que o DST seja o mesmo registro). Uma alternativa ao uso de texldp é executar manualmente a divisão de projeção no sombreador. No entanto, a execução da divisão no código do sombreador é geralmente mais lenta do que quando executada pela instrução texldp, portanto, evite essa matemática adicional quando possível.

O número de coordenadas necessárias para src0 executar o exemplo de textura depende de como src1 foi declarado, além do componente. w. Os tipos de amostra são declarados com o tipo de [ \_ amostra DCL (SM2, SM3-PS ASM)](dcl-samplertype---ps.md). Se src1 for declarado como um classificador 2D, então src0 deverá conter coordenadas. xyw; se src1 for declarado como uma amostra de cubo ou uma amostra de volume, então src0 deverá conter coordenadas. xyzw. A amostragem de uma textura 2D com coordenadas. xyzw é permitida (a coordenada z é ignorada).

Se a textura de origem contiver menos de quatro componentes, os padrões serão colocados nos componentes ausentes. Os padrões dependem do formato de textura, conforme mostrado na tabela a seguir.



| Formato de textura                                                                                          | Valores padrão para componentes ausentes |
|---------------------------------------------------------------------------------------------------------|---------------------------------------|
| D3DFMT \_ R5G6B5, D3DFMT \_ R8G8B8, D3DFMT \_ L8, D3DFMT \_ L16, D3DFMT \_ R3G3B2, D3DFMT \_ CxV8U8, D3DFMT \_ L6V5U5 | A = 1,0                               |
| D3DFMT \_ V8U8, D3DFMT \_ V16U16, D3DFMT \_ G16R16, D3DFMT G16R16F \_ , D3DFMT \_ G32R32F                          | B = A = 1,0                           |
| D3DFMT \_ a8                                                                                              | R = G = B = 0,0                       |
| D3DFMT \_ R16F, D3DFMT \_ R32F                                                                              | G = B = A = 1,0                       |
| Todos os formatos de profundidade/estêncil                                                                               | R = B = 0,0, A = 1,0                  |



 

Essa instrução tem suporte nas seguintes versões:



| Versões do sombreador de pixel | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| texldp                |      |      |      |      | x    | x    | x     | x    | x     |



 

### <a name="ps_2_0-and-ps_2_x"></a>PS \_ 2 \_ 0 e PS \_ 2 \_ x

o horário de verão deve ser um [registro temporário](dx9-graphics-reference-asm-ps-registers-temporary.md) (r \# ) e somente a máscara de xyzw (máscara padrão) é permitida.

src0 deve ser um [registro de coordenadas de textura](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md) (t \# ) ou um [registro temporário](dx9-graphics-reference-asm-ps-registers-temporary.md) (r \# ), sem modificador ou swizzle.

src1 deve ser uma [amostra (Direct3D 9 ASM-PS)](dx9-graphics-reference-asm-ps-registers-sampler.md) (s \# ), sem modificador ou swizzle.

Se o \_ bit D3DD3DPSHADERCAPS2 0 \_ NODEPENDENTREADLIMIT Cap não estiver definido (em D3DPSHADERCAPS2 \_ 0), uma instrução de textura específica ([texld](texld---ps-1-4.md), texldp, [texldb-PS](texldb---ps.md), [texldd](texldd---ps.md) ) poderá ser dependente, no máximo, terceiro pedido. Uma instrução de textura dependente de primeira ordem é uma instrução de textura na qual:

-   src0 é um [registro temporário](dx9-graphics-reference-asm-ps-registers-temporary.md) (r \# )
-   o DST foi gravado anteriormente, agora sendo gravado novamente.

Uma instrução de textura dependente de segunda ordem é definida como uma instrução de textura que lê ou grava em um [registro temporário](dx9-graphics-reference-asm-ps-registers-temporary.md) (r \# ) cujo conteúdo, antes de executar a instrução de textura, dependa (talvez indiretamente) no resultado de uma instrução de textura dependente de primeira ordem. Uma instrução de textura dependente de ordem<sup>th</sup>é derivada de uma instrução de textura de ordem (n-<sup>1).</sup>

### <a name="ps_3_0"></a>PS \_ 3 \_ 0

Para \_ o PS 3 \_ 0, src1 deve ser uma [amostra (Direct3D 9 ASM-PS)](dx9-graphics-reference-asm-ps-registers-sampler.md) (s \# ), sem modificador. Swizzle é permitido em src1 e, quando aplicado, os resultados da pesquisa de textura são pré-swizzled antes de gravados no DST.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Instruções do sombreador de pixel](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 