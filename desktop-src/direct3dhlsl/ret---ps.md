---
title: RET-PS
description: Pega o endereço de uma instrução da pilha de endereços de retorno e continua a execução a partir dela. No caso da função main, essa instrução interrompe a execução do sombreador.
ms.assetid: f853a137-8944-4f6e-89c0-7fd37d1a468e
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b0535a4fcd66a1872b5eaa9ec97c292de710b48c
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104967099"
---
# <a name="ret---ps"></a>RET-PS

Pega o endereço de uma instrução da pilha de endereços de retorno e continua a execução a partir dela. No caso da função main, essa instrução interrompe a execução do sombreador.

## <a name="syntax"></a>Syntax



| RET |
|-----|



 

## <a name="remarks"></a>Comentários



| Versões do sombreador de pixel | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| RET                   |      |      |      |      |      | x    | x     | x    | x     |



 

Essa instrução usa o endereço de uma instrução da pilha de endereços de retorno e continua a execução a partir dela. No caso da função main, essa instrução interrompe a execução do sombreador.

A instrução RET consome um slot de instrução de sombreador de vértice.

Se um sombreador não contiver nenhuma sub-rotina, o uso de RET no final do programa principal será opcional.

Várias instruções de retorno não são permitidas no programa principal ou em qualquer sub-rotina, a primeira instrução de retorno é tratada como o fim do programa principal ou da sub-rotina.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Instruções do sombreador de pixel](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




