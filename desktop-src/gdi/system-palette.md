---
description: O sistema mantém uma paleta do sistema para cada dispositivo que usa paletas.
ms.assetid: 4c93ce8c-6b3a-4016-bb47-786c25b93374
title: Paleta do sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d8738cf63eef0b77f2d184f2cf95b6550b81053
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104988957"
---
# <a name="system-palette"></a>Paleta do sistema

O sistema mantém uma *paleta do sistema* para cada dispositivo que usa paletas. A paleta do sistema contém os valores de cor para todas as cores que podem ser exibidas ou desenhadas no momento pelo dispositivo. Além de exibir o conteúdo da paleta do sistema, os aplicativos não podem acessar a paleta do sistema diretamente. Em vez disso, o sistema tem controle total da paleta do sistema e permite o acesso somente por meio do uso de paletas lógicas.

Um aplicativo pode exibir o conteúdo da paleta do sistema usando a função [**GetSystemPaletteEntries**](/windows/desktop/api/Wingdi/nf-wingdi-getsystempaletteentries) . Essa função recupera o conteúdo de uma ou mais entradas, até o número total de entradas na paleta do sistema. O total é sempre igual ao número retornado para o valor SIZEPALETTE pela função [**GetDeviceCaps**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) e é igual ao tamanho máximo de qualquer paleta lógica específica.

Embora os aplicativos não possam alterar as cores diretamente na paleta do sistema, eles podem causar alterações ao concretizar paletas lógicas. Para obter uma paleta, o sistema examina cada cor solicitada e tenta encontrar uma entrada na paleta do sistema que contém uma correspondência exata. Se o sistema encontrar uma cor correspondente, ele mapeará o índice de paleta lógica para o índice de paleta do sistema correspondente. Se o sistema não encontrar uma correspondência exata, ele copiará a cor solicitada para uma entrada da paleta do sistema não usada antes de mapear os índices. Se todas as entradas da paleta do sistema estiverem em uso, o sistema mapeará o índice da paleta lógica para a entrada da paleta do sistema cuja cor corresponde à cor solicitada mais próxima. Depois que esse mapeamento é definido, os aplicativos não podem substituí-lo. Por exemplo, os aplicativos não podem usar índices da paleta do sistema para especificar cores; somente os índices lógicos de paleta são permitidos.

Os aplicativos podem modificar a maneira como os índices são mapeados definindo o membro **peFlags** da estrutura [**PaletteEntry**](/previous-versions//dd162769(v=vs.85)) para valores selecionados ao criar a paleta lógica. Por exemplo, o \_ sinalizador de DESrecolhimento do PC direciona o sistema para copiar imediatamente a cor solicitada para uma entrada da paleta do sistema não usada, independentemente de uma entrada da paleta do sistema já conter essa cor. Além disso, o \_ sinalizador PC Explicit direciona o sistema para mapear o índice de paleta lógica para um índice de paleta do sistema explicitamente determinado. (O aplicativo fornece o índice da paleta do sistema na palavra de ordem inferior da estrutura **PaletteEntry** .)

As paletas podem ser obtidas como uma paleta de plano de fundo ou uma paleta de primeiro plano especificando **true** ou **false** respectivamente para o parâmetro *bForceBackground* na função [**SelectPalette**](/windows/desktop/api/Wingdi/nf-wingdi-selectpalette) . Pode haver apenas uma paleta de primeiro plano no sistema de cada vez. Se a janela for a janela ativa no momento ou um descendente da janela ativa no momento, ela poderá obter uma paleta de primeiro plano. Caso contrário, a paleta será percebida como uma paleta de plano de fundo, independentemente do valor do parâmetro *bForceBackground* . A propriedade Critical de uma paleta de primeiro plano é que, quando realizada, ela pode substituir todas as entradas (exceto as entradas estáticas) na paleta do sistema. O sistema realiza isso marcando todas as entradas que não são estáticas na paleta do sistema como não utilizadas antes da realização de uma paleta de primeiro plano, eliminando assim todas as entradas usadas. Nenhum pré-processamento ocorre na paleta do sistema para uma realização de uma paleta de plano de fundo. A paleta de primeiro plano define todas as cores não estáticas possíveis. As paletas de plano de fundo podem definir apenas o que permanece aberto e são priorizadas de maneira primeiro, de primeira a chegar. Normalmente, os aplicativos usam paletas de plano de fundo para janelas filhas que percebem suas próprias paletas individuais. Isso ajuda a minimizar o número de alterações que ocorrem na paleta do sistema.

Uma entrada da paleta do sistema não usada é qualquer entrada que não esteja reservada e não contenha uma cor estática. As entradas reservadas são explicitamente marcadas com o \_ valor reservado do PC. Essas entradas são criadas quando um aplicativo percebe uma paleta lógica para a animação da paleta. As entradas de cores estáticas são criadas pelo sistema e correspondem às cores na paleta padrão. A função [**GetDeviceCaps**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) pode ser usada para recuperar o valor de NUMRESERVED, que especifica o número de entradas da paleta do sistema reservadas para cores estáticas.

Como a paleta do sistema tem um número limitado de entradas, a seleção e a realização de uma paleta lógica para um determinado dispositivo podem afetar as cores associadas a outras paletas lógicas para o mesmo dispositivo. Essas alterações de cor são especialmente dramáticas quando ocorrem na tela. Um aplicativo pode garantir que cores razoáveis sejam usadas para sua paleta lógica selecionada no momento, redefinindo a paleta antes de cada uso. Um aplicativo redefine a paleta chamando as funções [**unpercebeuobject**](/windows/desktop/api/Wingdi/nf-wingdi-unrealizeobject) e [**RealizePalette**](/windows/desktop/api/Wingdi/nf-wingdi-realizepalette) . O uso dessas funções faz com que o sistema Remapeie as cores na paleta lógica para cores razoáveis na paleta do sistema.

 

 
