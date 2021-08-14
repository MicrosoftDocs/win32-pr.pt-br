---
title: dcl_usage entrada (sm1, sm2, sm3 – vs asm)
description: Declare a associação entre o uso de um elemento de vértice e um índice de uso para um registro de entrada do sombreador de vértice.
ms.assetid: e0360f4d-1250-4dc5-b790-372b303a37a8
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f94a9fb8e46da811652b334824779d59153c87616f7f9815dbebd8224870ddec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118792818"
---
# <a name="dcl_usage-input-sm1-sm2-sm3---vs-asm"></a>entrada de \_ uso dcl (sm1, sm2, sm3 – vs asm)

Declare a associação entre o uso de um elemento de vértice e um índice de uso para um registro de entrada do sombreador de vértice.

## <a name="syntax"></a>Sintaxe

dcl \_ usage \[ index \_ \] v\#



 

Em que:

-   O uso de dcl \_ identifica como os dados de registro serão usados. Esse é o mesmo valor que os membros [**de D3DDECLUSAGE**](/windows/desktop/direct3d9/d3ddeclusage) sem o prefixo D3DDECLUSAGE.
-   índice \_ de uso é um índice inteiro opcional entre 0 e 15. Modifica os dados de uso. O índice corresponde ao índice de uso em uma declaração de vértice. Consulte [Declaração de vértice (Direct3D 9)](/windows/desktop/direct3d9/vertex-declaration). O índice é anexado ao valor de uso (uso de dcl \_ ) sem espaço. Se não for fornecido, supõe-se que seja 0.
-   v \# é um Registro de [Entrada](dx9-graphics-reference-asm-vs-registers-input.md).

## <a name="remarks"></a>Comentários



| Versões do sombreador de vértice | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|------------------------|------|------|------|-------|------|-------|
| uso \_ de dcl             | x    | x    | x    | x     | x    | x     |



 

Todas as instruções de uso de dcl \_ devem aparecer antes da primeira instrução executável.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Instruções do sombreador de vértice](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 
