---
description: A mensagem do botão de telefone TAPI \_ é enviada para notificar o aplicativo de que o monitoramento de pressionamento de botão está habilitado caso tenha detectado um pressionamento de botão no telefone local.
ms.assetid: fe47eed7-89d1-488b-b945-9e1aedc1f63c
title: Mensagem de PHONE_BUTTON (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2da810630a937f8415e070373f359dca06a694e6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105757201"
---
# <a name="phone_button-message"></a>\_Mensagem do botão telefone

A mensagem **do \_ botão de telefone** TAPI é enviada para notificar o aplicativo de que o monitoramento de pressionamento de botão está habilitado caso tenha detectado um pressionamento de botão no telefone local.


```C++
            
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hPhone* 
</dt> <dd>

Um identificador para o dispositivo de telefone.

</dd> <dt>

*dwCallbackInstance* 
</dt> <dd>

A instância de retorno de chamada do aplicativo fornecida ao abrir o dispositivo de telefone.

</dd> <dt>

*dwParam1* 
</dt> <dd>

O identificador de botão/lâmpada do botão que foi pressionado. Observe que os identificadores de botão de zero a 11 são sempre os botões do teclado, sendo que ' 0 ' é o identificador de botão zero, ' 1 ', sendo o identificador de botão 1 (e assim por diante, por meio do identificador de botão 9) e com ' \* ' sendo o identificador de botão 10 e ' \# ' sendo o identificador de botão 11. Informações adicionais sobre um identificador de botão estão disponíveis com [**phoneGetDevCaps**](/windows/desktop/api/Tapi/nf-tapi-phonegetdevcaps) e [**phoneGetButtonInfo**](/windows/desktop/api/Tapi/nf-tapi-phonegetbuttoninfo).

</dd> <dt>

*dwParam2* 
</dt> <dd>

O modo de botão do botão. Esse parâmetro usa uma das [**\_ constantes PHONEBUTTONMODE**](phonebuttonmode--constants.md).

</dd> <dt>

*dwParam3* 
</dt> <dd>

Especifica se este é um evento de botão suspenso ou um evento de botão. Esse parâmetro usa uma das [**\_ constantes PHONEBUTTONSTATE**](phonebuttonstate--constants.md).

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Sem valor de retorno.

## <a name="remarks"></a>Comentários

Uma mensagem de **\_ botão de telefone** é enviada sempre que um botão muda de estado. Um aplicativo tem a garantia de que, para cada evento de botão abaixo, ele é eventualmente enviado um evento de botão correspondente. Um provedor de serviços que é incapaz de detectar o botão real é necessário para gerar a mensagem de botão para cima logo após a mensagem do botão para baixo para cada pressionamento de botão.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|-----------------------------------------------------------------------------------|
| Versão da TAPI<br/> | Requer TAPI 2,0 ou posterior<br/>                                             |
| parâmetro<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**phoneGetButtonInfo**](/windows/desktop/api/Tapi/nf-tapi-phonegetbuttoninfo)
</dt> <dt>

[**phoneGetDevCaps**](/windows/desktop/api/Tapi/nf-tapi-phonegetdevcaps)
</dt> </dl>

 

 




