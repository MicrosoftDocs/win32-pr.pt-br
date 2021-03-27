---
title: Registro de endereço
description: O registro a0 é um registro de endereço.
ms.assetid: ad86013c-3358-4770-a01c-544c868691f4
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e58f42848034d12063611e14b82cb2f2d132cb43
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822851"
---
# <a name="address-register"></a>Registro de endereço

O registro a0 é um registro de endereço. Um único registro está disponível na versão vs \_ 1 \_ 1. O registro de endereço, designado como a0. x no vs \_ 1 \_ 1, pode ser usado como um deslocamento de inteiro assinado para o endereçamento relativo no arquivo de registro constante. Para versões vs \_ 2 \_ 0 e superiores, todos os quatro componentes (. x,. y,. z,. w) estão disponíveis para endereçamento relativo.


```
c[a0.x + n]
```



O registro de endereço não pode ser lido por um sombreador de vértice, ele só pode ser usado para endereçamento relativo de um registro constante. A leitura de valores fora do intervalo legal retornará (0,0, 0,0, 0,0, 0,0). O registro de endereço só pode ser um destino para a instrução [Mov-vs](mov---vs.md) . Se um número de ponto flutuante for movido para um registro de número inteiro, ocorrerá uma conversão de arredondamento mais próximo.

Todos os sombreadores devem inicializar o registro de endereço antes de usá-lo. Para a versão vs \_ 2 \_ 0 e superior, a instrução [mova-vs](mova---vs.md) pode mover um valor de ponto flutuante para um registro de endereço.



| Versões do sombreador de vértice | 1\_1 | 2 \_ 0 | 2 \_ SW | 2 \_ x | 3 \_ 0 | 3 \_ SW |
|------------------------|------|------|-------|------|------|-------|
| Registro de endereço       | x    | x    | x     | x    | x    | x     |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Registros de sombreador de vértice](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 




