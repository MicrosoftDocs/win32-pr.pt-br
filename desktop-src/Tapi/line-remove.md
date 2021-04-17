---
description: A mensagem de remoção de linha TAPI \_ é enviada para informar a um aplicativo sobre a remoção (exclusão do sistema) de um dispositivo de linha.
ms.assetid: 21b912d6-34aa-4ac0-b019-be3c851cc96d
title: Mensagem de LINE_REMOVE (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 567ead3ad2941845dd22405f0d8706eca74bfbd8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105766218"
---
# <a name="line_remove-message"></a>Mensagem de remoção de linha \_

A mensagem **de \_ remoção de linha** TAPI é enviada para informar a um aplicativo sobre a remoção (exclusão do sistema) de um dispositivo de linha. Em geral, isso não é usado para remoções temporárias, como a extração de dispositivos PCMCIA, mas apenas para remoções permanentes nas quais o dispositivo não seria mais relatado pelo provedor de serviços se a TAPI fosse reinicializada.


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

Identificador do dispositivo de linha que foi removido.

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

Os aplicativos que dão suporte à TAPI versão 2,0 ou posterior são enviados uma mensagem de **\_ remoção de linha** . Isso informa que o dispositivo foi removido do sistema. A mensagem de **\_ remoção de linha** é precedida por uma mensagem de [**\_ fechamento de linha**](line-close.md) em cada alça de linha, se o aplicativo tivesse a linha aberta. Essa mensagem é enviada para todos os aplicativos que dão suporte à TAPI versão 2,0 ou posterior que tenha chamado [**lineInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-lineinitializeexa), incluindo aqueles que não têm dispositivos de linha abertos no momento.

Os aplicativos mais antigos são enviados uma mensagem de [**\_ LINEDEVSTATE de linha**](line-linedevstate.md) especificando LINEDEVSTATE \_ removido, seguido por uma mensagem de fechamento de linha \_ . Ao contrário da mensagem de **\_ remoção de linha** , no entanto, esses aplicativos mais antigos podem receber essas mensagens somente se tiverem a linha aberta quando ela for removida. Se eles não tiverem a linha aberta, sua única indicação de que o dispositivo foi removido estaria recebendo um \_ erro NODEVICE LINEERR ao tentar acessar o dispositivo.

Depois que um dispositivo for removido, qualquer tentativa de acessar o dispositivo pelo identificador de dispositivo resultará em um \_ erro NOdevice do LINEERR. Depois que todos os aplicativos TAPI tiverem sido desligados para que a TAPI possa ser reiniciada e quando a TAPI for reinicializada, o dispositivo removido não ocupará mais um identificador de dispositivo.

> [!Note]  
> Implementação: é TAPI que retorna este LINEERR \_ nodevice; depois que uma mensagem de **\_ remoção de linha** é recebida de um provedor de serviços; nenhuma chamada adicional é feita ao provedor de serviços usando esse identificador de dispositivo de linha.

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|-----------------------------------------------------------------------------------|
| Versão da TAPI<br/> | Requer TAPI 2,0 ou posterior<br/>                                             |
| parâmetro<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**fechamento de linha \_**](line-close.md)
</dt> <dt>

[**LINEDEVSTATE de linha \_**](line-linedevstate.md)
</dt> <dt>

[**lineInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-lineinitializeexa)
</dt> </dl>

 

 




