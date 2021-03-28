---
title: Call-vs
description: Executa uma chamada de função para a instrução marcada com o rótulo fornecido. | Call-vs
ms.assetid: 3c1ec529-1ee4-40d9-8ce5-f8e7a61fde9c
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c797e7ef6745f5710752fe059d2a2ff1f94a8aa3
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "103930520"
---
# <a name="call---vs"></a>Call-vs

Executa uma chamada de função para a instrução marcada com o rótulo fornecido.

## <a name="syntax"></a>Syntax



| chamar l\# |
|----------|



 

Onde l \# é um [rótulo-vs](label---vs.md) marcando o início da sub-rotina a ser chamada.

## <a name="remarks"></a>Comentários



| Versões do sombreador de vértice | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|------------------------|------|------|------|-------|------|-------|
| chamada                   |      | x    | x    | x     | x    | x     |



 

Essa instrução faz o seguinte:

1.  Endereço de push da próxima instrução para a pilha de endereços de retorno.
2.  Continue a execução da instrução marcada pelo rótulo.

No sombreador de vértice 2 \_ 0, não são permitidas chamadas de aninhamento.

No sombreador de vértice 2 \_ x, a profundidade de aninhamento é limitada pelo elemento StaticFlowControlDepth da estrutura [**D3DVSHADERCAPS2 \_ 0**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dvshadercaps2_0) . Para obter mais informações, consulte [**GetDeviceCaps**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9-getdevicecaps).

No sombreador de vértice 3 \_ 0, são permitidos quatro níveis de aninhamento de chamada.

Somente chamadas de encaminhamento são permitidas. Isso significa que o local do rótulo dentro do sombreador de vértice deve ser após a instrução Call que faz referência a ele.

Se uma instrução Call for invocada dentro do [loop](loop---vs.md)... bloco [ENDLOOP](endloop---vs.md) , o valor do [registro do contador de loop](dx9-graphics-reference-asm-vs-registers-loop-counter.md) (al) é acessível dentro da sub-rotina.

Se uma sub-rotina fizer referência ao [registro do contador de loop](dx9-graphics-reference-asm-vs-registers-loop-counter.md) (al) localizado fora da sub-rotina, cada instância da chamada para essa sub-rotina deverá ser circundada por um [loop](loop---vs.md)... bloco [ENDLOOP](endloop---vs.md) .

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Instruções do sombreador de vértice](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 
