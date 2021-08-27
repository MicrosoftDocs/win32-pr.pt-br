---
description: O método Abort anula um método Send do WinHTTP.
ms.assetid: 8326feef-8611-4441-b52d-74855e6acfff
title: 'Método IWinHttpRequest:: Abort'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWinHttpRequest.Abort
- WinHttpRequest.Abort
api_type:
- COM
api_location:
- Winhttp.dll
ms.openlocfilehash: ca70917139059e8b0d038797ad61b137a259d615f6098a52bc86466f8054c7b4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120071766"
---
# <a name="iwinhttprequestabort-method"></a>Método IWinHttpRequest:: Abort

O método **Abort** anula um método [](about-winhttp.md) [**Send**](iwinhttprequest-send.md) do WinHTTP.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Abort();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

O valor de retorno será **S \_ OK** em caso de êxito ou um valor de erro, caso contrário.

## <a name="remarks"></a>Comentários

Você pode anular os métodos de [**envio**](iwinhttprequest-send.md) assíncronos e síncronos. Para anular um método [**Send**](iwinhttprequest-send.md) síncrono, você deve chamar **Abort** de dentro de um evento [**IWinHttpRequestEvents**](iwinhttprequestevents-interface.md) .

> [!Note]  
> para Windows XP e Windows 2000, consulte a seção [requisitos de tempo de execução](winhttp-start-page.md) da página inicial do WinHttp.

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows XP, Windows 2000 Professional somente com \[ aplicativos da área de trabalho do SP3\]<br/>            |
| Servidor mínimo com suporte<br/> | Windows servidor 2003, Windows 2000 servidor somente com \[ aplicativos de área de trabalho do SP3\]<br/>         |
| Redistribuível<br/>          | WinHTTP 5,0 e Internet Explorer 5, 1 ou posterior em Windows XP e Windows 2000.<br/> |
| INSERI<br/>                      | <dl> <dt>HttpRequest. idl</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>WinHTTP. lib</dt> </dl>     |
| DLL<br/>                      | <dl> <dt>Winhttp.dll</dt> </dl>     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IWinHttpRequest**](iwinhttprequest-interface.md)
</dt> <dt>

[**WinHttpRequest**](winhttprequest.md)
</dt> <dt>

[Versões do WinHTTP](winhttp-versions.md)
</dt> </dl>

 

 




