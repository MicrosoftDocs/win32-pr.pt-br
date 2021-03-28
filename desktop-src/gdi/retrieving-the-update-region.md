---
description: As funções GetUpdateRect e GetUpdateRgn recuperam a região de atualização atual para a janela.
ms.assetid: c0729c4f-3b00-4ab9-91b2-4a2fecee8727
title: Recuperando a região de atualização
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8115f47a6c585d5b660d73bbf4fb3de21334b6c2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104165049"
---
# <a name="retrieving-the-update-region"></a>Recuperando a região de atualização

As funções [**GetUpdateRect**](/windows/desktop/api/Winuser/nf-winuser-getupdaterect) e [**GetUpdateRgn**](/windows/desktop/api/Winuser/nf-winuser-getupdatergn) recuperam a região de atualização atual para a janela. GetUpdateRect recupera o menor retângulo (em coordenadas lógicas) que inclui toda a região de atualização. GetUpdateRgn recupera a própria região de atualização. Essas funções podem ser usadas para calcular o tamanho atual da região de atualização para determinar onde executar uma operação de desenho.

[**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint) também recupera as dimensões do menor retângulo que envolve a região de atualização atual, copiando as dimensões para o membro **RcPaint** na estrutura [**PAINTSTRUCT**](/windows/win32/api/winuser/ns-winuser-paintstruct) . Como **BeginPaint** valida a região de atualização, qualquer chamada para [**GetUpdateRect**](/windows/desktop/api/Winuser/nf-winuser-getupdaterect) e [**GetUpdateRgn**](/windows/desktop/api/Winuser/nf-winuser-getupdatergn) imediatamente após uma chamada para **BeginPaint** retorna uma região de atualização vazia.

 

 



