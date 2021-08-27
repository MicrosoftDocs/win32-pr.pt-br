---
description: O Winlogon envia mensagens para a GINA enquanto as caixas de diálogo são exibidas. Essas mensagens são todas encapsuladas na \_ mensagem SAS do WLX WM da \_ seguinte maneira.
ms.assetid: 3da1c3d2-5116-47c3-98e4-f29b33693c69
title: Enviando mensagens para a GINA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb52da6a2a66d901207485ed97592a97286902ba51c54ec4924240ab9403a885
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118918315"
---
# <a name="sending-messages-to-the-gina"></a>Enviando mensagens para a GINA

O [*Winlogon*](../secgloss/w-gly.md) envia mensagens para a [*Gina*](../secgloss/g-gly.md) enquanto as caixas de diálogo são exibidas. Essas mensagens são todas encapsuladas na \_ mensagem SAS do WLX WM da \_ seguinte maneira.



| Tipo de sequência de atenção segura no parâmetro wParam | Descrição                                                                                                                                   |
|----------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| \_tipo de SAS WLX \_ \_ Ctrl \_ ALT \_ del                     | Indica que uma sequência de teclas CTRL + ALT + DEL foi recebida.                                                                                      |
| WLX \_ SAS \_ tipo \_ sc \_ Insert                         | Indica que um [*cartão inteligente*](../secgloss/s-gly.md) foi inserido em um dispositivo compatível. |
| WLX \_ SAS \_ tipo \_ sc \_ Remove                         | Indica que um cartão inteligente foi removido de um dispositivo compatível.                                                                        |
| \_logoff do \_ usuário do tipo SAS \_ WLX \_                       | Indica que um usuário solicitou o logoff.                                                                                                       |
| WLX \_ SAS \_ tipo \_ SCRNSVR \_ Timeout                   | Indica que a proteção de tela deve ser executada devido à falta de entrada do usuário.                                                                      |
| \_ \_ tempo limite de tipo SAS WLX \_                            | Indica que nenhuma entrada de usuário foi recebida dentro do período de tempo limite especificado.                                                               |



 

Para tempos limite e logoffs, o Winlogon fechará a caixa de diálogo depois que a mensagem for enviada. Essa mensagem é enviada para que a operação da caixa de diálogo possa responder de uma maneira útil (por exemplo, fechando-a inativamente se um logoff tiver ocorrido).

Para tempos limite de entrada, a caixa de diálogo é fechada com o tempo limite de entrada de WLX de código \_ DLG \_ \_ .

Para tempos limite de proteção de tela, a caixa de diálogo é fechada com o \_ tempo limite de proteção de tela DLG do código WLX \_ \_ \_ .

Para logoffs, a operação da caixa de diálogo é fechada com o WLX do código de \_ \_ logoff do usuário \_ .

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Inicializando Winlogon](initializing-winlogon.md)
</dt> <dt>

[Estados do Winlogon](winlogon-states.md)
</dt> <dt>

[Caixa de diálogo com suporte Tempo de Serviço operações de saída](supported-dialog-box-service-time-out-operations.md)
</dt> <dt>

[Funções de suporte do Winlogon](authentication-functions.md)
</dt> </dl>

 

 
