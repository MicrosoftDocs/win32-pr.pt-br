---
description: Desenvolvendo componentes na fila
ms.assetid: 867b7512-82ad-4877-8675-aa2d7e62ff8a
title: Desenvolvendo componentes na fila
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77cddcbbdf9048d94b9d0269db070961fcdf6c25c0323d28f2ad37f4fd37081d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118813937"
---
# <a name="developing-queued-components"></a>Desenvolvendo componentes na fila

O serviço de componentes em fila COM+ requer que todos os métodos de aplicativo contenham somente em \[ \] parâmetros, sem valores de retorno. Como o objeto de servidor não está necessariamente disponível quando o cliente faz a chamada, os resultados do servidor podem ser retornados enviando uma mensagem que cria outro objeto. Dessa forma, a comunicação de duas vias ocorre não em todos os casos, mas apenas quando ela é necessária, por uma série de mensagens únicas entre objetos.

Para usar o serviço de componentes em fila COM+, você deve ter o serviço [de En fila de](/previous-versions/windows/desktop/legacy/ms711472(v=vs.85)) mensagens já instalado. O En fila de mensagens não é instalado automaticamente. O En fila de mensagens deve ser selecionado durante a configuração do sistema operacional ou usando **Adicionar/Remover programas**. Um certificado interno de En fila de mensagens é criado automaticamente no logon.

Os tópicos descritos na tabela a seguir fornecem considerações adicionais para situações mais especializadas.



| Tópico                                                                                           | Descrição                                                                                            |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [Passando objetos como parâmetro](passing-objects-as-parameters.md)s<br/>                   | Descreve como passar objetos como \[ \] parâmetros para componentes na fila.<br/>                    |
| [Limitações de segurança no modo de grupo de trabalho](security-limitations-in-workgroup-mode.md)<br/> | Descreve as limitações do uso da autenticação de Enxuamento de Mensagens no modo de grupo de trabalho.<br/>       |
| [Considerações de thread](threading-considerations.md)<br/>                             | Descreve preocupações específicas relacionadas à passagem de ponteiros de interface de gravador entre threads.<br/> |
| [Recebendo uma resposta](receiving-a-response.md)<br/>                                     | Descreve como construir uma resposta a uma chamada de componente na fila.<br/>                           |



 

 

 




