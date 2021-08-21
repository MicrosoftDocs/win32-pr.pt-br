---
description: A mensagem TAPI PHONE BUTTON é enviada para notificar o aplicativo de que o monitoramento de pressionamento de botão está habilitado se tiver detectado um pressionamento de botão \_ no telefone local.
ms.assetid: fe47eed7-89d1-488b-b945-9e1aedc1f63c
title: PHONE_BUTTON mensagem (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aec64f754725e5926a8cab1d98b25e4cb379a444bf4208d6e8f3e976dafee82f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120072996"
---
# <a name="phone_button-message"></a>Mensagem PHONE \_ BUTTON

A mensagem TAPI **PHONE \_ BUTTON** é enviada para notificar o aplicativo de que o monitoramento de pressionamento de botão está habilitado se tiver detectado um pressionamento de botão no telefone local.


```C++
            
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hPhone* 
</dt> <dd>

Um alça para o dispositivo de telefone.

</dd> <dt>

*dwCallbackInstance* 
</dt> <dd>

A instância de retorno de chamada do aplicativo fornecida ao abrir o dispositivo de telefone.

</dd> <dt>

*Dwparam1* 
</dt> <dd>

O identificador de botão/lâmpada do botão que foi pressionado. Observe que os identificadores de botão zero a 11 são sempre os botões KEYPAD, com '0' sendo o identificador de botão zero, '1' sendo o identificador de botão 1 (e assim por diante por meio do identificador de botão 9) e com ' sendo identificador de botão 10 e ' sendo identificador de botão \* \# 11. Informações adicionais sobre um identificador de botão estão disponíveis com [**phoneGetDevCaps**](/windows/desktop/api/Tapi/nf-tapi-phonegetdevcaps) e [**phoneGetButtonInfo.**](/windows/desktop/api/Tapi/nf-tapi-phonegetbuttoninfo)

</dd> <dt>

*Dwparam2* 
</dt> <dd>

O modo de botão do botão. Esse parâmetro usa uma das [**\_ constantes PHONEBUTTONMODE**](phonebuttonmode--constants.md).

</dd> <dt>

*dwParam3* 
</dt> <dd>

Especifica se este é um evento de botão para baixo ou um evento de botão para cima. Esse parâmetro usa uma das [**\_ constantes PHONEBUTTONSTATE**](phonebuttonstate--constants.md).

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Sem valor de retorno.

## <a name="remarks"></a>Comentários

Uma **mensagem PHONE \_ BUTTON** é enviada sempre que um botão altera o estado. Um aplicativo tem a garantia de que, para cada evento de botão para baixo, ele é eventualmente enviado um evento de botão correspondente para cima. Um provedor de serviços que não consegue detectar o botão real para cima é necessário para gerar a mensagem de botão para cima logo após a mensagem de botão para baixo para cada pressionamento de botão.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|-----------------------------------------------------------------------------------|
| Versão do TAPI<br/> | Requer TAPI 2.0 ou posterior<br/>                                             |
| Cabeçalho<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**phoneGetButtonInfo**](/windows/desktop/api/Tapi/nf-tapi-phonegetbuttoninfo)
</dt> <dt>

[**Phonegetdevcaps**](/windows/desktop/api/Tapi/nf-tapi-phonegetdevcaps)
</dt> </dl>

 

 




