---
description: O conjunto de trabalho de um programa é uma coleção dessas páginas em seu espaço de endereço virtual que foi referenciado recentemente.
ms.assetid: 6017ef59-d2e9-4245-a406-8965024dbb35
title: Conjunto de trabalho do processo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 900b5d8a19c756a9087a9b2c006259857691dc11
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104169499"
---
# <a name="process-working-set"></a>Conjunto de trabalho do processo

O *conjunto de trabalho* de um programa é uma coleção dessas páginas em seu espaço de endereço virtual que foi referenciado recentemente. Ele inclui dados compartilhados e privados. Os dados compartilhados incluem páginas que contêm todas as instruções que seu aplicativo executa, incluindo aquelas em suas DLLs e as DLLs do sistema. À medida que o tamanho do conjunto de trabalho aumenta, a demanda de memória aumenta.

Um processo tem um tamanho de conjunto de trabalho mínimo associado e o tamanho máximo do conjunto de trabalho. Cada vez que você chama [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa), ele reserva o tamanho mínimo do conjunto de trabalho para o processo. O Gerenciador de memória virtual tenta manter memória suficiente para o conjunto de trabalho mínimo residente quando o processo está ativo, mas não mantém mais do que o tamanho máximo.

Para obter os tamanhos mínimo e máximo solicitados do conjunto de trabalho para seu aplicativo, chame a função [**GetProcessWorkingSetSize**](/windows/desktop/api/WinBase/nf-winbase-getprocessworkingsetsize) .

O sistema define os tamanhos de conjunto de trabalho padrão. Você também pode modificar os tamanhos de conjunto de trabalho usando a função [**SetProcessWorkingSetSize**](/windows/desktop/api/WinBase/nf-winbase-setprocessworkingsetsize) . Definir esses valores não é uma garantia de que a memória será reservada ou residente. Tenha cuidado ao solicitar um tamanho de conjunto de trabalho mínimo ou máximo, pois isso pode prejudicar o desempenho do sistema.

Para obter o tamanho atual ou de pico do conjunto de trabalho para seu processo, use a função [**GetProcessMemoryInfo**](/windows/win32/api/psapi/nf-psapi-getprocessmemoryinfo) .

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Informações de desempenho da memória](/previous-versions/windows/desktop/legacy/aa965225(v=vs.85))
</dt> <dt>

[Conjunto de trabalho](../memory/working-set.md)
</dt> </dl>

 

 
