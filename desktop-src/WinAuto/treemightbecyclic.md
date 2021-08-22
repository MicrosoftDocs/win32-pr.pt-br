---
title: TreeMightBeCyclic
description: TreeMightBeCyclic
ms.assetid: 9A997949-A1A2-448C-9739-BE176621F1B4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0af2f8d93c3b38b52871db031419756507e009f7d8adb369fde9b5b2c154fbec
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119614427"
---
# <a name="treemightbecyclic"></a>TreeMightBeCyclic

## <a name="text"></a>Texto

A árvore tem {0} níveis profundos. Isso pode indicar que a árvore de acessibilidade é cíclica e, portanto, pareceria ser infinita.

## <a name="type"></a>Tipo

Erro

## <a name="description"></a>Descrição

A árvore de elementos é cíclica e a profundidade da árvore pode ser infinita.

Esse problema causa problemas para pessoas que dependem de um leitor de tela e teclado para navegação, pois não haverá nenhum limite aparente para a travessia de elementos no aplicativo de destino.

## <a name="possible-causes"></a>Possíveis causas

Vários elementos, ou seus pais, são controles personalizados que não implementam tabulação corretamente. Por exemplo, a propriedade [](state-property.md) Estado da MSAA não foi atualizada corretamente.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Diretrizes para design de Interface do Usuário teclado](/previous-versions/windows/desktop/dnacc/guidelines-for-keyboard-user-interface-design)
</dt> <dt>

[Windows Diretrizes de interação da experiência do usuário – teclado](https://msdn.microsoft.com/library/bb545460.aspx#guidelines)
</dt> </dl>

 

 