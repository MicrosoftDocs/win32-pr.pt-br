---
title: label (sm4 – asm)
description: Indica o início de uma sub-rotina.
ms.assetid: B966AE64-47CA-4A13-A26F-184D9FD26C26
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d9075aa14d72893d7c7862361b44ff636dd9bb6fda62563087ca2404bd1d70b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118986456"
---
# <a name="label-sm4---asm"></a>label (sm4 – asm)

Indica o início de uma sub-rotina.



| label l\# |
|-----------|



 



| Item                                                       | Descrição                         |
|------------------------------------------------------------|-------------------------------------|
| <span id="l_"></span><span id="L_"></span>*L\#*<br/> | \[em \] O número do rótulo.<br/> |



 

## <a name="remarks"></a>Comentários

Um **rótulo** só pode aparecer diretamente após uma [**instrução ret**](ret--sm4---asm-.md) que não está aninhada em nenhuma instrução de controle de fluxo.

O código antes do primeiro **rótulo** em um programa é o programa principal. Todas as sub-rotinas aparecem no final do programa, indicadas por instruções **de** rótulo.

O exemplo a seguir mostra como usar essa instrução.

``` syntax
 
               ...
                call l3
                ...
                ret
                label l3
                    ...
                    if_nz r0.x
                        ret
                    endif
                    ...
                ret
```

Essa instrução se aplica aos seguintes estágios do sombreador:



| Sombreador de vértice | Sombreador de geometria | Sombreador de pixel |
|---------------|-----------------|--------------|
| x             | x               | x            |



 

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

 

 





