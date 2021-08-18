---
description: A MPR (Roteador Múltiplo Provedor) chama NPGetCaps para descobrir quando os provedores de rede serão iniciados (nIndex está definido como WNNC \_ START).
ms.assetid: f57bd8ff-647d-42f8-abaf-7937b24416dd
title: Substituindo o intervalo de tempo-out da MPR padrão
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c51c2c9db2fb892b7c2fc9646a9328fb9de4b7f9782ff5204ed261b16471ca4c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118921130"
---
# <a name="overriding-the-default-mpr-time-out-interval"></a>Substituindo o intervalo de tempo-out da MPR padrão

A [*MPR*](../secgloss/m-gly.md) (Roteador De Vários Provedores) chama [**NPGetCaps**](/windows/desktop/api/Npapi/nf-npapi-npgetcaps) para descobrir quando os provedores de rede iniciarão (*nIndex* está definido como WNNC \_ START). Em seguida, a MPR aguarda o período de tempo máximo mais longo especificado por todos os provedores de rede antes de apresentar a rede consolidada ao usuário. Se um dos provedores de rede não sabe quando ele será iniciar, a MPR usará um tempo de tempo decorro padrão de 60 segundos para esse provedor.

Se necessário, o administrador pode substituir o tempo-tempo-out padrão criando o seguinte tempo-out do registro **REG \_ DWORD,** em que *n* é o intervalo de tempo-fora em milissegundos:

**HKEY \_ Rede \_ de controle** Local MACHINE \\ **SYSTEM** \\ **CurrentControlSetProvider** \\  \\  \\ **RestoreTimeout**  =  *n*

O pseudocódigo a seguir mostra o fluxo lógico completo para a manipulação de tempo-out pela MPR.


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



 

 
