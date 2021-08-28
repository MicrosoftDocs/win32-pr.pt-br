---
title: Desconectando
description: Quando um aplicativo cliente RAS inicia uma operação de conexão, a chamada RasDial recebe um identificador de conexão HRASCONN para identificar a conexão.
ms.assetid: a0fddc69-44bb-4bb0-ae57-ebecbe85cbe9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1fde205dfeb838639447c9f9359ee5b1258b2426eb55dbdd592291aea002fad6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120101856"
---
# <a name="disconnecting"></a>Desconectando

Quando um aplicativo cliente RAS inicia uma operação de conexão, a [**chamada RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) recebe um identificador de conexão **HRASCONN** para identificar a conexão. Se o alça retornado não for **NULL,** o cliente deverá, eventualmente, chamar a [**função Ras Tabulação**](/windows/desktop/api/Ras/nf-ras-rashangupa) para encerrar a conexão. Se ocorrer um erro durante a operação de conexão, o cliente deverá chamar **RasArgemUp** mesmo que a conexão nunca tenha sido estabelecida.

O aplicativo que chama [**Ras Ltdaup**](/windows/desktop/api/Ras/nf-ras-rashangupa) não deve sair imediatamente porque o Gerenciador de Conexões remoto precisa de tempo para encerrar corretamente a conexão. Em vez disso, o aplicativo deve aguardar até que a [**função RasGetConnectStatus**](/windows/desktop/api/Ras/nf-ras-rasgetconnectstatusa) retorne ERROR INVALID HANDLE, indicando que a \_ conexão foi \_ excluída.

Um aplicativo cliente RAS pode precisar encerrar uma conexão, mesmo que ele não tenha o handle retornado pelo [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala). Por exemplo, o aplicativo que chamou **RasDial** pode ter sido exitado depois que a conexão foi estabelecida com êxito. Nesse caso, o aplicativo de desconexão pode usar a [**função RasEnumConnections**](/windows/desktop/api/Ras/nf-ras-rasenumconnectionsa) para obter todas as conexões atuais. Para cada conexão, **RasEnumConnections** retorna uma estrutura [**RASCONN**](/previous-versions/windows/desktop/legacy/aa376725(v=vs.85)) que contém a alça de conexão **HRASCONN** e o nome de entrada de lista de telefone ou o número de telefone especificados quando a operação de conexão foi iniciada. Essas informações podem ser usadas para exibir uma lista de conexões das quais o usuário pode selecionar a conexão para encerrar.

 

 