---
description: Um aplicativo obtém um controlador de domínio de exibição chamando a função BeginPaint, GetDC ou GetDCEx e identificando a janela na qual a saída correspondente aparecerá.
ms.assetid: 8f952d68-ee52-4e63-9f09-80a14c755d31
title: Exibir contextos de dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41d0eeb3055209ad99a6a50fd129f9f9c064bf52
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103661618"
---
# <a name="display-device-contexts"></a>Exibir contextos de dispositivo

Um aplicativo obtém um controlador de domínio de exibição chamando a função [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint), [**GetDC**](/windows/desktop/api/Winuser/nf-winuser-getdc)ou [**GetDCEx**](/windows/desktop/api/Winuser/nf-winuser-getdcex) e identificando a janela na qual a saída correspondente aparecerá. Normalmente, um aplicativo obtém um controlador de domínio de exibição somente quando ele deve desenhar na área do cliente. No entanto, uma pode obter um [contexto de dispositivo de janela](#window-device-contexts) chamando a função [**GetWindowDC**](/windows/desktop/api/Winuser/nf-winuser-getwindowdc) . Quando o desenho do aplicativo é concluído, ele deve liberar o controlador de domínio chamando a função [**Endpaintt**](/windows/desktop/api/Winuser/nf-winuser-endpaint) ou [**ReleaseDC**](/windows/desktop/api/Winuser/nf-winuser-releasedc) .

Há cinco tipos de DCs para vídeos de vídeo:

-   Classe
-   Comum
-   Privados
-   Janela
-   Pai

## <a name="class-device-contexts"></a>Contextos de dispositivo de classe

Os *contextos de dispositivo de classe* têm suporte estritamente para compatibilidade com versões de 16 bits do Windows. Ao escrever seu aplicativo, evite usar o contexto de dispositivo de classe; em vez disso, use um contexto de dispositivo privado.

## <a name="common-device-contexts"></a>Contextos de dispositivo comuns

*Contextos de dispositivo comuns* são DCS de exibição mantidos em um cache especial pelo sistema. Contextos de dispositivo comuns são usados em aplicativos que executam operações de desenho infrequentes. Antes que o sistema retorne o identificador de DC, ele inicializa o contexto de dispositivo comum com objetos, atributos e modos padrão. Todas as operações de desenho executadas pelo aplicativo usam esses padrões, a menos que uma das funções GDI seja chamada para selecionar um novo objeto, alterar os atributos de um objeto existente ou selecionar um novo modo.

Como há apenas um número limitado de contextos de dispositivo comuns, um aplicativo deve liberá-los após a conclusão do desenho. Quando o aplicativo libera um contexto de dispositivo comum, todas as alterações nos dados padrão são perdidas.

## <a name="private-device-contexts"></a>Contextos de dispositivo privado

*Contextos de dispositivo privado* são DCS que, ao contrário de contextos de dispositivo comuns, mantêm quaisquer alterações nos dados padrão mesmo depois que um aplicativo os libera. Contextos de dispositivo privado são usados em aplicativos que executam várias operações de desenho, como aplicativos de projeto auxiliados por computador (CAD), aplicativos de publicação de área de trabalho, aplicativos de desenho e pintura e assim por diante. Os contextos de dispositivo privado não fazem parte do cache do sistema e, portanto, não precisam ser liberados após o uso. O sistema removerá automaticamente um contexto de dispositivo privado depois que a última janela dessa classe tiver sido destruída.

Um aplicativo cria um contexto de dispositivo privado, primeiro especificando o \_ estilo de classe de janela cs OWNDC quando Inicializa o membro **Style** da estrutura [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) e chama a função [**registerClass**](/windows/win32/api/winuser/nf-winuser-registerclassa) . (Para obter mais informações sobre classes de janela, consulte [classes de janela](../winmsg/window-classes.md).)

Depois de criar uma janela com o \_ estilo cs OWNDC, um aplicativo pode chamar a função [**GetDC**](/windows/desktop/api/Winuser/nf-winuser-getdc), [**GetDCEx**](/windows/desktop/api/Winuser/nf-winuser-getdcex)ou [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint) uma vez para obter um identificador que identifica um contexto de dispositivo privado. O aplicativo pode continuar usando esse identificador (e o DC associado) até que ele exclua a janela criada com essa classe. Todas as alterações em objetos gráficos e seus atributos, ou modos gráficos, são mantidas pelo sistema até que a janela seja excluída.

## <a name="window-device-contexts"></a>Contextos de dispositivo de janela

Um *contexto de dispositivo de janela* permite que um aplicativo desenhe em qualquer lugar em uma janela, incluindo a área não cliente. Os contextos de dispositivo de janela normalmente são usados por aplicativos que processam as mensagens do [**WM \_ NCPAINT**](wm-ncpaint.md) e do [**WM \_ NCACTIVATE**](../winmsg/wm-ncactivate.md) para Windows com áreas personalizadas que não são do cliente. O uso de um contexto de dispositivo de janela não é recomendado para nenhuma outra finalidade. Para obter mais informações, consulte [**GetWindowDC**](/windows/desktop/api/Winuser/nf-winuser-getwindowdc).

## <a name="parent-device-contexts"></a>Contextos de dispositivo pai

Um *contexto de dispositivo pai* permite que um aplicativo minimize o tempo necessário para configurar a região de recorte para uma janela. Um aplicativo normalmente usa contextos de dispositivo pai para acelerar o desenho de janelas de controle sem a necessidade de um contexto de dispositivo privado ou de classe. Por exemplo, o sistema usa contextos de dispositivo pai para botão de ação e controles de edição. Os contextos de dispositivo pai destinam-se ao uso somente com janelas filhas, nunca com janelas de nível superior ou pop-up. Para obter mais informações, consulte [contextos de dispositivo de exibição pai](parent-display-device-contexts.md).

 

 
