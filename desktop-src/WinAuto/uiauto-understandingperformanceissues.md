---
title: Noções básicas sobre problemas de desempenho
description: Este tópico descreve os problemas de desempenho associados ao uso dos padrões de controle Text e TextRange.
ms.assetid: D78BFFA8-E303-441D-9D32-AD22E1B1A249
keywords:
- clientes, compreendendo problemas de desempenho
- clientes, controles baseados em texto
- clientes, intervalos de texto
- clientes, padrão de controle de texto
- clientes, padrão de controle TextRange
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61d8d9b9b6c5cb0ef3ed34c6960e5aeafa623068
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/04/2020
ms.locfileid: "104294623"
---
# <a name="understanding-performance-issues"></a>Noções básicas sobre problemas de desempenho

Este tópico descreve os problemas de desempenho associados ao uso dos padrões de controle [Text e TextRange](uiauto-implementingtextandtextrange.md) .


As interfaces [**IUIAutomationTextPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtextpattern) e [**IUIAutomationTextRange**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtextrange) dependem de chamadas de processo cruzado — elas não fornecem um mecanismo de cache para melhorar o desempenho ao recuperar ou processar conteúdo textual.

Um aplicativo cliente pode melhorar o desempenho usando o método [**IUIAutomationTextRange:: gettext**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-gettext) para recuperar blocos de texto de tamanho moderado. Por exemplo, usar **gettext** para recuperar caracteres únicos incorrerá em um impacto de desempenho entre processos para cada caractere, enquanto não especificar um comprimento máximo ao chamar **gettext** incorrerá em um impacto entre processos, mas poderá ter alta latência dependendo do tamanho do intervalo de texto.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Padrões de controle Text e TextRange](uiauto-implementingtextandtextrange.md)
</dt> <dt>

[Suporte à automação da interface do usuário para conteúdo textual](uiauto-ui-automation-textpattern-overview.md)
</dt> <dt>

[Trabalhando com controles baseados em texto](uiauto-workingwithtextbasedcontrols.md)
</dt> </dl>

 

 




