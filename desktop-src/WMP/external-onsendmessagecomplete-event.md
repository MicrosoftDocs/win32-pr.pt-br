---
title: Evento external. OnSendMessageComplete
description: Observação Este tópico descreve a funcionalidade projetada para uso por lojas online. | Evento external. OnSendMessageComplete
ms.assetid: 9ae60aa5-4ecd-41dd-aeb0-afb1a3686982
keywords:
- Windows Media Player de evento external. OnSendMessageComplete
topic_type:
- apiref
api_name:
- External.OnSendMessageComplete Event
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a1dede59d2c52f20050a490e6ded1389e63884e598868e9736195280e3269a72
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119648726"
---
# <a name="externalonsendmessagecomplete-event"></a>Evento external. OnSendMessageComplete

> [!Note]  
> Este tópico descreve a funcionalidade projetada para uso por lojas online. Não há suporte para o uso dessa funcionalidade fora do contexto de uma loja online.

 

O evento **OnSendMessageComplete** ocorre quando o armazenamento online termina de processar uma mensagem. O script na página de descoberta enviou a mensagem anteriormente chamando [external. SendMessage](external-sendmessage.md).

``` syntax
window.external.OnSendMessageComplete = FunctionName
```

## <a name="possible-values"></a>Valores possíveis

essa é uma propriedade somente gravação que especifica o nome da função no script que Windows Media Player chama quando o evento ocorre.

## <a name="parameters"></a>Parâmetros

A função que manipula esse evento tem os parâmetros a seguir.

<dl> <dt>

<span id="Msg"></span><span id="msg"></span><span id="MSG"></span>*MSG*
</dt> <dd>

A mesma cadeia de caracteres que foi passada no parâmetro **msg** de **SendMessage**.

</dd> <dt>

<span id="Param"></span><span id="param"></span><span id="PARAM"></span>*Param*
</dt> <dd>

A mesma cadeia de caracteres que foi passada no parâmetro **param** de **SendMessage**.

</dd> <dt>

<span id="Result"></span><span id="result"></span><span id="RESULT"></span>*Disso*
</dt> <dd>

**Cadeia de caracteres** que contém o resultado da manipulação de mensagens. Consulte Observações.

</dd> </dl>

## <a name="remarks"></a>Comentários

O método **SendMessage** chama [IWMPContentPartner:: SendMessage](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-sendmessage), que retorna de forma assíncrona. Ou seja, ele retorna antes que a loja online termine de processar a mensagem. Quando o armazenamento online termina de processar a mensagem, ele chama [IWMPContentPartnerCallback:: SendMessageComplete](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-sendmessagecomplete), que, por sua vez, chama o manipulador de eventos **OnSendMessageComplete** do script.

Quando o armazenamento online chama **IWMPContentPartnerCallback:: SendMessageComplete**, ele fornece um código de resultado no parâmetro *bstrResult* . Windows Media Player não interpreta esse código de resultado. em vez disso, Windows Media Player passa o código de resultado ao manipulador de eventos **OnSendMessageComplete** no parâmetro de *resultado* .

Nenhum dos parâmetros (*msg*, *param*, *Result*) do manipulador de eventos **OnSendMessageComplete** é interpretado por Windows Media Player. Os parâmetros têm significado apenas para a loja online.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versão<br/> | Windows Media Player 11<br/>                                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objeto externo para repositórios online do tipo 1**](external-object-for-type-1-online-stores.md)
</dt> <dt>

[**External. sendMessage**](external-sendmessage.md)
</dt> <dt>

[**IWMPContentPartner:: SendMessage**](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-sendmessage)
</dt> <dt>

[**IWMPContentPartnerCallback::SendMessageComplete**](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-sendmessagecomplete)
</dt> </dl>

 

 





