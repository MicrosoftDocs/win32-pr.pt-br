---
description: Esquemas de Internet com suporte do WinHTTP.
ms.assetid: 31e45879-807e-4dd5-9f99-94a46011e55e
title: INTERNET_SCHEME (WinHTTP. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cc7b73dcc13b2623e3a6f28d2d49d1965464070f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829726"
---
# <a name="internet_scheme"></a>esquema de INTERNET \_

Esquemas de Internet com suporte do WinHTTP.

<dl> <dt>

<span id="INTERNET_SCHEME_HTTP"></span><span id="internet_scheme_http"></span>**esquema de INTERNET \_ \_ http**
</dt> <dd> <dl> <dt>

1
</dt> <dt>



Um esquema de Internet HTTP.


</dt> </dl> </dd> <dt>

<span id="INTERNET_SCHEME_HTTPS"></span><span id="internet_scheme_https"></span>**\_https de esquema de Internet \_**
</dt> <dd> <dl> <dt>

2
</dt> <dt>



Um esquema de Internet HTTPS (SSL).


</dt> </dl> </dd> <dt>

<span id="INTERNET_SCHEME_FTP"></span><span id="internet_scheme_ftp"></span>**\_FTP do esquema de Internet \_**
</dt> <dd> <dl> <dt>

3
</dt> <dt>



Um esquema de Internet FTP. Esse esquema só tem suporte para uso em [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) e [**WinHttpGetProxyForUrlEx**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurlex).


</dt> </dl> </dd> <dt>

<span id="INTERNET_SCHEME_SOCKS"></span><span id="internet_scheme_socks"></span>**esquema de INTERNET \_ \_ Socks**
</dt> <dd> <dl> <dt>

4
</dt> <dt>



Um esquema de Internet Socks. Esse esquema só tem suporte para uso na [**\_ entrada de \_ resultado \_ do proxy WinHTTP**](/windows/desktop/api/winhttp/ns-winhttp-winhttp_proxy_result_entry).


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Somente Windows XP, Windows 2000 Professional com \[ aplicativos de área de trabalho do SP3\]<br/>      |
| Servidor mínimo com suporte<br/> | Windows Server 2003, Windows 2000 Server com aplicativos de área de trabalho do SP3 \[ somente\]<br/>   |
| parâmetro<br/>                   | <dl> <dt>WinHTTP. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_entrada de \_ resultado do proxy WinHTTP \_**](/windows/desktop/api/winhttp/ns-winhttp-winhttp_proxy_result_entry)
</dt> </dl>

 

 




