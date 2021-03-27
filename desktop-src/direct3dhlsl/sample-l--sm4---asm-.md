---
title: sample_l (sm4-ASM)
description: Amostras de dados do elemento/textura especificado usando o endereço especificado e o modo de filtragem identificados pelo determinado exemplo. | sample_l (sm4-ASM)
ms.assetid: D285F63E-1026-45F1-9959-6F5AB2A27C95
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5acd83d81e4648cc9eae5f8e0166013dcca512a8
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104298321"
---
# <a name="sample_l-sm4---asm"></a>exemplo \_ l (sm4-ASM)

Amostras de dados do elemento/textura especificado usando o endereço especificado e o modo de filtragem identificados pelo determinado exemplo.



| exemplo \_ l \[ \_ aoffimmi (u, v, w) \] dest \[ . Mask \] , srcAddress \[ . swizzle \] , srcResource \[ . swizzle \] , srcSampler, srcLOD. selecionar \_ componente |
|-------------------------------------------------------------------------------------------------------------------------------------|



 



| Item                                                                                                               | Descrição                                                                                                                |
|--------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/>                                                    | \[no \] endereço dos resultados da operação.<br/>                                                             |
| <span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*<br/>     | \[em \] um conjunto de coordenadas de textura. Para obter mais informações, consulte a instrução de [exemplo](sample--sm4---asm-.md) .<br/> |
| <span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*<br/> | \[em \] um registro de textura. Para obter mais informações, consulte a instrução de **exemplo** .<br/>                                 |
| <span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcSampler*<br/>     | \[em \] um registro de amostra. Para obter mais informações, consulte a instrução de **exemplo** .<br/>                                 |
| <span id="srcLOD"></span><span id="srclod"></span><span id="SRCLOD"></span>*srcLOD*<br/>                     | \[no \] LOD.<br/>                                                                                                 |



 

## <a name="remarks"></a>Comentários

Essa instrução é idêntica à [amostra](sample--sm4---asm-.md), exceto que LOD é fornecido diretamente pelo aplicativo como um valor escalar, que não representa anisotropy. Essa instrução está disponível em todos os estágios do sombreador progammable.

o **exemplo \_ l amostra** a textura usando *SRCLOD* para ser a LOD. Se o valor de LOD for <= 0, o zero'th (maior mapa) será escolhido, com o filtro de ampliação aplicado (se for aplicável com base no modo de filtro). Como *srcLOD* é um valor de ponto flutuante, o valor fracionário é usado para interpolar entre dois níveis MIP, se o filtro reduzir for linear ou com filtragem anisotropic.

o **exemplo \_ l** ignora as derivações de endereço, portanto, o comportamento de filtragem é puramente isotropic. Como derivações são ignoradas, a filtragem de anisotropic se comporta como filtragem de isotropic.

Os Estados de amostra MIPLODBIAS e MAX/MINMIPLEVEL são respeitados.

Quando usado no sombreador de pixel, o **exemplo \_ l** indica que a escolha de LOD é por pixel, sem efeito de pixels vizinhos, por exemplo, no mesmo carimbo 2x2.

A busca de um slot de entrada que não tem nada associado a ele retorna 0 para todos os componentes.

Essa instrução se aplica aos seguintes estágios de sombreador:



| Sombreador de vértice | Sombreador de geometria | Sombreador de pixel |
|---------------|-----------------|--------------|
| X             | X               | x            |



 

## <a name="minimum-shader-model"></a>Modelo de sombreamento mínimo

Essa função tem suporte nos seguintes modelos de sombreador.



| Modelo de Sombreador                                              | Com suporte |
|-----------------------------------------------------------|-----------|
| [Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)        | sim       |
| [Modelo do sombreador 4,1](dx-graphics-hlsl-sm4.md)              | sim       |
| [Modelo de sombreador 4](dx-graphics-hlsl-sm4.md)                | sim       |
| [Modelo de sombreador 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | não        |
| [Modelo de sombreador 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | não        |
| [Modelo de sombreador 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | não        |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Assembly do Shader Model 4 (DirectX HLSL)](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





