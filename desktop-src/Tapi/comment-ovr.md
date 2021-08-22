---
description: Um aplicativo pode definir um comentário durante o início de uma sessão. Os comentários geralmente são usados para fins de registro em log.
ms.assetid: 46201166-de07-47b8-8d9a-c8edb7fb6926
title: Comentário
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 757570651315e0d4e9b313af9e926daf12cd25f3a6415037aaf92079bff5b824
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118868074"
---
# <a name="comment"></a>Comentário

Um aplicativo pode definir um comentário durante o início de uma sessão. Os comentários geralmente são usados para fins de registro em log.

Nem todos os provedores de serviços suportam o uso dessas informações.

**TAPI 2.x:** Consulte [**os membros lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo) (**dwCommentSize** e **dwCommentOffset** de *lpCallInfo*).

**TAPI 3.x:** Consulte [**ITCallInfo::get \_ CallInfoString**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfostring) (**CIL \_ COMMENT member** of [**CALLINFO \_ STRING**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_string)).

 

 
