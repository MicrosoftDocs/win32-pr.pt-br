---
title: Evento external. OnLoginChange
description: Observação Este tópico descreve a funcionalidade projetada para uso por lojas online. | Evento external. OnLoginChange
ms.assetid: 096794d5-977a-414f-8a98-b7998674c268
keywords:
- Evento external. OnLoginChange do Windows Media Player
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
ms.openlocfilehash: 9b7d54da86ffdde896a44580567b0cd381725d5e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105760437"
---
# <a name="externalonloginchange-event"></a>Evento external. OnLoginChange

> [!Note]  
> Este tópico descreve a funcionalidade projetada para uso por lojas online. Não há suporte para o uso dessa funcionalidade fora do contexto de uma loja online.

 

O evento **OnLoginChange** ocorre quando o status de logon do usuário é alterado ou quando uma tentativa de logon falha.

``` syntax
window.external.OnLoginChange = FunctionName
```

## <a name="possible-values"></a>Valores possíveis

Essa é uma propriedade somente gravação que especifica o nome da função no script que o Windows Media Player chama quando o evento ocorre.

## <a name="parameters"></a>Parâmetros

A função que manipula esse evento não usa parâmetros.

## <a name="remarks"></a>Comentários

Esse evento ocorre toda vez que o plug-in do repositório online chama [IWMPContentPartnerCallback:: Notify](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-notify), passando wmpcnLoginStateChange no parâmetro de *tipo* . Às vezes, o plug-in faz essa chamada para notificar o Windows Media Player de que houve uma alteração no estado de logon do usuário. Em outras ocasiões, o plug-in faz essa chamada para notificar o player que uma tentativa de fazer logon falhou. O parâmetro *pContext* do método **Notify** especifica se a notificação é para uma alteração de estado de logon ou para uma tentativa de logon com falha.

Como cada chamada para `Notify(wmpcnLoginStateChange, ...)` faz com que o Windows Media Player gere o evento **OnLoginChange** , o manipulador de eventos **OnLoginChange** é chamado às vezes como resultado de uma alteração no estado de logon e, às vezes, do resultado de uma tentativa de logon com falha. Para determinar o estado de logon atual do usuário, o manipulador de eventos **OnLoginChange** deve chamar [external. userlogind](external-userloggedin.md).

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

 

 





