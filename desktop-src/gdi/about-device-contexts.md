---
description: A independência do dispositivo é um dos principais recursos do Microsoft Windows.
ms.assetid: f2a4c4cf-55e9-4129-8067-256552af49d2
title: Sobre contextos de dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9439e3091b3138917e24ab4a49ff89c21a1e1b53480d4a138bd2bbad3288fcd0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119105871"
---
# <a name="about-device-contexts"></a>Sobre contextos de dispositivo

A independência do dispositivo é um dos principais recursos do Microsoft Windows. Os aplicativos podem desenhar e imprimir a saída em uma variedade de dispositivos. O software que dá suporte a essa independência de dispositivo está contido em duas bibliotecas de vínculo dinâmico. O primeiro, Gdi.dll, é chamado de interface de dispositivo de gráficos (GDI); o segundo é conhecido como um driver de dispositivo. O nome do segundo depende do dispositivo em que o aplicativo desenha a saída. Por exemplo, se o aplicativo desenhar a saída na área do cliente de sua janela em uma tela VGA, essa biblioteca será Vga.dll; Se o aplicativo imprimir a saída em uma impressora Epson FX-80, essa biblioteca será Epson9.dll.

Um aplicativo deve informar a GDI para carregar um driver de dispositivo específico e, depois que o driver for carregado, para preparar o dispositivo para operações de desenho (como selecionar uma cor e uma largura de linha, um padrão de pincel e uma cor, um tipo de fonte, uma região de recorte e assim por diante). Essas tarefas são realizadas criando e mantendo um contexto de dispositivo (DC). Um DC é uma estrutura que define um conjunto de objetos gráficos e seus atributos associados e os modos gráficos que afetam a saída. Os objetos gráficos incluem uma caneta para desenho de linha, um pincel para pintar e preencher, um bitmap para copiar ou rolar partes da tela, uma paleta para definir o conjunto de cores disponíveis, uma região para recorte e outras operações e um caminho para operações de pintura e de desenho. Ao contrário da maioria das estruturas, um aplicativo nunca tem acesso direto ao controlador de domínio; em vez disso, ele opera na estrutura indiretamente chamando várias funções.

Esta visão geral fornece informações sobre os seguintes tópicos:

-   [Objetos gráficos](graphic-objects.md)
-   [Modos gráficos](graphic-modes.md)
-   [Tipos de contexto do dispositivo](device-context-types.md)
-   [Operações de contexto do dispositivo](device-context-operations.md)
-   [funções de contexto de dispositivo habilitadas para ICM](icm-enabled-device-context-functions.md)

Um conceito importante é o layout de um controlador de domínio ou de uma janela, que descreve a ordem na qual os objetos GDI e o texto são revelados (da esquerda para a direita ou da direita para a esquerda). Para obter mais informações, consulte "layout e espelhamento de janela" em [**recursos de janela**](../winmsg/window-features.md) e as funções [**GetLayout**](/windows/desktop/api/Wingdi/nf-wingdi-getlayout) e [**SetLayout**](/windows/desktop/api/Wingdi/nf-wingdi-setlayout) .

 

 
