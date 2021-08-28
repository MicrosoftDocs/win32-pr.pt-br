---
description: O retângulo delimitado acumulado é o menor retângulo que delimita a parte de uma janela ou área do cliente afetada por operações de desenho recentes.
ms.assetid: 8ae13486-a9e2-4841-ada3-c70d30450ac8
title: Retângulo delimitado acumulado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94d90b2f92b50dbaede477c0a712be970bf0af46b25c5e5edd956fe428d46559
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119779346"
---
# <a name="accumulated-bounding-rectangle"></a>Retângulo delimitado acumulado

O *retângulo delimitado acumulado é* o menor retângulo que delimita a parte de uma janela ou área do cliente afetada por operações de desenho recentes. Um aplicativo pode usar esse retângulo para determinar convenientemente a extensão das alterações causadas por operações de desenho. Às vezes, ele é usado em conjunto com [**LockWindowUpdate**](/windows/desktop/api/Winuser/nf-winuser-lockwindowupdate) para determinar qual parte da área do cliente deve ser redesenhada depois que o bloqueio de atualização é limpo.

Um aplicativo usa a [**função SetBoundsRect**](/windows/desktop/api/Wingdi/nf-wingdi-setboundsrect) (especificando DCB ENABLE) para começar \_ a acumular o retângulo delimitador. Posteriormente, o sistema acumula pontos para o retângulo delimitativo, pois o aplicativo usa o contexto do dispositivo de exibição especificado. O aplicativo pode recuperar o retângulo delimitador atual a qualquer momento usando a [**função GetBoundsRect.**](/windows/desktop/api/Wingdi/nf-wingdi-getboundsrect) O aplicativo interrompe o acúmulo chamando **SetBoundsRect** novamente, especificando o valor DISABLE \_ de DCB.

 

 



