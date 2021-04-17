---
description: Ocorre quando os dados de resposta começam a ser recebidos.
ms.assetid: 7245725b-40dd-4282-b681-f0b2c191db94
title: 'Evento IWinHttpRequestEvents:: OnResponseStart'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a299c535dd854bff07f2c24989096f7b9e49fc3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105782675"
---
# <a name="iwinhttprequesteventsonresponsestart-event"></a>Evento IWinHttpRequestEvents:: OnResponseStart

O evento **OnResponseStart** ocorre quando os dados de resposta começam a ser recebidos.

## <a name="syntax"></a>Sintaxe


```C++
void OnResponseStart(
  [in] long Status,
  [in] BSTR ContentType
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Status* \[ do no\]
</dt> <dd>

Recebe o código de status padrão retornado com os dados de resposta. Os códigos de status são definidos no [RFC 2616](https://www.ietf.org/rfc/rfc2616.txt).

</dd> <dt>

*ContentType* \[ no\]
</dt> <dd>

Especifica o tipo de conteúdo recebido, como "texto/HTML" ou "imagem/GIF".

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse evento não retorna um valor.

## <a name="remarks"></a>Comentários

Para que esse evento ocorra, use [**abrir**](iwinhttprequest-open.md) para enviar uma conexão http no modo assíncrono e use [**Enviar**](iwinhttprequest-send.md) para enviar uma solicitação de dados a um servidor de Internet.

Esse é o primeiro evento WinHTTP a ocorrer após o [**envio**](iwinhttprequest-send.md).

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

 

 




