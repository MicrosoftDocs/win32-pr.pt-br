---
description: Você pode usar o controle InkPicture para renderizar tinta nas edições Microsoft Windows 2000, Windows Server 2003 e não Tablet PC do Windows XP. No entanto, você não pode usar o controle para inserir tinta nesses sistemas operacionais.
ms.assetid: e5d00b0f-0a4f-4ea2-ae63-dfb6bc8c2caf
title: Usando o InkPicture em versões anteriores do Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3cbd2bf8545524787c9e37f70c43d954ab440910
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105785225"
---
# <a name="using-inkpicture-on-earlier-versions-of-windows"></a>Usando o InkPicture em versões anteriores do Windows

Você pode usar o [controle InkPicture](inkpicture-control.md) para renderizar tinta nas edições Microsoft Windows 2000, windows Server 2003 e não Tablet PC do Windows XP. No entanto, você não pode usar o controle para inserir tinta nesses sistemas operacionais.

A propriedade [**InkEnabled**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_inkenabled) do controle está definida como **false** e a tentativa de alterar a propriedade não tem nenhum efeito. Você pode atribuir valores a outras propriedades e manipular a tinta de forma programática, mas não pode usar o controle para coletar tinta.

 

 



