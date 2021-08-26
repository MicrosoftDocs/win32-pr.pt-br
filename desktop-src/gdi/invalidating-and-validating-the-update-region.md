---
description: Um aplicativo invalida uma parte de uma janela e define a região de atualização usando a função InvalidateRect ou InvalidateRgn.
ms.assetid: ec8abb77-47bc-4198-9daf-f2ccb0864ccc
title: Invalidando e validando a região de atualização
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6813d88674ef0339cfd3501b561e5a7c95fa5b41f0c7f212e625f9846f5beb5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119944166"
---
# <a name="invalidating-and-validating-the-update-region"></a>Invalidando e validando a região de atualização

Um aplicativo invalida uma parte de uma janela e define a região de atualização usando a [**função InvalidateRect**](/windows/desktop/api/Winuser/nf-winuser-invalidaterect) [**ou InvalidateRgn.**](/windows/desktop/api/Winuser/nf-winuser-invalidatergn) Essas funções adicionam o retângulo ou a região especificada (nas coordenadas do cliente) à região de atualização, combinando o retângulo ou a região com qualquer coisa que o sistema ou o aplicativo possa ter adicionado anteriormente à região de atualização.

As [**funções InvalidateRect**](/windows/desktop/api/Winuser/nf-winuser-invalidaterect) [**e InvalidateRgn**](/windows/desktop/api/Winuser/nf-winuser-invalidatergn) não geram [**mensagens WM \_ PAINT.**](wm-paint.md) Em vez disso, o sistema acumula as alterações feitas por essas funções e suas próprias alterações enquanto uma janela processa outras mensagens em sua fila de mensagens. Ao acumular alterações, uma janela processa todas as alterações de uma vez, em vez de atualizar bits e partes uma etapa por vez.

As [**funções ValidateRect**](/windows/desktop/api/Winuser/nf-winuser-validaterect) e [**ValidateRgn**](/windows/desktop/api/Winuser/nf-winuser-validatergn) validam uma parte da janela removendo um retângulo ou região especificado da região de atualização. Essas funções normalmente são usadas quando a janela atualiza uma parte específica da tela na região de atualização antes de receber a [**mensagem WM \_ PAINT.**](wm-paint.md)

 

 



