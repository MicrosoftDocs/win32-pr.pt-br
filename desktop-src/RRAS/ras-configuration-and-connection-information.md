---
title: Informações de conexão e configuração de RAS
description: Os aplicativos executados no Windows NT 4,0 e versões posteriores e no Windows 95 podem usar a função RasEnumConnections para obter informações sobre as conexões existentes no computador local.
ms.assetid: b738ed87-1ff5-4366-9e83-08ac08ec261c
keywords:
- Configuração e conexão, RAS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44c4e768f4686a24857a75212e40f2e64bc91109
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105778527"
---
# <a name="ras-configuration-and-connection-information"></a><span data-ttu-id="d162e-104">Informações de conexão e configuração de RAS</span><span class="sxs-lookup"><span data-stu-id="d162e-104">RAS Configuration and Connection Information</span></span>

<span data-ttu-id="d162e-105">Os aplicativos executados no Windows NT 4,0 e versões posteriores e no Windows 95 podem usar a função [**RasEnumConnections**](/windows/desktop/api/Ras/nf-ras-rasenumconnectionsa) para obter informações sobre as conexões existentes no computador local.</span><span class="sxs-lookup"><span data-stu-id="d162e-105">Applications running on Windows NT 4.0 and later versions, and Windows 95, can use the [**RasEnumConnections**](/windows/desktop/api/Ras/nf-ras-rasenumconnectionsa) function to get information about the existing connections on the local computer.</span></span> <span data-ttu-id="d162e-106">As informações de cada conexão incluem um identificador de conexão e o nome da entrada do catálogo telefônico usado para estabelecer a conexão.</span><span class="sxs-lookup"><span data-stu-id="d162e-106">The information for each connection includes a connection handle and the name of the phone-book entry used to establish the connection.</span></span> <span data-ttu-id="d162e-107">Você pode usar o identificador de conexão em uma chamada para a função [**RasGetConnectStatus**](/windows/desktop/api/Ras/nf-ras-rasgetconnectstatusa) obter o status atual da conexão.</span><span class="sxs-lookup"><span data-stu-id="d162e-107">You can use the connection handle in a call to the [**RasGetConnectStatus**](/windows/desktop/api/Ras/nf-ras-rasgetconnectstatusa) function get the current status of the connection.</span></span>

<span data-ttu-id="d162e-108">O Windows NT Server 4,0 e versões posteriores fornecem duas novas funções para recuperar informações de RAS.</span><span class="sxs-lookup"><span data-stu-id="d162e-108">Windows NT Server 4.0 and later versions provide two new functions for retrieving RAS information.</span></span> <span data-ttu-id="d162e-109">O Windows 95does não oferece suporte a essas funções.</span><span class="sxs-lookup"><span data-stu-id="d162e-109">Windows 95does not support these functions.</span></span>

<span data-ttu-id="d162e-110">A função [**RasEnumDevices**](/windows/desktop/api/Ras/nf-ras-rasenumdevicesa) retorna o nome e o tipo dos dispositivos compatíveis com RAS configurados no computador local.</span><span class="sxs-lookup"><span data-stu-id="d162e-110">The [**RasEnumDevices**](/windows/desktop/api/Ras/nf-ras-rasenumdevicesa) function returns the name and type of the RAS-capable devices that are configured on the local computer.</span></span>

<span data-ttu-id="d162e-111">A função [**RasConnectionNotification**](/windows/desktop/api/Ras/nf-ras-rasconnectionnotificationa) especifica um objeto de evento que o sistema sinaliza quando uma conexão RAS é criada ou encerrada.</span><span class="sxs-lookup"><span data-stu-id="d162e-111">The [**RasConnectionNotification**](/windows/desktop/api/Ras/nf-ras-rasconnectionnotificationa) function specifies an event object that the system signals when a RAS connection is created or terminated.</span></span>

 

 




