---
title: texldp – ps
description: Instrução de carregamento de textura projetada. Essa instrução divide a coordenada de textura de entrada pelo quarto elemento (.a ou .w) logo antes da amostragem.
ms.assetid: 82e62ba3-a9f5-4afb-8dca-4c54a00843eb
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d5c362e81af22b46cd443ade7cd4b466112ba9a4d98bd5852ee3d92a285936aa
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120117846"
---
# <a name="texldp---ps"></a>texldp – ps

Instrução de carregamento de textura projetada. Essa instrução divide a coordenada de textura de entrada pelo quarto elemento (.a ou .w) logo antes da amostragem.

## <a name="syntax"></a>Syntax



| texldp dst, src0, src1 |
|------------------------|



 

onde

-   dst é o registro de destino.
-   src0 é um registro de origem que fornece as coordenadas de textura para a amostra de textura. Consulte [Registro de coordenadas de textura.](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md)
-   src1 identifica o [Sampler (Direct3D 9 asm-ps)](dx9-graphics-reference-asm-ps-registers-sampler.md) (s), em que especifica qual número \# de amostra de textura deve ser \# amostrado. O amostrador associou a ela uma textura e um estado de amostra definido por [**D3DSAMPLERSTATETYPE**](/windows/desktop/direct3d9/d3dsamplerstatetype).

Para o conjunto de restrições ao usar o texldp, consulte [texld](texld---ps-2-0.md).

## <a name="remarks"></a>Comentários

O texldp executa a projeção nas coordenadas lidas de src0 antes de executar o exemplo. Cada coordenada de textura é dividida por src0.w e, em seguida, a textura é amostrada. Quando o texldp é concluído, o conteúdo de src0 não é afetado (a menos que dst seja o mesmo registro). Uma alternativa ao uso do texldp é executar manualmente a divisão de projeção no sombreador. No entanto, executar a divisão no código do sombreador geralmente é mais lento do que quando executado pela instrução texldp, portanto, evite essa matemática adicional quando possível.

O número de coordenadas necessárias para src0 executar a amostra de textura depende de como src1 foi declarado, além do componente .w. Os tipos de amostra são declarados com [dcl \_ samplerType (sm2, sm3 – ps asm)](dcl-samplertype---ps.md). Se src1 for declarado como um exemplo 2D, o src0 deverá conter coordenadas .xyw; se src1 for declarado como um sampler de cubo ou um exemplo de volume, o src0 deverá conter coordenadas .xyzw. A amostragem de uma textura 2D com coordenadas .xyzw é permitida (a coordenada .z é ignorada).

Se a textura de origem contiver menos de quatro componentes, os padrões serão colocados nos componentes ausentes. Os padrões dependem do formato de textura, conforme mostrado na tabela a seguir.



| Formato de textura                                                                                          | Valores padrão para componentes ausentes |
|---------------------------------------------------------------------------------------------------------|---------------------------------------|
| D3DFMT \_ R5G6B5, D3DFMT \_ R8G8B8, D3DFMT \_ L8, D3DFMT \_ L16, D3DFMT \_ R3G3B2, D3DFMT \_ CxV8U8, D3DFMT \_ L6V5U5 | A = 1,0                               |
| D3DFMT \_ V8U8, D3DFMT \_ V16U16, D3DFMT \_ G16R16, D3DFMT \_ G16R16F, D3DFMT \_ G32R32F                          | B = A = 1,0                           |
| D3DFMT \_ A8                                                                                              | R = G = B = 0,0                       |
| D3DFMT \_ R16F, D3DFMT \_ R32F                                                                              | G = B = A = 1,0                       |
| Todos os formatos de profundidade/estêncil                                                                               | R = B = 0,0, A = 1,0                  |



 

Essa instrução tem suporte nas seguintes versões:



| Versões do sombreador de pixel | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| texldp                |      |      |      |      | x    | x    | x     | x    | x     |



 

### <a name="ps_2_0-and-ps_2_x"></a>ps \_ 2 \_ 0 e ps \_ 2 \_ x

dst deve ser um [Registro Temporário](dx9-graphics-reference-asm-ps-registers-temporary.md) (r ) e somente a máscara \# .xyzw (máscara padrão) é permitida.

src0 deve ser um Registro de [Coordenadas](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md) de Textura (t ) ou um Registro Temporário (r ), sem \# nenhum [](dx9-graphics-reference-asm-ps-registers-temporary.md) \# modificador ou swizzle.

src1 deve ser um [Sampler (Direct3D 9 asm-ps)](dx9-graphics-reference-asm-ps-registers-sampler.md) (s ), sem \# modificador ou swizzle.

Se o bit de limite D3DD3DPSHADERCAPS2 \_ 0 NODEPENDENTREADLIMIT não estiver definido \_ (em D3DPSHADERCAPS2 0), uma determinada instrução de textura ( \_ [texld](texld---ps-1-4.md), texldp, [texldb - ps](texldb---ps.md), [texldd](texldd---ps.md) ) poderá depender, no máximo, da terceira ordem. Uma instrução de textura dependente de primeira ordem é uma instrução de textura na qual:

-   src0 é um [Registro Temporário](dx9-graphics-reference-asm-ps-registers-temporary.md) (r \# )
-   dst foi escrito anteriormente, agora sendo gravado novamente.

Uma instrução de textura dependente de segunda ordem é definida como uma instrução de textura que lê ou grava em um registro temporário [(r](dx9-graphics-reference-asm-ps-registers-temporary.md) ) cujo conteúdo, antes de executar a instrução de textura, depende (talvez indiretamente) do resultado de uma instrução de textura dependente de primeira \# ordem. Uma (n)<sup>instrução</sup>de textura dependente de ordem deriva de uma (n - 1)<sup>instrução</sup>de textura da ordem 1.

### <a name="ps_3_0"></a>ps \_ 3 \_ 0

Para ps \_ 3 \_ 0, src1 deve ser um [Sampler (Direct3D 9 asm-ps)](dx9-graphics-reference-asm-ps-registers-sampler.md) (s \# ), sem modificador. Swizzle é permitido em src1 e, quando aplicado, os resultados da pesquisa de textura são pré-swizzled antes de gravados em dst.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Instruções do sombreador de pixel](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 