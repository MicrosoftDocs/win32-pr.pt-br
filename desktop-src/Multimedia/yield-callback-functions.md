---
title: Gerar funções de retorno de chamada
description: Gerar funções de retorno de chamada
ms.assetid: 8c9b43ea-fdba-41a2-ba2d-1eaa4516e14f
keywords:
- Funções de retorno de chamada AVICap, yield
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3666ea24a1d37402ffc13c09ca8ab95fcd19e1f7
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103640738"
---
# <a name="yield-callback-functions"></a>Gerar funções de retorno de chamada

Os aplicativos podem usar funções de retorno de chamada yield durante a captura de streaming. (Uma função yield callback normalmente consiste em um loop de mensagem que chama [PeekMessage](/windows/win32/api/winuser/nf-winuser-peekmessagea), [TranslateMessage](/windows/win32/api/winuser/nf-winuser-translatemessage)e [DispatchMessage](/windows/win32/api/winuser/nf-winuser-dispatchmessage).) A janela de captura chama a função de retorno de chamada yield pelo menos uma vez para cada quadro de vídeo capturado, mas a taxa exata depende da taxa de quadros e da sobrecarga do driver de captura e do disco.

 

 