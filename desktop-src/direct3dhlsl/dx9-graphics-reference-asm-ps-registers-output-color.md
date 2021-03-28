---
title: Registro de cor de saída
description: Os registros de saída de cor do sombreador de pixel (oC \) são registros somente gravação que geram resultados de saída para vários destinos de renderização.
ms.assetid: 88e69189-3956-47de-a336-921f1e62c025
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 316160e39ce172d56e4ecac17dfbd1d53077005b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366509"
---
# <a name="output-color-register"></a>Registro de cor de saída

Os registros de saída de cor do sombreador de pixel (oC #) são registros somente gravação que geram resultados de saída para vários destinos de renderização.

Syntax



| oC # |
|------|



 

Em que:



| Name | Descrição       |
|------|-------------------|
| oC0  | renderizar destino \# 0 |
| oC1  | destino de renderização \# 1 |
| oC2  | destino de renderização \# 2 |
| oC3  | destino de renderização \# 3 |



 

## <a name="remarks"></a>Comentários

-   Se oCn for gravado, mas não houver nenhum destino de renderização correspondente, essa gravação em oCn será ignorada.
-   Os Estados de renderização D3DRS \_ COLORWRITEENABLE, D3DRS \_ COLORWRITEENABLE1, D3DRS \_ COLORWRITEENABLE2 e D3DRS COLORWRITEENABLE3 \_ determinam quais componentes de oCn, por fim, são gravados no destino de renderização (após Blend, se aplicável). Se o sombreador gravar alguns, mas não todos os componentes definidos pelos \_ Estados de RENDERIZAÇÃO D3DRS COLORWRITEENABLE \* para um determinado registro oCn, os canais não gravados produzirão valores indefinidos no destino de renderização correspondente. Se nenhum dos componentes de um oCn for gravado, o destino de renderização correspondente não deverá ser atualizado (como mencionado acima), de modo que os \_ Estados de RENDERIZAÇÃO D3DRS COLORWRITEENABLE \* não se aplicarão.

### <a name="shader-model-2-restrictions"></a>Restrições do modelo de sombreador 2

-   oCn só pode ser escrito com a instrução [Mov-PS](mov---ps.md) .
-   oC0 deve ser sempre escrito no sombreador.
-   Nenhum swizzle de origem (exceto. xyzw = default swizzle) ou modificador de origem é permitido ao gravar em qualquer oCn.
-   Nenhuma máscara de gravação de destino (exceto. xyzw = máscara padrão) ou modificador de instrução é permitido ao gravar em qualquer oCn.
-   Se oCn for gravado, oC0-oCn-1 também deverá ser gravado. Por exemplo, para gravar em oC2, você também deve gravar em oC0 e oC1.
-   É permitido no máximo uma gravação para qualquer oC # por sombreador.
-   Para o PS \_ 2 \_ x e o PS \_ 3 \_ 0, não é possível gravar nos registros OC # e OD \# no controle de fluxo dinâmico ou predicação (as gravações para o OC # dentro do controle de fluxo estático estão corretas).

### <a name="shader-model-3-restrictions"></a>Restrições do modelo do sombreador 3

-   Para o PS \_ 3 \_ 0, os registros de saída OC # e OD \# podem ser gravados várias vezes. A saída do sombreador de pixel é proveniente do conteúdo dos registros de saída no final da execução do sombreador. Se uma gravação em um registro de saída não ocorrer, talvez devido ao controle de fluxo ou se o sombreador simplesmente não o escreveu, o renderTarget correspondente também não será atualizado. Se um subconjunto dos canais em um registro de saída for gravado, os valores indefinidos serão gravados nos canais restantes.
-   Para \_ o PS 3 \_ 0, os registros de OC # podem ser gravados com qualquer writemasks.
-   Para o PS \_ 2 \_ x e o PS \_ 3 \_ 0, não é possível gravar nos registros OC # e OD \# no controle de fluxo dinâmico ou predicação (as gravações para o OC # dentro do controle de fluxo estático estão corretas).
-   Você não pode executar cálculos de gradiente (ou operações que invocam implicitamente cálculos de gradiente, como [texld-PS \_ 2 \_ 0 e up](texld---ps-2-0.md), [texldb-PS](texldb---ps.md), [texldp-PS](texldp---ps.md)) dentro de instruções de controle de fluxo cujas condições de ramificação variam em uma base por primitiva (isto é: instruções de controle de fluxo dinâmico). Instrução predicação não é considerada controle de fluxo dinâmico.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Register](dx9-graphics-reference-asm-ps-registers.md)
</dt> <dt>

[Vários destinos de renderização (Direct3D 9)](/windows/desktop/direct3d9/multiple-render-targets)
</dt> </dl>

 

 