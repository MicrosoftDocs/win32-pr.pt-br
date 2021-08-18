---
description: Ocorre quando os dados da resposta são concluídos.
ms.assetid: 0df2031e-826f-436e-a689-201fa8b5c38f
title: 'Evento IWinHttpRequestEvents:: OnResponseFinished'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2114135c17f3e2eb2f9d60a7044f7441271f257fe099de31ea70c6030de769df
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117744246"
---
# <a name="iwinhttprequesteventsonresponsefinished-event"></a>Evento IWinHttpRequestEvents:: OnResponseFinished

O evento **OnResponseFinished** ocorre quando os dados da resposta são concluídos.

## <a name="syntax"></a>Sintaxe


```C++
void OnResponseFinished();
```



## <a name="parameters"></a>Parâmetros

Este evento não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Esse evento não retorna um valor.

## <a name="remarks"></a>Comentários

Esse evento sinaliza que todos os dados de resposta que pertencem à solicitação mais recente foram recebidos. [**OnResponseDataAvailable**](iwinhttprequestevents-onresponsedataavailable.md) não ocorre novamente até a próxima solicitação.

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

 

 




