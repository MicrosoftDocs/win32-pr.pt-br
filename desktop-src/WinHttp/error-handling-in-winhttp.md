---
description: Tratamento de erro no WinHTTP
ms.assetid: 96bceda2-ca96-4f88-ab38-35021889c2dd
title: Tratamento de erro no WinHTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72dac7775934684afe6cc9c9d54bc36bb8f3295c91deef7449e9a00600bc687e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119899176"
---
# <a name="error-handling-in-winhttp"></a>Tratamento de erro no WinHTTP

Nem todas as funções da API WinHTTP relatam erros da mesma maneira.

Algumas funções, como [**WinHttpSetTimeouts,**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsettimeouts)retornam um **BOOL** que indica falha quando **FALSE**. Se **FALSE** for retornado, os chamadores interessados no erro deverão chamar [**GetLastError.**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) Se **GetLastError** for chamado quando a função tiver sucesso (retornou qualquer coisa, menos **FALSE),** o valor retornado será imprevisível e poderá mudar entre versões Windows, Service Packs ou até mesmo entre chamadas para a mesma função.

Algumas funções, como [**WinHttpConnect,**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpconnect)retornam um pseudocódigo [HINTERNET.](hinternet-handles-in-winhttp.md) Essas funções são exatamente as mesmas, exceto que a falha é indicada retornando **NULL.** Se **NULL** for retornado, os chamadores interessados no erro deverão chamar [**GetLastError.**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) Se **GetLastError** for chamado quando a função tiver sucesso (retornou qualquer coisa, menos **NULL),** o valor retornado será imprevisível e poderá mudar entre versões Windows, Service Packs ou até mesmo entre chamadas para a mesma função.

Algumas funções, como [**WinHttpGetProxyResult,**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyresult)retornam um código de erro **DWORD** e não é necessário chamar nenhuma outra função para obter mais informações de erro. Para essas funções, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) não deve ser chamado. Se **GetLastError** for chamado, independentemente do êxito ou da falha da função, o valor retornado será imprevisível e poderá mudar entre versões Windows, Service Packs ou até mesmo entre chamadas para a mesma função.

 

 
