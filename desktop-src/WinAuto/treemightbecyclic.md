---
title: TreeMightBeCyclic
description: TreeMightBeCyclic
ms.assetid: 9A997949-A1A2-448C-9739-BE176621F1B4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d9647f4429ba17226f342a8dceb3c51b033d08b4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104294108"
---
# <a name="treemightbecyclic"></a>TreeMightBeCyclic

## <a name="text"></a>Texto

A árvore tem {0} níveis de profundidade. Isso pode indicar que a árvore de acessibilidade é cíclica e, portanto, pareceria infinita.

## <a name="type"></a>Tipo

Erro

## <a name="description"></a>Descrição

A árvore de elementos é cíclica e a profundidade da árvore pode ser infinita.

Esse problema causa problemas para as pessoas que contam com um leitor de tela e um teclado para navegação porque não haverá nenhum limite aparente para a passagem de elementos no aplicativo de destino.

## <a name="possible-causes"></a>Possíveis causas

Vários elementos, ou seus pais, são controles personalizados que não implementam a Tabulação corretamente. Por exemplo, a propriedade de [estado](state-property.md) MSAA não é atualizada corretamente.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Diretrizes para design de interface de usuário de teclado](/previous-versions/windows/desktop/dnacc/guidelines-for-keyboard-user-interface-design)
</dt> <dt>

[Diretrizes de interação da experiência do usuário do Windows – teclado](https://msdn.microsoft.com/library/bb545460.aspx#guidelines)
</dt> </dl>

 

 