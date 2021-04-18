---
description: As enumerações a seguir são usadas na comunicação assíncrona entre aplicativos e componentes que são hospedados pelo spooler de impressão, como drivers de impressora e monitores de porta.
ms.assetid: 732a552b-caf9-45da-9a9e-a325c4f6341b
title: Enumerações de notificação de impressão assíncrona
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e2baf2a4476ac858a883dda55b2864a79d78cf6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105763293"
---
# <a name="asynchronous-printing-notification-enumerations"></a><span data-ttu-id="1b685-103">Enumerações de notificação de impressão assíncrona</span><span class="sxs-lookup"><span data-stu-id="1b685-103">Asynchronous Printing Notification Enumerations</span></span>

<span data-ttu-id="1b685-104">As enumerações a seguir são usadas na comunicação assíncrona entre aplicativos e componentes que são hospedados pelo spooler de impressão, como drivers de impressora e monitores de porta.</span><span class="sxs-lookup"><span data-stu-id="1b685-104">The following enumerations are used in asynchronous communication between applications and components that are hosted by the print spooler, such as printer drivers and port monitors.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="1b685-105">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="1b685-105">In this section</span></span>



| <span data-ttu-id="1b685-106">Enumeração</span><span class="sxs-lookup"><span data-stu-id="1b685-106">Enumeration</span></span>                                                                               | <span data-ttu-id="1b685-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="1b685-107">Description</span></span>                                                                                                                                                                                                    |
|-------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1b685-108">**PrintAsyncNotifyConversationStyle**</span><span class="sxs-lookup"><span data-stu-id="1b685-108">**PrintAsyncNotifyConversationStyle**</span></span>](/windows/desktop/api/prnasnot/ne-prnasnot-printasyncnotifyconversationstyle)<br/> | <span data-ttu-id="1b685-109">Especifica se a comunicação é bidirecional ou unidirecional entre aplicativos e componentes hospedados no spooler de impressão, como drivers de impressora, processadores de impressão e monitores de porta.</span><span class="sxs-lookup"><span data-stu-id="1b685-109">Specifies whether communication is bidirectional or unidirectional between applications and Print Spooler-hosted components such as printer drivers, print processors, and port monitors.</span></span><br/>           |
| [<span data-ttu-id="1b685-110">**PrintAsyncNotifyError**</span><span class="sxs-lookup"><span data-stu-id="1b685-110">**PrintAsyncNotifyError**</span></span>](/windows/desktop/api/prnasnot/ne-prnasnot-printasyncnotifyerror)<br/>                         | <span data-ttu-id="1b685-111">Especifica a parte do código de erro do **HRESULT** retornado após uma falha de notificação assíncrona.</span><span class="sxs-lookup"><span data-stu-id="1b685-111">Specifies the error code portion of the **HRESULT** returned after an asynchronous notification failure.</span></span><br/>                                                                                            |
| [<span data-ttu-id="1b685-112">**PrintAsyncNotifyUserFilter**</span><span class="sxs-lookup"><span data-stu-id="1b685-112">**PrintAsyncNotifyUserFilter**</span></span>](/windows/desktop/api/prnasnot/ne-prnasnot-printasyncnotifyuserfilter)<br/>               | <span data-ttu-id="1b685-113">Especifica se as notificações vão apenas para os aplicativos de escuta associados ao mesmo usuário que o remetente hospedado pelo spooler de impressão ou vão para um conjunto mais amplo de aplicativos de escuta.</span><span class="sxs-lookup"><span data-stu-id="1b685-113">Specifies whether notifications will go only to listening applications that are associated with the same user as the Print Spooler-hosted sender, or go to a broader set of listening applications.</span></span><br/> |



 

 

 




