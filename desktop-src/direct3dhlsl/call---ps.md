---
title: Call-PS
description: Executa uma chamada de função para a instrução marcada com o rótulo fornecido. | Call-PS
ms.assetid: d5f5e5a1-f205-477d-a11b-ff9eeeec6c95
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 27be29c478afdf92c29fefd16a82319e0899d2ec
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104989186"
---
# <a name="call---ps"></a>Call-PS

Executa uma chamada de função para a instrução marcada com o rótulo fornecido.

## <a name="syntax"></a>Syntax



| chamar l\# |
|----------|



 

Em que:

-   l \# é um [rótulo-PS](label---ps.md) marcando o início da sub-rotina a ser chamada.

## <a name="remarks"></a>Comentários



| Versões do sombreador de pixel | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| chamada                  |      |      |      |      |      | x    | x     | x    | x     |



 

Essa instrução faz o seguinte:

1.  Endereço de push da próxima instrução para a pilha de endereços de retorno.
2.  Continue a execução da instrução marcada pelo rótulo.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Instruções do sombreador de pixel](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




