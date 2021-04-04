---
title: Desconectando
description: Quando um aplicativo cliente RAS inicia uma operação de conexão, a chamada RasDial recebe um identificador de conexão HRASCONN para identificar a conexão.
ms.assetid: a0fddc69-44bb-4bb0-ae57-ebecbe85cbe9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 859a3751bcbaf7d95927cdf6d14de859ddcc731e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104008085"
---
# <a name="disconnecting"></a>Desconectando

Quando um aplicativo cliente RAS inicia uma operação de conexão, a chamada [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) recebe um identificador de conexão **HRASCONN** para identificar a conexão. Se o identificador retornado não for **nulo**, o cliente deverá eventualmente chamar a função [**RasHangUp**](/windows/desktop/api/Ras/nf-ras-rashangupa) para encerrar a conexão. Se ocorrer um erro durante a operação de conexão, o cliente deverá chamar **RasHangUp** mesmo que a conexão nunca tenha sido estabelecida.

O aplicativo que chama [**RasHangUp**](/windows/desktop/api/Ras/nf-ras-rashangupa) não deve sair imediatamente porque o Gerenciador de conexões de acesso remoto precisa de tempo para encerrar corretamente a conexão. Em vez disso, o aplicativo deve aguardar até que a função [**RasGetConnectStatus**](/windows/desktop/api/Ras/nf-ras-rasgetconnectstatusa) retorne um \_ identificador inválido de erro \_ , indicando que a conexão foi excluída.

Um aplicativo cliente RAS pode precisar encerrar uma conexão, mesmo que não tenha o identificador retornado por [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala). Por exemplo, o aplicativo que chamou **RasDial** pode ter saído depois que a conexão foi estabelecida com êxito. Nesse caso, o aplicativo de desconexão pode usar a função [**RasEnumConnections**](/windows/desktop/api/Ras/nf-ras-rasenumconnectionsa) para obter todas as conexões atuais. Para cada conexão, **RasEnumConnections** retorna uma estrutura [**RASCONN**](/previous-versions/windows/desktop/legacy/aa376725(v=vs.85)) que contém o identificador de conexão **HRASCONN** e o nome da entrada do catálogo telefônico ou o número de telefone especificado quando a operação de conexão foi iniciada. Essas informações podem ser usadas para exibir uma lista de conexões da qual o usuário pode selecionar a conexão final.

 

 