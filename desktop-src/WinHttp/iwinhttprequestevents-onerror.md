---
description: Ocorre quando há um erro em tempo de execução no aplicativo.
ms.assetid: d99400a4-3661-4162-bfd6-8c2a27e0f328
title: 'Evento IWinHttpRequestEvents:: OnError'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c8582deec90eb6bfc2985460f3127d5c7ee9c01b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922672"
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

## <a name="return-value"></a>Retornar valor

Esse evento não retorna um valor.

## <a name="remarks"></a>Comentários

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

[**IWinHttpRequestEvents**](iwinhttprequestevents-interface.md)
</dt> <dt>

[**WinHttpRequest**](winhttprequest.md)
</dt> <dt>

[Versões do WinHTTP](winhttp-versions.md)
</dt> </dl>

 

 




