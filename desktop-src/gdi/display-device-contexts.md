---
description: Um aplicativo obtém um DC de exibição chamando a função BeginPaint, GetDC ou GetDCEx e identificando a janela na qual a saída correspondente será exibida.
ms.assetid: 8f952d68-ee52-4e63-9f09-80a14c755d31
title: Exibir contextos de dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e2e2bbd847d1a473ff08de7db52da7513b91377e8a891b2c6fdde04a82bf1d0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118761318"
---
# <a name="display-device-contexts"></a>Exibir contextos de dispositivo

Um aplicativo obtém um DC de exibição chamando a função [**BeginPaint,**](/windows/desktop/api/Winuser/nf-winuser-beginpaint) [**GetDC**](/windows/desktop/api/Winuser/nf-winuser-getdc) [**ou GetDCEx**](/windows/desktop/api/Winuser/nf-winuser-getdcex) e identificando a janela na qual a saída correspondente será exibida. Normalmente, um aplicativo obtém um DC de exibição somente quando precisa desenhar na área do cliente. No entanto, é possível obter um [contexto de dispositivo de janela](#window-device-contexts) chamando a função [**GetWindowDC.**](/windows/desktop/api/Winuser/nf-winuser-getwindowdc) Quando o aplicativo terminar de desenhar, ele deverá liberar o DC chamando a [**função EndPaint**](/windows/desktop/api/Winuser/nf-winuser-endpaint) ou [**ReleaseDC.**](/windows/desktop/api/Winuser/nf-winuser-releasedc)

Há cinco tipos de DCs para exibições de vídeo:

-   Classe
-   Comum
-   Privados
-   Janela
-   Pai

## <a name="class-device-contexts"></a>Contextos de dispositivo de classe

*Os contextos de dispositivo de* classe têm suporte estritamente para compatibilidade com versões de 16 bits do Windows. Ao escrever seu aplicativo, evite usar o contexto do dispositivo de classe; em vez disso, use um contexto de dispositivo privado.

## <a name="common-device-contexts"></a>Contextos comuns do dispositivo

*Contextos de dispositivo comuns* são os DCs de exibição mantidos em um cache especial pelo sistema. Contextos de dispositivo comuns são usados em aplicativos que executam operações de desenho pouco frequentes. Antes que o sistema retorne o handle dc, ele inicializa o contexto de dispositivo comum com objetos, atributos e modos padrão. Todas as operações de desenho executadas pelo aplicativo usam esses padrões, a menos que uma das funções GDI seja chamada para selecionar um novo objeto, alterar os atributos de um objeto existente ou selecionar um novo modo.

Como há apenas um número limitado de contextos de dispositivo comuns, um aplicativo deve liberá-los depois de terminar o desenho. Quando o aplicativo libera um contexto de dispositivo comum, todas as alterações nos dados padrão são perdidas.

## <a name="private-device-contexts"></a>Contextos de dispositivo privado

*Os contextos de dispositivo privado* são exibir DCs que, ao contrário dos contextos comuns do dispositivo, retêm as alterações nos dados padrão mesmo depois que um aplicativo as libera. Os contextos de dispositivo privado são usados em aplicativos que executam várias operações de desenho, como aplicativos CAD (design auxiliado por computador), aplicativos de publicação de área de trabalho, desenho e pintura de aplicativos e assim por diante. Os contextos de dispositivo privado não fazem parte do cache do sistema e, portanto, não precisam ser liberados após o uso. O sistema remove automaticamente um contexto de dispositivo privado após a última janela dessa classe ter sido destruída.

Um aplicativo cria um contexto de dispositivo privado especificando primeiro o estilo da classe de janela CS OWNDC quando inicializa o membro de estilo da estrutura WNDCLASS e chama a \_ [**função RegisterClass.**](/windows/win32/api/winuser/nf-winuser-registerclassa)  [](/windows/win32/api/winuser/ns-winuser-wndclassa) (Para obter mais informações sobre classes de janela, consulte [Classes de janela](../winmsg/window-classes.md).)

Depois de criar uma janela com o estilo OWNDC do CS, um aplicativo pode chamar a função \_ [**GetDC,**](/windows/desktop/api/Winuser/nf-winuser-getdc) [**GetDCEx**](/windows/desktop/api/Winuser/nf-winuser-getdcex)ou [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint) uma vez para obter um identificador que identifica um contexto de dispositivo privado. O aplicativo pode continuar usando esse handle (e o DC associado) até excluir a janela criada com essa classe. Todas as alterações em objetos gráficos e seus atributos ou modos gráficos são mantidas pelo sistema até que a janela seja excluída.

## <a name="window-device-contexts"></a>Contextos de dispositivo de janela

Um *contexto de dispositivo de* janela permite que um aplicativo desenhe em qualquer lugar em uma janela, incluindo a área não dependente. Os contextos de dispositivo de janela normalmente são usados por aplicativos que processam as mensagens [**WM \_ NCPAINT**](wm-ncpaint.md) e [**WM \_ NCACTIVATE**](../winmsg/wm-ncactivate.md) para janelas com áreas não dependentes personalizadas. O uso de um contexto de dispositivo de janela não é recomendado para nenhuma outra finalidade. Para obter mais informações; consulte [**GetWindowDC**](/windows/desktop/api/Winuser/nf-winuser-getwindowdc).

## <a name="parent-device-contexts"></a>Contextos do dispositivo pai

Um *contexto de dispositivo* pai permite que um aplicativo minimize o tempo necessário para configurar a região de recorte para uma janela. Um aplicativo normalmente usa contextos de dispositivo pai para acelerar o desenho para janelas de controle sem exigir um contexto de dispositivo particular ou de classe. Por exemplo, o sistema usa contextos de dispositivo pai para controles de edição e botão de push. Os contextos de dispositivo pai destinam-se a uso somente com janelas filho, nunca com janelas pop-up ou de nível superior. Para obter mais informações; consulte [Contextos de dispositivo de exibição pai.](parent-display-device-contexts.md)

 

 
