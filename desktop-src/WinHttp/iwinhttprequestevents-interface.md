---
description: Fornece eventos para o Microsoft Windows HTTP Services (WinHTTP).
ms.assetid: 0721d7f9-2e84-41a9-be52-89c8d638eb90
title: Interface IWinHttpRequestEvents
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWinHttpRequestEvents
api_type:
- COM
api_location:
- HttpRequest.idl
ms.openlocfilehash: 3cdd0bf10c0d4bd75351ddaab6e88ce7182850fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105789728"
---
# <a name="iwinhttprequestevents-interface"></a>Interface IWinHttpRequestEvents

A interface **IWinHttpRequestEvents** fornece eventos para [o Microsoft Windows http Services (WinHTTP)](about-winhttp.md). Ele usa apenas métodos de evento.

## <a name="members"></a>Membros

A interface **IWinHttpRequestEvents** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IWinHttpRequestEvents** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **IWinHttpRequestEvents** tem esses métodos.



| Método                                                                           | Descrição                                                          |
|:---------------------------------------------------------------------------------|:---------------------------------------------------------------------|
| [**OnError**](iwinhttprequestevents-onerror.md)                                 | Ocorre quando há um erro em tempo de execução no aplicativo.<br/> |
| [**OnResponseDataAvailable**](iwinhttprequestevents-onresponsedataavailable.md) | Ocorre quando os dados estão disponíveis da resposta.<br/>          |
| [**OnResponseFinished**](iwinhttprequestevents-onresponsefinished.md)           | Ocorre quando os dados da resposta são concluídos.<br/>                |
| [**OnResponseStart**](iwinhttprequestevents-onresponsestart.md)                 | Ocorre quando os dados de resposta começam a ser recebidos.<br/>      |



 

## <a name="remarks"></a>Comentários

O procedimento a seguir descreve como registrar-se para notificações.

1.  Obtenha uma interface [IConnectionPointContainer](/windows/win32/api/ocidl/nn-ocidl-iconnectionpointcontainer) chamando **QueryInterface** em um objeto [**IWinHttpRequest**](iwinhttprequest-interface.md) .
2.  Chame [FindConnectionPoint](/windows/win32/api/ocidl/nf-ocidl-iconnectionpointcontainer-findconnectionpoint) na interface retornada e passe **\_ IWinHttpRequestEvents de IID** para *riid*.
3.  Chame [Advise](/windows/win32/api/ocidl/nf-ocidl-iconnectionpoint-advise) no ponto de conexão retornado e passe um ponteiro para uma interface **IUnknown** em um objeto que implementa **IWinHttpRequestEvents** para *punk*.

As notificações podem ser encerradas chamando [Unadvise](/windows/win32/api/ocidl/nf-ocidl-iconnectionpoint-unadvise) no ponto de conexão retornado na etapa 2.

Para exibir algum código que se registra para notificações COM, consulte a seção cliente do artigo [pontos de conexão com](/archive/msdn-magazine/2007/september/clr-inside-out-com-connection-points) .

> [!Note]  
> Para o Windows XP e o Windows 2000, consulte a seção [requisitos de tempo de execução](winhttp-start-page.md) da página inicial do WinHTTP.

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Somente Windows XP, Windows 2000 Professional com \[ aplicativos de área de trabalho do SP3\]<br/>            |
| Servidor mínimo com suporte<br/> | Windows Server 2003, Windows 2000 Server com aplicativos de área de trabalho do SP3 \[ somente\]<br/>         |
| Redistribuível<br/>          | WinHTTP 5,0 e Internet Explorer 5, 1 ou posterior no Windows XP e no Windows 2000.<br/> |
| INSERI<br/>                      | <dl> <dt>HttpRequest. idl</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IWinHttpRequest**](iwinhttprequest-interface.md)
</dt> <dt>

[Versões do WinHTTP](winhttp-versions.md)
</dt> </dl>

 

