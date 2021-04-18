---
description: Devido à falta de reconhecedores em edições que não são do Tablet PC do Microsoft Windows XP, não é possível usar InkEdit para renderizar tinta nas edições Windows 2000, Windows Server 2003 e não Tablet PC do Windows XP, e você não pode usar o controle para inserir tinta nesses sistemas operacionais.
ms.assetid: eb80ff91-5c09-43d1-afd4-6391097000c1
title: Usando InkEdit em versões anteriores do Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08343b3d379a3f45985b1f586254e7a370998f15
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105788664"
---
# <a name="using-inkedit-on-earlier-versions-of-windows"></a>Usando InkEdit em versões anteriores do Windows

Devido à falta de reconhecedores em edições que não são do Tablet PC do Microsoft Windows XP, não é possível usar [InkEdit](inkedit-control.md) para renderizar tinta nas edições Windows 2000, windows Server 2003 e não Tablet PC do Windows XP, e você não pode usar o controle para inserir tinta nesses sistemas operacionais.

A propriedade [**InkMode**](/windows/desktop/api/inked/nf-inked-iinkedit-get_inkmode) do controle está definida como **desabilitada** (**IEM \_ desabilitado** para C++) e a tentativa de alterar a propriedade não tem efeito. Você pode atribuir valores a outras propriedades e copiar e colar a tinta em outros aplicativos, mas não pode usar o controle para aceitar gestos ou coletar tinta.

 

 



