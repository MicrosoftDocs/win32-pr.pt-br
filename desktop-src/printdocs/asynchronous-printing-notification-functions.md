---
description: As interfaces a seguir são usadas na comunicação assíncrona entre aplicativos e componentes que são hospedados pelo spooler de impressão, como drivers de impressora e monitores de porta.
ms.assetid: 7e98e63f-616c-4cd1-a8aa-482d27529b8c
title: Funções de notificação de impressão assíncrona
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72fa7b0b61de15af9f7117e7c36104eb51abbb7c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105770570"
---
# <a name="asynchronous-printing-notification-functions"></a>Funções de notificação de impressão assíncrona

As interfaces a seguir são usadas na comunicação assíncrona entre aplicativos e componentes que são hospedados pelo spooler de impressão, como drivers de impressora e monitores de porta.

## <a name="in-this-section"></a>Nesta seção



| Função                                                                                        | Descrição                                                                                                                                                                                              |
|-------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CreatePrintAsyncNotifyChannel**](/windows/desktop/api/prnasnot/nf-prnasnot-createprintasyncnotifychannel)<br/>               | Cria um canal de comunicação entre um componente de impressão hospedado no spooler de impressão, como um driver de impressão ou monitor de porta, e um aplicativo que recebe notificações do componente.<br/> |
| [**RegisterForPrintAsyncNotifications**](/windows/desktop/api/prnasnot/nf-prnasnot-registerforprintasyncnotifications)<br/>     | Permite que um aplicativo se registre para notificações de componentes de impressão hospedados no spooler de impressão, como drivers de impressora, processadores de impressão e monitores de porta.<br/>                              |
| [**UnRegisterForPrintAsyncNotifications**](/windows/desktop/api/prnasnot/nf-prnasnot-unregisterforprintasyncnotifications)<br/> | Habilita um aplicativo que se registrou para receber notificações de componentes de impressão hospedados no spooler de impressão para cancelar o registro.<br/>                                                              |



 

 

 




