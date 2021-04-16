---
description: Um evento de gerenciamento de energia do sistema é uma alteração no status de energia do sistema, no modo operacional de um dispositivo ou sistema ou no valor de uma configuração de energia.
ms.assetid: f73b072a-1f69-4e26-9712-dab428edca18
title: Eventos de gerenciamento de energia do sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ab18fad9116cfff9e1cd35703e32a49e3b12c8b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105757486"
---
# <a name="system-power-management-events"></a>Eventos de gerenciamento de energia do sistema

Um evento de gerenciamento de energia do sistema é uma alteração no status de energia do sistema, no modo operacional de um dispositivo ou sistema ou no valor de uma configuração de energia. Como esses eventos podem afetar a operação de aplicativos e drivers instaláveis, o sistema notifica todos os aplicativos e drivers instaláveis transmitindo uma notificação para cada evento. Os aplicativos e serviços se registram para notificações usando a função [**RegisterPowerSettingNotification**](/windows/desktop/api/WinUser/nf-winuser-registerpowersettingnotification) . As notificações são recebidas por meio da mensagem do [**WM \_ POWERBROADCAST**](wm-powerbroadcast.md) , que contém o evento de gerenciamento de energia e quaisquer dados específicos de evento associados.

## <a name="system-power-status-events"></a>Eventos de status de energia do sistema

Um *evento de status de energia do sistema* ocorre quando há uma alteração na fonte de alimentação ou no status da bateria do sistema. Por exemplo, o sistema transmite um evento [PBT \_ APMPOWERSTATUSCHANGE](pbt-apmpowerstatuschange.md) sempre que o usuário alterna da bateria para a alimentação AC ou vice-versa. O sistema também transmite esse evento quando a energia restante da bateria fica abaixo do limite especificado pelo usuário ou se a energia da bateria for alterada em um percentual especificado.

## <a name="operational-mode-events"></a>Eventos de modo operacional

Um *evento de modo operacional* ocorre quando há uma alteração no consumo de energia, como o sistema que está alternando para um estado de suspensão devido à inatividade ou ao usuário que está colocando o sistema em suspensão manualmente. O sistema transmite eventos sobre essas alterações antes que a alteração no consumo de energia seja feita. Por exemplo, se o sistema determinar que ele está ocioso, ele difunde um evento [PBT \_ APMSUSPEND](pbt-apmsuspend.md) que notifica os aplicativos e drivers que ele está prestes a suspender a operação e a suspensão para conservar energia. Os aplicativos e os drivers podem se preparar para o estado de suspensão fechando arquivos e salvando dados para evitar possíveis perdas de dados.

Quando o sistema executa uma *suspensão crítica*, o sistema é imediatamente colocado em suspensão devido a uma condição crítica, como um alarme de bateria crítico. Ao contrário de uma transição de suspensão normal, o sistema não notifica aplicativos e drivers antes de realizar uma suspensão crítica. Portanto, os aplicativos devem estar preparados para lidar com suspensões críticas.

Quando a operação do sistema é restaurada após ter sido suspensa, o sistema notifica todos os aplicativos e drivers. Ele também indica se o sistema está retomando de uma suspensão crítica para que o aplicativo ou driver possa tomar as medidas apropriadas para restaurar seus dados e continuar a operação.

Os aplicativos devem fazer cada tentativa de lidar com a transição para o estado de suspensão sem nenhuma intervenção do usuário, pois talvez não seja possível que o usuário responda. Por exemplo, a tampa no computador do notebook pode ser fechada. Quando um aplicativo recebe uma notificação de que o sistema está prestes a entrar em suspensão, ele deve executar todas as operações necessárias rapidamente e retornar o loop de mensagem. O sistema permite um máximo de dois segundos por aplicativo ao lidar com essa mensagem antes de atingir o tempo limite.

## <a name="power-setting-change-events"></a>Eventos de alteração de configuração de energia

Um evento de alteração de configuração de energia ocorre quando há uma alteração no valor de uma configuração de energia. Por exemplo, o usuário altera o plano de energia de alto desempenho para balanceado no aplicativo de opções de energia no painel de controle. Nesse caso, o sistema transmitiria um evento que indicasse que o plano de energia foi alterado. Esse evento inclui o novo valor para a configuração de energia.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sobre o gerenciamento de energia](about-power-management.md)
</dt> </dl>

 

 



