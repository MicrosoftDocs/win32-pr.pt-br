---
title: Método external. sendMessage
description: Observação Este tópico descreve a funcionalidade projetada para uso por lojas online. Não há suporte para o uso dessa funcionalidade fora do contexto de uma loja online. O método sendMessage envia uma mensagem para o plug-in da loja online.
ms.assetid: 72d34dcc-3284-4446-804f-0fc93a7d8dab
keywords:
- método sendMessage Windows Media Player
- método sendMessage Windows Media Player, classe externa
- classe externa Windows Media Player, método sendMessage
topic_type:
- apiref
api_name:
- External.sendMessage
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4985bae2f9170bdb0db1d6cdb995f2c14fe813bcb061485c179bc058539e84c9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119648356"
---
# <a name="externalsendmessage-method"></a>Método external. sendMessage

> [!Note]  
> Este tópico descreve a funcionalidade projetada para uso por lojas online. Não há suporte para o uso dessa funcionalidade fora do contexto de uma loja online.

 

O método **SendMessage** envia uma mensagem para o plug-in da loja online.

## <a name="syntax"></a>Sintaxe


```JScript
External.sendMessage(
  Msg,
  Param
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Mensagem* \[ no\]
</dt> <dd>

**Cadeia de caracteres** que contém a mensagem.

</dd> <dt>

*Parâmetro* \[ no\]
</dt> <dd>

**Cadeia de caracteres** que contém parâmetros associados à mensagem.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

A mensagem é enviada de forma assíncrona. Ou seja, esse método retorna imediatamente em vez de aguardar a mensagem ser processada. Quando o plug-in termina de processar a mensagem, ele chama o método [IWMPContentPartnerCallback:: SendMessageComplete](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-sendmessagecomplete) , que, por sua vez, chama o manipulador de eventos [OnSendMessageComplete](external-onsendmessagecomplete-event.md) do script.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versão<br/> | Windows Media Player 11.<br/>                                                |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objeto externo para repositórios online do tipo 1**](external-object-for-type-1-online-stores.md)
</dt> <dt>

[**External. OnSendMessageComplete**](external-onsendmessagecomplete-event.md)
</dt> <dt>

[**IWMPContentPartner:: SendMessage**](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-sendmessage)
</dt> <dt>

[**IWMPContentPartnerCallback::SendMessageComplete**](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-sendmessagecomplete)
</dt> </dl>

 

 





