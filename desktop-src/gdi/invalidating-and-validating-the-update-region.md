---
description: Um aplicativo invalida uma parte de uma janela e define a região de atualização usando a função InvalidateRect ou InvalidateRgn.
ms.assetid: ec8abb77-47bc-4198-9daf-f2ccb0864ccc
title: Invalidando e validando a região de atualização
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ba895875f9ec1350b6eb28ccb8f1721df6999ce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967657"
---
# <a name="invalidating-and-validating-the-update-region"></a>Invalidando e validando a região de atualização

Um aplicativo invalida uma parte de uma janela e define a região de atualização usando a função [**InvalidateRect**](/windows/desktop/api/Winuser/nf-winuser-invalidaterect) ou [**InvalidateRgn**](/windows/desktop/api/Winuser/nf-winuser-invalidatergn) . Essas funções adicionam o retângulo ou a região especificada (em coordenadas do cliente) à região de atualização, combinando o retângulo ou a região com qualquer coisa que o sistema ou o aplicativo possa ter adicionado anteriormente à região de atualização.

As funções [**InvalidateRect**](/windows/desktop/api/Winuser/nf-winuser-invalidaterect) e [**InvalidateRgn**](/windows/desktop/api/Winuser/nf-winuser-invalidatergn) não geram mensagens do [**WM \_ Paint**](wm-paint.md) . Em vez disso, o sistema acumula as alterações feitas por essas funções e suas próprias alterações enquanto uma janela processa outras mensagens em sua fila de mensagens. Ao acumular alterações, uma janela processa todas as alterações de uma vez em vez de atualizar bits e partes uma etapa por vez.

As funções [**ValidateRect**](/windows/desktop/api/Winuser/nf-winuser-validaterect) e [**ValidateRgn**](/windows/desktop/api/Winuser/nf-winuser-validatergn) validam uma parte da janela removendo um retângulo ou uma região especificada da região de atualização. Essas funções normalmente são usadas quando a janela atualizou uma parte específica da tela na região de atualização antes de receber a mensagem de [**\_ pintura do WM**](wm-paint.md) .

 

 



