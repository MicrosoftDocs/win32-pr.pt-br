---
description: Considerações de thread
ms.assetid: 4d27f0b3-3e30-4e88-b2b2-d57218da4ffa
title: Considerações de thread
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8acde9a06802a867cb6a93e7c52be8066ad483c3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010282"
---
# <a name="threading-considerations"></a>Considerações de thread

O gravador de componentes em fila do COM+ é capaz de ser executado no MTA (multithreaded apartment) do processo ou em um STA (single-threaded apartment). Quando o gravador é executado no STA, o COM+ requer que cada apartamento contendo objetos deva ter uma fila de [enfileiramento de mensagens](/previous-versions/windows/desktop/legacy/ms711472(v=vs.85)) para manipular chamadas de outros processos e Apartments dentro do mesmo processo. Isso significa que a função de trabalho do thread deve ter um loop de mensagem. Quando um componente em fila é instanciado, o ponteiro de interface retornado é sempre um ponteiro de interface proxy em vez de um ponteiro de interface direta. O ponteiro é, na verdade, uma referência a uma instância do gravador. Se essa referência da interface do gravador for passada para outro thread, o thread original ainda deverá estar executando o loop de mensagem do Windows para que o thread receptor possa desempacotar a interface. Se esse não for o caso, o thread de recebimento travará em uma chamada para [**CoUnmarshalInterface**](/windows/desktop/api/combaseapi/nf-combaseapi-counmarshalinterface).

Se você estiver usando primitivos para sincronizar os threads, considere usar [**MsgWaitForMultipleObjects**](/windows/desktop/api/winuser/nf-winuser-msgwaitformultipleobjects) em vez de outras funções de sincronização. Isso verifica as mensagens na fila, bem como o estado do objeto de sincronização.

 

 
