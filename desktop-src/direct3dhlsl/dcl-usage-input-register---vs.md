---
title: entrada de dcl_usage (SM1, SM2, SM3-vs ASM)
description: Declare a associação entre um uso de elemento de vértice e um índice de uso para um registro de entrada de sombreador de vértice.
ms.assetid: e0360f4d-1250-4dc5-b790-372b303a37a8
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 44bd976d05c0734ca2e498b5de405564f689e20d
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107998383"
---
# <a name="dcl_usage-input-sm1-sm2-sm3---vs-asm"></a>\_entrada de uso de DCL (SM1, SM2, SM3-vs ASM)

Declare a associação entre um uso de elemento de vértice e um índice de uso para um registro de entrada de sombreador de vértice.

## <a name="syntax"></a>Sintaxe



|                                |
|--------------------------------|
| índice de uso de uso de DCL \_ \[ \_ \] v\# |



 

Em que:

-   \_o uso de DCL identifica como os dados de registro serão usados. Esse é o mesmo valor que os membros de [**D3DDECLUSAGE**](/windows/desktop/direct3d9/d3ddeclusage) sem o prefixo D3DDECLUSAGE.
-   \_o índice de uso é um índice de inteiro opcional entre 0 e 15. Ele modifica os dados de uso. O índice corresponde ao índice de uso em uma declaração de vértice. Consulte [declaração de vértice (Direct3D 9)](/windows/desktop/direct3d9/vertex-declaration). O índice é anexado ao valor de uso (uso de DCL \_ ) sem espaço. Se não for fornecido, será considerado 0.
-   v \# é um [registro de entrada](dx9-graphics-reference-asm-vs-registers-input.md).

## <a name="remarks"></a>Comentários



| Versões do sombreador de vértice | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|------------------------|------|------|------|-------|------|-------|
| uso de DCL \_             | x    | x    | x    | x     | x    | x     |



 

Todas as \_ instruções de uso de DCL devem aparecer antes da primeira instrução executável.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Instruções do sombreador de vértice](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 
