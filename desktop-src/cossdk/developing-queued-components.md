---
description: Desenvolvendo componentes em fila
ms.assetid: 867b7512-82ad-4877-8675-aa2d7e62ff8a
title: Desenvolvendo componentes em fila
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8808ef3e6cba8ff561dd94473fca8f00631081f2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646285"
---
# <a name="developing-queued-components"></a>Desenvolvendo componentes em fila

O serviço de componentes na fila do COM+ requer que todos os métodos de aplicativo contenham somente \[ \] parâmetros de parâmetro, sem valores de retorno. Como o objeto Server não está necessariamente disponível quando o cliente faz a chamada, os resultados do servidor podem ser retornados enviando uma mensagem que cria outro objeto. Dessa forma, a comunicação bidirecional não ocorre em todos os casos, mas apenas quando ela é necessária, por uma série de mensagens unidirecionais entre objetos.

Para usar o serviço de componentes na fila COM+, você deve ter o serviço de [enfileiramento de mensagens](/previous-versions/windows/desktop/legacy/ms711472(v=vs.85)) já instalado. O enfileiramento de mensagens não é instalado automaticamente. O enfileiramento de mensagens deve ser selecionado durante a configuração do sistema operacional ou usando **Adicionar/remover programas**. Um certificado interno do enfileiramento de mensagens é criado automaticamente no logon.

Os tópicos descritos na tabela a seguir fornecem considerações adicionais para situações mais especializadas.



| Tópico                                                                                           | Descrição                                                                                            |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [Passando objetos como parâmetros](passing-objects-as-parameters.md)s<br/>                   | Descreve como transmitir objetos como \[ parâmetros em \] componentes em fila.<br/>                    |
| [Limitações de segurança no modo de grupo de trabalho](security-limitations-in-workgroup-mode.md)<br/> | Descreve as limitações no uso da autenticação do serviço de enfileiramento de mensagens no modo de grupo de trabalho.<br/>       |
| [Considerações de thread](threading-considerations.md)<br/>                             | Descreve as preocupações específicas relacionadas à passagem de ponteiros de interface do gravador entre threads.<br/> |
| [Recebendo uma resposta](receiving-a-response.md)<br/>                                     | Descreve como construir uma resposta a uma chamada de componente enfileirada.<br/>                           |



 

 

 




