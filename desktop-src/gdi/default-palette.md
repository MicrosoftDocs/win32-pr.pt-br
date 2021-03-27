---
description: A paleta padrão é uma matriz de valores de cor que identifica as cores que podem ser usadas com um contexto de dispositivo por padrão.
ms.assetid: 7972d5da-2b73-4cd7-a2ee-fca3a571f611
title: Paleta padrão
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c100eeb144ab4f6483281b33739578642880a91f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827664"
---
# <a name="default-palette"></a>Paleta padrão

A *paleta padrão* é uma matriz de valores de cor que identifica as cores que podem ser usadas com um contexto de dispositivo por padrão. o sistema associa a paleta padrão a um contexto sempre que um aplicativo cria um contexto para um dispositivo que dá suporte a paletas de cores. A paleta padrão garante que as cores estejam disponíveis para uso por um aplicativo sem nenhuma ação adicional.

A paleta padrão geralmente tem 20 entradas (cores), mas o número exato de entradas pode variar de dispositivo para dispositivo. Esse número é igual ao valor de NUMCOLORS retornado pela função [**GetDeviceCaps**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) . Um aplicativo pode recuperar os valores de cor de cores na paleta padrão enumerando canetas sólidas, a mesma técnica usada para descobrir as cores disponíveis em dispositivos que não são de paleta. As cores na paleta padrão dependem do dispositivo. Os dispositivos de vídeo, por exemplo, geralmente usam as 16 cores padrão da tela VGA e quatro outras cores definidas pelo Windows. Os dispositivos de impressão podem usar outras cores padrão.

Ao usar a paleta padrão, os aplicativos usam valores de cor para especificar cores de caneta e de texto. Se a cor solicitada não estiver na paleta, o sistema aproximará a cor usando a cor mais próxima na paleta. Se um aplicativo solicitar uma cor de pincel sólida que não esteja na paleta, o sistema simulará a cor pontilhando com cores que estão na paleta.

Para evitar as aproximações e o pontilhamento, os aplicativos também podem especificar cores de caneta, pincel e texto usando índices de paleta de cores em vez de valores de cores. Um índice de paleta de cores é um valor inteiro que identifica uma entrada de paleta específica. Os aplicativos podem usar índices de paleta de cores no lugar de valores de cor, mas devem usar a macro [**PALETTEINDEX**](/windows/desktop/api/Wingdi/nf-wingdi-paletteindex) para criar os índices.

Os índices de paleta de cores só são úteis para dispositivos que dão suporte a paletas de cores. Para evitar essa dependência de dispositivo, os aplicativos que usam o mesmo código para desenhar os dispositivos de paleta e não da paleta devem usar valores de cor relativos à paleta para especificar cores de caneta, pincel e texto. Esses valores são idênticos aos valores de cor, exceto ao criar pincéis sólidos. (Em dispositivos de paleta, uma cor de pincel sólida especificada por um valor de cor relativa à paleta está sujeita à aproximação de cor em vez de pontilhada.) Os aplicativos devem usar a macro [**PALETTERGB**](/windows/desktop/api/Wingdi/nf-wingdi-palettergb) para criar valores de cor relativos à paleta.

O sistema não permite que um aplicativo altere as entradas na paleta padrão. Para usar cores diferentes daquelas na paleta padrão, um aplicativo deve criar sua própria paleta lógica e selecionar a paleta no contexto do dispositivo.

 

 



