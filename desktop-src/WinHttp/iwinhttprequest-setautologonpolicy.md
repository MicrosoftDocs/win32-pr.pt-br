---
description: Define a política de logon automático atual.
ms.assetid: bc8e8c9c-574e-4392-b336-2c06947022ee
title: Método IWinHttpRequest::SetAutoLogonPolicy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWinHttpRequest.SetAutoLogonPolicy
- WinHttpRequest.SetAutoLogonPolicy
api_type:
- COM
api_location:
- Winhttp.dll
ms.openlocfilehash: b6375d5c5b6c9b6c8acebcdd05a2ad778bb37e75c067a44100a5c67a92876248
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118562882"
---
# <a name="iwinhttprequestsetautologonpolicy-method"></a>Método IWinHttpRequest::SetAutoLogonPolicy

O **método SetAutoLogonPolicy** define a Política [de Logon Automática atual.](authentication-in-winhttp.md)

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetAutoLogonPolicy(
  [in] WinHttpRequestAutoLogonPolicy AutoLogonPolicy
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*AutoLogonPolicy* \[ Em\]
</dt> <dd>

Especifica a política de logon automático atual.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O valor de retorno é **S \_ OK em** caso de êxito ou um valor de erro, caso contrário.

## <a name="remarks"></a>Comentários

A política padrão é [**AutoLogonPolicy \_ OnlyIfBypassProxy.**](winhttprequestautologonpolicy.md)

Chame **SetAutoLogonPolicy** para definir a política de logon automático antes de [**chamar Enviar**](iwinhttprequest-send.md) para enviar a solicitação.

> [!Note]  
> Para Windows XP e Windows 2000, consulte [](winhttp-start-page.md) a seção Requisitos de tempo de executar da página inicial do WinHTTP.

 

## <a name="examples"></a>Exemplos

O exemplo de script a seguir mostra como definir a política de logon automático para nunca usar a autenticação NTLM ou Negotiate automaticamente.


```JScript
// Instantiate a WinHttpRequest object.
var HttpReq = new ActiveXObject("WinHttp.WinHttpRequest.5.1");
    
// Open an HTTP connection.
HttpReq.Open("GET", "https://www.fabrikam.com/", false);
    
// Do not automatically send user credentials.
HttpReq.SetAutoLogonPolicy(2);

// Send the HTTP Request.
HttpReq.Send();
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows XP, Windows 2000 Professional somente com aplicativos da área de trabalho SP3 \[\]<br/>            |
| Servidor mínimo com suporte<br/> | Windows Server 2003, Windows 2000 Server com somente aplicativos da área de trabalho SP3 \[\]<br/>         |
| Redistribuível<br/>          | WinHTTP 5.0 e Internet Explorer 5.01 ou posterior no Windows XP e Windows 2000.<br/> |
| Idl<br/>                      | <dl> <dt>HttpRequest.idl</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Winhttp.lib</dt> </dl>     |
| DLL<br/>                      | <dl> <dt>Winhttp.dll</dt> </dl>     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IWinHttpRequest**](iwinhttprequest-interface.md)
</dt> <dt>

[**WinHttpRequest**](winhttprequest.md)
</dt> <dt>

[Autenticação no WinHTTP](authentication-in-winhttp.md)
</dt> <dt>

[Versões do WinHTTP](winhttp-versions.md)
</dt> </dl>

 

 




