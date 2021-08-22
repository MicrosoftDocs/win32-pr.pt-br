---
title: Funções do utilitário NAP
description: As funções do utilitário a seguir dão suporte à API NAP.
ms.assetid: 0819067c-cca5-4140-8b4d-f3b996826152
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d9b421069804a4047b511b775c7ffafe5b4b987eb0b0ad5105f48df0ed990e22
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118620777"
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

 

 




