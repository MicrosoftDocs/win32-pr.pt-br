---
title: Conclusão da sessão de autenticação
description: Depois que a sessão de autenticação for concluída, o serviço de autenticação chamará a função RasEapEnd para permitir que o protocolo de autenticação desaloque seu buffer de trabalho.
ms.assetid: 466795ac-fee5-4b82-adc7-af14b6ef3fc3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8ee29ac4c4139fc8a575e7570e3c04fbe449aa4d619cea3e096cd12dfcf19bb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119948466"
---
# <a name="completion-of-the-authentication-session"></a>Conclusão da sessão de autenticação

Depois que a sessão de autenticação for concluída, o serviço de autenticação chamará a [**função RasEapEnd**](/previous-versions/windows/desktop/legacy/aa363521(v=vs.85)) para permitir que o protocolo de autenticação desaloque seu buffer de trabalho. Essa ação é tomada independentemente de a autenticação ter sido bem-sucedida. Chamar a **função RasEapEnd** garante que nenhuma outra chamada seja feita ao protocolo de autenticação usando esse usuário ou contexto específico sem primeiro chamar [**RasEapBegin.**](/previous-versions/windows/desktop/legacy/aa363520(v=vs.85))

 

 