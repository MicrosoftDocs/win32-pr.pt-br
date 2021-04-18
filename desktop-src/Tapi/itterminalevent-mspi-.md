---
description: 'Quando o método ITTAPIEventNotification:: Event retorna um \_ evento TAPI igual a \_ fileterminal, os métodos expostos pela interface ITTerminalEvent podem ser usados para recuperar informações relacionadas ao evento de terminal que ocorreu, se existir um msp.'
ms.assetid: 5277776e-0471-41b6-b662-4346a9d237ec
title: ITTerminalEvent (MSPI)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 593b9a7d048db9843825ccde8b22d0585a0c07fb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105760338"
---
# <a name="itterminalevent-mspi"></a><span data-ttu-id="0f3fe-103">ITTerminalEvent (MSPI)</span><span class="sxs-lookup"><span data-stu-id="0f3fe-103">ITTerminalEvent (MSPI)</span></span>

<span data-ttu-id="0f3fe-104">Quando o método [**ITTAPIEventNotification:: Event**](/windows/desktop/api/Tapi3if/nf-tapi3if-ittapieventnotification-event) retorna [**um \_ evento TAPI**](/windows/desktop/api/Tapi3if/ne-tapi3if-tapi_event) igual **a \_ fileterminal**, os métodos expostos pela interface **ITTerminalEvent** podem ser usados para recuperar informações relacionadas ao evento de terminal que ocorreu, se existir um msp.</span><span class="sxs-lookup"><span data-stu-id="0f3fe-104">When the [**ITTAPIEventNotification::Event**](/windows/desktop/api/Tapi3if/nf-tapi3if-ittapieventnotification-event) method returns [**TAPI\_EVENT**](/windows/desktop/api/Tapi3if/ne-tapi3if-tapi_event) equal to **TE\_TERMINAL**, the methods exposed by the **ITTerminalEvent** interface can be used to retrieve information concerning the terminal event that has occurred, if an MSP exists.</span></span>

<span data-ttu-id="0f3fe-105">A interface **ITTerminalEvent** é implementada por um msp e não estará disponível se não houver nenhum provedor de serviços de mídia associado ao endereço.</span><span class="sxs-lookup"><span data-stu-id="0f3fe-105">The **ITTerminalEvent** interface is implemented by an MSP and is not available if there is no media service provider associated with the address.</span></span> <span data-ttu-id="0f3fe-106">Consulte **ITTerminalEvent** na seção de interface msp para obter detalhes sobre essa interface.</span><span class="sxs-lookup"><span data-stu-id="0f3fe-106">Please see **ITTerminalEvent** in the MSP Interface section for details on this interface.</span></span>

 

 



