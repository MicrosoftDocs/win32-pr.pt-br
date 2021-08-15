---
title: Gerar funções de retorno de chamada
description: Gerar funções de retorno de chamada
ms.assetid: 8c9b43ea-fdba-41a2-ba2d-1eaa4516e14f
keywords:
- Funções de retorno de chamada AVICap, yield
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e87a3c986378bee05078b8cab28a0647827a1102ef1809558a47dcd5123af2e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118369130"
---
# <a name="yield-callback-functions"></a>Gerar funções de retorno de chamada

Os aplicativos podem usar funções de retorno de chamada yield durante a captura de streaming. (Uma função yield callback normalmente consiste em um loop de mensagem que chama [PeekMessage](/windows/win32/api/winuser/nf-winuser-peekmessagea), [TranslateMessage](/windows/win32/api/winuser/nf-winuser-translatemessage)e [DispatchMessage](/windows/win32/api/winuser/nf-winuser-dispatchmessage).) A janela de captura chama a função de retorno de chamada yield pelo menos uma vez para cada quadro de vídeo capturado, mas a taxa exata depende da taxa de quadros e da sobrecarga do driver de captura e do disco.

 

 