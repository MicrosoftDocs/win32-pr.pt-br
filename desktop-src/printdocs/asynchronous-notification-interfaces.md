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
# <a name="asynchronous-printing-notification-interfaces"></a><span data-ttu-id="3977e-103">Interfaces de notificação de impressão assíncrona</span><span class="sxs-lookup"><span data-stu-id="3977e-103">Asynchronous Printing Notification Interfaces</span></span>

<span data-ttu-id="3977e-104">As interfaces a seguir são usadas na comunicação assíncrona entre aplicativos e componentes que são hospedados pelo spooler de impressão, como drivers de impressora e monitores de porta.</span><span class="sxs-lookup"><span data-stu-id="3977e-104">The following interfaces are used in asynchronous communication between applications and components that are hosted by the print spooler, such as printer drivers and port monitors.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="3977e-105">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="3977e-105">In this section</span></span>



| <span data-ttu-id="3977e-106">Interface</span><span class="sxs-lookup"><span data-stu-id="3977e-106">Interface</span></span>                                                                     | <span data-ttu-id="3977e-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="3977e-107">Description</span></span>                                                                                                                                                                                                                                                   |
|-------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3977e-108">**IPrintAsyncNotifyCallback**</span><span class="sxs-lookup"><span data-stu-id="3977e-108">**IPrintAsyncNotifyCallback**</span></span>](/windows/desktop/api/prnasnot/nn-prnasnot-iprintasyncnotifycallback)<br/>     | <span data-ttu-id="3977e-109">Cria e gerencia um canal de comunicação usado por aplicativos e componentes que são hospedados pelo spooler de impressão.</span><span class="sxs-lookup"><span data-stu-id="3977e-109">Creates and manages a communication channel used by applications and components that are hosted by the print spooler.</span></span><br/>                                                                                                                              |
| [<span data-ttu-id="3977e-110">**IPrintAsyncNotifyChannel**</span><span class="sxs-lookup"><span data-stu-id="3977e-110">**IPrintAsyncNotifyChannel**</span></span>](/windows/desktop/api/prnasnot/nn-prnasnot-iprintasyncnotifychannel)<br/>       | <span data-ttu-id="3977e-111">Representa um canal de comunicação que os componentes que são hospedados pelo spooler de impressão usam para enviar notificações aos aplicativos.</span><span class="sxs-lookup"><span data-stu-id="3977e-111">Represents a communication channel that components that are hosted by the print spooler use to send notifications to applications.</span></span> <span data-ttu-id="3977e-112">Se o canal for bidirecional, os aplicativos poderão usar o mesmo canal para enviar respostas de volta para o componente.</span><span class="sxs-lookup"><span data-stu-id="3977e-112">If the channel is bidirectional, applications can use the same channel to send responses back to the component.</span></span><br/> |
| [<span data-ttu-id="3977e-113">**IPrintAsyncNotifyDataObject**</span><span class="sxs-lookup"><span data-stu-id="3977e-113">**IPrintAsyncNotifyDataObject**</span></span>](/windows/desktop/api/prnasnot/nn-prnasnot-iprintasyncnotifydataobject)<br/> | <span data-ttu-id="3977e-114">Encapsula os dados enviados em um canal de notificação.</span><span class="sxs-lookup"><span data-stu-id="3977e-114">Encapsulates the data sent in a notification channel.</span></span> <br/>                                                                                                                                                                                             |



 

 

 




