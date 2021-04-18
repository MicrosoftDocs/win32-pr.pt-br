---
description: As mensagens são usadas para notificar a aplicação de eventos assíncronos. Todas essas mensagens são enviadas para o aplicativo por meio do mecanismo de notificação de mensagem que o aplicativo especificou em lineInitializeEx.
ms.assetid: d302819e-c522-470a-be5e-52625c9223a4
title: Mensagens TAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58307a0230b76c6ad98c57f4590098f0dcf6b236
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105789447"
---
# <a name="tapi-messages"></a><span data-ttu-id="e7a9c-104">Mensagens TAPI</span><span class="sxs-lookup"><span data-stu-id="e7a9c-104">TAPI Messages</span></span>

<span data-ttu-id="e7a9c-105">As mensagens são usadas para notificar a aplicação de eventos assíncronos.</span><span class="sxs-lookup"><span data-stu-id="e7a9c-105">Messages are used to notify the application of asynchronous events.</span></span> <span data-ttu-id="e7a9c-106">Todas essas mensagens são enviadas para o aplicativo por meio do mecanismo de notificação de mensagem que o aplicativo especificou em [**lineInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-lineinitializeexa).</span><span class="sxs-lookup"><span data-stu-id="e7a9c-106">All of these messages are sent to the application through the message notification mechanism that the application specified in [**lineInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-lineinitializeexa).</span></span>

<span data-ttu-id="e7a9c-107">A mensagem sempre contém um identificador para o objeto relevante (telefone, linha ou chamada), que o aplicativo pode usar para determinar o tipo de mensagem.</span><span class="sxs-lookup"><span data-stu-id="e7a9c-107">The message always contains a handle to the relevant object (phone, line, or call), which the application can use to determine the message type.</span></span>

<span data-ttu-id="e7a9c-108">Determinadas mensagens são usadas para notificar o aplicativo sobre uma alteração no status de um objeto.</span><span class="sxs-lookup"><span data-stu-id="e7a9c-108">Certain messages are used to notify the application about a change in an object's status.</span></span> <span data-ttu-id="e7a9c-109">Essas mensagens fornecem o identificador de objeto e fornecem uma indicação de qual item de status foi alterado.</span><span class="sxs-lookup"><span data-stu-id="e7a9c-109">These messages provide the object handle and give an indication of which status item has changed.</span></span> <span data-ttu-id="e7a9c-110">O aplicativo pode chamar a função "Get status" apropriada do objeto para obter o status completo do objeto.</span><span class="sxs-lookup"><span data-stu-id="e7a9c-110">The application can call the appropriate "get status" function of the object to obtain the object's full status.</span></span>

<span data-ttu-id="e7a9c-111">Quando ocorre um evento, as mensagens podem ser enviadas para zero, um ou mais aplicativos.</span><span class="sxs-lookup"><span data-stu-id="e7a9c-111">When an event occurs, messages can be sent to zero, one, or more applications.</span></span> <span data-ttu-id="e7a9c-112">Os aplicativos de destino para uma mensagem são determinados por vários fatores diferentes, incluindo o significado da mensagem, o privilégio do aplicativo para o objeto, se o aplicativo iniciou ou não a solicitação para a qual a mensagem é um resultado direto e o mascaramento de mensagens que foi definido pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="e7a9c-112">The target applications for a message are determined by a number of different factors including the meaning of the message, the application's privilege to the object, whether or not the application initiated the request for which the message is a direct result, and the message masking that has been set by the application.</span></span> <span data-ttu-id="e7a9c-113">Observe os seguintes pontos sobre as mensagens:</span><span class="sxs-lookup"><span data-stu-id="e7a9c-113">Note the following points about messages:</span></span>

-   <span data-ttu-id="e7a9c-114">As mensagens de resposta assíncronas são enviadas somente ao aplicativo que originou a solicitação e não podem ser mascaradas.</span><span class="sxs-lookup"><span data-stu-id="e7a9c-114">Asynchronous reply messages are only sent to the application that originated the request and cannot be masked.</span></span>
-   <span data-ttu-id="e7a9c-115">As mensagens que sinalizam a conclusão da geração de dígitos ou tons ou a coleta de dígitos são enviadas somente ao aplicativo que solicitou a geração de dígitos ou tons.</span><span class="sxs-lookup"><span data-stu-id="e7a9c-115">Messages that signal the completion of digit or tone generation or the gathering of digits are only sent to the application that requested the digit or tone generation.</span></span>
-   <span data-ttu-id="e7a9c-116">As mensagens que indicam alterações de estado de linha ou endereço são enviadas a todos os aplicativos que abriram a linha, desde que a mensagem tenha sido habilitada por meio de [**lineSetStatusMessages**](/windows/desktop/api/Tapi/nf-tapi-linesetstatusmessages).</span><span class="sxs-lookup"><span data-stu-id="e7a9c-116">Messages that indicate line or address state changes are sent to all applications that have opened the line, so long as the message has been enabled through [**lineSetStatusMessages**](/windows/desktop/api/Tapi/nf-tapi-linesetstatusmessages).</span></span>
-   <span data-ttu-id="e7a9c-117">As mensagens que indicam as alterações de estado de chamada e informações de chamada são enviadas a todos os aplicativos que têm um identificador para a chamada.</span><span class="sxs-lookup"><span data-stu-id="e7a9c-117">Messages that indicate call state and call information changes are sent to all applications that have a handle to the call.</span></span>
-   <span data-ttu-id="e7a9c-118">As mensagens que sinalizam uma detecção de dígito, detecção de Tom ou detecção de tipo de mídia são enviadas para os aplicativos que solicitaram o monitoramento desse evento.</span><span class="sxs-lookup"><span data-stu-id="e7a9c-118">Messages that signal a digit detection, tone detection, or media type detection are sent to the applications that requested monitoring of that event.</span></span>

<span data-ttu-id="e7a9c-119">Esta seção contém as informações de referência para as seguintes mensagens TAPI:</span><span class="sxs-lookup"><span data-stu-id="e7a9c-119">This section contains the reference information for the following TAPI messages:</span></span>

-   [<span data-ttu-id="e7a9c-120">Mensagens de telefonia assistidas</span><span class="sxs-lookup"><span data-stu-id="e7a9c-120">Assisted Telephony Messages</span></span>](assisted-telephony-messages.md)
-   [<span data-ttu-id="e7a9c-121">Mensagens do Call Center</span><span class="sxs-lookup"><span data-stu-id="e7a9c-121">Call Center Messages</span></span>](call-center-messages.md)
-   [<span data-ttu-id="e7a9c-122">Mensagens de erro formatadas</span><span class="sxs-lookup"><span data-stu-id="e7a9c-122">Formatted Error Messages</span></span>](formatted-error-messages.md)
-   [<span data-ttu-id="e7a9c-123">Mensagens do dispositivo de linha</span><span class="sxs-lookup"><span data-stu-id="e7a9c-123">Line Device Messages</span></span>](line-device-messages.md)
-   [<span data-ttu-id="e7a9c-124">Mensagens do dispositivo de telefone</span><span class="sxs-lookup"><span data-stu-id="e7a9c-124">Phone Device Messages</span></span>](phone-device-messages.md)

 

 



