---
description: O sistema reduz a janela principal de um aplicativo (estilo sobreposto) a uma janela minimizada quando o usuário clica em Minimizar no menu da janela ou o aplicativo chama a função ShowWindow e especifica um valor como SW \_ MINIMIZE.
ms.assetid: a52dba49-e4ec-45e2-a00f-211a58e28773
title: Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d9633c3bcba452e4708c6a48557fe547eff03c4e2a6801e3669da2faa768272
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118760026"
---
# <a name="minimized-windows"></a>Windows

O sistema reduz a janela principal de um aplicativo (estilo sobreposto) a uma janela minimizada quando o usuário clica em Minimizar no menu da janela ou o aplicativo chama a [**função ShowWindow**](/windows/win32/api/winuser/nf-winuser-showwindow) e especifica um valor como SW \_ MINIMIZE. Minimizar uma janela acelera o desempenho do sistema reduzindo a quantidade de trabalho que um aplicativo deve fazer ao atualizar sua janela principal.

Para um aplicativo típico, o sistema desenha um ícone, chamado de ícone de classe, quando a janela é minimizada, rotulando o ícone com o nome da janela. O ícone de classe, uma imagem estática que representa o aplicativo, é especificado pelo aplicativo quando ele registra a classe de janela. O aplicativo atribui um handle ao ícone de classe ao membro **hIcon** do [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) antes de [**chamar RegisterClass**](/windows/win32/api/winuser/nf-winuser-registerclassa). O aplicativo pode usar a [**função LoadIcon**](/windows/win32/api/winuser/nf-winuser-loadicona) para recuperar o controle de ícone.

 

 
