---
description: Tratamento de erro no WinHTTP
ms.assetid: 96bceda2-ca96-4f88-ab38-35021889c2dd
title: Tratamento de erro no WinHTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bbf234220d0973e86c830063e4ecc25312fa2d77
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105813701"
---
# <a name="error-handling-in-winhttp"></a>Tratamento de erro no WinHTTP

Nem todas as funções da API do WinHTTP relatam erros da mesma maneira.

Algumas funções, como [**WinHttpSetTimeouts**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsettimeouts), retornam um **bool** que indica falha quando **false**. Se **false** for retornado, os chamadores interessados no erro devem chamar [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror). Se **GetLastError** for chamado quando a função êxito na (retornou qualquer coisa, exceto **false**), o valor retornado será imprevisível e poderá mudar entre as versões do Windows, Service Packs ou até mesmo entre as chamadas para a mesma função.

Algumas funções, como [**WinHttpConnect**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpconnect), retornam um pseudodispositivo [HINTERNET](hinternet-handles-in-winhttp.md) . Essas funções são exatamente as mesmas, exceto que a falha é indicada retornando **NULL**. Se **NULL** for retornado, os chamadores interessados no erro devem chamar [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror). Se **GetLastError** for chamado quando a função êxito na (retornou qualquer coisa, exceto **NULL**), o valor retornado será imprevisível e poderá mudar entre as versões do Windows, Service Packs ou até mesmo entre as chamadas para a mesma função.

Algumas funções, como [**WinHttpGetProxyResult**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyresult), retornam um código de erro **DWORD** e não há necessidade de chamar outras funções para obter mais informações sobre o erro. Para essas funções, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) não deve ser chamado. Se **GetLastError** for chamado, independentemente do êxito ou da falha da função, o valor retornado será imprevisível e poderá mudar entre as versões do Windows, Service Packs ou até mesmo entre as chamadas para a mesma função.

 

 
