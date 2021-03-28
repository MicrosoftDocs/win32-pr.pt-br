---
title: Tex-PS
description: Carrega o registro de destino com dados de cor (RGBA) amostrados de uma textura. A textura deve estar associada a um estágio de textura específico (n) usando SetTexture. A amostragem de textura é controlada por setsamplestate.
ms.assetid: vs|directx_sdk|~\tex___ps.htm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a3070883b167d26cf31f7d7f388f6bd3736a4bde
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103917459"
---
# <a name="tex---ps"></a>Tex-PS

Carrega o registro de destino com dados de cor (RGBA) amostrados de uma textura. A textura deve estar associada a um estágio de textura específico (n) usando [**SetTexture**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture). A amostragem de textura é controlada por [**Setsamplestate**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-setsamplerstate).

## <a name="syntax"></a>Syntax



| Tex DST |
|---------|



 

onde

-   DST é o registro de destino.

## <a name="remarks"></a>Comentários



| Versões do sombreador de pixel | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| tex                   | x    | x    | x    |      |      |      |       |      |       |



 

O número de registro de destino especifica o número de estágio de textura.

A amostragem de textura usa coordenadas de textura para pesquisar ou obter um valor de cor nas coordenadas especificadas (u, v, w, q) ao levar em conta os atributos de estado do estágio de textura.

Os dados de coordenadas de textura são interpolados dos dados de coordenadas de textura de vértice e associados a um estágio de textura específico. A associação padrão é um mapeamento de um para um entre o número de estágio de textura e a ordem de declaração de coordenada de textura. Isso significa que o primeiro conjunto de coordenadas de textura definido no formato de vértice é, por padrão, associado ao estágio 0 da textura.

As coordenadas de textura podem ser associadas a qualquer estágio usando duas técnicas. Ao usar um sombreador de vértice de função fixa ou o pipeline de função fixa, o sinalizador de estado de estágio de textura TSS \_ TEXCOORDINDEX pode ser usado no [**SetTextureStageState**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate) para associar coordenadas a um estágio. Caso contrário, as coordenadas de textura são geradas pelo oTn do sombreador de vértice que registra ao usar um sombreador de vértice programável.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Instruções do sombreador de pixel](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 