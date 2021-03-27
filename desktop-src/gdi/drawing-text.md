---
description: Texto de desenho
ms.assetid: 8a06f659-4e08-4738-b7a9-956b599c1344
title: Texto de desenho (GDI do Windows)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7db44a756ff211bcae7605cb87bdac77005b34f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103661612"
---
# <a name="drawing-text-windows-gdi"></a>Texto de desenho (GDI do Windows)

Depois que um aplicativo seleciona a fonte apropriada, define as opções de formatação de texto necessárias e computa os valores necessários de largura e altura de caractere para uma cadeia de texto, ele pode começar a desenhar caracteres e símbolos chamando qualquer uma das funções de saída de texto:

-   [DrawText](/windows/desktop/api/Winuser/nf-winuser-drawtext)
-   [DrawTextEx](/windows/desktop/api/Winuser/nf-winuser-drawtextexa)
-   [ExtTextOut](/windows/desktop/api/Wingdi/nf-wingdi-exttextouta)
-   [Semitextoout](/windows/desktop/api/Wingdi/nf-wingdi-polytextouta)
-   [TabbedTextOut](/windows/desktop/api/Winuser/nf-winuser-tabbedtextouta)
-   [Texto](/windows/desktop/api/Wingdi/nf-wingdi-textouta)

Quando um aplicativo chama uma dessas funções, o sistema operacional passa a chamada para o mecanismo de gráficos que, por sua vez, passa a chamada para o driver de dispositivo apropriado. No nível de driver de dispositivo, todas essas chamadas têm suporte por uma ou mais chamadas para a própria função [ExtTextOut](/windows/desktop/api/Wingdi/nf-wingdi-exttextouta) ou [TextOut](/windows/desktop/api/Wingdi/nf-wingdi-textouta) do driver. Um aplicativo obterá a execução mais rápida chamando [**ExtTextOut**](/windows/win32/api/wingdi/nf-wingdi-exttextouta), que é rapidamente convertido em uma chamada **ExtTextOut** para o dispositivo. No entanto, há instâncias em que um aplicativo deve chamar uma das outras três funções; por exemplo, para desenhar várias linhas de texto dentro das bordas de uma região retangular especificada, é mais eficiente chamar [**DrawText**](/windows/win32/api/winuser/nf-winuser-drawtext). Para criar uma tabela de várias colunas com colunas justificadas de texto, é mais eficiente chamar [**TabbedTextOut**](/windows/win32/api/winuser/nf-winuser-tabbedtextouta).

 

 
