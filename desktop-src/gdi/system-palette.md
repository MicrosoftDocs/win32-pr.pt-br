---
description: O sistema mantém uma paleta de sistema para cada dispositivo que usa paletas.
ms.assetid: 4c93ce8c-6b3a-4016-bb47-786c25b93374
title: Paleta do Sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e540bd4068989a3c457568c2451dbc91f77755065f3bc70af03f9577fcebee9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117698128"
---
# <a name="system-palette"></a>Paleta do Sistema

O sistema mantém uma *paleta de sistema* para cada dispositivo que usa paletas. A paleta do sistema contém os valores de cor para todas as cores que podem ser exibidas ou desenhadas pelo dispositivo no momento. Além de exibir o conteúdo da paleta do sistema, os aplicativos não podem acessar a paleta do sistema diretamente. Em vez disso, o sistema tem controle total da paleta do sistema e permite o acesso somente por meio do uso de paletas lógicas.

Um aplicativo pode exibir o conteúdo da paleta do sistema usando a [**função GetSystemPaletteEntries.**](/windows/desktop/api/Wingdi/nf-wingdi-getsystempaletteentries) Essa função recupera o conteúdo de uma ou mais entradas, até o número total de entradas na paleta do sistema. O total é sempre igual ao número retornado para o valor SIZEPALETTE pela função [**GetDeviceCaps**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) e é igual ao tamanho máximo de qualquer paleta lógica específica.

Embora os aplicativos não possam alterar as cores diretamente na paleta do sistema, eles podem causar alterações ao perceber paletas lógicas. Para realizar uma paleta, o sistema examina cada cor solicitada e tenta encontrar uma entrada na paleta do sistema que contém uma combinação exata. Se o sistema encontrar uma cor correspondente, ele mapeia o índice da paleta lógica para o índice de paleta do sistema correspondente. Se o sistema não encontrar uma combinação exata, ele copia a cor solicitada para uma entrada de paleta de sistema nãousada antes de mapear os índices. Se todas as entradas da paleta do sistema estão em uso, o sistema mapeia o índice de paleta lógica para a entrada da paleta do sistema cuja cor corresponde mais próxima à cor solicitada. Depois que esse mapeamento for definido, os aplicativos não poderão substituí-lo. Por exemplo, os aplicativos não podem usar índices de paleta do sistema para especificar cores; somente índices de paleta lógica são permitidos.

Os aplicativos podem modificar a maneira como os índices são mapeados definindo o membro **peFlags** da estrutura [**PALETTEENTRY**](/previous-versions//dd162769(v=vs.85)) como valores selecionados ao criar a paleta lógica. Por exemplo, o sinalizador NOCOLLAPSE do PC direciona o sistema para copiar imediatamente a cor solicitada para uma entrada de paleta de sistema nãousada, independentemente de uma entrada de paleta do sistema já conter essa \_ cor. Além disso, o sinalizador PC EXPLICIT direciona o sistema para mapear o índice da paleta lógica para um índice de \_ paleta de sistema explicitamente determinado. (O aplicativo fornece o índice da paleta do sistema na palavra de ordem baixa da **estrutura PALETTEENTRY.)**

As paletas podem ser realizadas como uma paleta de plano de fundo ou uma paleta de primeiro plano especificando **TRUE** ou **FALSE,** respectivamente, para o parâmetro *bForceBackground* na [**função SelectPalette.**](/windows/desktop/api/Wingdi/nf-wingdi-selectpalette) Pode haver apenas uma paleta de primeiro plano no sistema por vez. Se a janela for a janela ativa no momento ou uma descendente da janela ativa no momento, ela poderá perceber uma paleta de primeiro plano. Caso contrário, a paleta será realizada como uma paleta de plano de fundo, independentemente do valor do *parâmetro bForceBackground.* A propriedade crítica de uma paleta de primeiro plano é que, quando realizada, ela pode substituir todas as entradas (exceto as entradas estáticas) na paleta do sistema. O sistema faz isso marcando todas as entradas que não são estáticas na paleta do sistema como não utilizadas antes da realização de uma paleta de primeiro plano, eliminando assim todas as entradas usadas. Nenhum pré-processamento ocorre na paleta do sistema para uma realização de paleta em segundo plano. A paleta de primeiro plano define todas as cores não estáticas possíveis. As paletas de plano de fundo podem definir apenas o que permanece aberto e são priorizados de uma maneira de primeira vez. Normalmente, os aplicativos usam paletas de plano de fundo para janelas filho que têm suas próprias paletas individuais. Isso ajuda a minimizar o número de alterações que ocorrem na paleta do sistema.

Uma entrada de paleta de sistema nãoutilada é qualquer entrada que não seja reservada e não contenha uma cor estática. As entradas reservadas são marcadas explicitamente com o valor \_ RESERVED do PC. Essas entradas são criadas quando um aplicativo realiza uma paleta lógica para animação de paleta. Entradas de cores estáticas são criadas pelo sistema e correspondem às cores na paleta padrão. A [**função GetDeviceCaps**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) pode ser usada para recuperar o valor NUMRESERVED, que especifica o número de entradas da paleta do sistema reservadas para cores estáticas.

Como a paleta do sistema tem um número limitado de entradas, selecionar e perceber uma paleta lógica para um determinado dispositivo pode afetar as cores associadas a outras paletas lógicas para o mesmo dispositivo. Essas alterações de cor são especialmente significativas quando ocorrem na exibição. Um aplicativo pode garantir que cores razoáveis sejam usadas para sua paleta lógica selecionada no momento redefinindo a paleta antes de cada uso. Um aplicativo redefine a paleta chamando as [**funções UnrealizeObject**](/windows/desktop/api/Wingdi/nf-wingdi-unrealizeobject) [**e RealizePalette.**](/windows/desktop/api/Wingdi/nf-wingdi-realizepalette) O uso dessas funções faz com que o sistema remape as cores na paleta lógica para cores razoáveis na paleta do sistema.

 

 
