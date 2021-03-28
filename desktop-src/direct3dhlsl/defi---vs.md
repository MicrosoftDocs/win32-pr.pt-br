---
title: defi-vs
description: Define um valor constante inteiro, que deve ser carregado sempre que um sombreador for definido como um dispositivo.
ms.assetid: d6067a7d-58fb-4553-a42f-192c29bf78b7
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 897a544cc9974b8ffa727f2d39219cfeab82d52a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104499117"
---
# <a name="defi---vs"></a>defi-vs

Define um valor constante inteiro, que deve ser carregado sempre que um sombreador for definido como um dispositivo.

## <a name="syntax"></a>Syntax



| defi DST, integerValue0, integerValue1, integerValue2, integerValue3 |
|----------------------------------------------------------------------|



 

-   DST é o registro de destino.
-   integerValue \# é um valor inteiro constante.

## <a name="remarks"></a>Comentários



| Versões do sombreador de vértice | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|------------------------|------|------|------|-------|------|-------|
| defi                   |      | x    | x    | x     | x    | x     |



 

A instrução defi define uma constante de sombreador inteiro cujo valor é carregado sempre que um sombreador é definido como um dispositivo. Elas são chamadas de constantes imediatas. Constantes imediatas têm precedência sobre constantes definidas pelo método de API SetVertexShaderConstantI.

Há duas maneiras de definir uma constante de inteiro em um sombreador.

1.  Use defi para definir o vetor de constante de inteiro diretamente dentro de um sombreador.
2.  Use os métodos de API para definir uma constante.
    -   Use [**SetVertexShaderConstantI**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshaderconstanti) para definir uma constante de inteiro.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Instruções do sombreador de vértice](dx9-graphics-reference-asm-vs-instructions.md)
</dt> <dt>

[def-vs](def---vs.md)
</dt> <dt>

[DEFB-vs](defb---vs.md)
</dt> </dl>

 

 