---
description: A mensagem de \_ criação de telefone TAPI é enviada para informar os aplicativos sobre a criação de um novo dispositivo de telefone.
ms.assetid: 62895b10-76ce-456e-ad02-e2b7764616a8
title: Mensagem de PHONE_CREATE (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c92dfaad5d4007279f18890021f5cb39c22c4da9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105766966"
---
# <a name="phone_create-message"></a>\_Criar mensagem de telefone

A mensagem **de \_ criação de telefone** TAPI é enviada para informar os aplicativos sobre a criação de um novo dispositivo de telefone.


```C++
            
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hPhone* 
</dt> <dd>

Não utilizado.

</dd> <dt>

*dwCallbackInstance* 
</dt> <dd>

Não utilizado.

</dd> <dt>

*dwParam1* 
</dt> <dd>

O *hDeviceID* do dispositivo recém-criado.

</dd> <dt>

*dwParam2* 
</dt> <dd>

Não utilizado.

</dd> <dt>

*dwParam3* 
</dt> <dd>

Não utilizado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Sem valor de retorno.

## <a name="remarks"></a>Comentários

Os aplicativos que negociaram a versão 1,3 da API recebem uma mensagem de [**\_ estado do telefone**](phone-state.md) que especifica o \_ REinicialização de PHONESTATE, o que exige que eles desliguem o uso da API e chamem [**phoneInitialize**](/windows/desktop/api/Tapi/nf-tapi-phoneinitialize) novamente para obter o novo número de dispositivos. No entanto, a TAPI versão 1,4 e superior não exigem que todos os aplicativos sejam desligados antes de permitir que os aplicativos reinicialize; a reinicialização pode ocorrer imediatamente quando um novo dispositivo é criado.

Os aplicativos que dão suporte à TAPI versão 1,4 ou posterior são enviados para uma mensagem de **\_ criação de telefone** . Isso informa a existência do novo dispositivo e seu novo identificador de dispositivo. Em seguida, o aplicativo pode escolher se deseja ou não tentar trabalhar com o novo dispositivo a seu lazer.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|-----------------------------------------------------------------------------------|
| Versão da TAPI<br/> | Requer TAPI 2,0 ou posterior<br/>                                             |
| parâmetro<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Estado do telefone \_**](phone-state.md)
</dt> <dt>

[**phoneInitialize**](/windows/desktop/api/Tapi/nf-tapi-phoneinitialize)
</dt> <dt>

[**phoneInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-phoneinitializeexa)
</dt> </dl>

 

 




