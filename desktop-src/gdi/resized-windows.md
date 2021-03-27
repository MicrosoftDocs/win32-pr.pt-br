---
description: O sistema altera o tamanho de uma janela quando o usuário escolhe comandos de menu da janela, como tamanho e maximizar, ou quando o aplicativo chama funções, como a função SetWindowPos.
ms.assetid: 6f997cba-e4c9-4e27-8309-42b9892ec620
title: Janelas redimensionadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88f740191f8b85038f17a687ebc547305f882383
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827643"
---
# <a name="resized-windows"></a>Janelas redimensionadas

O sistema altera o tamanho de uma janela quando o usuário escolhe comandos de menu da janela, como tamanho e maximizar, ou quando o aplicativo chama funções, como a função [**SetWindowPos**](/windows/win32/api/winuser/nf-winuser-setwindowpos) . Quando uma janela muda de tamanho, o sistema assume que o conteúdo da parte exposta anteriormente da janela não é afetado e não precisa ser redesenhado. O sistema invalida apenas a parte recentemente exposta da janela, o que poupa tempo quando a mensagem eventual de [**\_ pintura do WM**](wm-paint.md) é processada pelo aplicativo. Nesse caso, o **WM \_ Paint** não é gerado quando o tamanho da janela é reduzido.

Para algumas janelas, qualquer alteração no tamanho da janela invalida o conteúdo. Por exemplo, um aplicativo de relógio que adapte a face do relógio para se ajustar perfeitamente dentro de sua janela deve redesenhar o relógio sempre que a janela mudar de tamanho. Para forçar o sistema a invalidar toda a área do cliente da janela quando uma alteração vertical, horizontal ou vertical e horizontal for feita, um aplicativo deverá especificar o \_ estilo cs VREDRAW ou cs \_ HREDRAW, ou ambos, ao registrar a classe Window. Qualquer janela pertencente a uma classe de janela que tenha esses estilos é invalidada sempre que o usuário ou o aplicativo altera o tamanho da janela.

 

 
