---
title: call - ps
description: Executa uma chamada de função para a instrução marcada com o rótulo fornecido. | call - ps
ms.assetid: d5f5e5a1-f205-477d-a11b-ff9eeeec6c95
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 7ae1b8a19178b0a6633a98472814e225e9ac2f7de9e3e2f016720f2f5b1a9b3a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118794080"
---
# <a name="call---ps"></a>call - ps

Executa uma chamada de função para a instrução marcada com o rótulo fornecido.

## <a name="syntax"></a>Syntax



| call l\# |
|----------|



 

Em que:

-   l \# é um rótulo – [ps](label---ps.md) marcando o início da sub-rotina a ser chamada.

## <a name="remarks"></a>Comentários



| Versões do sombreador de pixel | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| chamada                  |      |      |      |      |      | x    | x     | x    | x     |



 

Essa instrução faz o seguinte:

1.  Endereço de push da próxima instrução para a pilha de endereços de retorno.
2.  Continue a execução da instrução marcada pelo rótulo.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Instruções do sombreador de pixel](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




