---
description: Uma paleta lógica é uma paleta de cores que um aplicativo cria e associa a um determinado contexto de dispositivo.
ms.assetid: 7cc86771-237d-4539-8f48-2474edb764a4
title: Paleta lógica
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 950252fa6b6bad03d139d60d08dc565fc56e74e19ecb305a05ebd23978d5327b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117698870"
---
# <a name="logical-palette"></a>Paleta lógica

Uma *paleta lógica é* uma paleta de cores que um aplicativo cria e associa a um determinado contexto de dispositivo. Paletas lógicas permitem que os aplicativos definam e usem cores que atendem às suas necessidades específicas. Os aplicativos podem criar qualquer número de paletas lógicas, usando-as para contextos de dispositivo separados ou alternando entre elas para um único contexto de dispositivo. O número máximo de paletas que um aplicativo pode criar depende dos recursos do sistema.

Um aplicativo cria uma paleta lógica usando a [**função CreatePalette.**](/windows/desktop/api/Wingdi/nf-wingdi-createpalette) O aplicativo preenche uma estrutura [**LOGPALETTE,**](/windows/win32/api/wingdi/ns-wingdi-logpalette) que especifica o número de entradas e os valores de cor para cada entrada e, em seguida, o aplicativo passa a estrutura para **CreatePalette.** A função retorna um identificador de paleta que o aplicativo usa em todas as operações subsequentes para identificar a paleta. Para usar cores na paleta lógica, o aplicativo seleciona a paleta em um contexto de dispositivo usando a função [**SelectPalette**](/windows/desktop/api/Wingdi/nf-wingdi-selectpalette) e, em seguida, realiza a paleta usando a [**função RealizePalette.**](/windows/desktop/api/Wingdi/nf-wingdi-realizepalette) As cores na paleta estão disponíveis assim que a paleta lógica é realizada.

Um aplicativo deve limitar o tamanho de suas paletas lógicas a apenas entradas suficientes para representar as cores necessárias. Os aplicativos não podem criar paletas lógicas maiores que o tamanho máximo da paleta, um valor dependente do dispositivo. Os aplicativos podem obter o tamanho máximo usando a [**função GetDeviceCaps**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) para recuperar o valor SIZEPALETTE.

Embora um aplicativo possa especificar qualquer valor de cor para uma determinada entrada em uma paleta lógica, nem todas as cores podem ser geradas pelo dispositivo especificado. O sistema não fornece uma maneira de descobrir quais cores têm suporte, mas o aplicativo pode descobrir o número total dessas cores recuperando a resolução de cores do dispositivo. A resolução de cores, especificada em bits de cor por pixel, é igual ao valor COLORRES retornado pela [**função GetDeviceCaps.**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) Um dispositivo que tem uma resolução de cores de 18 tem 262.144 cores possíveis. Se um aplicativo solicitar uma cor sem suporte, o sistema escolherá uma aproximação apropriada.

Depois que uma paleta lógica é criada, um aplicativo pode alterar as cores na paleta usando a [**função SetPaletteEntries.**](/windows/desktop/api/Wingdi/nf-wingdi-setpaletteentries) Se a paleta lógica tiver sido selecionada e realizada, alterar a paleta não afetará imediatamente as cores que estão sendo exibidas. O aplicativo deve usar as [**funções UnrealizeObject**](/windows/desktop/api/Wingdi/nf-wingdi-unrealizeobject) e [**RealizePalette**](/windows/desktop/api/Wingdi/nf-wingdi-realizepalette) para atualizar as cores. Em alguns casos, o aplicativo pode precisar desmarcar, não realizar, selecionar e perceber a paleta lógica para garantir que as cores sejam atualizadas exatamente conforme solicitado. Se um aplicativo selecionar uma paleta lógica em mais de um contexto de dispositivo, as alterações na paleta lógica afetarão todos os contextos de dispositivo para os quais ele está selecionado.

Um aplicativo pode alterar o número de entradas em uma paleta lógica usando a [**função ResizePalette.**](/windows/desktop/api/Wingdi/nf-wingdi-resizepalette) Se o aplicativo reduzir o tamanho, as entradas restantes permanecerão inalteradas. Se o aplicativo estender o tamanho, o sistema define a cor de cada nova entrada como preta (0, 0, 0) e o sinalizador como zero.

Um aplicativo pode recuperar os valores de cor e sinalizador para entradas em uma determinada paleta lógica usando a [**função GetPaletteEntries.**](/windows/desktop/api/Wingdi/nf-wingdi-getpaletteentries) Um aplicativo pode recuperar o índice para a entrada em uma determinada paleta lógica que mais corresponde a um valor de cor especificado usando a [**função GetNelettePaletteIndex.**](/windows/desktop/api/Wingdi/nf-wingdi-getnearestpaletteindex)

Quando um aplicativo não precisa mais de uma paleta lógica, ele pode excluí-lo usando a [**função DeleteObject.**](/windows/desktop/api/Wingdi/nf-wingdi-deleteobject) O aplicativo deve garantir que a paleta lógica não está mais selecionada em um contexto de dispositivo antes de excluir a paleta.

 

 



