---
title: RET-vs
description: Retornar de uma sub-rotina ou de uma função main.
ms.assetid: ee3a6a7a-c068-442f-9f86-c637b5707224
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 3b91a9f2fb30dbd243e29043a1655d441215bc75
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104293563"
---
# <a name="ret---vs"></a>RET-vs

Retornar de uma sub-rotina ou de uma função main.

## <a name="syntax"></a>Syntax



| RET |
|-----|



 

## <a name="remarks"></a>Comentários



| Versões do sombreador de vértice | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|------------------------|------|------|------|-------|------|-------|
| RET                    |      | x    | x    | x     | x    | x     |



 

Essa instrução usa o endereço de uma instrução da pilha de endereços de retorno e continua a execução a partir dela. No caso da função main, essa instrução interrompe a execução do sombreador.

A instrução RET consome um slot de instrução de sombreador de vértice.

Se um sombreador não contiver nenhuma sub-rotina, o uso de RET no final do programa principal será opcional.

Várias instruções de retorno não são permitidas no programa principal ou em qualquer sub-rotina, a primeira instrução de retorno é tratada como o fim do programa principal ou da sub-rotina.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Instruções do sombreador de vértice](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




