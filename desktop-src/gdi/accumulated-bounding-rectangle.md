---
description: O retângulo delimitador acumulado é o menor retângulo que envolve a parte de uma janela ou área de cliente afetada por operações de desenho recentes.
ms.assetid: 8ae13486-a9e2-4841-ada3-c70d30450ac8
title: Retângulo delimitador acumulado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5ae3237304af68a4b8ff447b7ea2d64d3f81053
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104502438"
---
# <a name="accumulated-bounding-rectangle"></a>Retângulo delimitador acumulado

O *retângulo delimitador acumulado* é o menor retângulo que envolve a parte de uma janela ou área de cliente afetada por operações de desenho recentes. Um aplicativo pode usar esse retângulo para determinar convenientemente a extensão das alterações causadas por operações de desenho. Às vezes, ele é usado em conjunto com [**LockWindowUpdate**](/windows/desktop/api/Winuser/nf-winuser-lockwindowupdate) para determinar qual parte da área do cliente deve ser redesenhada após a limpeza do bloqueio de atualização.

Um aplicativo usa a função [**SetBoundsRect**](/windows/desktop/api/Wingdi/nf-wingdi-setboundsrect) (especificando DCB \_ enable) para começar a acumular o retângulo delimitador. O sistema, subsequentemente, acumula pontos para o retângulo delimitador, pois o aplicativo usa o contexto do dispositivo de exibição especificado. O aplicativo pode recuperar o retângulo delimitador atual a qualquer momento usando a função [**GetBoundsRect**](/windows/desktop/api/Wingdi/nf-wingdi-getboundsrect) . O aplicativo interrompe a acumulação chamando **SetBoundsRect** novamente, especificando o \_ valor de desabilitação de DCB.

 

 



