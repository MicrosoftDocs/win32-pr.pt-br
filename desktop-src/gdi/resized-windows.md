---
description: O sistema altera o tamanho de uma janela quando o usuário escolhe comandos de menu de janela, como Tamanho e Maximizar, ou quando o aplicativo chama funções, como a função SetWindowPos.
ms.assetid: 6f997cba-e4c9-4e27-8309-42b9892ec620
title: Resized Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9efd6f71d1657c0d01b3df9101fc15fa35f54ecfc01b1588b696cd9110dad317
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119602716"
---
# <a name="resized-windows"></a>Resized Windows

O sistema altera o tamanho de uma janela quando o usuário escolhe comandos de menu de janela, como Tamanho e Maximizar, ou quando o aplicativo chama funções, como a [**função SetWindowPos.**](/windows/win32/api/winuser/nf-winuser-setwindowpos) Quando uma janela altera o tamanho, o sistema assume que o conteúdo da parte exposta anteriormente da janela não é afetado e não precisa ser redesenhado. O sistema invalida apenas a parte recém-exposta da janela, o que economiza tempo quando a mensagem [**WM \_ PAINT**](wm-paint.md) eventual é processada pelo aplicativo. Nesse caso, **WM \_ PAINT** não é gerado quando o tamanho da janela é reduzido.

Para algumas janelas, qualquer alteração no tamanho da janela invalida o conteúdo. Por exemplo, um aplicativo de relógio que adapta a face do relógio para se ajustar perfeitamente em sua janela deve redesenhar o relógio sempre que a janela mudar de tamanho. Para forçar o sistema a invalidar toda a área de cliente da janela quando uma alteração vertical, horizontal ou vertical e horizontal é feita, um aplicativo deve especificar o estilo \_ CS VREDRAW ou CS HREDRAW ou ambos, ao registrar a classe \_ de janela. Qualquer janela que pertença a uma classe de janela que tenha esses estilos é invalidada sempre que o usuário ou o aplicativo altera o tamanho da janela.

 

 
