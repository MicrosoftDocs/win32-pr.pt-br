---
title: TabbingNotCyclic
description: TabbingNotCyclic
ms.assetid: F6BCC613-1EA1-438C-AC09-8A282870E021
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ce9c914f5919d0433d653b8b61bd04832fb24bf3c9e78da4b1754fee40600e2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117929093"
---
# <a name="tabbingnotcyclic"></a>TabbingNotCyclic

## <a name="text"></a>Texto

A tabulação neste aplicativo não é cíclica. A tabulação para frente ou para {0} trás não volta para o mesmo controle.

## <a name="type"></a>Tipo

Erro do

## <a name="description"></a>Descrição

Ao usar a navegação de teclado padrão (Tab ou Shift+Tab), não é possível percorrer a árvore de elementos do destino de verificação até que o elemento inicial se torne o elemento final (usando o mesmo número de teclas) revertendo a direção da travessia. Por exemplo, a tabulação para frente (Tab) x vezes do elemento A(0) para o elemento A(x) e, em seguida, a tabulação para trás (Shift+Tab) x vezes não resulta no elemento A(0) recuperar o foco.

Esse problema causa problemas para as pessoas que dependem de um leitor de tela e teclado para navegação porque não há uma maneira previsível de retornar a um controle depois que ele foi visitado.

## <a name="possible-causes"></a>Possíveis causas

-   O elemento ou seu pai é um controle personalizado que não implementa a tabulação corretamente. Por exemplo, a propriedade Estado da MSAA não está definida corretamente.
-   Alguns aplicativos, como o Bloco de notas, exibem esse comportamento inatamente.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Diretrizes para design de Interface do Usuário teclado](/previous-versions/windows/desktop/dnacc/guidelines-for-keyboard-user-interface-design)
</dt> </dl>

 

 