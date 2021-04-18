---
description: O Winlogon envia mensagens para a GINA enquanto as caixas de diálogo são exibidas. Essas mensagens são todas encapsuladas na \_ mensagem SAS do WLX WM da \_ seguinte maneira.
ms.assetid: 3da1c3d2-5116-47c3-98e4-f29b33693c69
title: Enviando mensagens para a GINA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d2f7b5b0d8fbecafad0bcc36c84cf395813f767
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105811303"
---
# <a name="sending-messages-to-the-gina"></a><span data-ttu-id="f1dc3-104">Enviando mensagens para a GINA</span><span class="sxs-lookup"><span data-stu-id="f1dc3-104">Sending Messages to the GINA</span></span>

<span data-ttu-id="f1dc3-105">O [*Winlogon*](../secgloss/w-gly.md) envia mensagens para a [*Gina*](../secgloss/g-gly.md) enquanto as caixas de diálogo são exibidas.</span><span class="sxs-lookup"><span data-stu-id="f1dc3-105">[*Winlogon*](../secgloss/w-gly.md) sends messages to the [*GINA*](../secgloss/g-gly.md) while dialog boxes are displayed.</span></span> <span data-ttu-id="f1dc3-106">Essas mensagens são todas encapsuladas na \_ mensagem SAS do WLX WM da \_ seguinte maneira.</span><span class="sxs-lookup"><span data-stu-id="f1dc3-106">These messages are all encapsulated in the WLX\_WM\_SAS message as follows.</span></span>



| <span data-ttu-id="f1dc3-107">Tipo de sequência de atenção segura no parâmetro wParam</span><span class="sxs-lookup"><span data-stu-id="f1dc3-107">Secure attention sequence type in wParam parameter</span></span> | <span data-ttu-id="f1dc3-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="f1dc3-108">Description</span></span>                                                                                                                                   |
|----------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f1dc3-109">\_tipo de SAS WLX \_ \_ Ctrl \_ ALT \_ del</span><span class="sxs-lookup"><span data-stu-id="f1dc3-109">WLX\_SAS\_TYPE\_CTRL\_ALT\_DEL</span></span>                     | <span data-ttu-id="f1dc3-110">Indica que uma sequência de teclas CTRL + ALT + DEL foi recebida.</span><span class="sxs-lookup"><span data-stu-id="f1dc3-110">Indicates that a CTRL+ALT+DEL key sequence was received.</span></span>                                                                                      |
| <span data-ttu-id="f1dc3-111">WLX \_ SAS \_ tipo \_ sc \_ Insert</span><span class="sxs-lookup"><span data-stu-id="f1dc3-111">WLX\_SAS\_TYPE\_SC\_INSERT</span></span>                         | <span data-ttu-id="f1dc3-112">Indica que um [*cartão inteligente*](../secgloss/s-gly.md) foi inserido em um dispositivo compatível.</span><span class="sxs-lookup"><span data-stu-id="f1dc3-112">Indicates that a [*smart card*](../secgloss/s-gly.md) has been inserted into a compatible device.</span></span> |
| <span data-ttu-id="f1dc3-113">WLX \_ SAS \_ tipo \_ sc \_ Remove</span><span class="sxs-lookup"><span data-stu-id="f1dc3-113">WLX\_SAS\_TYPE\_SC\_REMOVE</span></span>                         | <span data-ttu-id="f1dc3-114">Indica que um cartão inteligente foi removido de um dispositivo compatível.</span><span class="sxs-lookup"><span data-stu-id="f1dc3-114">Indicates that a smart card has been removed from a compatible device.</span></span>                                                                        |
| <span data-ttu-id="f1dc3-115">\_logoff do \_ usuário do tipo SAS \_ WLX \_</span><span class="sxs-lookup"><span data-stu-id="f1dc3-115">WLX\_SAS\_TYPE\_USER\_LOGOFF</span></span>                       | <span data-ttu-id="f1dc3-116">Indica que um usuário solicitou o logoff.</span><span class="sxs-lookup"><span data-stu-id="f1dc3-116">Indicates that a user requested logoff.</span></span>                                                                                                       |
| <span data-ttu-id="f1dc3-117">WLX \_ SAS \_ tipo \_ SCRNSVR \_ Timeout</span><span class="sxs-lookup"><span data-stu-id="f1dc3-117">WLX\_SAS\_TYPE\_SCRNSVR\_TIMEOUT</span></span>                   | <span data-ttu-id="f1dc3-118">Indica que a proteção de tela deve ser executada devido à falta de entrada do usuário.</span><span class="sxs-lookup"><span data-stu-id="f1dc3-118">Indicates that the screen saver should be run due to lack of user input.</span></span>                                                                      |
| <span data-ttu-id="f1dc3-119">\_ \_ tempo limite de tipo SAS WLX \_</span><span class="sxs-lookup"><span data-stu-id="f1dc3-119">WLX\_SAS\_TYPE\_TIMEOUT</span></span>                            | <span data-ttu-id="f1dc3-120">Indica que nenhuma entrada de usuário foi recebida dentro do período de tempo limite especificado.</span><span class="sxs-lookup"><span data-stu-id="f1dc3-120">Indicates that no user input was received within the specified time-out period.</span></span>                                                               |



 

<span data-ttu-id="f1dc3-121">Para tempos limite e logoffs, o Winlogon fechará a caixa de diálogo depois que a mensagem for enviada.</span><span class="sxs-lookup"><span data-stu-id="f1dc3-121">For time-outs and logoffs, Winlogon will close the dialog box after the message has been sent.</span></span> <span data-ttu-id="f1dc3-122">Essa mensagem é enviada para que a operação da caixa de diálogo possa responder de uma maneira útil (por exemplo, fechando-a inativamente se um logoff tiver ocorrido).</span><span class="sxs-lookup"><span data-stu-id="f1dc3-122">This message is sent so the dialog box operation can respond in a useful manner (for example, by closing itself down if a logoff has occurred).</span></span>

<span data-ttu-id="f1dc3-123">Para tempos limite de entrada, a caixa de diálogo é fechada com o tempo limite de entrada de WLX de código \_ DLG \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="f1dc3-123">For input time-outs, the dialog box is closed with the code WLX\_DLG\_INPUT\_TIMEOUT.</span></span>

<span data-ttu-id="f1dc3-124">Para tempos limite de proteção de tela, a caixa de diálogo é fechada com o \_ tempo limite de proteção de tela DLG do código WLX \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="f1dc3-124">For screen saver time-outs, the dialog box is closed with the code WLX\_DLG\_SCREEN\_SAVER\_TIMEOUT.</span></span>

<span data-ttu-id="f1dc3-125">Para logoffs, a operação da caixa de diálogo é fechada com o WLX do código de \_ \_ logoff do usuário \_ .</span><span class="sxs-lookup"><span data-stu-id="f1dc3-125">For logoffs, the dialog box operation is closed with the code WLX\_DLG\_USER\_LOGOFF.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f1dc3-126">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f1dc3-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f1dc3-127">Inicializando Winlogon</span><span class="sxs-lookup"><span data-stu-id="f1dc3-127">Initializing Winlogon</span></span>](initializing-winlogon.md)
</dt> <dt>

[<span data-ttu-id="f1dc3-128">Estados do Winlogon</span><span class="sxs-lookup"><span data-stu-id="f1dc3-128">Winlogon States</span></span>](winlogon-states.md)
</dt> <dt>

[<span data-ttu-id="f1dc3-129">Caixa de diálogo com suporte Tempo de Serviço operações de saída</span><span class="sxs-lookup"><span data-stu-id="f1dc3-129">Supported Dialog Box Service Time-out Operations</span></span>](supported-dialog-box-service-time-out-operations.md)
</dt> <dt>

[<span data-ttu-id="f1dc3-130">Funções de suporte do Winlogon</span><span class="sxs-lookup"><span data-stu-id="f1dc3-130">Winlogon Support Functions</span></span>](authentication-functions.md)
</dt> </dl>

 

 
