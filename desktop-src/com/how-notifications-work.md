---
title: Como as notificações funcionam
description: Como as notificações funcionam
ms.assetid: faf66654-8233-49ac-a0fa-6cae51df0bea
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9665b327d164a4e105f8adba3328be284fbe1fa0
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104366777"
---
# <a name="how-notifications-work"></a><span data-ttu-id="15170-103">Como as notificações funcionam</span><span class="sxs-lookup"><span data-stu-id="15170-103">How Notifications Work</span></span>

<span data-ttu-id="15170-104">As notificações são originadas no aplicativo de objeto e fluem para o contêiner por meio do manipulador de objetos.</span><span class="sxs-lookup"><span data-stu-id="15170-104">Notifications originate in the object application and flow to the container by way of the object handler.</span></span> <span data-ttu-id="15170-105">Se o objeto for um objeto vinculado, o objeto vinculado interceptará as notificações do manipulador de objetos e notificará o contêiner diretamente.</span><span class="sxs-lookup"><span data-stu-id="15170-105">If the object is a linked object, the linked object intercepts the notifications from the object handler and notifies the container directly.</span></span>

<span data-ttu-id="15170-106">Um aplicativo de objeto deve gerenciar solicitações de registro, controlando para onde enviar as notificações e enviá-las quando apropriado.</span><span class="sxs-lookup"><span data-stu-id="15170-106">An object application must manage registration requests, keeping track of where to send which notifications and sending those notifications when appropriate.</span></span> <span data-ttu-id="15170-107">O OLE fornece dois objetos de componente para simplificar esta tarefa: o OleAdviseHolder para notificações de documentos compostos e o DataAdviseHolder para notificações de dados.</span><span class="sxs-lookup"><span data-stu-id="15170-107">OLE provides two component objects to simplify this task: the OleAdviseHolder for compound document notifications and the DataAdviseHolder for data notifications.</span></span>

<span data-ttu-id="15170-108">Os aplicativos de objeto determinam as condições que solicitam o envio de cada notificação específica e a frequência com a qual cada notificação deve ser enviada.</span><span class="sxs-lookup"><span data-stu-id="15170-108">Object applications determine the conditions that prompt the sending of each specific notification and the frequency with which each notification should be sent.</span></span> <span data-ttu-id="15170-109">Quando for apropriado que várias notificações sejam enviadas, não importa qual notificação é enviada primeiro; Eles podem ser enviados em qualquer ordem.</span><span class="sxs-lookup"><span data-stu-id="15170-109">When it is appropriate for multiple notifications to be sent, it does not matter which notification is sent first; they can be sent in any order.</span></span>

<span data-ttu-id="15170-110">O tempo das notificações afeta o desempenho e a coordenação entre um aplicativo de objeto e seus contêineres.</span><span class="sxs-lookup"><span data-stu-id="15170-110">The timing of notifications affects the performance and coordination between an object application and its containers.</span></span> <span data-ttu-id="15170-111">Enquanto as notificações são enviadas com muito frequência, as notificações enviadas com pouca frequência resultam em um contêiner fora de sincronia.</span><span class="sxs-lookup"><span data-stu-id="15170-111">Whereas notifications sent too frequently slow processing, notifications sent too infrequently result in an out-of-sync container.</span></span> <span data-ttu-id="15170-112">A frequência de notificação pode ser comparada com a taxa de repintura de um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="15170-112">Notification frequency can be compared with the rate at which an application repaints.</span></span> <span data-ttu-id="15170-113">Portanto, usar uma lógica semelhante para o tempo das notificações (como é usado para repintura) é inteligente.</span><span class="sxs-lookup"><span data-stu-id="15170-113">Therefore, using similar logic for the timing of notifications (as is used for repainting) is wise.</span></span>

## <a name="related-topics"></a><span data-ttu-id="15170-114">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="15170-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="15170-115">**CreateDataAdviseHolder**</span><span class="sxs-lookup"><span data-stu-id="15170-115">**CreateDataAdviseHolder**</span></span>](/windows/win32/api/ole2/nf-ole2-createdataadviseholder)
</dt> <dt>

[<span data-ttu-id="15170-116">**CreateOleAdviseHolder**</span><span class="sxs-lookup"><span data-stu-id="15170-116">**CreateOleAdviseHolder**</span></span>](/windows/desktop/api/Ole2/nf-ole2-createoleadviseholder)
</dt> <dt>

[<span data-ttu-id="15170-117">Notificações</span><span class="sxs-lookup"><span data-stu-id="15170-117">Notifications</span></span>](notifications.md)
</dt> </dl>

 

 