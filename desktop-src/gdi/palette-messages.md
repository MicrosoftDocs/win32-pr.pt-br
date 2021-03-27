---
description: As alterações na paleta do sistema para o dispositivo de vídeo podem ter efeitos expressivos e, às vezes, indesejáveis sobre as cores usadas no Windows na área de trabalho.
ms.assetid: 9c470b6f-c0d3-462e-9649-1f39b06bd543
title: Mensagens da paleta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f19a5458ec89d8d9a0524fd2ec383de740c0179
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967625"
---
# <a name="palette-messages"></a>Mensagens da paleta

As alterações na paleta do sistema para o dispositivo de vídeo podem ter efeitos expressivos e, às vezes, indesejáveis sobre as cores usadas no Windows na área de trabalho. Para minimizar o impacto dessas alterações, o sistema fornece um conjunto de mensagens que ajudam os aplicativos a gerenciar suas paletas lógicas, garantindo que as cores na janela ativa fiquem o mais próximas possível das cores pretendidas.

O sistema envia uma mensagem do [**WM \_ QUERYNEWPALETTE**](wm-querynewpalette.md) para uma janela de nível superior ou sobreposto logo antes de ativar a janela. Essa mensagem dá a um aplicativo a oportunidade de selecionar e perceber sua paleta lógica para que ela receba o melhor mapeamento possível de cores para sua paleta lógica. Quando o aplicativo recebe a mensagem, ele deve usar as funções [**SelectPalette**](/windows/desktop/api/Wingdi/nf-wingdi-selectpalette), [**unpercebidoobject**](/windows/desktop/api/Wingdi/nf-wingdi-unrealizeobject)e [**RealizePalette**](/windows/desktop/api/Wingdi/nf-wingdi-realizepalette) para selecionar e perceber a paleta lógica. Fazer isso direciona o sistema para atualizar as cores na paleta do sistema para que suas cores correspondam ao máximo de cores na paleta lógica.

Quando um aplicativo faz alterações na paleta do sistema como resultado da realização de sua paleta lógica, o sistema envia uma mensagem da [**\_ paleta do WM**](wm-palettechanged.md) para todas as janelas de nível superior e sobreposto. Essa mensagem dá aos aplicativos a oportunidade de atualizar as cores nas áreas do cliente de suas janelas, substituindo as cores que foram alteradas com cores que correspondem mais às cores pretendidas. Um aplicativo que recebe a mensagem de **\_ paletachanged do WM** deve usar [**unpercebeuobject**](/windows/desktop/api/Wingdi/nf-wingdi-unrealizeobject) e [**RealizePalette**](/windows/desktop/api/Wingdi/nf-wingdi-realizepalette) para redefinir as paletas lógicas associadas a todas as janelas inativas e, em seguida, atualizar as cores na área do cliente para cada janela inativa usando a função [**UpdateColors**](/windows/desktop/api/Wingdi/nf-wingdi-updatecolors) . Essa técnica não garante o maior número de correspondências exatas de cor; no entanto, ele garante que as cores na paleta lógica sejam mapeadas para cores razoáveis na paleta do sistema.

> [!Note]  
> Para evitar a criação de um loop infinito, um aplicativo nunca deve perceber a paleta da janela cujo identificador corresponde ao identificador passado no parâmetro *wParam* da mensagem [**da \_ paleta do WM**](wm-palettechanged.md) .

 

A função [**UpdateColors**](/windows/desktop/api/Wingdi/nf-wingdi-updatecolors) normalmente atualiza uma área do cliente de uma janela inativa mais rapidamente do que redesenhar a área. No entanto, como **UpdateColors** executa a tradução de cores com base na cor de cada pixel antes da alteração da paleta do sistema, cada chamada para essa função resulta na perda de alguma precisão de cor. Isso significa que **UpdateColors** não pode ser usado para atualizar cores quando a janela se torna ativa. Nesses casos, o aplicativo deve redesenhar a área do cliente.

O sistema pode enviar a mensagem do [**WM \_ QUERYNEWPALETTE**](wm-querynewpalette.md) quando forem feitas alterações na paleta lógica. Além disso, o sistema pode enviar a mensagem do [**WM \_ PALETTEISCHANGING**](wm-paletteischanging.md) para todas as janelas de nível superior e Overlapped quando a paleta do sistema está prestes a ser alterada.

 

 



