---
description: A \_ mensagem de remoção de telefone TAPI é enviada para informar a um aplicativo sobre a remoção (exclusão do sistema) de um dispositivo de telefone.
ms.assetid: 7c888976-65da-477a-b5a6-6e78d5f603b1
title: Mensagem de PHONE_REMOVE (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ab32ba8b8a8e003c5d87109dd2d0c9dbe98c236
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105760332"
---
# <a name="phone_remove-message"></a>\_Remover mensagem de telefone

A mensagem **de \_ remoção de telefone** TAPI é enviada para informar a um aplicativo sobre a remoção (exclusão do sistema) de um dispositivo de telefone. Em geral, isso não é usado para remoções temporárias, como a extração de dispositivos PCMCIA, mas apenas para remoções permanentes nas quais o dispositivo não seria mais relatado pelo provedor de serviços se a TAPI fosse reinicializada.


```C++
            
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hDevice* 
</dt> <dd>

Reservado. Definido como zero.

</dd> <dt>

*dwCallbackInstance* 
</dt> <dd>

Reservado. Definido como zero.

</dd> <dt>

*dwParam1* 
</dt> <dd>

Identificador do dispositivo de telefone que foi removido.

</dd> <dt>

*dwParam2* 
</dt> <dd>

Reservado. Definido como zero.

</dd> <dt>

*dwParam3* 
</dt> <dd>

Reservado. Definido como zero.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Sem valor de retorno.

## <a name="remarks"></a>Comentários

Os aplicativos da TAPI versão 2,0 ou posterior são enviados uma mensagem de **\_ remoção de telefone** . Isso informa que o dispositivo foi removido do sistema. A mensagem de **\_ remoção de telefone** é precedida por uma mensagem de [**\_ fechamento de telefone**](phone-close.md) em cada identificador de telefone, se o aplicativo tiver o telefone aberto. Essa mensagem é enviada para todos os aplicativos que dão suporte à TAPI versão 2,0 ou posterior que tenha chamado [**phoneInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-phoneinitializeexa), incluindo aqueles que não têm dispositivos de telefone abertos no momento.

Os aplicativos mais antigos (que negociaram a TAPI versão 1,4 ou anterior) recebem uma mensagem de [**\_ estado de telefone**](phone-state.md) que especifica o PHONESTATE \_ removido, seguido por uma mensagem de [**\_ fechamento de telefone**](phone-close.md) . Ao contrário da mensagem de **\_ remoção de telefone** , no entanto, esses aplicativos mais antigos podem receber essas mensagens somente se tiverem o telefone aberto quando ele for removido. Se eles não tiverem o telefone aberto, sua única indicação de que o dispositivo foi removido estaria recebendo um PHONEERR \_ nodevice quando ele tentar acessar o dispositivo.

Depois que um dispositivo for removido, qualquer tentativa de acessar o dispositivo pelo identificador de dispositivo resultará em um \_ erro NOdevice do PHONEERR. Depois que todos os aplicativos TAPI tiverem sido desligados para que a TAPI possa ser reiniciada e quando a TAPI for reinicializada, o dispositivo removido não ocupará mais um identificador de dispositivo.

> [!Note]  
> Implementação: é a TAPI que retorna essa mensagem do PHONEERR \_ nodevice depois que uma \_ mensagem de remoção de telefone é recebida de um provedor de serviços; nenhuma chamada adicional é feita ao provedor de serviços usando esse identificador de dispositivo de telefone.

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|-----------------------------------------------------------------------------------|
| Versão da TAPI<br/> | Requer TAPI 2,0 ou posterior<br/>                                             |
| parâmetro<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_fechar telefone**](phone-close.md)
</dt> <dt>

[**Estado do telefone \_**](phone-state.md)
</dt> <dt>

[**phoneInitialize**](/windows/desktop/api/Tapi/nf-tapi-phoneinitialize)
</dt> <dt>

[**phoneInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-phoneinitializeexa)
</dt> </dl>

 

 




