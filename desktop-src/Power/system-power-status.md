---
description: O status de energia do sistema indica se a fonte de energia de um computador é uma bateria do sistema ou uma energia CA. Para computadores que usam baterias, o status de energia do sistema também indica o quanto a vida útil da bateria permanece e se a bateria está carregando.
ms.assetid: b9a5e7de-a603-4bd9-b854-1e58572c3b2b
title: Status de energia do sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e221142b5d39a4cb5bc49dbe85271c99837d0a20
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105778531"
---
# <a name="system-power-status"></a>Status de energia do sistema

O status de energia do sistema indica se a fonte de energia de um computador é uma bateria do sistema ou uma energia CA. Para computadores que usam baterias, o status de energia do sistema também indica o quanto a vida útil da bateria permanece e se a bateria está carregando.

As informações de energia são recuperadas pelo registro para notificações de configuração de energia por meio da função [**RegisterPowerSettingNotification**](/windows/desktop/api/WinUser/nf-winuser-registerpowersettingnotification) . Essa função permite que os aplicativos se registrem em configurações de energia específicas e sejam notificados quando forem alterados.

> [!Note]  
> Para consultar informações de status de energia sem notificações, use [**CallNtPowerInformation**](/windows/desktop/api/Powerbase/nf-powerbase-callntpowerinformation).

 

Aplicativos e drivers instaláveis normalmente usam o status de energia do sistema para determinar se a operação contínua é viável. Por exemplo, antes que um aplicativo execute operações em segundo plano, como compactar ou paginar um arquivo, ele deve verificar se o sistema está em baterias. Como outro exemplo, um aplicativo que inicia uma operação demorada deve verificar o status para determinar se há energia suficiente de bateria para concluir a operação.

Por padrão, o sistema não consulta aplicativos ou drivers durante transições de suspensão.

> [!Note]  
> Se a energia for baixa, um aplicativo poderá solicitar a intervenção do usuário ou solicitar que o sistema se suspenda. Você pode suspender a operação do sistema usando a função [**Setsuspendestate**](/windows/desktop/api/PowrProf/nf-powrprof-setsuspendstate) .

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sobre o gerenciamento de energia](about-power-management.md)
</dt> </dl>

 

 



