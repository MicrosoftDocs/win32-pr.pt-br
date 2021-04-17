---
description: O SDK do Windows (WSDK) contém três DLLs de desempenho de exemplo completas.
ms.assetid: 862be53a-3d58-42b9-adf0-2f913dc6fb06
title: Amostras de DLL de desempenho
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 13e2210899651a065218474eb49175553a05aa8c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105783250"
---
# <a name="performance-dll-samples"></a>Amostras de DLL de desempenho

O SDK do Windows (WSDK) contém três DLLs de desempenho de exemplo completas. Esses exemplos estão localizados no diretório Samples \\ WinBase \\ WinNT \\ PerfTool \\ PerfDlls. A raiz desse caminho é o diretório de instalação base do WSDK. Você pode baixar o WSDK do [SDK (Software Development Kit) do Microsoft Windows](https://developer.microsoft.com/windows/downloads/windows-10-sdk/) (pesquise por SDK do Windows e selecione o download para o sistema operacional mais recente).

Os exemplos contidos neste diretório são:

-   **AppMem**— fornece contrapartes das funções [**GlobalAlloc**](/windows/desktop/api/winbase/nf-winbase-globalalloc), [**GlobalRealloc**](/windows/desktop/api/winbase/nf-winbase-globalrealloc)e [**GlobalFree**](/windows/desktop/api/winbase/nf-winbase-globalfree) que relatam informações de desempenho. Os contadores de desempenho no registro e a ferramenta de desempenho podem ler as informações de desempenho.
-   **LeakyBin**– demonstra o uso de contadores de desempenho do aplicativo.
-   **PerfGen**— fornece três ondas em cinco períodos diferentes para uso com a ferramenta de desempenho para fornecer dados a uma taxa e um valor conhecidos. Isso pode ser útil em aplicativos de teste que usam dados de desempenho e precisam de valores previsíveis para teste.

 

 
