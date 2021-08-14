---
description: a quantidade máxima de memória física com suporte do Microsoft Windows varia de 2 GB a 2 TB, dependendo da versão do Windows.
ms.assetid: 5e8fca7a-b85f-4bbd-80c1-e580a815fdce
title: espaço de endereço Virtual e Armazenamento físico
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 774e0af302fbd965f16b09a88d6dabb7c95948855c8d939d3c856ebe098337d4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118386151"
---
# <a name="virtual-address-space-and-physical-storage"></a>espaço de endereço Virtual e Armazenamento físico

a quantidade máxima de memória física com suporte do Microsoft Windows varia de 2 GB a 24 TB, dependendo da versão do Windows. para obter mais informações, consulte [limites de memória para versões de Windows](memory-limits-for-windows-releases.md). O espaço de endereço virtual de cada processo pode ser menor ou maior do que a memória física total disponível no computador. O subconjunto do espaço de endereço virtual de um processo que reside na memória física é conhecido como o *conjunto de trabalho*. Se os threads de um processo tentarem usar mais memória física do que o disponível no momento, o sistema paginará parte do conteúdo da memória para o disco. A quantidade total de espaço de endereço virtual disponível para um processo é limitada pela memória física e o espaço livre em disco disponível para o arquivo de paginação.

O armazenamento físico e o espaço de endereço virtual de cada processo são organizados em *páginas*, unidades de memória, cujo tamanho depende do computador host. Por exemplo, em computadores x86, o tamanho da página do host é de 4 quilobytes.

Para maximizar sua flexibilidade no gerenciamento de memória, o sistema pode mover páginas de memória física de e para um arquivo de paginação no disco. Quando uma página é movida na memória física, o sistema atualiza os mapas de página dos processos afetados. Quando o sistema precisa de espaço na memória física, ele move as páginas usadas menos recentemente da memória física para o arquivo de paginação. A manipulação de memória física pelo sistema é completamente transparente para aplicativos, que operam somente em seus espaços de endereço virtual.

 

 



