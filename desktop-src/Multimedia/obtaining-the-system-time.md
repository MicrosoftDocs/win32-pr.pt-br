---
title: Obtendo a hora do sistema
description: Obtendo a hora do sistema
ms.assetid: 33dfcd56-11d9-45b9-b983-8354526101a7
keywords:
- temporizadores de multimídia, hora do sistema
- temporizadores, hora do sistema
- hora do sistema
- Função timeGetTime
- Função timeGetSystemTime
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45460078776732234510d7308bd1e8f490e3871334bdf950bcedd77943b430e6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119806466"
---
# <a name="obtaining-the-system-time"></a>Obtendo a hora do sistema

Normalmente, antes de um aplicativo começar a usar os serviços de temporizador multimídia, ele recupera a hora *atual do sistema.* A hora do sistema é a hora, em milissegundos, desde que o sistema operacional microsoft Windows foi iniciado. Você pode usar a [**função timeGetTime**](/windows/desktop/api/TimeAPI/nf-timeapi-timegettime) ou [**timeGetSystemTime**](/windows/desktop/api/TimeAPI/nf-timeapi-timegetsystemtime) para recuperar a hora do sistema. Essas duas funções são muito semelhantes: **timeGetTime** retorna a hora do sistema e **timeGetSystemTime** preenche uma estrutura [**MMTIME**](/previous-versions//dd757347(v=vs.85)) com a hora do sistema.

 

 