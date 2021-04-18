---
description: 'Há três funções que geram caixas de diálogo para manipular erros: SetupCopyError, SetupDeleteError e SetupRenameError.'
ms.assetid: fcb310e1-5db7-47f3-b3d6-d528eb17e19a
title: Tratamento de erro (API de instalação)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5fb1347a3bec800200c2b6bda81e3f1eeeb866de
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105755787"
---
# <a name="error-handling-setup-api"></a>Tratamento de erro (API de instalação)

Há três funções que geram caixas de diálogo para manipular erros: [**SetupCopyError**](/windows/desktop/api/Setupapi/nf-setupapi-setupcopyerrora), [**SetupDeleteError**](/windows/desktop/api/Setupapi/nf-setupapi-setupdeleteerrora)e [**SetupRenameError**](/windows/desktop/api/Setupapi/nf-setupapi-setuprenameerrora).

As rotinas de retorno de chamada podem usar essas funções para gerar uma interface do usuário para lidar com notificações [**SPFILENOTIFY \_ COPYERROR**](spfilenotify-copyerror.md), [**SPFILENOTIFY \_ DELETEERROR**](spfilenotify-deleteerror.md)e [**SPFILENOTIFY \_ RENAMEERROR**](spfilenotify-renameerror.md) .

Cada uma dessas funções de tratamento de erros gera uma caixa de diálogo que solicita ao usuário informações sobre como proceder. Assim como com o [**SetupPromptForDisk**](/windows/desktop/api/Setupapi/nf-setupapi-setuppromptfordiska), você pode modificar o layout e o comportamento da caixa de diálogo especificando sinalizadores durante a chamada de função.

 

 



