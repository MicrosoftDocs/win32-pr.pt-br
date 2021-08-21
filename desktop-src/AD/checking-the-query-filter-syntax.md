---
title: Verificando a sintaxe do filtro de consulta
description: A API LDAP fornece uma função de verificação de sintaxe simples. Lembre-se de que ele só verifica a sintaxe e não a existência das propriedades especificadas no filtro.
ms.assetid: 4e564cd9-2f8b-4e70-928c-3a8bd804aeba
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24a95f6acc6f872950fe6314b32b94282f6869d8acb3578f35d52fa19588b63b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118022830"
---
# <a name="checking-the-query-filter-syntax"></a>Verificando a sintaxe do filtro de consulta

A API LDAP fornece uma função de verificação de sintaxe simples. Lembre-se de que ele só verifica a sintaxe e não a existência das propriedades especificadas no filtro.

A função a seguir verifica a sintaxe do filtro de consulta e retorna **s \_ OK** se o filtro for válido ou S \_ false se não for.


```C++
HRESULT CheckFilterSyntax(
    LPOLESTR szServer, // NULL binds to a DC in the current domain.
    LPOLESTR szFilter) // Filter to check.
{
HRESULT hr = S_OK;
DWORD dwReturn;
LDAP *hConnect = NULL;  // Connection handle
 
if (!szFilter)
  return E_POINTER;
 
// LDAP_PORT is the default port, 389
 
hConnect  = ldap_open(szServer,  LDAP_PORT);
 
// Bind using the preferred authentication method on Windows 2000
// and the calling thread's security context.
 
dwReturn = ldap_bind_s( hConnect, NULL, NULL, LDAP_AUTH_NEGOTIATE );
if (dwReturn==LDAP_SUCCESS) {
    dwReturn = ldap_check_filter(hConnect, szFilter);
    if (dwReturn==LDAP_SUCCESS)
        hr = S_OK;
    else
        hr = S_FALSE;
}
 
// Unbind to free the connection.
 
ldap_unbind( hConnect );
 
return hr;
}
```



 

 




