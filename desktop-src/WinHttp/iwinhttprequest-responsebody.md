---
description: Recupera o corpo da entidade de resposta como uma matriz de bytes não assinados.
ms.assetid: 557913e0-9f19-42fc-bfca-9ed248972b4b
title: Propriedade IWinHttpRequest::ResponseBody
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWinHttpRequest.ResponseBody
- IWinHttpRequest.get_ResponseBody
- WinHttpRequest.ResponseBody
api_type:
- COM
api_location:
- Winhttp.dll
ms.openlocfilehash: 56eac42d41054cf7c01ff0c69ffcb82353db7182acf15765b25149560d5f7391
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118563224"
---
# <a name="iwinhttprequestresponsebody-property"></a>Propriedade IWinHttpRequest::ResponseBody

A **propriedade ResponseBody** recupera o corpo da entidade de resposta como uma matriz de bytes não assinados.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_ResponseBody(
  [out, retval] VARIANT *Body
);
```


```JScript

vtResponseBody = WinHttpRequest.ResponseBody
```





## <a name="property-value"></a>Valor da propriedade

Um **valor** Variant que recebe o corpo da entidade de resposta como uma matriz de bytes não assinados. Essa matriz contém os dados brutos recebidos diretamente do servidor.

## <a name="error-codes"></a>Códigos do Erro

O valor de retorno é **S \_ OK em** caso de êxito ou um valor de erro, caso contrário.

## <a name="remarks"></a>Comentários

Essa propriedade retorna os dados de resposta em uma matriz de bytes não assinados. Se a resposta não tiver um corpo de resposta, uma variante vazia será retornada. Essa propriedade só poderá ser invocada depois que [**o método Send**](iwinhttprequest-send.md) tiver sido chamado.

> [!Note]  
> Para obter mais informações sobre a implementação Windows XP e Windows 2000, consulte [Requisitos de tempo de execução.](winhttp-start-page.md)

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows XP, Windows 2000 Professional somente com aplicativos da área de trabalho SP3 \[\]<br/>            |
| Servidor mínimo com suporte<br/> | Windows Server 2003, Windows 2000 Server somente com aplicativos da área de trabalho SP3 \[\]<br/>         |
| Redistribuível<br/>          | WinHTTP 5.0 e Internet Explorer 5.01 ou posterior no Windows XP e Windows 2000.<br/> |
| Idl<br/>                      | <dl> <dt>HttpRequest.idl</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Winhttp.lib</dt> </dl>     |
| DLL<br/>                      | <dl> <dt>Winhttp.dll</dt> </dl>     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IWinHttpRequest**](iwinhttprequest-interface.md)
</dt> <dt>

[**WinHttpRequest**](winhttprequest.md)
</dt> <dt>

[**ResponseStream**](iwinhttprequest-responsestream.md)
</dt> <dt>

[**ResponseText**](iwinhttprequest-responsetext.md)
</dt> <dt>

[Versões do WinHTTP](winhttp-versions.md)
</dt> </dl>

 

 




