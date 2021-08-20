---
description: Ocorre quando os dados estão disponíveis na resposta.
ms.assetid: 62d02e3b-466a-4d3d-994b-0a1ae12049e1
title: Evento IWinHttpRequestEvents::OnResponseDataAvailable
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 12b55f87584164a47b47920caf961f02f0bd9cc6596c4c90f76f381027af545e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118114240"
---
# <a name="iwinhttprequesteventsonresponsedataavailable-event"></a>Evento IWinHttpRequestEvents::OnResponseDataAvailable

O **evento OnResponseDataAvailable** ocorre quando os dados estão disponíveis na resposta.

## <a name="syntax"></a>Sintaxe


```C++
void OnResponseDataAvailable(
  [in] SAFEARRAY(unsigned char) *Data
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Dados* \[ Em\]
</dt> <dd>

Uma matriz de bytes baseada em zero que recebe os dados de resposta recebidos pelo Microsoft Windows HTTP Services (WinHTTP) até o ponto em que esse evento ocorre. Essa é uma **VARIANTE do** tipo VT \_ ARRAY \| VT \_ UI1.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse evento não retorna um valor.

## <a name="remarks"></a>Comentários

Como os dados estão em bytes, eles devem ser convertidos em caracteres largos quando colocados em uma cadeia de caracteres largos (Unicode).

> [!Note]  
> Para Windows XP e Windows 2000, consulte [](winhttp-start-page.md) a seção Requisitos de tempo de executar da página inicial do WinHTTP.

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows XP, Windows 2000 Professional somente com aplicativos da área de trabalho SP3 \[\]<br/>            |
| Servidor mínimo com suporte<br/> | Windows Server 2003, Windows 2000 Server com somente aplicativos da área de trabalho SP3 \[\]<br/>         |
| Redistribuível<br/>          | WinHTTP 5.0 e Internet Explorer 5.01 ou posterior no Windows XP e Windows 2000.<br/> |
| Idl<br/>                      | <dl> <dt>HttpRequest.idl</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IWinHttpRequestEvents**](iwinhttprequestevents-interface.md)
</dt> <dt>

[**WinHttpRequest**](winhttprequest.md)
</dt> <dt>

[Versões do WinHTTP](winhttp-versions.md)
</dt> </dl>

 

 




