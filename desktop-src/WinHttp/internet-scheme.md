---
description: Esquemas de Internet com suporte no WinHTTP.
ms.assetid: 31e45879-807e-4dd5-9f99-94a46011e55e
title: INTERNET_SCHEME (Winhttp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0429d07ef366acdc881a82373194e153ad3c8f367172b7e64221ecf479e7bf3c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119644016"
---
# <a name="internet_scheme"></a>ESQUEMA DE \_ INTERNET

Esquemas de Internet com suporte no WinHTTP.

<dl> <dt>

<span id="INTERNET_SCHEME_HTTP"></span><span id="internet_scheme_http"></span>**\_ESQUEMA DE INTERNET \_ HTTP**
</dt> <dd> <dl> <dt>

1
</dt> <dt>



Um esquema de Internet HTTP.


</dt> </dl> </dd> <dt>

<span id="INTERNET_SCHEME_HTTPS"></span><span id="internet_scheme_https"></span>**\_ESQUEMA DE INTERNET \_ HTTPS**
</dt> <dd> <dl> <dt>

2
</dt> <dt>



Um esquema de Internet HTTPS (SSL).


</dt> </dl> </dd> <dt>

<span id="INTERNET_SCHEME_FTP"></span><span id="internet_scheme_ftp"></span>**\_FTP DE ESQUEMA \_ DE INTERNET**
</dt> <dd> <dl> <dt>

3
</dt> <dt>



Um esquema de Internet de FTP. Esse esquema só tem suporte para uso em [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) e [**WinHttpGetProxyForUrlEx**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurlex).


</dt> </dl> </dd> <dt>

<span id="INTERNET_SCHEME_SOCKS"></span><span id="internet_scheme_socks"></span>**MEIA \_ DE ESQUEMA DA INTERNET \_**
</dt> <dd> <dl> <dt>

4
</dt> <dt>



Um esquema de Internet SOCKS. Esse esquema só tem suporte para uso em [**WINHTTP \_ PROXY \_ RESULT \_ ENTRY**](/windows/desktop/api/winhttp/ns-winhttp-winhttp_proxy_result_entry).


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows XP, Windows 2000 Professional somente com aplicativos da área de trabalho SP3 \[\]<br/>      |
| Servidor mínimo com suporte<br/> | Windows Server 2003, Windows 2000 Server com somente aplicativos da área de trabalho SP3 \[\]<br/>   |
| Cabeçalho<br/>                   | <dl> <dt>Winhttp.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ENTRADA DE RESULTADO DO PROXY WINHTTP \_ \_ \_**](/windows/desktop/api/winhttp/ns-winhttp-winhttp_proxy_result_entry)
</dt> </dl>

 

 




