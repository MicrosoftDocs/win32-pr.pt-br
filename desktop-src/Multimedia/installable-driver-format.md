---
title: Formato de driver instalável
description: Formato de driver instalável
ms.assetid: 4573567e-237d-47f9-9510-31d01326205f
keywords:
- drivers instaláveis, formatos
- drivers instaláveis, função DriverProc
- drivers instaláveis, mensagens
- mensagens do driver
- formatos de driver
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86fbbdcb8a49184dee6e9cf13c9f434506b1b48f
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104294000"
---
# <a name="installable-driver-format"></a><span data-ttu-id="f3cf6-108">Formato de driver instalável</span><span class="sxs-lookup"><span data-stu-id="f3cf6-108">Installable Driver Format</span></span>

<span data-ttu-id="f3cf6-109">Cada driver instalável exporta uma função [DriverProc](/windows/win32/api/mmiscapi/nc-mmiscapi-driverproc) .</span><span class="sxs-lookup"><span data-stu-id="f3cf6-109">Every installable driver exports a [DriverProc](/windows/win32/api/mmiscapi/nc-mmiscapi-driverproc) function.</span></span> <span data-ttu-id="f3cf6-110">Essa função de ponto de entrada comum recebe *mensagens de driver* do sistema que orientam o driver a realizar ações ou fornecer informações.</span><span class="sxs-lookup"><span data-stu-id="f3cf6-110">This common entry-point function receives *driver messages* from the system that direct the driver to carry out actions or provide information.</span></span> <span data-ttu-id="f3cf6-111">O sistema envia mensagens de driver para a função **DriverProc** quando um aplicativo ou uma dll abre ou fecha o driver ou solicita que uma mensagem seja enviada ao driver.</span><span class="sxs-lookup"><span data-stu-id="f3cf6-111">The system sends driver messages to the **DriverProc** function when an application or DLL opens or closes the driver or requests that a message be sent to the driver.</span></span> <span data-ttu-id="f3cf6-112">A função **DriverProc** processa a mensagem ou passa a mensagem para o manipulador de mensagens padrão, a função [DefDriverProc](/windows/win32/api/mmiscapi/nf-mmiscapi-defdriverproc) .</span><span class="sxs-lookup"><span data-stu-id="f3cf6-112">The **DriverProc** function either processes the message or passes the message to the default message handler, the [DefDriverProc](/windows/win32/api/mmiscapi/nf-mmiscapi-defdriverproc) function.</span></span> <span data-ttu-id="f3cf6-113">Em ambos os casos, **DriverProc** deve retornar um valor indicando se a ação solicitada foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="f3cf6-113">In either case, **DriverProc** must return a value indicating whether the requested action was successful.</span></span>

 

 