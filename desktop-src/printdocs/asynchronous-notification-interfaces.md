---
description: Saiba mais sobre as interfaces usadas na comunicação assíncrona entre aplicativos e componentes hospedados pelo spooler de impressão.
ms.assetid: e96c957f-3972-4afc-9d76-a4725b8688f8
title: Interfaces de notificação de impressão assíncrona
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ecfe0de2cf8510b1bb039907067b62fce08a4145
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112396091"
---
# <a name="asynchronous-printing-notification-interfaces"></a>Interfaces de notificação de impressão assíncrona

As interfaces a seguir são usadas na comunicação assíncrona entre aplicativos e componentes hospedados pelo spooler de impressão, como drivers de impressora e monitores de porta.

## <a name="in-this-section"></a>Nesta seção



| Interface                                                                     | Descrição                                                                                                                                                                                                                                                   |
|-------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IPrintAsyncNotifyCallback**](/windows/desktop/api/prnasnot/nn-prnasnot-iprintasyncnotifycallback)<br/>     | Cria e gerencia um canal de comunicação usado por aplicativos e componentes hospedados pelo spooler de impressão.<br/>                                                                                                                              |
| [**IPrintAsyncNotifyChannel**](/windows/desktop/api/prnasnot/nn-prnasnot-iprintasyncnotifychannel)<br/>       | Representa um canal de comunicação que os componentes hospedados pelo spooler de impressão usam para enviar notificações aos aplicativos. Se o canal for bidirecional, os aplicativos poderão usar o mesmo canal para enviar respostas de volta ao componente.<br/> |
| [**IPrintAsyncNotifyDataObject**](/windows/desktop/api/prnasnot/nn-prnasnot-iprintasyncnotifydataobject)<br/> | Encapsula os dados enviados em um canal de notificação. <br/>                                                                                                                                                                                             |



 

 

 




