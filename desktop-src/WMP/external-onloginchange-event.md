---
title: Evento external. OnLoginChange
description: Observação Este tópico descreve a funcionalidade projetada para uso por lojas online. | Evento external. OnLoginChange
ms.assetid: 096794d5-977a-414f-8a98-b7998674c268
keywords:
- Windows Media Player de evento external. OnLoginChange
topic_type:
- apiref
api_name:
- External.OnLoginChange Event
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a0697aff759309bc3a988e6f24a024d5c05bd8ec27dae85921ee09d3847f3dfa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119648736"
---
# <a name="externalonloginchange-event"></a>Evento external. OnLoginChange

> [!Note]  
> Este tópico descreve a funcionalidade projetada para uso por lojas online. Não há suporte para o uso dessa funcionalidade fora do contexto de uma loja online.

 

O evento **OnLoginChange** ocorre quando o status de logon do usuário é alterado ou quando uma tentativa de logon falha.

``` syntax
window.external.OnLoginChange = FunctionName
```

## <a name="possible-values"></a>Valores possíveis

essa é uma propriedade somente gravação que especifica o nome da função no script que Windows Media Player chama quando o evento ocorre.

## <a name="parameters"></a>Parâmetros

A função que manipula esse evento não usa parâmetros.

## <a name="remarks"></a>Comentários

Esse evento ocorre toda vez que o plug-in do repositório online chama [IWMPContentPartnerCallback:: Notify](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-notify), passando wmpcnLoginStateChange no parâmetro de *tipo* . às vezes, o plug-in faz essa chamada para notificar Windows Media Player que houve uma alteração no estado de logon do usuário. Em outras ocasiões, o plug-in faz essa chamada para notificar o player que uma tentativa de fazer logon falhou. O parâmetro *pContext* do método **Notify** especifica se a notificação é para uma alteração de estado de logon ou para uma tentativa de logon com falha.

como cada chamada para `Notify(wmpcnLoginStateChange, ...)` faz com que Windows Media Player acionar o evento **OnLoginChange** , o manipulador de eventos **OnLoginChange** é chamado às vezes como resultado de uma alteração no estado de logon e, às vezes, como resultado de uma tentativa de logon com falha. Para determinar o estado de logon atual do usuário, o manipulador de eventos **OnLoginChange** deve chamar [external. userlogind](external-userloggedin.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versão<br/> | Windows Media Player 11<br/>                                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objeto externo para repositórios online do tipo 1**](external-object-for-type-1-online-stores.md)
</dt> <dt>

[**External. attemptLogin**](external-attemptlogin.md)
</dt> <dt>

[**External. userlogado**](external-userloggedin.md)
</dt> </dl>

 

 





