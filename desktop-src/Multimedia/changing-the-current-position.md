---
title: Alterando a posição atual
description: Alterando a posição atual
ms.assetid: f8c4b9b5-c5fb-4292-8418-41650dcd65c0
keywords:
- MCI_SEEK de comando
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a14f062fc93a89f54fb89a30b6ac3e53c8d6240cfc28b661a25da48a0b1b2fbe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118941284"
---
# <a name="changing-the-current-position"></a>Alterando a posição atual

Para alterar a posição atual em um elemento de dispositivo, use a mensagem de comando [**MCI \_ SEEK**](mci-seek.md) junto com o sinalizador MCI TO e a estrutura \_ [**MCI \_ SEEK \_ PARMS.**](mci-seek-parms.md) Se você usar o **membro dwTo** para especificar uma posição de busca com MCI SEEK, deverá consultar o formato de hora e \_ defini-lo, se necessário.

Além de especificar uma posição com o membro **dwTo,** você pode especificar os sinalizadores MCI SEEK TO START ou MCI SEEK TO END para o \_ \_ parâmetro \_ \_ \_ \_ *dwParam1* da [**função mciSendCommand**](/previous-versions//dd757160(v=vs.85)) para encontrar as posições inicial e final do elemento do dispositivo. Se você usar um desses sinalizadores, não especifique o sinalizador MCI \_ TO.

 

 