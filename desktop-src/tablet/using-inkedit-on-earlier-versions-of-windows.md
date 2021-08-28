---
description: devido à falta de reconhecedores em edições que não são do Tablet PC do Microsoft Windows XP, não é possível usar InkEdit para renderizar a tinta nas edições Windows 2000, Windows Server 2003 e não Tablet PC do Windows XP, e você não pode usar o controle para inserir tinta nesses sistemas operacionais.
ms.assetid: eb80ff91-5c09-43d1-afd4-6391097000c1
title: Usando InkEdit em versões anteriores do Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eefa98089a2ede778be09719767f96a1129a1be0d4004828172651e637cd81d6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118966605"
---
# <a name="using-inkedit-on-earlier-versions-of-windows"></a>Usando InkEdit em versões anteriores do Windows

devido à falta de reconhecedores em edições que não são do Tablet PC do Microsoft Windows XP, não é possível usar [InkEdit](inkedit-control.md) para renderizar a tinta nas edições Windows 2000, Windows Server 2003 e não Tablet PC do Windows XP, e você não pode usar o controle para inserir tinta nesses sistemas operacionais.

A propriedade [**InkMode**](/windows/desktop/api/inked/nf-inked-iinkedit-get_inkmode) do controle está definida como **desabilitada** (**IEM \_ desabilitado** para C++) e a tentativa de alterar a propriedade não tem efeito. Você pode atribuir valores a outras propriedades e copiar e colar a tinta em outros aplicativos, mas não pode usar o controle para aceitar gestos ou coletar tinta.

 

 



