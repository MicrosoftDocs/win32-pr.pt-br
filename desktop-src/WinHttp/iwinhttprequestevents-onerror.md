---
description: Ocorre quando há um erro em tempo de execução no aplicativo.
ms.assetid: d99400a4-3661-4162-bfd6-8c2a27e0f328
title: 'Evento IWinHttpRequestEvents:: OnError'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 31127dcc3155b804bbda1c3ab94ee8a410c73f5a96c3ecfc6f787479ccd51539
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117744334"
---
# <a name="iwinhttprequesteventsonerror-event"></a>Evento IWinHttpRequestEvents:: OnError

O evento **OnError** ocorre quando há um erro em tempo de execução no aplicativo.

## <a name="syntax"></a>Sintaxe


```C++
void OnError(
  [in] long ErrorNumber,
  [in] BSTR ErrorDescription
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ErrorNumber* \[ no\]
</dt> <dd>

Recebe o valor numérico do erro. Os 16 bits inferiores desse número de erro correspondem a um dos erros listados em [**mensagens de erro**](error-messages.md).

</dd> <dt>

*ErrorDescription* \[ no\]
</dt> <dd>

Especifica uma breve descrição do erro que ocorreu.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse evento não retorna um valor.

## <a name="remarks"></a>Comentários

> [!Note]  
> para Windows XP e Windows 2000, consulte a seção [requisitos de tempo de execução](winhttp-start-page.md) da página inicial do WinHTTP.

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows XP, Windows 2000 Professional somente com \[ aplicativos da área de trabalho do SP3\]<br/>            |
| Servidor mínimo com suporte<br/> | Windows servidor 2003, Windows 2000 servidor somente com \[ aplicativos de área de trabalho do SP3\]<br/>         |
| Redistribuível<br/>          | WinHTTP 5,0 e Internet Explorer 5, 1 ou posterior em Windows XP e Windows 2000.<br/> |
| INSERI<br/>                      | <dl> <dt>HttpRequest. idl</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IWinHttpRequestEvents**](iwinhttprequestevents-interface.md)
</dt> <dt>

[**WinHttpRequest**](winhttprequest.md)
</dt> <dt>

[Versões do WinHTTP](winhttp-versions.md)
</dt> </dl>

 

 




