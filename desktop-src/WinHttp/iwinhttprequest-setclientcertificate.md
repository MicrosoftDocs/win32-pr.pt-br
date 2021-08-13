---
description: Seleciona um certificado do cliente a ser enviado para um servidor HTTPS (Secure Hypertext Transfer Protocol).
ms.assetid: e76f1e76-5efe-46f2-9a21-064aa06fb3a8
title: Método IWinHttpRequest::SetClientCertificate
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWinHttpRequest.SetClientCertificate
- WinHttpRequest.SetClientCertificate
api_type:
- COM
api_location:
- Winhttp.dll
ms.openlocfilehash: 1f878b93fe0db24334f406c2a6c85663e7f37a05095998f157cbf44878b39daf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118562892"
---
# <a name="iwinhttprequestsetclientcertificate-method"></a>Método IWinHttpRequest::SetClientCertificate

O **método SetClientCertificate** seleciona um certificado de cliente a ser enviado para um servidor HTTPS (Secure Hypertext Transfer Protocol).

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetClientCertificate(
  [in] BSTR ClientCertificate
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ClientCertificate* \[ Em\]
</dt> <dd>

Especifica o local, o [*armazenamento de certificados*](glossary.md)e o assunto de um certificado do cliente.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O valor de retorno é **S \_ OK em** caso de êxito ou um valor de erro, caso contrário.

## <a name="remarks"></a>Comentários

A cadeia de caracteres especificada no parâmetro *ClientCertificate* consiste no local do certificado, no armazenamento de certificados e no nome da assunto delimitados por malhas incertas. Para obter mais informações sobre os componentes da cadeia de caracteres de certificado, consulte [Certificados do cliente](ssl-in-winhttp.md).

O nome e o local do armazenamento de certificados são opcionais. No entanto, se você especificar um armazenamento de certificados, também deverá especificar o local desse armazenamento de certificados. O local padrão é CURRENT \_ USER e o armazenamento de certificados padrão é "MY". Um assunto em branco indica que o primeiro certificado no armazenamento de certificados deve ser usado.

Chame **SetClientCertificate para selecionar** um certificado antes de chamar [**Enviar**](iwinhttprequest-send.md) para enviar a solicitação.

O Microsoft Windows Http Services (WinHTTP) não fornece certificados de cliente para servidores proxy que solicitam certificados para autenticação.

> [!Note]  
> Para Windows XP e Windows 2000, consulte [](winhttp-start-page.md) a seção Requisitos de tempo de executar da página inicial do WinHTTP.

 

## <a name="examples"></a>Exemplos

O exemplo de script a seguir mostra como selecionar um certificado do cliente a ser enviado com uma solicitação. Um certificado com o assunto "Meu Middle-Tier Certificado" é escolhido do armazenamento de certificados "Pessoal" no Registro em **HKEY \_ LOCAL \_ MACHINE**. Como este exemplo de código é específico do Microsoft JScript, que usa a faixa invertida como um caractere de escape, duas barras invertida adjacentes são necessárias para delimitar componentes da cadeia de caracteres de certificado.


```JScript
// Instantiate a WinHttpRequest object.
var HttpReq = new ActiveXObject("WinHttp.WinHttpRequest.5.1");
    
// Open an HTTP connection.
HttpReq.Open("GET", "https://www.fabrikam.com/", false);
    
// Select a client certificate.
HttpReq.SetClientCertificate(
            "LOCAL_MACHINE\\Personal\\My Middle-Tier Certificate");

// Send the HTTP Request.
HttpReq.Send();
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows XP, Windows 2000 Professional somente com aplicativos da área de trabalho SP3 \[\]<br/>            |
| Servidor mínimo com suporte<br/> | Windows Server 2003, Windows 2000 Server somente com aplicativos da área de trabalho SP3 \[\]<br/>         |
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

[SSL no WinHTTP](ssl-in-winhttp.md)
</dt> <dt>

[Versões do WinHTTP](winhttp-versions.md)
</dt> </dl>

 

 




