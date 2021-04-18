---
description: Um aplicativo pode definir um comentário durante a inicialização de uma sessão. Os comentários são geralmente usados para fins de log.
ms.assetid: 46201166-de07-47b8-8d9a-c8edb7fb6926
title: Comentário
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a12b9530e2fbb0c08b928607a71ee6b14cbdf6ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105789462"
---
# <a name="comment"></a>Comentário

Um aplicativo pode definir um comentário durante a inicialização de uma sessão. Os comentários são geralmente usados para fins de log.

Nem todos os provedores de serviços dão suporte ao uso dessas informações.

**TAPI 2. x:** Consulte [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo) (Membros **dwCommentSize** e **dwCommentOffset** de *lpCallInfo*).

**TAPI 3. x:** Consulte [**ITCallInfo:: get \_ CallInfoString**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfostring) (membro de **\_ Comentário cil** da [**cadeia de \_ caracteres CALLINFO**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_string)).

 

 
