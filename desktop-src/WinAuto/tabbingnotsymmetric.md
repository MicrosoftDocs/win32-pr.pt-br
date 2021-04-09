---
title: TabbingNotSymmetric
description: TabbingNotSymmetric
ms.assetid: 1E14ED9F-27C1-4054-B0A6-702167222196
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc19efbbbce0f299044726466dd8f87b133fc26d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104084661"
---
# <a name="tabbingnotsymmetric"></a>TabbingNotSymmetric

## <a name="text"></a>Texto

A tabulação para trás e para frente não produz o mesmo elemento. Esperado {0} , mas recebido {1}

## <a name="type"></a>Tipo

Erro

## <a name="description"></a>Descrição

Ao usar a navegação de teclado padrão (TAB ou Shift + Tab), não é possível repetir o caminho de passagem por meio da árvore de elementos do destino de verificação se a direção de passagem for invertida. Por exemplo, a tabulação (Tab) x vezes do elemento A (0) para o elemento A (x) e, em seguida, tabulação retroativa (Shift + Tab) x vezes resulta no elemento A (0) recuperando o foco por meio de um conjunto diferente de elementos intermediários.

Esse problema causa problemas para as pessoas que contam com um leitor de tela e um teclado para navegação porque a passagem de elementos parece irregular e imprevisível.

## <a name="possible-causes"></a>Possíveis causas

-   Vários elementos ou seus pais são controles personalizados que não implementam a Tabulação corretamente. Por exemplo, a propriedade de estado MSAA não está definida corretamente.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Diretrizes para design de interface de usuário de teclado](/previous-versions/windows/desktop/dnacc/guidelines-for-keyboard-user-interface-design)
</dt> </dl>

 

 