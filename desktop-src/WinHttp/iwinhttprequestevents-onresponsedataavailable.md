---
description: Ocorre quando os dados estão disponíveis da resposta.
ms.assetid: 62d02e3b-466a-4d3d-994b-0a1ae12049e1
title: 'Evento IWinHttpRequestEvents:: OnResponseDataAvailable'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41cb2fbc680b1f6739a66bb68565188c8a5d78b4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105757346"
---
# <a name="iwinhttprequesteventsonresponsedataavailable-event"></a>Evento IWinHttpRequestEvents:: OnResponseDataAvailable

O evento **OnResponseDataAvailable** ocorre quando os dados estão disponíveis da resposta.

## <a name="syntax"></a>Sintaxe


```C++
void OnResponseDataAvailable(
  [in] SAFEARRAY(unsigned char) *Data
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Dados* \[ do no\]
</dt> <dd>

Uma matriz de bytes baseada em zero que recebe os dados de resposta recebidos pelo Microsoft Windows HTTP Services (WinHTTP) até o ponto em que esse evento ocorre. Esta é uma **variante** do tipo VT da \_ matriz \| VT \_ UI1.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse evento não retorna um valor.

## <a name="remarks"></a>Comentários

Como os dados estão em bytes, eles devem ser convertidos em caracteres largos quando colocados em uma cadeia de caracteres de caractere largo (Unicode).

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

 

 




