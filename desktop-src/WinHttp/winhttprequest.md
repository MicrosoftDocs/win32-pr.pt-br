---
Description: Este tópico fornece informações sobre como usar o objeto COM do WinHTTP WinHttpRequest com linguagens de script.
ms.assetid: 0bbbf3dc-84b8-41d8-8627-e3d80ddcb783
title: Objeto WinHttpRequest
ms.topic: reference
ms.custom: snippet-project
ms.date: 07/22/2020
topic_type:
- APIRef
- kbSyntax
api_name:
- WinHttpRequest
api_type:
- COM
api_location:
- Winhttp.dll
ms.openlocfilehash: 907e94a731b2ec150a331347480c461d0d0fa319
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105812152"
---
# <a name="winhttprequest-object"></a>Objeto WinHttpRequest

Este tópico fornece informações sobre como usar o objeto com do WinHTTP **WinHttpRequest** com linguagens de script. Para obter mais informações, incluindo a API do C++ (WinHTTP), consulte [sobre WinHTTP](about-winhttp.md). Consulte [escolhendo uma interface WinHTTP](choosing-a-winhttp-interface.md) para uma comparação dessas interfaces.

## <a name="example"></a>Exemplo

```javascript
// Instantiate a WinHttpRequest object.
var WinHttpReq = new ActiveXObject("WinHttp.WinHttpRequest.5.1");
```

```cpp
 IWinHttpRequest *  pIWinHttpRequest = NULL;
 \\..
    hr = CLSIDFromProgID(L"WinHttp.WinHttpRequest.5.1", &clsid);

    if (SUCCEEDED(hr))
    {
        hr = CoCreateInstance(clsid, NULL,
                              CLSCTX_INPROC_SERVER,
                              IID_IWinHttpRequest,
                              (void **)&pIWinHttpRequest);
    }
```

Exemplos de código obtidos da [Propriedade IWinHttpRequest:: status](iwinhttprequest-status.md).



## <a name="members"></a>Membros

O objeto **WinHttpRequest** tem estes tipos de membros:

-   [Eventos](#events)
-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="events"></a>Eventos

O objeto **WinHttpRequest** tem esses eventos.



| Evento                                                                            | Descrição                                                          |
|:---------------------------------------------------------------------------------|:---------------------------------------------------------------------|
| [**OnError**](iwinhttprequestevents-onerror.md)                                 | Ocorre quando há um erro em tempo de execução no aplicativo.<br/> |
| [**OnResponseDataAvailable**](iwinhttprequestevents-onresponsedataavailable.md) | Ocorre quando os dados estão disponíveis da resposta.<br/>          |
| [**OnResponseFinished**](iwinhttprequestevents-onresponsefinished.md)           | Ocorre quando os dados da resposta são concluídos.<br/>                |
| [**OnResponseStart**](iwinhttprequestevents-onresponsestart.md)                 | Ocorre quando os dados de resposta começam a ser recebidos.<br/>      |



 

### <a name="methods"></a>Métodos

O objeto **WinHttpRequest** tem esses métodos.



| Método                                                                 | Descrição                                                                                                                                                |
|:-----------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Anular**](iwinhttprequest-abort.md)                                 | Anula um método de [**envio**](iwinhttprequest-send.md) [WinHTTP](about-winhttp.md) .<br/>                                                              |
| [**GetAllResponseHeaders**](iwinhttprequest-getallresponseheaders.md) | Recupera todos os cabeçalhos de resposta HTTP.<br/>                                                                                                            |
| [**GetResponseHeader**](iwinhttprequest-getresponseheader.md)         | Recupera os cabeçalhos de resposta HTTP.<br/>                                                                                                            |
| [**Aberto**](iwinhttprequest-open.md)                                   | Abre uma conexão HTTP para um recurso HTTP.<br/>                                                                                                   |
| [**Enviar**](iwinhttprequest-send.md)                                   | Envia uma solicitação HTTP para um servidor HTTP.<br/>                                                                                                        |
| [**SetAutoLogonPolicy**](iwinhttprequest-setautologonpolicy.md)       | Define a [política de logon automático](authentication-in-winhttp.md)atual.<br/>                                                |
| [**SetClientCertificate**](iwinhttprequest-setclientcertificate.md)   | Seleciona um certificado de cliente para enviar a um servidor HTTPS (protocolo de transferência de hipertexto) seguro.<br/>                                                    |
| [**SetCredentials**](iwinhttprequest-setcredentials.md)               | Define as credenciais a serem usadas com um servidor HTTP como uma origem ou um servidor proxy.<br/>                                                             |
| [**SetProxy**](iwinhttprequest-setproxy.md)                           | Define informações do servidor proxy.<br/>                                                                                                                  |
| [**SetRequestHeader**](iwinhttprequest-setrequestheader.md)           | Adiciona, altera ou exclui um cabeçalho de solicitação HTTP.<br/>                                                                                               |
| [**Settempo_limites**](iwinhttprequest-settimeouts.md)                     | Especifica, em milissegundos, os componentes de tempo limite individuais de uma operação de envio/recebimento.<br/>                                                     |
| [**WaitForResponse**](iwinhttprequest-waitforresponse.md)             | Especifica o tempo de espera, em segundos, para que um método de [**envio**](iwinhttprequest-send.md) assíncrono seja concluído, com valor de tempo limite opcional.<br/> |



 

### <a name="properties"></a>Propriedades

O objeto **WinHttpRequest** tem essas propriedades.



| Propriedade                                                            | Tipo de acesso           | Descrição                                                                     |
|:--------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------|
| [**Opção**](iwinhttprequest-option.md)<br/>                 | Leitura/gravação<br/> | Define ou recupera um valor de opção de WinHTTP.<br/>                            |
| [**ResponseBody**](iwinhttprequest-responsebody.md)<br/>     | Somente leitura<br/>  | Recupera o corpo da entidade de resposta como uma matriz de bytes não assinados.<br/>    |
| [**ResponseStream**](iwinhttprequest-responsestream.md)<br/> | Somente leitura<br/>  | Recupera o corpo da entidade de resposta como um [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream).<br/> |
| [**ResponseText**](iwinhttprequest-responsetext.md)<br/>     | Somente leitura<br/>  | Recupera o corpo da entidade de resposta como texto.<br/>                          |
| [**Status**](iwinhttprequest-status.md)<br/>                 | Somente leitura<br/>  | Recupera o código de status HTTP da última resposta.<br/>               |
| [**StatusText**](iwinhttprequest-statustext.md)<br/>         | Somente leitura<br/>  | Recupera o texto de status HTTP.<br/>                                          |



 

## <a name="remarks"></a>Comentários

O objeto **WinHttpRequest** usa a interface [**IErrorInfo**](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-ierrorinfo) para fornecer dados de erro. Uma descrição e um valor numérico de erro podem ser obtidos com o objeto [Err](/previous-versions//sbf5ze0e(v=vs.85)) no Microsoft Visual Basic Scripting Edition (VBScript) e o objeto [Error](https://msdn.microsoft.com/library/dww52sbt.aspx) no Microsoft JScript. Os 16 bits inferiores de um número de erro correspondem aos valores encontrados em [**mensagens de erro**](error-messages.md).

> [!Note]  
> Para o Windows XP e o Windows 2000, consulte [requisitos de tempo de execução](winhttp-start-page.md).

 

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

[Versões do WinHTTP](winhttp-versions.md)
</dt> </dl>

 

