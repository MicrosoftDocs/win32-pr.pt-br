---
title: Permitindo que o usuário especifique dispositivos e arquivos
description: Permitindo que o usuário especifique dispositivos e arquivos
ms.assetid: cc542b56-c66e-4622-b2d1-505d31aab25b
keywords:
- Macro MCIWndOpenDialog
- Macro MCIWndOpen
- Macro MCIWndOpenInterface
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac4191f18409a1fb1f23ba3a2128b4aaed1b30e8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103636063"
---
# <a name="allowing-the-user-to-specify-devices-and-files"></a>Permitindo que o usuário especifique dispositivos e arquivos

Você pode associar um dispositivo ou arquivo a uma janela MCIWnd existente usando as macros [**MCIWndOpenDialog**](/windows/desktop/api/Vfw/nf-vfw-mciwndopendialog), [**MCIWndOpen**](/windows/desktop/api/Vfw/nf-vfw-mciwndopen)e [**MCIWndOpenInterface**](/windows/desktop/api/Vfw/nf-vfw-mciwndopeninterface) e a função [**GetOpenFileNamePreview**](/windows/desktop/api/Vfw/nf-vfw-getopenfilenamepreviewa) .

Para permitir que um usuário do seu aplicativo selecione um arquivo a ser reproduzido, use **MCIWndOpenDialog**. Essa macro exibe a caixa de diálogo **abrir** (mostrada na captura de tela a seguir) para escolher um arquivo e associar o arquivo selecionado à janela MCIWnd atual.

![imagem da janela MCIWnd](images/mciwnd3.gif)

Você pode permitir que um usuário do seu aplicativo selecione um arquivo a ser associado a uma janela do MCIWnd e visualize esse arquivo usando [**GetOpenFileNamePreview**](/windows/desktop/api/Vfw/nf-vfw-getopenfilenamepreviewa) e [**MCIWndOpen**](/windows/desktop/api/Vfw/nf-vfw-mciwndopen). A função **GetOpenFileNamePreview** exibe a caixa de diálogo **abrir** para escolher um arquivo e permite que o usuário visualize (reproduza) seu conteúdo. Quando o nome de um arquivo existente é especificado na caixa de diálogo, **GetOpenFileNamePreview** fornece um pequeno controle para permitir que o usuário visualize o conteúdo do arquivo. Você pode associar um arquivo especificado, selecionado com **GetOpenFileNamePreview** ou especificado de outra maneira, com uma janela MCIWnd usando **MCIWndOpen**.

Você também pode usar **MCIWndOpen** para especificar um dispositivo a ser associado a uma janela MCIWnd. Por exemplo, você pode usar um nome de dispositivo, como "CDAudio".

Para associar uma janela MCIWnd a uma interface de arquivo ou a uma interface de fluxo de dados a dados de multimídia, use a macro [**MCIWndOpenInterface**](/windows/desktop/api/Vfw/nf-vfw-mciwndopeninterface) . Para obter mais informações sobre interfaces de fluxo de dados e arquivo, consulte [funções e macros do avifile](avifile-functions-and-macros.md).

> [!Note]  
> Antes de associar um novo arquivo ou dispositivo a uma janela MCIWnd, o [**MCIWndOpenDialog**](/windows/desktop/api/Vfw/nf-vfw-mciwndopendialog) e o [**MCIWndOpen**](/windows/desktop/api/Vfw/nf-vfw-mciwndopen) fecham qualquer dispositivo atualmente associado à janela. Seu aplicativo não precisa fechar nenhum dispositivo aberto antes de usar essas macros.

 

 

 




