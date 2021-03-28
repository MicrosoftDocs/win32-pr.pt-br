---
description: Um bloqueio de atualização de janela é uma suspensão temporária de desenho em uma janela.
ms.assetid: 92b1ba04-ff79-4a37-9633-99412cdafe95
title: Bloqueio de atualização de janela
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4897915020134387947c7a77009c4bdbd63cfdd6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104169131"
---
# <a name="window-update-lock"></a>Bloqueio de atualização de janela

Um *bloqueio de atualização de janela* é uma suspensão temporária de desenho em uma janela. O sistema usa o bloqueio para impedir que outras janelas sejam desenhadas no retângulo de controle sempre que o usuário move ou dimensiona uma janela. Os aplicativos podem usar o bloqueio para evitar o desenho se executarem operações de movimentação ou de dimensionamento semelhantes com suas próprias janelas.

Um aplicativo usa a função [**LockWindowUpdate**](/windows/desktop/api/Winuser/nf-winuser-lockwindowupdate) para definir ou limpar um bloqueio de atualização de janela, especificando a janela a ser bloqueada. O bloqueio se aplica à janela especificada e a todas as suas janelas filhas. Quando o bloqueio é definido, as funções [**GetDC**](/windows/desktop/api/Winuser/nf-winuser-getdc) e [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint) retornam um contexto de dispositivo de exibição com uma região visível que está vazia. Considerando isso, o aplicativo pode continuar a desenhar na janela, mas toda a saída é recortada. O bloqueio persiste até que o aplicativo o apague chamando **LockWindowUpdate**, especificando **NULL** para a janela. Embora **LockWindowUpdate** force a região visível de uma janela a ficar vazia, a função não torna a janela especificada invisível e não limpa o bit de \_ estilo WS visível.

Depois que o bloqueio é definido, o aplicativo pode usar a função [**GetDCEx**](/windows/desktop/api/Winuser/nf-winuser-getdcex) , com o \_ valor de LOCKWINDOWUPDATE do DCX, para recuperar um contexto de dispositivo de exibição para desenhar sobre a janela bloqueada. Isso permite que o aplicativo desenhe um retângulo de controle ao processar mensagens de teclado ou mouse. O sistema usa esse método quando o usuário move e dimensiona janelas. **GetDCEx** recupera o contexto do dispositivo de vídeo do cache de contexto do dispositivo de vídeo, de modo que o aplicativo deve liberar o contexto do dispositivo assim que possível após o desenho.

Enquanto um bloqueio de atualização de janela é definido, o sistema cria um retângulo delimitador acumulado para cada janela bloqueada. Quando o bloqueio é eliminado, o sistema usa esse retângulo delimitador para definir a região de atualização para a janela e suas janelas filhas, forçando uma eventual mensagem de [**\_ pintura do WM**](wm-paint.md) . Se o retângulo delimitador acumulado estiver vazio (ou seja, se nenhum desenho tiver ocorrido enquanto o bloqueio foi definido), a região de atualização não será definida.

 

 



