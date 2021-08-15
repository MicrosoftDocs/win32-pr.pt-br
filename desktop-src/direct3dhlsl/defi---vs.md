---
title: defi – vs
description: Define um valor constante inteiro, que deve ser carregado sempre que um sombreador é definido como um dispositivo.
ms.assetid: d6067a7d-58fb-4553-a42f-192c29bf78b7
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 5568a9d1db49dadb9e0e6497cfd4e5af357054f930c35ec6a7e05d59d5f60965
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117726676"
---
# <a name="defi---vs"></a>defi – vs

Define um valor constante inteiro, que deve ser carregado sempre que um sombreador é definido como um dispositivo.

## <a name="syntax"></a>Syntax



| defi dst, integerValue0, integerValue1, integerValue2, integerValue3 |
|----------------------------------------------------------------------|



 

-   dst é o registro de destino.
-   integerValue \# é um valor inteiro constante.

## <a name="remarks"></a>Comentários



| Versões do sombreador de vértice | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|------------------------|------|------|------|-------|------|-------|
| Defi                   |      | x    | x    | x     | x    | x     |



 

A instrução defi define uma constante de sombreador de inteiro cujo valor é carregado sempre que um sombreador é definido como um dispositivo. Elas são chamadas constantes imediatas. Constantes imediatas têm precedência sobre constantes definidas pelo método de API SetVertexShaderConstantI.

Há duas maneiras de definir uma constante de inteiro em um sombreador.

1.  Use defi para definir o vetor de constante de inteiro diretamente dentro de um sombreador.
2.  Use os métodos de API para definir uma constante.
    -   Use [**SetVertexShaderConstantI**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshaderconstanti) para definir uma constante de inteiro.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Instruções do sombreador de vértice](dx9-graphics-reference-asm-vs-instructions.md)
</dt> <dt>

[def – vs](def---vs.md)
</dt> <dt>

[defb – vs](defb---vs.md)
</dt> </dl>

 

 