---
title: Nomes de Version-Independent WFP e versões específicas de destino do Windows
description: Em muitos casos, a API Windows WFP (Plataforma de Filtragem de Dados) fornece mais de uma versão de uma função ou estrutura.
ms.assetid: FBDF53E5-F7DE-4DEB-AC18-6D2BB59FE670
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: baf5fbef08c3284d94eb215e0cce2fc44fc9b827b686e531057db22b60020132
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119766666"
---
# <a name="wfp-version-independent-names-and-targeting-specific-versions-of-windows"></a>Nomes de Version-Independent WFP e versões específicas de destino do Windows

Em muitos casos, a API Windows WFP (Plataforma de Filtragem de Dados) fornece mais de uma versão de uma função ou estrutura.

A maioria dos dados e nomes de função na API do WFP termina com um número de versão, como "0" ou "1", mesmo que haja apenas uma versão.

## <a name="version-mapping-in-fwpvih"></a>Mapeamento de versão em fwpvi.h

O arquivo de título fwpvi.h está incluído a partir do SDK Windows 7 e WDK. Esse arquivo de header mapeia o nome da API sem versão para a versão apropriada para uso com um determinado sistema operacional.

Por exemplo, aqui está um breve trecho da versão de fwpvi.h incluído no SDK Windows 8.


```C++
#define FwpmNetEventCreateEnumHandle FwpmNetEventCreateEnumHandle0
#if (NTDDI_VERSION >= NTDDI_WIN8)
#define FwpmNetEventEnum FwpmNetEventEnum2
#elif (NTDDI_VERSION >= NTDDI_WIN7)
#define FwpmNetEventEnum FwpmNetEventEnum1
#else
#define FwpmNetEventEnum FwpmNetEventEnum0
#endif
```



Conforme mostrado acima, há apenas uma versão de **FwpmNetEventCreateEnumHandle** – [**FwpmNetEventCreateEnumHandle0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventcreateenumhandle0) – portanto, qualquer chamada para **FwpmNetEventCreateEnumHandle** sempre chamará **FwpmNetEventCreateEnumHandle0,** independentemente do sistema operacional direcionado.

No entanto, há três versões de **FwpmNetEventEnum:** [**FwpmNetEventEnum0,**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventenum0) [**FwpmNetEventEnum1**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventenum1)e [**FwpmNetEventEnum2**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventenum2). O arquivo de header fwpvi.h garante que uma chamada para **FwpmNetEventEnum** chame a versão mais apropriada para o sistema operacional de o alvo:

-   [**FwpmNetEventEnum2**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventenum2) para Windows 8 (ou posterior)
-   [**FwpmNetEventEnum1 para**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventenum1) Windows 7 é direcionado
-   [**FwpmNetEventEnum0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventenum0) para sistemas operacionais anteriores (como Windows Vista ou Windows Vista com Service Pack 1 (SP1))

## <a name="calling-version-independent-functions-and-structures"></a>Chamando Version-Independent funções e estruturas

Os desenvolvedores do WFP destinados a um sistema operacional específico ou versão do WDK são incentivados a sempre programar em relação às macros independentes de versão. Isso selecionará automaticamente a versão mais recente com suporte no sistema operacional que você está direcionando. O uso dos arquivos de header mais recentes é recomendado, mesmo ao direcionar para um sistema operacional anterior. Fazer isso de forma consistente garantirá que a versão mais recente com suporte seja usada e também poderá facilitar a manutenção e atualização do código.

A [documentação de referência da API do WFP](fwp-reference.md) descreve cada versão de uma API numerada. Se houver mais de uma versão, o sistema operacional de o alvo será marcado. No entanto, os desenvolvedores geralmente querem chamar as APIs independentes de versão (sem número) e indicar o sistema operacional de o alvo (como **NTDDI \_ WIN6** para Windows Vista ou **NTDDI \_ WIN8** para Windows 8).

Para garantir o tratamento adequado de funções que têm parâmetros diferentes em versões diferentes, você pode incluir blocos condicionais, como `#if (NTDDI_VERSION >= NTDDI_WIN7)` .

 

 




