---
description: Erros de componentes na fila
ms.assetid: 29a1bf52-7252-4f8a-bdb7-61b152fb907e
title: Erros de componentes na fila
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 422ea9c7ff77f2d69633d6db8b8d48c63fabc071
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105793901"
---
# <a name="queued-components-errors"></a>Erros de componentes na fila

Quando uma chamada para um componente em fila falha, porque não pôde ser transmitida ao servidor (falha no lado do cliente) ou porque ele não pôde ser executado quando chegou (uma falha no servidor), a mensagem de [enfileiramento de mensagens](/previous-versions/windows/desktop/legacy/ms711472(v=vs.85)) correspondente é chamada de *mensagem suspeita*.

O serviço de componentes em fila COM+ manipula mensagens suspeitas usando uma série de filas de repetição. Após várias tentativas, a mensagem é movida para uma fila de repouso final. As mensagens permanecem na fila de repouso até que sejam movidas manualmente usando o utilitário enfileiramento de mensagens dos componentes em fila. Para obter mais informações sobre como usar o movimentador de mensagem, consulte [Manipulando erros](handling-errors-in-queued-components.md).

Descrições detalhadas da sequência de eventos que ocorrem para vários tipos de erros podem ser encontradas nos tópicos descritos na tabela a seguir.



| Tópico                                                                             | Descrição                                                                                                             |
|-----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [Erros do lado do servidor](server-side-errors.md)<br/>                           | Descreve em detalhes a resposta do serviço de componentes em fila COM+ para uma falha no servidor.<br/>             |
| [Erros do lado do cliente](client-side-errors.md)<br/>                           | Descreve em detalhes a resposta do serviço de componentes em fila COM+ para uma falha do lado do cliente.<br/>             |
| [Falhas de Client-Side persistentes](persistent-client-side-failures.md)<br/> | Descreve em detalhes a resposta do serviço de componentes em fila COM+ para falhas repetidas do lado do cliente.<br/> |



 

 

 




