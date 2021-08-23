---
description: você pode usar o controle InkPicture para renderizar tinta nas edições Microsoft Windows 2000, Windows Server 2003 e não Tablet PC do Windows XP. No entanto, você não pode usar o controle para inserir tinta nesses sistemas operacionais.
ms.assetid: e5d00b0f-0a4f-4ea2-ae63-dfb6bc8c2caf
title: Usando o InkPicture em versões anteriores do Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52423e8eb3e4c7f59da7a7caac299428dd8efcdce2192819444bfe91070f10b1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119091350"
---
# <a name="using-inkpicture-on-earlier-versions-of-windows"></a>Usando o InkPicture em versões anteriores do Windows

você pode usar o [controle InkPicture](inkpicture-control.md) para renderizar tinta nas edições Microsoft Windows 2000, Windows Server 2003 e não Tablet PC do Windows XP. No entanto, você não pode usar o controle para inserir tinta nesses sistemas operacionais.

A propriedade [**InkEnabled**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_inkenabled) do controle está definida como **false** e a tentativa de alterar a propriedade não tem nenhum efeito. Você pode atribuir valores a outras propriedades e manipular a tinta de forma programática, mas não pode usar o controle para coletar tinta.

 

 



