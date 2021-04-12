---
title: Obtendo a hora do sistema
description: Obtendo a hora do sistema
ms.assetid: 33dfcd56-11d9-45b9-b983-8354526101a7
keywords:
- Timers de multimídia, hora do sistema
- temporizadores, hora do sistema
- hora do sistema
- função timeGetTime
- função timeGetSystemTime
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89fdcc905569a500afe689658676137c460d19d8
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104453990"
---
# <a name="obtaining-the-system-time"></a>Obtendo a hora do sistema

Normalmente, antes que um aplicativo comece a usar os serviços de timer de multimídia, ele recupera a hora atual do *sistema*. A hora do sistema é o tempo, em milissegundos, desde que o sistema operacional Microsoft Windows foi iniciado. Você pode usar a função [**timeGetTime**](/windows/desktop/api/TimeAPI/nf-timeapi-timegettime) ou [**timeGetSystemTime**](/windows/desktop/api/TimeAPI/nf-timeapi-timegetsystemtime) para recuperar a hora do sistema. Essas duas funções são muito semelhantes: **timeGetTime** retorna a hora do sistema e **timeGetSystemTime** preenche uma estrutura [**MMTIME**](/previous-versions//dd757347(v=vs.85)) com a hora do sistema.

 

 