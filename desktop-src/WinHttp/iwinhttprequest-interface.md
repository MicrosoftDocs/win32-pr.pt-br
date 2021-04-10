---
description: A interface IWinHttpRequest fornece todos os métodos não uniformes para o Microsoft Windows HTTP Services (WinHTTP).
ms.assetid: 6417b3b5-b74a-4c7b-acf9-87e2e814a4df
title: Interface IWinHttpRequest
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWinHttpRequest
api_type:
- COM
api_location:
- Winhttp.dll
ms.openlocfilehash: 77ebc8947ad36d2dc9efba121cdd6da2d6de359b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104169816"
---
# <a name="iwinhttprequest-interface"></a>Interface IWinHttpRequest

A interface **IWinHttpRequest** fornece todos os métodos não uniformes para [o Microsoft Windows http Services (WinHTTP)](about-winhttp.md).

## <a name="members"></a>Membros

A interface **IWinHttpRequest** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IWinHttpRequest** também tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

A interface **IWinHttpRequest** tem esses métodos.



| Método                                                                 | Descrição                                                                                                                             |
|:-----------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------|
| [**Anular**](iwinhttprequest-abort.md)                                 | Anula um método de [**envio**](iwinhttprequest-send.md) [WinHTTP](about-winhttp.md) .<br/>                                           |
| [**GetAllResponseHeaders**](iwinhttprequest-getallresponseheaders.md) | Recupera todos os cabeçalhos de resposta HTTP.<br/>                                                                                         |
| [**GetResponseHeader**](iwinhttprequest-getresponseheader.md)         | Recupera os cabeçalhos de resposta HTTP.<br/>                                                                                         |
| [**Aberto**](iwinhttprequest-open.md)                                   | Abre uma conexão HTTP para um recurso HTTP.<br/>                                                                                |
| [**Enviar**](iwinhttprequest-send.md)                                   | Envia uma solicitação HTTP para um servidor HTTP.<br/>                                                                                     |
| [**SetAutoLogonPolicy**](iwinhttprequest-setautologonpolicy.md)       | Define a [política de logon automático](authentication-in-winhttp.md)atual.<br/>                             |
| [**SetClientCertificate**](iwinhttprequest-setclientcertificate.md)   | Seleciona um certificado de cliente para enviar a um servidor HTTPS (protocolo de transferência de hipertexto) seguro.<br/>                                 |
| [**SetCredentials**](iwinhttprequest-setcredentials.md)               | Define as credenciais a serem usadas com um servidor HTTP, um servidor proxy ou um servidor de origem.<br/>                             |
| [**SetProxy**](iwinhttprequest-setproxy.md)                           | Define informações do servidor proxy.<br/>                                                                                               |
| [**SetRequestHeader**](iwinhttprequest-setrequestheader.md)           | Adiciona, altera ou exclui um cabeçalho de solicitação HTTP.<br/>                                                                            |
| [**Settempo_limites**](iwinhttprequest-settimeouts.md)                     | Especifica os componentes de tempo limite individuais de uma operação de envio/recebimento, em milissegundos.<br/>                                   |
| [**WaitForResponse**](iwinhttprequest-waitforresponse.md)             | Aguarda a conclusão de um método [**Send**](iwinhttprequest-send.md) assíncrono, com valor de tempo limite opcional, em segundos.<br/> |



 

### <a name="properties"></a>Propriedades

A interface **IWinHttpRequest** tem essas propriedades.



| Propriedade                                                            | Tipo de acesso           | Descrição                                                           |
|:--------------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------|
| [**Opção**](iwinhttprequest-option.md)<br/>                 | Leitura/gravação<br/> | Um valor de opção de WinHTTP.<br/>                                    |
| [**ResponseBody**](iwinhttprequest-responsebody.md)<br/>     | Somente leitura<br/>  | O corpo da entidade de resposta como uma matriz de bytes não assinados.<br/>    |
| [**ResponseStream**](iwinhttprequest-responsestream.md)<br/> | Somente leitura<br/>  | O corpo da entidade de resposta como um [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream).<br/> |
| [**ResponseText**](iwinhttprequest-responsetext.md)<br/>     | Somente leitura<br/>  | O corpo da entidade de resposta.<br/>                                  |
| [**Status**](iwinhttprequest-status.md)<br/>                 | Somente leitura<br/>  | O código de status HTTP da última resposta.<br/>               |
| [**StatusText**](iwinhttprequest-statustext.md)<br/>         | Somente leitura<br/>  | O texto de status HTTP.<br/>                                      |



 

## <a name="remarks"></a>Comentários

A interface **IWinHttpRequest** definida em HttpRequest. idl é implementada por uma classe com ID de **CLSID \_ WinHttpRequest**. Um aplicativo obtém essa interface chamando [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) com uma ID de classe de **CLSID \_ WinHttpRequest** e uma ID de interface **de \_ IWinHttpRequest de IID**.

> [!Note]  
> Para o Windows XP e o Windows 2000, consulte a seção [requisitos de tempo de execução](winhttp-start-page.md) da página inicial do WinHTTP.

 

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

[**IWinHttpRequestEvents**](iwinhttprequestevents-interface.md)
</dt> <dt>

[Versões do WinHTTP](winhttp-versions.md)
</dt> </dl>

 

