---
description: As interfaces a seguir são usadas na comunicação assíncrona entre aplicativos e componentes que são hospedados pelo spooler de impressão, como drivers de impressora e monitores de porta.
ms.assetid: e96c957f-3972-4afc-9d76-a4725b8688f8
title: Interfaces de notificação de impressão assíncrona
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7da8d320b33224e81852542e39f435b45b6dab5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103663174"
---
# <a name="asynchronous-printing-notification-interfaces"></a>Interfaces de notificação de impressão assíncrona

As interfaces a seguir são usadas na comunicação assíncrona entre aplicativos e componentes que são hospedados pelo spooler de impressão, como drivers de impressora e monitores de porta.

## <a name="in-this-section"></a>Nesta seção



| Interface                                                                     | Descrição                                                                                                                                                                                                                                                   |
|-------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IPrintAsyncNotifyCallback**](/windows/desktop/api/prnasnot/nn-prnasnot-iprintasyncnotifycallback)<br/>     | Cria e gerencia um canal de comunicação usado por aplicativos e componentes que são hospedados pelo spooler de impressão.<br/>                                                                                                                              |
| [**IPrintAsyncNotifyChannel**](/windows/desktop/api/prnasnot/nn-prnasnot-iprintasyncnotifychannel)<br/>       | Representa um canal de comunicação que os componentes que são hospedados pelo spooler de impressão usam para enviar notificações aos aplicativos. Se o canal for bidirecional, os aplicativos poderão usar o mesmo canal para enviar respostas de volta para o componente.<br/> |
| [**IPrintAsyncNotifyDataObject**](/windows/desktop/api/prnasnot/nn-prnasnot-iprintasyncnotifydataobject)<br/> | Encapsula os dados enviados em um canal de notificação. <br/>                                                                                                                                                                                             |



 

 

 




