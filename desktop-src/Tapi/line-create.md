---
description: A mensagem TAPI \_ de criação de linha é enviada para informar o aplicativo sobre a criação de um novo dispositivo de linha.
ms.assetid: d4735eab-392f-49d9-a1d9-5895d9232624
title: Mensagem de LINE_CREATE (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd9973849c3942b5427dfb6b3fe7c47bc4d2a716
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105782908"
---
# <a name="line_create-message"></a>LINHA \_ criar mensagem

A mensagem TAPI de **\_ criação de linha** é enviada para informar o aplicativo sobre a criação de um novo dispositivo de linha.


```C++
            
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hDevice* 
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

Os aplicativos mais antigos (que negociaram a TAPI versão 1,3) recebem uma mensagem de [**\_ LINEDEVSTATE de linha**](line-linedevstate.md) ESPECIFICANDO LINEDEVSTATE \_ REINIT, o que exige que eles desliguem o uso da API e chamem [**lineInitialize**](/windows/desktop/api/Tapi/nf-tapi-lineinitialize) novamente para obter o novo número de dispositivos. No entanto, ao contrário das versões anteriores da TAPI, essa versão não exige que todos os aplicativos sejam desligados antes de permitir que os aplicativos reinicialize; a reinicialização pode ocorrer imediatamente quando um novo dispositivo é criado (o desligamento completo ainda é necessário quando um provedor de serviços é removido do sistema).

Os aplicativos que dão suporte à TAPI versão 1,4 ou posterior são enviados uma mensagem de **\_ criação de linha** . Isso informa a existência do novo dispositivo e seu novo identificador de dispositivo. Em seguida, o aplicativo pode escolher se deseja ou não tentar trabalhar com o novo dispositivo a seu lazer. Essa mensagem é enviada a todos os aplicativos que dão suporte a esta ou a versões subsequentes da API que chamaram [**lineInitialize**](/windows/desktop/api/Tapi/nf-tapi-lineinitialize) ou [**lineInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-lineinitializeexa), incluindo aquelas que não têm dispositivos de linha abertos no momento.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|-----------------------------------------------------------------------------------|
| Versão da TAPI<br/> | Requer TAPI 2,0 ou posterior<br/>                                             |
| parâmetro<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**LINEDEVSTATE de linha \_**](line-linedevstate.md)
</dt> <dt>

[**lineInitialize**](/windows/desktop/api/Tapi/nf-tapi-lineinitialize)
</dt> <dt>

[**lineInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-lineinitializeexa)
</dt> </dl>

 

 




