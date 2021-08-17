---
title: Registro de Cor de Saída
description: Os registros de saída de cor do sombreador de pixel (oC\ ) são registros somente gravação que saídam resultados para vários destinos de renderização.
ms.assetid: 88e69189-3956-47de-a336-921f1e62c025
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 038446bb7d588222e04028727a447b6a47c941ab6a18a3ba4216f46e93440961
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119119700"
---
# <a name="output-color-register"></a>Registro de Cor de Saída

Os registros de saída de cor do sombreador de pixel (oC#) são registros somente gravação que saídam resultados para vários destinos de renderização.

Syntax



| Oc # |
|------|



 

Em que:



| Nome | Descrição       |
|------|-------------------|
| oC0  | renderizar destino \# 0 |
| oC1  | renderizar destino \# 1 |
| oC2  | renderizar destino \# 2 |
| oC3  | renderizar destino \# 3 |



 

## <a name="remarks"></a>Comentários

-   Se oCn for gravado, mas não houver nenhum destino de renderização correspondente, essa gravação em oCn será ignorada.
-   Os estados de renderização D3DRS \_ COLORWRITEENABLE, D3DRS \_ COLORWRITEENABLE1, D3DRS \_ COLORWRITEENABLE2 e D3DRS COLORWRITEENABLE3 determinam quais componentes da oCn são gravados no destino de \_ renderização (após a combinação, se aplicável). Se o sombreador grava alguns, mas não todos os componentes definidos pelos estados de renderização D3DRS COLORWRITEENABLE para um determinado registro oCn, os canais não escritos produzirão valores indefinido no destino de \_ \* renderização correspondente. Se nenhum dos componentes de um oCn for gravado, o destino de renderização correspondente não deverá ser atualizado (conforme indicado acima), portanto, os estados de renderização COLORWRITEENABLE D3DRS não serão \_ \* aplicados.

### <a name="shader-model-2-restrictions"></a>Restrições do modelo de sombreador 2

-   oCn só pode ser escrito com a [instrução mov - ps.](mov---ps.md)
-   OC0 deve ser sempre gravado no sombreador.
-   Nenhuma swizzle de origem (exceto .xyzw = swizzle padrão) ou modificador de origem é permitido ao escrever em qualquer oCn.
-   Nenhuma máscara de gravação de destino (exceto .xyzw = máscara padrão) ou modificador de instrução é permitida ao gravar em qualquer oCn.
-   Se oCn for gravado, oC0 – oCn-1 também deverá ser gravado. Por exemplo, para gravar em oC2, você também deve gravar em oC0 e oC1.
-   No máximo uma gravação em qualquer oC# por sombreador é permitida.
-   Para ps 2 x e \_ ps 3 0, não é possível gravar em registros oC# e oD no controle de fluxo dinâmico ou na \_ \_ predicação (gravações em \_ oC# dentro do controle de fluxo estático é \# bom).

### <a name="shader-model-3-restrictions"></a>Restrições do modelo de sombreador 3

-   Para ps 3 0, os registros de saída \_ \_ oC# e oD podem ser \# gravados várias vezes. A saída do sombreador de pixel vem do conteúdo dos registros de saída no final da execução do sombreador. Se uma gravação em um registro de saída não acontecer, talvez devido ao controle de fluxo ou se o sombreador simplesmente não o tiver escrito, o rendertarget correspondente também não será atualizado. Se um subconjunto dos canais em um registro de saída for gravado, os valores indefinido serão gravados nos canais restantes.
-   Para ps \_ 3 \_ 0, os registros oC# podem ser gravados com qualquer writemasks.
-   Para ps 2 x e \_ ps 3 0, não é possível gravar em registros oC# e oD no controle de fluxo dinâmico ou na \_ \_ predicação (gravações em \_ oC# dentro do controle de fluxo estático é \# bom).
-   Você não pode executar nenhum cálculo de gradiente (ou operações que invocam implicitamente cálculos de gradiente, como [texld - ps \_ 2 \_ 0](texld---ps-2-0.md)e up , [texldb - ps](texldb---ps.md), [texldp - ps](texldp---ps.md)) dentro de instruções de controle de fluxo cujas condições de ramificação variam por primitivo (ou seja: instruções de controle de fluxo dinâmico). A predicação de instrução não é considerada controle de fluxo dinâmico.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Registros](dx9-graphics-reference-asm-ps-registers.md)
</dt> <dt>

[Vários destinos de renderização (Direct3D 9)](/windows/desktop/direct3d9/multiple-render-targets)
</dt> </dl>

 

 