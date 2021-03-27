---
description: Além da região de atualização, cada janela tem uma região visível que define a parte da janela visível para o usuário.
ms.assetid: 9d8beba1-93c0-437d-a138-76880a40bc79
title: Regiões da janela
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02555339412c604f79f69294febbab524fc92a70
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011410"
---
# <a name="window-regions"></a>Regiões da janela

Além da região de atualização, cada janela tem uma *região visível* que define a parte da janela visível para o usuário. O sistema altera a região visível para a janela sempre que a janela muda de tamanho ou sempre que outra janela é movida, de modo que ela obscurece ou expõe uma parte da janela. Os aplicativos não podem alterar a região visível diretamente, mas o sistema usa automaticamente a região visível para criar a região de recorte para qualquer contexto de dispositivo de exibição recuperado para a janela.

A *região de recorte* determina onde o sistema permite desenhar. Quando o aplicativo recupera um contexto de dispositivo de exibição usando a função [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint), [**GetDC**](/windows/desktop/api/Winuser/nf-winuser-getdc)ou [**GetDCEx**](/windows/desktop/api/Winuser/nf-winuser-getdcex) , o sistema define a região de recorte para o contexto do dispositivo para a interseção da região visível e a região de atualização. Os aplicativos podem alterar a região de recorte usando funções como [**SetWindowRgn**](/windows/desktop/api/Winuser/nf-winuser-setwindowrgn), [**SelectClipPath**](/windows/desktop/api/Wingdi/nf-wingdi-selectclippath) e [**SelectClipRgn**](/windows/desktop/api/Wingdi/nf-wingdi-selectcliprgn), para limitar ainda mais o desenho a uma parte específica da área de atualização.

Os \_ estilos WS CLIPCHILDREN e WS \_ CLIPSIBLINGS especificam ainda mais como o sistema calcula a região visível para uma janela. Se uma janela tiver um ou ambos os estilos, a região visível excluirá todas as janelas filhas ou irmãos (Windows com a mesma janela pai). Portanto, o desenho que, de outra forma, invasoria nessas janelas sempre será recortado.

 

 



