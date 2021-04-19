---
description: A instalação de um novo provedor de serviços é altamente específica do dispositivo e do sistema operacional, portanto, os detalhes estão fora do escopo deste SDK.
ms.assetid: 5b48e144-5092-4462-b74c-d3295d23afe1
title: Instalação e inicialização
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4391f8453d17cc70382d3ecb0dff65189b61c310
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105796328"
---
# <a name="installation-and-initialization"></a><span data-ttu-id="41525-103">Instalação e inicialização</span><span class="sxs-lookup"><span data-stu-id="41525-103">Installation and Initialization</span></span>

<span data-ttu-id="41525-104">A instalação de um novo provedor de serviços é altamente específica do dispositivo e do sistema operacional, portanto, os detalhes estão fora do escopo deste SDK.</span><span class="sxs-lookup"><span data-stu-id="41525-104">Installation of a new service provider is highly device- and operating-system-specific, so the details are outside the scope of this SDK.</span></span> <span data-ttu-id="41525-105">Em geral, o objetivo da instalação é a configuração do provedor de serviços para o ambiente de comunicação atual.</span><span class="sxs-lookup"><span data-stu-id="41525-105">Generally speaking, the goal of installation is configuration of the service provider for the current communications environment.</span></span> <span data-ttu-id="41525-106">Isso geralmente envolve entradas de registro e a configuração de dependências de serviço.</span><span class="sxs-lookup"><span data-stu-id="41525-106">This usually involves registry entries and the setting of service dependencies.</span></span>

<span data-ttu-id="41525-107">A inicialização de um provedor de serviços de telefonia começa com a negociação de versão.</span><span class="sxs-lookup"><span data-stu-id="41525-107">Initialization of a telephony service provider starts with version negotiation.</span></span> <span data-ttu-id="41525-108">Consulte [controle de versão do TSPI](tspi-versioning.md) para uma discussão sobre negociação de versão e versão atual.</span><span class="sxs-lookup"><span data-stu-id="41525-108">See [TSPI Versioning](tspi-versioning.md) for a discussion of version negotiation and current version.</span></span>

<span data-ttu-id="41525-109">Em seguida, a TAPI chama [**TSPI \_ providerInit**](/windows/win32/api/tspi/nf-tspi-tspi_providerinit), que passa o provedor de um ponteiro para uma função de retorno de chamada usada para relatar o progresso das funções assíncronas.</span><span class="sxs-lookup"><span data-stu-id="41525-109">TAPI then calls [**TSPI\_providerInit**](/windows/win32/api/tspi/nf-tspi-tspi_providerinit), which passes the provider a pointer to a callback function used to report on asynchronous functions progress.</span></span> <span data-ttu-id="41525-110">O TSP retorna uma contagem de dispositivos de linha e telefone associados ao identificador de dispositivo atual.</span><span class="sxs-lookup"><span data-stu-id="41525-110">The TSP returns a count of line and phone devices associated with the current device identifier.</span></span>

<span data-ttu-id="41525-111">Normalmente, a próxima etapa será o inventário de recursos, conduzido pela TAPI invocando [**TSPI \_ LineGetDevCaps**](/windows/win32/api/tspi/nf-tspi-tspi_linegetdevcaps) e [**TSPI \_ lineGetAddressCaps**](/windows/win32/api/tspi/nf-tspi-tspi_linegetaddresscaps).</span><span class="sxs-lookup"><span data-stu-id="41525-111">Typically, the next step will be resource inventory, conducted by TAPI invoking [**TSPI\_lineGetDevCaps**](/windows/win32/api/tspi/nf-tspi-tspi_linegetdevcaps) and [**TSPI\_lineGetAddressCaps**](/windows/win32/api/tspi/nf-tspi-tspi_linegetaddresscaps).</span></span> <span data-ttu-id="41525-112">O provedor de serviços deve preencher esses elementos das estruturas de dados envolvidas que pertencem aos recursos de dispositivo e de sessão que ele suporta.</span><span class="sxs-lookup"><span data-stu-id="41525-112">The service provider is expected to fill in those elements of the data structures involved that pertain to device and session capabilities it supports.</span></span>

<span data-ttu-id="41525-113">A TAPI coleta informações de vários aplicativos relacionados aos requisitos de notificação de eventos e instrui o TSP usando [**TSPI \_ lineSetDefaultMediaDetection**](/windows/win32/api/tspi/nf-tspi-tspi_linesetdefaultmediadetection) para indicar quais tipos de mídia serão detectados para uma linha e [**TSPI \_ lineSetStatusMessages**](/windows/win32/api/tspi/nf-tspi-tspi_linesetstatusmessages) para indicar quais eventos de linha e endereço devem ser relatados.</span><span class="sxs-lookup"><span data-stu-id="41525-113">TAPI collects information from the various applications concerning event notification requirements, and instructs the TSP using [**TSPI\_lineSetDefaultMediaDetection**](/windows/win32/api/tspi/nf-tspi-tspi_linesetdefaultmediadetection) to indicate which media types to detect for a line and [**TSPI\_lineSetStatusMessages**](/windows/win32/api/tspi/nf-tspi-tspi_linesetstatusmessages) to indicate which line and address events should be reported.</span></span>

 

 
