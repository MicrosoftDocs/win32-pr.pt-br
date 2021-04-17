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
# <a name="asynchronous-printing-notification-functions"></a><span data-ttu-id="09480-103">Funções de notificação de impressão assíncrona</span><span class="sxs-lookup"><span data-stu-id="09480-103">Asynchronous Printing Notification Functions</span></span>

<span data-ttu-id="09480-104">As interfaces a seguir são usadas na comunicação assíncrona entre aplicativos e componentes que são hospedados pelo spooler de impressão, como drivers de impressora e monitores de porta.</span><span class="sxs-lookup"><span data-stu-id="09480-104">The following interfaces are used in asynchronous communication between applications and components that are hosted by the print spooler, such as printer drivers and port monitors.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="09480-105">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="09480-105">In this section</span></span>



| <span data-ttu-id="09480-106">Função</span><span class="sxs-lookup"><span data-stu-id="09480-106">Function</span></span>                                                                                        | <span data-ttu-id="09480-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="09480-107">Description</span></span>                                                                                                                                                                                              |
|-------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="09480-108">**CreatePrintAsyncNotifyChannel**</span><span class="sxs-lookup"><span data-stu-id="09480-108">**CreatePrintAsyncNotifyChannel**</span></span>](/windows/desktop/api/prnasnot/nf-prnasnot-createprintasyncnotifychannel)<br/>               | <span data-ttu-id="09480-109">Cria um canal de comunicação entre um componente de impressão hospedado no spooler de impressão, como um driver de impressão ou monitor de porta, e um aplicativo que recebe notificações do componente.</span><span class="sxs-lookup"><span data-stu-id="09480-109">Creates a communication channel between a Print Spooler-hosted printing component, such as a print driver or port monitor, and an application that receives notifications from the component.</span></span><br/> |
| [<span data-ttu-id="09480-110">**RegisterForPrintAsyncNotifications**</span><span class="sxs-lookup"><span data-stu-id="09480-110">**RegisterForPrintAsyncNotifications**</span></span>](/windows/desktop/api/prnasnot/nf-prnasnot-registerforprintasyncnotifications)<br/>     | <span data-ttu-id="09480-111">Permite que um aplicativo se registre para notificações de componentes de impressão hospedados no spooler de impressão, como drivers de impressora, processadores de impressão e monitores de porta.</span><span class="sxs-lookup"><span data-stu-id="09480-111">Enables an application to register for notifications from Print Spooler-hosted printing components such as printer drivers, print processors, and port monitors.</span></span><br/>                              |
| [<span data-ttu-id="09480-112">**UnRegisterForPrintAsyncNotifications**</span><span class="sxs-lookup"><span data-stu-id="09480-112">**UnRegisterForPrintAsyncNotifications**</span></span>](/windows/desktop/api/prnasnot/nf-prnasnot-unregisterforprintasyncnotifications)<br/> | <span data-ttu-id="09480-113">Habilita um aplicativo que se registrou para receber notificações de componentes de impressão hospedados no spooler de impressão para cancelar o registro.</span><span class="sxs-lookup"><span data-stu-id="09480-113">Enables an application that has registered to receive notifications from Print Spooler-hosted printing components to unregister.</span></span><br/>                                                              |



 

 

 




