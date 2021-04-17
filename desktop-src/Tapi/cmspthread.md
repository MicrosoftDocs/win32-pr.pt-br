---
description: A classe CMSPThread implementa o thread de trabalho do MSPs.
ms.assetid: 9dc2373a-cdcf-4e60-95fa-56cb68bda15b
title: CMSPThread
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17a12b71668e81688b5de7f41e188a51b88944d6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105754199"
---
# <a name="cmspthread"></a><span data-ttu-id="c4afc-103">CMSPThread</span><span class="sxs-lookup"><span data-stu-id="c4afc-103">CMSPThread</span></span>

<span data-ttu-id="c4afc-104">A classe **CMSPThread** implementa o thread de trabalho do MSP.</span><span class="sxs-lookup"><span data-stu-id="c4afc-104">The **CMSPThread** class implements the MSP's worker thread.</span></span> <span data-ttu-id="c4afc-105">As classes base usam esse thread de trabalho para várias finalidades.</span><span class="sxs-lookup"><span data-stu-id="c4afc-105">The base classes use this worker thread for a number of purposes.</span></span> <span data-ttu-id="c4afc-106">Um mecanismo de item de trabalho leve e genérico é fornecido para permitir que o MSP derivado Use esse thread para seus próprios itens de trabalho síncronos ou assíncronos, o que for possível.</span><span class="sxs-lookup"><span data-stu-id="c4afc-106">A generic and lightweight work item mechanism is provided to allow the derived MSP to use this thread for its own synchronous or asynchronous work items, whatever they may be.</span></span> <span data-ttu-id="c4afc-107">O thread também bombas mensagens e dá suporte ao tratamento de APCs (embora APCs não sejam usados nas classes base).</span><span class="sxs-lookup"><span data-stu-id="c4afc-107">The thread also pumps messages and supports handling of APCs (although APCs are not used in the base classes).</span></span>

<span data-ttu-id="c4afc-108">Quando vários endereços like estão presentes (ou seja, quando a mesma implementação de MSP da mesma DLL é instanciada várias vezes), a classe thread garante a escalabilidade usando automaticamente um único thread para todos os endereços.</span><span class="sxs-lookup"><span data-stu-id="c4afc-108">When multiple like addresses are present (that is, when the same MSP implementation from the same DLL is instantiated multiple times), the thread class ensures scalability by automatically using a single thread for all the addresses.</span></span> <span data-ttu-id="c4afc-109">A interface para a classe thread é tal que a implementação MSP pode pensar na classe thread como um thread privado e não precisa se preocupar com os outros endereços que podem estar compartilhando.</span><span class="sxs-lookup"><span data-stu-id="c4afc-109">The interface to the thread class is such that the MSP implementation can think of the thread class as a private thread and need not care about the other addresses that may be sharing it.</span></span>

<span data-ttu-id="c4afc-110">Definido em MSPthrd. h.</span><span class="sxs-lookup"><span data-stu-id="c4afc-110">Defined in MSPthrd.h.</span></span>

 

 



