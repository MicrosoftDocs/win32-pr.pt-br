---
description: Saiba mais sobre as funções que são usadas na comunicação assíncrona entre aplicativos e componentes que são hospedados pelo spooler de impressão.
ms.assetid: 7e98e63f-616c-4cd1-a8aa-482d27529b8c
title: Funções de notificação de impressão assíncrona
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fdc9a404d1675c8ee87be31c7c57dd14a370697c
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112394851"
---
# <a name="asynchronous-printing-notification-functions"></a>Funções de notificação de impressão assíncrona

As funções a seguir são usadas na comunicação assíncrona entre aplicativos e componentes que são hospedados pelo spooler de impressão, como drivers de impressora e monitores de porta.

## <a name="in-this-section"></a>Nesta seção



| Função                                                                                        | Descrição                                                                                                                                                                                              |
|-------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CreatePrintAsyncNotifyChannel**](/windows/desktop/api/prnasnot/nf-prnasnot-createprintasyncnotifychannel)<br/>               | Cria um canal de comunicação entre um componente de impressão hospedado no spooler de impressão, como um driver de impressão ou monitor de porta, e um aplicativo que recebe notificações do componente.<br/> |
| [**RegisterForPrintAsyncNotifications**](/windows/desktop/api/prnasnot/nf-prnasnot-registerforprintasyncnotifications)<br/>     | Permite que um aplicativo se registre para notificações de componentes de impressão hospedados no spooler de impressão, como drivers de impressora, processadores de impressão e monitores de porta.<br/>                              |
| [**UnRegisterForPrintAsyncNotifications**](/windows/desktop/api/prnasnot/nf-prnasnot-unregisterforprintasyncnotifications)<br/> | Habilita um aplicativo que se registrou para receber notificações de componentes de impressão hospedados no spooler de impressão para cancelar o registro.<br/>                                                              |



 

 

 




