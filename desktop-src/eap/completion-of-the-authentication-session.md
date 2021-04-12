---
title: Conclusão da sessão de autenticação
description: Depois que a sessão de autenticação for concluída, o serviço de autenticação chamará a função RasEapEnd para permitir que o protocolo de autenticação desaloque seu buffer de trabalho.
ms.assetid: 466795ac-fee5-4b82-adc7-af14b6ef3fc3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 27899ef348630e412b3d52d066f59ea9b5255244
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104365904"
---
# <a name="completion-of-the-authentication-session"></a>Conclusão da sessão de autenticação

Depois que a sessão de autenticação for concluída, o serviço de autenticação chamará a função [**RasEapEnd**](/previous-versions/windows/desktop/legacy/aa363521(v=vs.85)) para permitir que o protocolo de autenticação desaloque seu buffer de trabalho. Essa ação é executada independentemente de a autenticação ter sido bem-sucedida. Chamar a função **RasEapEnd** garante que nenhuma chamada adicional seja feita ao protocolo de autenticação usando esse usuário ou contexto específico sem primeiro chamar [**RasEapBegin**](/previous-versions/windows/desktop/legacy/aa363520(v=vs.85)).

 

 