---
title: Funções do utilitário NAP
description: As funções do utilitário a seguir dão suporte à API NAP.
ms.assetid: 0819067c-cca5-4140-8b4d-f3b996826152
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 260c423909011c81f52ea89ce8d3137b35c55167
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103635668"
---
# <a name="nap-utility-functions"></a>Funções do utilitário NAP

> [!Note]  
> A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10

 

As funções do utilitário a seguir dão suporte à API NAP.

Todas as interfaces COM com suporte do sistema NAP usam regras de gerenciamento de memória COM padrão e o alocador de memória COM (CoTaskMemAlloc e CoTaskMemFree).

-   EM parâmetros — alocados e liberados pelo chamador.
-   Parâmetros de saída — alocados pelo receptor, liberados pelo chamador usando CoTaskMem \* ()
-   Parâmetros de entrada/saída — alocados pelo chamador, liberados e realocados pelo receptor, por fim liberados pelo chamador, usando CoTaskMem \* ()

Nas funções FreeXxx (), todos os ponteiros inseridos também serão liberados.

-   [**AllocConnections**](allocconnections-func.md)
-   [**AllocCountedString**](alloccountedstring-func.md)
-   [**AllocFixupInfo**](allocfixupinfo-func.md)
-   [**FreeConnections**](freeconnections-func.md)
-   [**FreeCountedString**](freecountedstring-func.md)
-   [**FreeFixupInfo**](freefixupinfo-func.md)
-   [**FreeIsolationInfo**](freeisolationinfo-func.md)
-   [**FreeIsolationInfoEx**](freeisolationinfoex.md)
-   [**FreeNapComponentRegistrationInfoArray**](freenapcomponentregistrationinfoarray-func.md)
-   [**FreeNetworkSoH**](freenetworksoh-func.md)
-   [**FreePrivateData**](freeprivatedata-func.md)
-   [**FreeSoH**](freesoh-func.md)
-   [**FreeSoHAttributeValue**](freesohattributevalue-func.md)
-   [**FreeSystemHealthAgentState**](freesystemhealthagentstate-func.md)
-   [**InitializeNapAgentNotifier**](initializenapagentnotifier.md)
-   [**UninitializeNapAgentNotifier**](uninitializenapagentnotifier.md)

 

 




