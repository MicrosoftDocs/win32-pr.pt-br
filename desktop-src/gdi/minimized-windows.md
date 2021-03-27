---
description: O sistema reduz a janela principal de um aplicativo (estilo sobreposto) a uma janela minimizada quando o usuário clica em minimizar no menu janela ou o aplicativo chama a função de janela e especifica um valor como a \_ minimização do SW.
ms.assetid: a52dba49-e4ec-45e2-a00f-211a58e28773
title: Janelas minimizadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c792a90dba2526b6d09fabf8281fc74ebfe96667
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103661601"
---
# <a name="minimized-windows"></a>Janelas minimizadas

O sistema reduz a janela principal de um aplicativo (estilo sobreposto) a uma janela minimizada quando o usuário clica em minimizar no menu janela ou o aplicativo chama a função de [**janela**](/windows/win32/api/winuser/nf-winuser-showwindow) e especifica um valor como a \_ minimização do SW. Minimizar uma janela acelera o desempenho do sistema reduzindo a quantidade de trabalho que um aplicativo deve fazer ao atualizar sua janela principal.

Para um aplicativo típico, o sistema desenha um ícone, chamado de ícone de classe, quando a janela é minimizada, rotulando o ícone com o nome da janela. O ícone de classe, uma imagem estática que representa o aplicativo, é especificado pelo aplicativo quando registra a classe de janela. O aplicativo atribui um identificador ao ícone de classe para o membro **HICON** de [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) antes de chamar [**registerClass**](/windows/win32/api/winuser/nf-winuser-registerclassa). O aplicativo pode usar a função [**LoadIcon**](/windows/win32/api/winuser/nf-winuser-loadicona) para recuperar o identificador de ícone.

 

 
