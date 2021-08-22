---
description: O Windows SDK (WSDK) contém três DLLs de desempenho de exemplo completas.
ms.assetid: 862be53a-3d58-42b9-adf0-2f913dc6fb06
title: Exemplos de DLL de desempenho
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b94e77ed35b1c328879ad5f83dded45fe92bf4a62ae15c794e5d9d9b23daeda1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119143879"
---
# <a name="performance-dll-samples"></a>Exemplos de DLL de desempenho

O Windows SDK (WSDK) contém três DLLs de desempenho de exemplo completas. Esses exemplos estão localizados no diretório \\ \\ PerfDlls Do WinBase WinNT \\ \\ PerfDlls de Exemplos. A raiz desse caminho é o diretório de instalação base do WSDK. Você pode baixar o WSDK do [SDK (Software Development Kit)](https://developer.microsoft.com/windows/downloads/windows-10-sdk/) do Microsoft Windows (pesquise o SDK do Windows e selecione o download para o sistema operacional mais recente lançado).

Os exemplos contidos neste diretório são:

-   **AppMem**— fornece equivalentes das funções [**GlobalAlloc,**](/windows/desktop/api/winbase/nf-winbase-globalalloc) [**GlobalReAlloc**](/windows/desktop/api/winbase/nf-winbase-globalrealloc)e [**GlobalFree**](/windows/desktop/api/winbase/nf-winbase-globalfree) que relatam informações de desempenho. Os contadores de desempenho no Registro e na ferramenta Desempenho podem ler as informações de desempenho.
-   **LeakyBin**— demonstra o uso de contadores de desempenho do aplicativo.
-   **PerfGen**— fornece três formas de onda em cinco períodos diferentes para uso com a ferramenta desempenho para fornecer dados a uma taxa e valor conhecidos. Isso pode ser útil no teste de aplicativos que usam dados de desempenho e precisam de valores previsíveis para teste.

 

 
