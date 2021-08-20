---
title: TabbedToUnknownElement
description: TabbedToUnknownElement
ms.assetid: B0447B19-E281-4D30-8ED8-FC0EE13571C8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5acee341066ee5a456d412554ead3342c8513ae89e50a056a2372a291b0a88b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119052394"
---
# <a name="tabbedtounknownelement"></a>TabbedToUnknownElement

## <a name="text"></a>Texto

A Tabulação foi movida para um elemento fora do HWND de destino.

## <a name="type"></a>Tipo

Erro

## <a name="description"></a>Descrição

Usar a navegação de teclado padrão (TAB ou Shift + Tab) faz com que o foco seja deslocado para fora do HWND do destino de verificação.

AccChecker move a árvore de elementos para o HWND de nível superior para o destino de verificação escolhido antes de executar qualquer tarefa de verificação. Isso reduz o número de erros falsos gerados se um HWND escolhido para verificação fizer parte de uma área de cliente mais complexa.

## <a name="possible-causes"></a>Possíveis causas

-   O destino de verificação não requer uma implementação de tabulação para fornecer funcionalidade completa.
-   A interação do usuário durante a verificação, como a movimentação do foco para um HWND não-alvo, interfere no processo de verificação.

 

 




