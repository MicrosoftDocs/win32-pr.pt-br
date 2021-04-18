---
description: Para enviar solicitações de controle para um serviço em execução, um programa de controle de serviço usa a função chamada ControlService.
ms.assetid: d6cdc876-8b74-460e-ad43-6455ddf428dd
title: Solicitações de controle de serviço
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6cb5edf56137e2c98ea7db440a4db5e55df5e8f0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105755308"
---
# <a name="service-control-requests"></a><span data-ttu-id="4e157-103">Solicitações de controle de serviço</span><span class="sxs-lookup"><span data-stu-id="4e157-103">Service Control Requests</span></span>

<span data-ttu-id="4e157-104">Para enviar solicitações de controle para um serviço em execução, um programa de controle de serviço usa a função [**chamada ControlService**](/windows/desktop/api/Winsvc/nf-winsvc-controlservice) .</span><span class="sxs-lookup"><span data-stu-id="4e157-104">To send control requests to a running service, a service control program uses the [**ControlService**](/windows/desktop/api/Winsvc/nf-winsvc-controlservice) function.</span></span> <span data-ttu-id="4e157-105">Essa função especifica um valor de controle que é passado para a função [**HandlerEx**](/windows/desktop/api/WinSvc/nc-winsvc-lphandler_function_ex) do serviço especificado.</span><span class="sxs-lookup"><span data-stu-id="4e157-105">This function specifies a control value that is passed to the [**HandlerEx**](/windows/desktop/api/WinSvc/nc-winsvc-lphandler_function_ex) function of the specified service.</span></span> <span data-ttu-id="4e157-106">Esse valor de controle pode ser um código definido pelo usuário ou pode ser um dos códigos padrão que permitem que o programa de chamada Execute as seguintes ações:</span><span class="sxs-lookup"><span data-stu-id="4e157-106">This control value can be a user-defined code, or it can be one of the standard codes that enable the calling program to perform the following actions:</span></span>

-   <span data-ttu-id="4e157-107">Parar um serviço (parada de controle de serviço \_ \_ ).</span><span class="sxs-lookup"><span data-stu-id="4e157-107">Stop a service (SERVICE\_CONTROL\_STOP).</span></span>
-   <span data-ttu-id="4e157-108">Pausar um serviço ( \_ pausa de controle de serviço \_ ).</span><span class="sxs-lookup"><span data-stu-id="4e157-108">Pause a service (SERVICE\_CONTROL\_PAUSE).</span></span>
-   <span data-ttu-id="4e157-109">Retomar a execução de um serviço em pausa (continuação do controle de serviço \_ \_ ).</span><span class="sxs-lookup"><span data-stu-id="4e157-109">Resume executing a paused service (SERVICE\_CONTROL\_CONTINUE).</span></span>
-   <span data-ttu-id="4e157-110">Recuperar informações de status atualizadas de um serviço ( \_ interrogação de controle de serviço \_ ).</span><span class="sxs-lookup"><span data-stu-id="4e157-110">Retrieve updated status information from a service (SERVICE\_CONTROL\_INTERROGATE).</span></span>

<span data-ttu-id="4e157-111">Cada serviço especifica os valores de controle que serão aceitos e processados.</span><span class="sxs-lookup"><span data-stu-id="4e157-111">Each service specifies the control values that it will accept and process.</span></span> <span data-ttu-id="4e157-112">Para determinar quais dos valores de controle padrão são aceitos por um serviço, use a função [**QueryServiceStatusEx**](/windows/desktop/api/Winsvc/nf-winsvc-queryservicestatusex) ou especifique o \_ valor de controle INTERROGATE de controle de serviço \_ em uma chamada para a função [**chamada ControlService**](/windows/desktop/api/Winsvc/nf-winsvc-controlservice) .</span><span class="sxs-lookup"><span data-stu-id="4e157-112">To determine which of the standard control values are accepted by a service, use the [**QueryServiceStatusEx**](/windows/desktop/api/Winsvc/nf-winsvc-queryservicestatusex) function or specify the SERVICE\_CONTROL\_INTERROGATE control value in a call to the [**ControlService**](/windows/desktop/api/Winsvc/nf-winsvc-controlservice) function.</span></span> <span data-ttu-id="4e157-113">O membro **dwControlsAccepted** da estrutura [**de \_ status do serviço**](/windows/desktop/api/Winsvc/ns-winsvc-service_status) retornada por essas funções indica se o serviço pode ser interrompido, pausado ou retomado.</span><span class="sxs-lookup"><span data-stu-id="4e157-113">The **dwControlsAccepted** member of the [**SERVICE\_STATUS**](/windows/desktop/api/Winsvc/ns-winsvc-service_status) structure returned by these functions indicates whether the service can be stopped, paused, or resumed.</span></span> <span data-ttu-id="4e157-114">Todos os serviços aceitam \_ o \_ valor de controle INTERROGATE de controle de serviço.</span><span class="sxs-lookup"><span data-stu-id="4e157-114">All services accept the SERVICE\_CONTROL\_INTERROGATE control value.</span></span>

<span data-ttu-id="4e157-115">A função [**QueryServiceStatusEx**](/windows/desktop/api/Winsvc/nf-winsvc-queryservicestatusex) relata o status mais recente de um serviço especificado, mas não obtém um status atualizado do próprio serviço.</span><span class="sxs-lookup"><span data-stu-id="4e157-115">The [**QueryServiceStatusEx**](/windows/desktop/api/Winsvc/nf-winsvc-queryservicestatusex) function reports the most recent status for a specified service, but does not get an updated status from the service itself.</span></span> <span data-ttu-id="4e157-116">O uso do \_ valor de controle INTERROGATE de controle de serviço \_ em uma chamada para [**chamada ControlService**](/windows/desktop/api/Winsvc/nf-winsvc-controlservice) garante que as informações de status retornadas sejam atuais.</span><span class="sxs-lookup"><span data-stu-id="4e157-116">Using the SERVICE\_CONTROL\_INTERROGATE control value in a call to [**ControlService**](/windows/desktop/api/Winsvc/nf-winsvc-controlservice) ensures that the status information returned is current.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4e157-117">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="4e157-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4e157-118">Controlando um serviço usando SC</span><span class="sxs-lookup"><span data-stu-id="4e157-118">Controlling a Service Using SC</span></span>](controlling-a-service-using-sc.md)
</dt> </dl>

 

 



