---
title: HTTP_RESPONSE (http. h)
description: A versão da estrutura de \_ resposta http é dependente da versão da fila de solicitações usada como a seguir fila de solicitação da API do servidor http versão 1,0 Esta é uma \_ estrutura de solicitação HTTP \_ v1. Fila de solicitações da API do servidor HTTP versão 2,0 Esta é uma \_ estrutura de solicitação HTTP \_ v2.
ms.assetid: F94646C0-7293-4543-842B-F08D8C7E2247
keywords:
- HTTP_RESPONSE
- HTTP_RESPONSE
- PHTTP_RESPONSE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4a8445021aa61b94ae83a55937b1db5ca4e3c577
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369486"
---
# <a name="http_response"></a>\_resposta http

A versão da estrutura **de \_ resposta http** depende da versão da fila de solicitações usada da seguinte maneira:

-   Fila de solicitações da API do servidor HTTP versão 1,0: esta é uma estrutura de [**\_ solicitação HTTP \_ v1**](/windows/desktop/api/Http/ns-http-http_request_v1) .
-   Fila de solicitações da API do servidor HTTP versão 2,0: esta é uma estrutura de [**\_ solicitação HTTP \_ v2**](/windows/desktop/api/Http/ns-http-http_request_v2) .

Não use a [**solicitação \_ http \_ v1**](/windows/desktop/api/Http/ns-http-http_request_v1) e a [**\_ solicitação HTTP \_ v2**](/windows/desktop/api/Http/ns-http-http_request_v2) diretamente em seu código; usar **\_ resposta http** , em vez disso, garante que a versão apropriada da estrutura seja usada com base na versão da fila de solicitações.


```C++
typedef HTTP_REQUEST_V1 HTTP_RESPONSE;
typedef HTTP_REQUEST_V2 HTTP_RESPONSE;
typedef HTTP_RESPONSE* PHTTP_RESPONSE;
```



<dl> <dt>

**\_resposta http**
</dt> <dd>

A solicitação foi de uma fila de solicitações v1.

</dd> <dt>

**\_resposta http**
</dt> <dd>

A solicitação foi de uma fila de solicitações v2.

</dd> <dt>

**resposta do PHTTP \_**
</dt> <dd>

Ponteiro para uma estrutura de **\_ resposta http** .

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                    |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                              |
| parâmetro<br/>                   | <dl> <dt>Http. h</dt> </dl> |



 

 





