---
description: TSPIMessage é um tipo de enumeração que define o conjunto de funções LINEEVENT e PHONEEVENT adicionais que aparecem em TSPI que não aparecem na TAPI.
ms.assetid: b3c4ce68-033f-42f1-8c37-66326d21bf32
title: TSPIMessage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75ed5f081c367c675c565f64146b2201890b8306
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647704"
---
# <a name="tspimessage"></a><span data-ttu-id="04101-103">TSPIMessage</span><span class="sxs-lookup"><span data-stu-id="04101-103">TSPIMessage</span></span>

<span data-ttu-id="04101-104">**TSPIMessage** é um tipo de enumeração que define o conjunto de funções [**LINEEVENT**](/windows/win32/api/tspi/nc-tspi-lineevent) e [**PHONEEVENT**](/windows/desktop/api/tspi/nc-tspi-phoneevent) adicionais que aparecem em TSPI que não aparecem na TAPI.</span><span class="sxs-lookup"><span data-stu-id="04101-104">**TSPIMessage** is an enumeration type that defines the set of additional [**LINEEVENT**](/windows/win32/api/tspi/nc-tspi-lineevent) and [**PHONEEVENT**](/windows/desktop/api/tspi/nc-tspi-phoneevent) functions appearing in TSPI that do not appear in TAPI.</span></span>

## <a name="parameters"></a><span data-ttu-id="04101-105">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="04101-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="04101-106"><span id="TSPI_MESSAGE_BASE"></span><span id="tspi_message_base"></span>\_base da mensagem TSPI \_</span><span class="sxs-lookup"><span data-stu-id="04101-106"><span id="TSPI_MESSAGE_BASE"></span><span id="tspi_message_base"></span>TSPI\_MESSAGE\_BASE</span></span>
</dt> <dd>

<span data-ttu-id="04101-107">O número mais baixo no intervalo de valores de mensagem específicos de TSPI.</span><span class="sxs-lookup"><span data-stu-id="04101-107">The lowest number in the range of TSPI-specific message values.</span></span> <span data-ttu-id="04101-108">Esse valor não tem nenhum significado, mas serve como base para definir os outros valores.</span><span class="sxs-lookup"><span data-stu-id="04101-108">This value has no meaning by itself, but serves as a base for defining the other values.</span></span>

</dd> <dt>

<span data-ttu-id="04101-109"><span id="LINE_NEWCALL"></span><span id="line_newcall"></span>NewCall de linha \_</span><span class="sxs-lookup"><span data-stu-id="04101-109"><span id="LINE_NEWCALL"></span><span id="line_newcall"></span>LINE\_NEWCALL</span></span>
</dt> <dd>

<span data-ttu-id="04101-110">Especifica que uma chamada nova recebida chegou e a apresenta à TAPI.</span><span class="sxs-lookup"><span data-stu-id="04101-110">Specifies that a new, incoming call has arrived and introduces it to TAPI.</span></span> <span data-ttu-id="04101-111">Essa deve ser a primeira mensagem enviada à TAPI para uma nova chamada de entrada.</span><span class="sxs-lookup"><span data-stu-id="04101-111">This must be the first message sent to TAPI for a new incoming call.</span></span> <span data-ttu-id="04101-112">A TAPI retorna seu identificador opaco para a chamada como parte de seu tratamento dessa mensagem.</span><span class="sxs-lookup"><span data-stu-id="04101-112">TAPI returns its opaque identifier for the call as part of its handling of this message.</span></span>

</dd> <dt>

<span data-ttu-id="04101-113"><span id="LINE_CALLDEVSPECIFIC"></span><span id="line_calldevspecific"></span>CALLDEVSPECIFIC de linha \_</span><span class="sxs-lookup"><span data-stu-id="04101-113"><span id="LINE_CALLDEVSPECIFIC"></span><span id="line_calldevspecific"></span>LINE\_CALLDEVSPECIFIC</span></span>
</dt> <dd>

<span data-ttu-id="04101-114">Especifica que um evento específico do dispositivo ocorreu em um dispositivo de chamada.</span><span class="sxs-lookup"><span data-stu-id="04101-114">Specifies that a device-specific event has occurred on a call device.</span></span>

</dd> <dt>

<span data-ttu-id="04101-115"><span id="LINE_CALLDEVSPECIFICFEATURE"></span><span id="line_calldevspecificfeature"></span>CALLDEVSPECIFICFEATURE de linha \_</span><span class="sxs-lookup"><span data-stu-id="04101-115"><span id="LINE_CALLDEVSPECIFICFEATURE"></span><span id="line_calldevspecificfeature"></span>LINE\_CALLDEVSPECIFICFEATURE</span></span>
</dt> <dd>

<span data-ttu-id="04101-116">Especifica que um evento de recurso específico do dispositivo ocorreu em um dispositivo de chamada.</span><span class="sxs-lookup"><span data-stu-id="04101-116">Specifies that a device-specific feature event has occurred on a call device.</span></span>

</dd> </dl>

 

 
