---
description: Seleciona um certificado de cliente para enviar a um servidor HTTPS (protocolo de transferência de hipertexto) seguro.
ms.assetid: e76f1e76-5efe-46f2-9a21-064aa06fb3a8
title: 'Método IWinHttpRequest:: SetClientCertificate'
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
ms.openlocfilehash: 0b346451e87b62116d7202b476e554c84604ea48
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297090"
---
# <a name="iwinhttprequestsetclientcertificate-method"></a>Método IWinHttpRequest:: SetClientCertificate

O método **SetClientCertificate** seleciona um certificado de cliente para enviar a um servidor HTTPS (protocolo de transferência de hipertexto) seguro.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetClientCertificate(
  [in] BSTR ClientCertificate
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ClientCertificate* \[ no\]
</dt> <dd>

Especifica o local, o [*repositório de certificados*](glossary.md)e o assunto de um certificado de cliente.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O valor de retorno será **S \_ OK** em caso de êxito ou um valor de erro, caso contrário.

## <a name="remarks"></a>Comentários

A cadeia de caracteres especificada no parâmetro *ClientCertificate* consiste no local do certificado, no repositório de certificados e no nome da entidade delimitada por barras invertidas. Para obter mais informações sobre os componentes da cadeia de caracteres do certificado, consulte [certificados do cliente](ssl-in-winhttp.md).

O nome e o local do repositório de certificados são opcionais. No entanto, se você especificar um repositório de certificados, também deverá especificar o local desse repositório de certificados. O local padrão é o \_ usuário atual e o repositório de certificados padrão é "My". Um assunto em branco indica que o primeiro certificado no repositório de certificados deve ser usado.

Chame **SetClientCertificate** para selecionar um certificado antes de chamar [**Send**](iwinhttprequest-send.md) para enviar a solicitação.

O Microsoft Windows HTTP Services (WinHTTP) não fornece certificados de cliente para servidores proxy que solicitam certificados para autenticação.

> [!Note]  
> Para o Windows XP e o Windows 2000, consulte a seção [requisitos de tempo de execução](winhttp-start-page.md) da página inicial do WinHTTP.

 

## <a name="examples"></a>Exemplos

O exemplo de script a seguir mostra como selecionar um certificado de cliente para enviar com uma solicitação. Um certificado com o assunto "meu certificado de Middle-Tier" é escolhido no repositório de certificados "pessoal" no registro em **HKEY \_ local \_ Machine**. Como este exemplo de código é específico do Microsoft JScript, que usa a barra invertida como um caractere de escape, duas barras invertidas adjacentes são necessárias para delimitar os componentes da cadeia de caracteres do certificado.


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
| Cliente mínimo com suporte<br/> | Somente Windows XP, Windows 2000 Professional com \[ aplicativos de área de trabalho do SP3\]<br/>            |
| Servidor mínimo com suporte<br/> | Windows Server 2003, Windows 2000 Server com aplicativos de área de trabalho do SP3 \[ somente\]<br/>         |
| Redistribuível<br/>          | WinHTTP 5,0 e Internet Explorer 5, 1 ou posterior no Windows XP e no Windows 2000.<br/> |
| INSERI<br/>                      | <dl> <dt>HttpRequest. idl</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>WinHTTP. lib</dt> </dl>     |
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

 

 




