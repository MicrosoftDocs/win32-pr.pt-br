---
description: Além da região de atualização, cada janela tem uma região visível que define a parte da janela visível para o usuário.
ms.assetid: 9d8beba1-93c0-437d-a138-76880a40bc79
title: Regiões de janela
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac3f751303d8a971d010ea7dabf7604c24db892f88d9a4029f0189d303cf5a80
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119727406"
---
# <a name="window-regions"></a>Regiões de janela

Além da região de atualização, cada janela tem uma região *visível* que define a parte da janela visível para o usuário. O sistema altera a região visível para a janela sempre que a janela altera o tamanho ou sempre que outra janela é movida, de forma que obscureça ou exponha uma parte da janela. Os aplicativos não podem alterar a região visível diretamente, mas o sistema usa automaticamente a região visível para criar a região de recorte para qualquer contexto de dispositivo de exibição recuperado para a janela.

A *região de recorte* determina onde o sistema permite o desenho. Quando o aplicativo recupera um contexto de dispositivo de exibição usando a função [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint), [**GetDC**](/windows/desktop/api/Winuser/nf-winuser-getdc) [**ou GetDCEx,**](/windows/desktop/api/Winuser/nf-winuser-getdcex) o sistema define a região de recorte para o contexto do dispositivo para a interseção da região visível e da região de atualização. Os aplicativos podem alterar a região de recorte usando funções como [**SetWindowRgn,**](/windows/desktop/api/Winuser/nf-winuser-setwindowrgn) [**SelectClipPath**](/windows/desktop/api/Wingdi/nf-wingdi-selectclippath) e [**SelectClipRgn**](/windows/desktop/api/Wingdi/nf-wingdi-selectcliprgn)para limitar ainda mais o desenho a uma parte específica da área de atualização.

Os estilos WS \_ CLIPCHILDREN e WS CLIPIBLINGS especificam ainda mais como o sistema calcula \_ a região visível de uma janela. Se uma janela tiver um ou ambos os estilos, a região visível excluirá qualquer janela filho ou janelas irmãos (janelas com a mesma janela pai). Portanto, o desenho que, de outra forma, seria desatrapado nessas janelas sempre será recortado.

 

 



