---
title: Mensagens do driver
description: Mensagens do driver
ms.assetid: ed3748ac-08e6-418e-b345-30c796fa38f3
keywords:
- drivers instaláveis, mensagens
- drivers instaláveis, mensagens personalizadas
- mensagens do driver
- mensagens de driver personalizado
- drivers instaláveis, função DriverProc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25e03f9d68254752655be8abe9040a17d44dc0ff
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104007412"
---
# <a name="driver-messages"></a><span data-ttu-id="2d0d5-108">Mensagens do driver</span><span class="sxs-lookup"><span data-stu-id="2d0d5-108">Driver Messages</span></span>

<span data-ttu-id="2d0d5-109">Cada mensagem de driver consiste em um identificador de mensagem e parâmetros de 2 32 bits.</span><span class="sxs-lookup"><span data-stu-id="2d0d5-109">Each driver message consists of a message identifier and two 32-bit parameters.</span></span> <span data-ttu-id="2d0d5-110">O identificador de mensagem é um valor exclusivo que a função [DriverProc](/windows/win32/api/mmiscapi/nc-mmiscapi-driverproc) verifica para determinar qual ação executar. O significado dos parâmetros da mensagem depende da mensagem.</span><span class="sxs-lookup"><span data-stu-id="2d0d5-110">The message identifier is a unique value that the [DriverProc](/windows/win32/api/mmiscapi/nc-mmiscapi-driverproc) function checks to determine which action to carry out. The meaning of the message parameters depends on the message.</span></span> <span data-ttu-id="2d0d5-111">Os parâmetros podem representar valores ou endereços.</span><span class="sxs-lookup"><span data-stu-id="2d0d5-111">The parameters may represent values or addresses.</span></span> <span data-ttu-id="2d0d5-112">Em muitos casos, os parâmetros não são usados e são definidos como zero.</span><span class="sxs-lookup"><span data-stu-id="2d0d5-112">In many cases, the parameters are not used and are set to zero.</span></span>

<span data-ttu-id="2d0d5-113">As mensagens de driver podem ser padrão ou personalizadas.</span><span class="sxs-lookup"><span data-stu-id="2d0d5-113">Driver messages can be standard or custom.</span></span> <span data-ttu-id="2d0d5-114">O Windows envia mensagens de driver padrão, como [**drv \_ Open**](drv-open.md), [**drv \_ Close**](drv-close.md)e [**drv \_ Configure**](drv-configure.md), para um driver instalável em resposta a uma solicitação para abrir, fechar ou configurar o driver.</span><span class="sxs-lookup"><span data-stu-id="2d0d5-114">Windows sends standard driver messages, such as [**DRV\_OPEN**](drv-open.md), [**DRV\_CLOSE**](drv-close.md), and [**DRV\_CONFIGURE**](drv-configure.md), to an installable driver in response to a request to open, close, or configure the driver.</span></span> <span data-ttu-id="2d0d5-115">As mensagens padrão direcionam o driver instalável para carregar ou descarregar seus recursos, habilitar ou desabilitar sua operação, abrir ou fechar uma instância de driver e exibir uma caixa de diálogo de configuração.</span><span class="sxs-lookup"><span data-stu-id="2d0d5-115">The standard messages direct the installable driver to load or unload its resources, enable or disable its operation, open or close a driver instance, and display a configuration dialog box.</span></span> <span data-ttu-id="2d0d5-116">Algumas mensagens padrão, como o [**drv \_ Power**](drv-power.md) e [**drv \_ EXITSESSION**](drv-exitsession.md), notificam o driver de eventos de todo o sistema que afetam a operação do driver ou de qualquer hardware relacionado.</span><span class="sxs-lookup"><span data-stu-id="2d0d5-116">Some standard messages, such as [**DRV\_POWER**](drv-power.md) and [**DRV\_EXITSESSION**](drv-exitsession.md), notify the driver of system-wide events that affect the operation of the driver or any related hardware.</span></span>

<span data-ttu-id="2d0d5-117">Aplicativos e DLLs enviam mensagens de driver personalizadas para direcionar um driver instalável para executar ações específicas do driver.</span><span class="sxs-lookup"><span data-stu-id="2d0d5-117">Applications and DLLs send custom driver messages to direct an installable driver to carry out driver-specific actions.</span></span> <span data-ttu-id="2d0d5-118">Os drivers instaláveis que dão suporte a mensagens personalizadas devem incluir o processamento apropriado na função **DriverProc** .</span><span class="sxs-lookup"><span data-stu-id="2d0d5-118">Installable drivers that support custom messages must include appropriate processing in the **DriverProc** function.</span></span> <span data-ttu-id="2d0d5-119">Para evitar conflitos entre mensagens de driver personalizadas e padrão, os identificadores de mensagens personalizados devem ter valores variando de DRV \_ reservados para o \_ usuário drv.</span><span class="sxs-lookup"><span data-stu-id="2d0d5-119">To prevent conflict between custom and standard driver messages, custom message identifiers must have values ranging from DRV\_RESERVED to DRV\_USER.</span></span> <span data-ttu-id="2d0d5-120">As mensagens personalizadas passadas para a função [DefDriverProc](/windows/win32/api/mmiscapi/nf-mmiscapi-defdriverproc) são ignoradas.</span><span class="sxs-lookup"><span data-stu-id="2d0d5-120">Custom messages passed to the [DefDriverProc](/windows/win32/api/mmiscapi/nf-mmiscapi-defdriverproc) function are ignored.</span></span>

 

 