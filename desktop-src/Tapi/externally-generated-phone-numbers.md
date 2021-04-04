---
description: Um provedor de serviços pode indicar números de telefone gerados externamente definindo membros da estrutura LINECALLINFO ao processar a \_ função lineGetCallInfo do TSPI.
ms.assetid: 10c83199-de7d-4a9b-84c4-ef8f5ea5055a
title: Números de telefone gerados externamente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b53e7039023ecec987a16c39367a569925c20ef8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647178"
---
# <a name="externally-generated-phone-numbers"></a><span data-ttu-id="5bf7a-103">Números de telefone gerados externamente</span><span class="sxs-lookup"><span data-stu-id="5bf7a-103">Externally Generated Phone Numbers</span></span>

<span data-ttu-id="5bf7a-104">Um provedor de serviços pode indicar números de telefone gerados externamente (ou seja, números para chamadas de saída geradas externamente para o computador) definindo os membros **DisplayableAddress**, **CalledParty** ou [comment](./comment-ovr.md) na estrutura [**LINECALLINFO**](/windows/win32/api/tapi/ns-tapi-linecallinfo) ao processar a função [**TSPI \_ lineGetCallInfo**](/windows/win32/api/tspi/nf-tspi-tspi_linegetcallinfo) .</span><span class="sxs-lookup"><span data-stu-id="5bf7a-104">A service provider can indicate externally generated phone numbers (that is, numbers for outbound calls generated externally to the computer) by setting the **DisplayableAddress**, **CalledParty**, or [Comment](./comment-ovr.md) members in the [**LINECALLINFO**](/windows/win32/api/tapi/ns-tapi-linecallinfo) structure when processing the [**TSPI\_lineGetCallInfo**](/windows/win32/api/tspi/nf-tspi-tspi_linegetcallinfo) function.</span></span> <span data-ttu-id="5bf7a-105">Se a TAPI não tiver salvo seus próprios dados para esses membros, ele deixará os dados definidos pelo provedor de serviços inalterados.</span><span class="sxs-lookup"><span data-stu-id="5bf7a-105">If TAPI has not saved its own data for these members, it leaves the data set by the service provider unchanged.</span></span> <span data-ttu-id="5bf7a-106">Se a TAPI tiver dados armazenados em cache para esses membros, a TAPI adicionará seu texto ao final da parte variável da estrutura **LINECALLINFO** e substituirá o tamanho e o deslocamento que o provedor de serviços colocou na parte fixa.</span><span class="sxs-lookup"><span data-stu-id="5bf7a-106">If TAPI does have cached data for these members, TAPI adds its text to the end of the variable portion of the **LINECALLINFO** structure and overwrites the size and offset the service provider has put into the fixed portion.</span></span>

<span data-ttu-id="5bf7a-107">Um provedor de serviços também pode copiar um número de saída para o membro **chamadoid** .</span><span class="sxs-lookup"><span data-stu-id="5bf7a-107">A service provider can also copy an outbound number into the **CalledID** member.</span></span> <span data-ttu-id="5bf7a-108">Portanto, os aplicativos de log devem verificar o membro **chamadoid** nas chamadas de saída se os membros **DisplayableAddress** e **CalledParty** estiverem vazios.</span><span class="sxs-lookup"><span data-stu-id="5bf7a-108">Therefore, logging applications should check the **CalledID** member on outbound calls if the **DisplayableAddress** and **CalledParty** members are empty.</span></span>

 

 
