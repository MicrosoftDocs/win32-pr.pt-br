---
title: Nomes de Version-Independent WFP e direcionamento de versões específicas do Windows
description: Em muitos casos, a API da WFP (Windows Filtering Platform) fornece mais de uma versão de uma função ou estrutura.
ms.assetid: FBDF53E5-F7DE-4DEB-AC18-6D2BB59FE670
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41be83a50b4786aa4b98cd7f8dd7405a33fe94be
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105783312"
---
# <a name="wfp-version-independent-names-and-targeting-specific-versions-of-windows"></a>Nomes de Version-Independent WFP e direcionamento de versões específicas do Windows

Em muitos casos, a API da WFP (Windows Filtering Platform) fornece mais de uma versão de uma função ou estrutura.

A maioria dos nomes de função e de dados na API WFP terminam com um número de versão, como "0" ou "1", mesmo se houver apenas uma versão.

## <a name="version-mapping-in-fwpvih"></a>Mapeamento de versão em fwpvi. h

O arquivo de cabeçalho fwpvi. h é incluído a partir do SDK do Windows 7 e do WDK. Esse arquivo de cabeçalho mapeia o nome da API sem versão para a versão apropriada para uso com um determinado sistema operacional.

Por exemplo, aqui está um breve trecho da versão do fwpvi. h incluída no SDK do Windows 8.


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



Como mostrado acima, há apenas uma versão do **FwpmNetEventCreateEnumHandle** – [**FwpmNetEventCreateEnumHandle0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventcreateenumhandle0) – portanto, qualquer chamada para **FwpmNetEventCreateEnumHandle** sempre chamará **FwpmNetEventCreateEnumHandle0**, independentemente do sistema operacional de destino.

No entanto, há três versões de de **FwpmNetEventEnum**: [**FwpmNetEventEnum0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventenum0), [**FwpmNetEventEnum1**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventenum1)e [**FwpmNetEventEnum2**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventenum2). O arquivo de cabeçalho fwpvi. h garante que uma chamada para **FwpmNetEventEnum** chamará a versão mais apropriada para o sistema operacional de destino:

-   [**FwpmNetEventEnum2**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventenum2) para Windows 8 (ou posterior)
-   O [**FwpmNetEventEnum1**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventenum1) para Windows 7 é direcionado
-   [**FwpmNetEventEnum0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventenum0) para sistemas operacionais anteriores (como o Windows Vista ou o Windows Vista com Service Pack 1 (SP1))

## <a name="calling-version-independent-functions-and-structures"></a>Chamando funções e estruturas Version-Independent

Os desenvolvedores de WFP destinados a um determinado sistema operacional ou versão do WDK são incentivados a sempre programar em relação às macros independentes de versão. Isso selecionará automaticamente a versão mais recente com suporte no sistema operacional que você está direcionando. O uso dos arquivos de cabeçalho mais recentes é recomendado, mesmo quando destinado a um sistema operacional anterior. Fazer isso de forma consistente garantirá que a versão mais recente com suporte seja usada e também possa facilitar a manutenção e a atualização do código.

A [documentação de referência da API WFP](fwp-reference.md) descreve cada versão de uma API numerada. Se houver mais de uma versão, o sistema operacional de destino será observado. No entanto, os desenvolvedores geralmente desejarão chamar as APIs independentes de versão (numéricas) e indicar o sistema operacional de destino (como **NTDDI \_ WIN6** para Windows Vista ou **NTDDI \_ WIN8** para Windows 8).

Para garantir a manipulação adequada das funções que usam parâmetros diferentes em versões diferentes, você pode incluir blocos condicionais, como `#if (NTDDI_VERSION >= NTDDI_WIN7)` .

 

 




