---
title: TabbingNotCyclic
description: TabbingNotCyclic
ms.assetid: F6BCC613-1EA1-438C-AC09-8A282870E021
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e08fd2e9f6613e07840f432b646c1bdc06a34b5f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104007771"
---
# <a name="tabbingnotcyclic"></a>TabbingNotCyclic

## <a name="text"></a>Texto

A Tabulação neste aplicativo não é cíclica. A Tabulação ou os horários anteriores não retornam {0} ao mesmo controle.

## <a name="type"></a>Tipo

Erro

## <a name="description"></a>Descrição

Ao usar a navegação de teclado padrão (TAB ou Shift + Tab), não é possível atravessar a árvore de elementos do destino de verificação até que o elemento inicial se torne o elemento final (usando o mesmo número de pressionamentos de teclas), revertendo a direção da passagem. Por exemplo, a tabulação (Tab) x vezes do elemento A (0) para o elemento A (x) e, em seguida, tabulação retroativa (Shift + Tab) x vezes não resulta no elemento A (0) ao obter o foco.

Esse problema causa problemas para as pessoas que contam com um leitor de tela e um teclado para navegação porque não há uma maneira previsível de retornar a um controle depois de ele ter sido visitado.

## <a name="possible-causes"></a>Possíveis causas

-   O elemento ou seu pai é um controle personalizado que não implementa a Tabulação corretamente. Por exemplo, a propriedade de estado MSAA não está definida corretamente.
-   Alguns aplicativos, como o bloco de notas, exibem esse comportamento innatemente.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Diretrizes para design de interface de usuário de teclado](/previous-versions/windows/desktop/dnacc/guidelines-for-keyboard-user-interface-design)
</dt> </dl>

 

 