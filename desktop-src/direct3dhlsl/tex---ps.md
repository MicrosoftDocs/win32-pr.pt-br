---
title: tex - ps
description: Carrega o registro de destino com dados de cor (RGBA) amostrados de uma textura. A textura deve ser vinculada a um estágio de textura específico (n) usando SetTexture. A amostragem de textura é controlada por SetSamplerState.
ms.assetid: vs|directx_sdk|~\tex___ps.htm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 0646a057fdc2fb96e5f72e7451b9b273191ced22f5092a14fab11a9042c5de25
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118788105"
---
# <a name="tex---ps"></a>tex - ps

Carrega o registro de destino com dados de cor (RGBA) amostrados de uma textura. A textura deve ser vinculada a um estágio de textura específico (n) usando [**SetTexture.**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) A amostragem de textura é [**controlada por SetSamplerState.**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-setsamplerstate)

## <a name="syntax"></a>Syntax



| tex dst |
|---------|



 

onde

-   dst é o registro de destino.

## <a name="remarks"></a>Comentários



| Versões do sombreador de pixel | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| Tex                   | x    | x    | x    |      |      |      |       |      |       |



 

O número do registro de destino especifica o número do estágio de textura.

A amostragem de textura usa coordenadas de textura para procurar ou amostrar um valor de cor nas coordenadas especificadas (u,v,w,q) ao levar em conta os atributos de estado do estágio de textura.

Os dados da coordenada de textura são interpolados dos dados de coordenadas de textura de vértice e estão associados a um estágio de textura específico. A associação padrão é um mapeamento de um para um entre o número do estágio de textura e a ordem de declaração da coordenada de textura. Isso significa que o primeiro conjunto de coordenadas de textura definido no formato de vértice está associado por padrão ao estágio de textura 0.

As coordenadas de textura podem ser associadas a qualquer estágio usando duas técnicas. Ao usar um sombreador de vértice de função fixa ou o pipeline de funções fixas, o sinalizador de estado de estágio de textura TSS TEXCOORDINDEX pode ser usado em \_ [**SetTextureStageState**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate) para associar coordenadas a um estágio. Caso contrário, as coordenadas de textura são saída pelo sombreador de vértice que oTn registra ao usar um sombreador de vértice programável.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Instruções do sombreador de pixel](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 