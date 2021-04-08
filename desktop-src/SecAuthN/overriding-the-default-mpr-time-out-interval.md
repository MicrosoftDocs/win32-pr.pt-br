---
description: O roteador de vários provedores (MPR) chama NPGetCaps para descobrir quando os provedores de rede serão iniciados (nIndex é definido como WNNC \_ Start).
ms.assetid: f57bd8ff-647d-42f8-abaf-7937b24416dd
title: Substituindo o intervalo de tempo limite de MPR padrão
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b4308d94f4b16a7f67786c8a0856f23922e6f25
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922315"
---
# <a name="overriding-the-default-mpr-time-out-interval"></a><span data-ttu-id="3cf31-103">Substituindo o intervalo de tempo limite de MPR padrão</span><span class="sxs-lookup"><span data-stu-id="3cf31-103">Overriding the Default MPR Time-out Interval</span></span>

<span data-ttu-id="3cf31-104">O [*roteador de vários provedores*](../secgloss/m-gly.md) (MPR) chama [**NPGetCaps**](/windows/desktop/api/Npapi/nf-npapi-npgetcaps) para descobrir quando os provedores de rede serão iniciados (*nIndex* é definido como WNNC \_ Start).</span><span class="sxs-lookup"><span data-stu-id="3cf31-104">The [*Multiple Provider Router*](../secgloss/m-gly.md) (MPR) calls [**NPGetCaps**](/windows/desktop/api/Npapi/nf-npapi-npgetcaps) to find out when the network providers will start (*nIndex* is set to WNNC\_START).</span></span> <span data-ttu-id="3cf31-105">Em seguida, o MPR aguarda o período de tempo limite mais longo especificado por todos os provedores de rede antes de apresentar a rede consolidada ao usuário.</span><span class="sxs-lookup"><span data-stu-id="3cf31-105">The MPR then waits for the longest time-out period specified by all network providers before it presents the consolidated network to the user.</span></span> <span data-ttu-id="3cf31-106">Se um dos provedores de rede não souber quando ele será iniciado, o MPR usará um tempo limite padrão de 60 segundos para esse provedor.</span><span class="sxs-lookup"><span data-stu-id="3cf31-106">If one of the network providers does not know when it will start, MPR uses a default time-out of 60 seconds for that provider.</span></span>

<span data-ttu-id="3cf31-107">Se necessário, o administrador pode substituir o tempo limite padrão criando o seguinte tempo limite do registro do **reg \_ DWORD** , em que *n* é o intervalo de tempo limite em milissegundos:</span><span class="sxs-lookup"><span data-stu-id="3cf31-107">If necessary, the administrator can override the default time-out by creating the following **REG\_DWORD** registry time-out, where *n* is the time-out interval in milliseconds:</span></span>

<span data-ttu-id="3cf31-108">**HKEY \_ Sistema de \_ máquina local** \\  \\ **CurrentControlSet** \\ **Control** \\ **NetworkProvider** \\ **RestoreTimeout**  =  *n*</span><span class="sxs-lookup"><span data-stu-id="3cf31-108">**HKEY\_LOCAL\_MACHINE**\\**SYSTEM**\\**CurrentControlSet**\\**Control**\\**NetworkProvider**\\**RestoreTimeout** = *n*</span></span>

<span data-ttu-id="3cf31-109">O pseudocódigo a seguir mostra o fluxo lógico completo para tratamento de tempo limite pelo MPR.</span><span class="sxs-lookup"><span data-stu-id="3cf31-109">The following pseudocode shows the complete logic flow for time-out handling by the MPR.</span></span>


```C++
If there is a RegistryTimeout,
Then MaxTimeout = RegistryTimeout.
Otherwise,
MaxTimeout = 0.
For each provider,
if the provider does not supply a time-out and
if there is a RegistryTimeout,
ProviderTimeout is set to RegistryTimeout.
Otherwise,
ProviderTimeout is set to DefaultTimeout.
Otherwise,
If the ProviderTimeout is longer than MaxTimeout,
MaxTimeout = ProviderTimeout.
```



 

 
