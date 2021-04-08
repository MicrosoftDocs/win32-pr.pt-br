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
# <a name="overriding-the-default-mpr-time-out-interval"></a>Substituindo o intervalo de tempo limite de MPR padrão

O [*roteador de vários provedores*](../secgloss/m-gly.md) (MPR) chama [**NPGetCaps**](/windows/desktop/api/Npapi/nf-npapi-npgetcaps) para descobrir quando os provedores de rede serão iniciados (*nIndex* é definido como WNNC \_ Start). Em seguida, o MPR aguarda o período de tempo limite mais longo especificado por todos os provedores de rede antes de apresentar a rede consolidada ao usuário. Se um dos provedores de rede não souber quando ele será iniciado, o MPR usará um tempo limite padrão de 60 segundos para esse provedor.

Se necessário, o administrador pode substituir o tempo limite padrão criando o seguinte tempo limite do registro do **reg \_ DWORD** , em que *n* é o intervalo de tempo limite em milissegundos:

**HKEY \_ Sistema de \_ máquina local** \\  \\ **CurrentControlSet** \\ **Control** \\ **NetworkProvider** \\ **RestoreTimeout**  =  *n*

O pseudocódigo a seguir mostra o fluxo lógico completo para tratamento de tempo limite pelo MPR.


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



 

 
