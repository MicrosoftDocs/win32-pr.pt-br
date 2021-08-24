---
description: As \_ constantes LINEADDRFEATURE listam as operações que podem ser invocadas em um endereço.
ms.assetid: dedeee7b-578b-4b19-8b99-5cd23779d661
title: Constantes de LINEADDRFEATURE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4bb545bdf0195d9fd8ed35833150b9cfd1f6b10bfbd3d1ead7e8ebff65c93132
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119682212"
---
# <a name="lineaddrfeature_-constants"></a>\_Constantes LINEADDRFEATURE

As **constantes \_ LINEADDRFEATURE** listam as operações que podem ser invocadas em um endereço.

<dl> <dt>

<span id="LINEADDRFEATURE_FORWARD"></span><span id="lineaddrfeature_forward"></span>**encaminhar LINEADDRFEATURE \_**
</dt> <dd> <dl> <dt>



O endereço pode ser encaminhado.


</dt> </dl> </dd> <dt>

<span id="LINEADDRFEATURE_MAKECALL"></span><span id="lineaddrfeature_makecall"></span>**LINEADDRFEATURE \_ MAKECALL**
</dt> <dd> <dl> <dt>



Uma chamada de saída pode ser colocada no endereço.


</dt> </dl> </dd> <dt>

<span id="LINEADDRFEATURE_PICKUP"></span><span id="lineaddrfeature_pickup"></span>**retirada de LINEADDRFEATURE \_**
</dt> <dd> <dl> <dt>



Uma chamada pode ser selecionada no endereço.


</dt> </dl> </dd> <dt>

<span id="LINEADDRFEATURE_PICKUPDIRECT"></span><span id="lineaddrfeature_pickupdirect"></span>**LINEADDRFEATURE \_ PICKUPDIRECT**
</dt> <dd> <dl> <dt>



A função [**linePickup**](/windows/desktop/api/Tapi/nf-tapi-linepickup) pode ser usada para pegar uma chamada em um endereço específico.


</dt> </dl> </dd> <dt>

<span id="LINEADDRFEATURE_PICKUPGROUP"></span><span id="lineaddrfeature_pickupgroup"></span>**LINEADDRFEATURE \_ pickup**
</dt> <dd> <dl> <dt>



A função [**linePickup**](/windows/desktop/api/Tapi/nf-tapi-linepickup) pode ser usada para pegar uma chamada no grupo.


</dt> </dl> </dd> <dt>

<span id="LINEADDRFEATURE_PICKUPHELD"></span><span id="lineaddrfeature_pickupheld"></span>**LINEADDRFEATURE \_ PICKUPHELD**
</dt> <dd> <dl> <dt>



A função [**linePickup**](/windows/desktop/api/Tapi/nf-tapi-linepickup) (com um endereço de destino **nulo** ) pode ser usada para pegar uma chamada que é mantida no endereço. Isso normalmente é usado apenas em uma organização exclusivamente em ponte.


</dt> </dl> </dd> <dt>

<span id="LINEADDRFEATURE_PICKUPWAITING"></span><span id="lineaddrfeature_pickupwaiting"></span>**LINEADDRFEATURE \_ PICKUPWAITING**
</dt> <dd> <dl> <dt>



A função [**linePickup**](/windows/desktop/api/Tapi/nf-tapi-linepickup) (com um endereço de destino **nulo** ) pode ser usada para pegar uma chamada em espera de chamada. Observe que isso não indica necessariamente que uma chamada em espera está realmente presente, porque geralmente é impossível para um dispositivo de telefonia detectar automaticamente tal chamada; no entanto, ele indica que a função Hook-flash será invocada para tentar alternar para tal chamada.


</dt> </dl> </dd> <dt>

<span id="LINEADDRFEATURE_SETMEDIACONTROL"></span><span id="lineaddrfeature_setmediacontrol"></span>**LINEADDRFEATURE \_ SETMEDIACONTROL**
</dt> <dd> <dl> <dt>



O controle de mídia pode ser definido nesse endereço.


</dt> </dl> </dd> <dt>

<span id="LINEADDRFEATURE_SETTERMINAL"></span><span id="lineaddrfeature_setterminal"></span>**LINEADDRFEATURE \_ SETterminal**
</dt> <dd> <dl> <dt>



Os modos de terminal para esse endereço podem ser definidos.


</dt> </dl> </dd> <dt>

<span id="LINEADDRFEATURE_SETUPCONF"></span><span id="lineaddrfeature_setupconf"></span>**LINEADDRFEATURE \_ SETUPCONF**
</dt> <dd> <dl> <dt>



Uma chamada de conferência com uma chamada inicial **nula** pode ser configurada nesse endereço.


</dt> </dl> </dd> <dt>

<span id="LINEADDRFEATURE_UNCOMPLETECALL"></span><span id="lineaddrfeature_uncompletecall"></span>**LINEADDRFEATURE \_ UNCOMPLETECALL**
</dt> <dd> <dl> <dt>



As solicitações de conclusão de chamada podem ser canceladas neste endereço.


</dt> </dl> </dd> <dt>

<span id="LINEADDRFEATURE_UNPARK"></span><span id="lineaddrfeature_unpark"></span>**LINEADDRFEATURE o \_ estacionamento**
</dt> <dd> <dl> <dt>



As chamadas podem ter o estacionamento anulado usando esse endereço.

> [!Note]  
> Se nenhum dos novos bits "PICKUP" modificados for definido no membro **dwAddressFeatures** em [**LINEADDRESSSTATUS**](/windows/desktop/api/Tapi/ns-tapi-lineaddressstatus) , mas o \_ bit de retirada LINEADDRFEATURE estiver definido, então qualquer um dos modos de retirada poderá funcionar; o provedor de serviços simplesmente não especificou quais deles.

 


</dt> </dl> </dd> <dt>

<span id="LINEADDRFEATURE_FORWARDDND"></span><span id="lineaddrfeature_forwarddnd"></span>**LINEADDRFEATURE \_ FORWARDDND**
</dt> <dd> <dl> <dt>



A função [**lineForward**](/windows/desktop/api/Tapi/nf-tapi-lineforward) (com um endereço de destino vazio) pode ser usada para ativar o recurso não incomodar no endereço. O LINEADDRFEATURE \_ Forward também será definido.


</dt> </dl> </dd> <dt>

<span id="LINEADDRFEATURE_FORWARDFWD"></span><span id="lineaddrfeature_forwardfwd"></span>**LINEADDRFEATURE \_ FORWARDFWD**
</dt> <dd> <dl> <dt>



A função [**lineForward**](/windows/desktop/api/Tapi/nf-tapi-lineforward) pode ser usada para encaminhar chamadas no endereço para outros números. O LINEADDRFEATURE \_ Forward também será definido.

> [!Note]  
> Se nenhum dos novos bits "encaminhar" modificados estiver definido no membro **dwAddressFeatures** em [**LINEADDRESSSTATUS**](/windows/desktop/api/Tapi/ns-tapi-lineaddressstatus) , mas o \_ bit de encaminhamento LINEADDRFEATURE estiver definido, qualquer um dos modos de encaminhamento poderá funcionar; o provedor de serviços simplesmente não especificou quais deles.

 


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Comentários

Sem extensibilidade. Todos os 32 bits são reservados.

Essa constante é usada em [**LINEADDRESSCAPS**](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps) (retornada por [**lineGetAddressCaps**](/windows/desktop/api/Tapi/nf-tapi-linegetaddresscaps)) e em [**LINEADDRESSSTATUS**](/windows/desktop/api/Tapi/ns-tapi-lineaddressstatus) (retornada por [**lineGetAddressStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetaddressstatus)). O **LINEADDRESSCAPS** relata a disponibilidade dos recursos de endereço pelo provedor de serviços (principalmente a opção) para um determinado endereço. Um aplicativo tornaria essa determinação quando ele for inicializado. Os relatórios de estrutura [**LINEADDRESSSTATUS**](/windows/desktop/api/Tapi/ns-tapi-lineaddressstatus) , para um determinado endereço, que os recursos de endereço podem realmente ser invocados enquanto o endereço está no estado atual. Um aplicativo tornaria essa determinação dinamicamente após as alterações de estado do endereço, geralmente causadas por atividades relacionadas à chamada no endereço.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|-----------------------------------------------------------------------------------|
| Versão da TAPI<br/> | Requer TAPI 2,0 ou posterior<br/>                                             |
| Cabeçalho<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**LINEADDRESSCAPS**](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps)
</dt> <dt>

[**LINEADDRESSSTATUS**](/windows/desktop/api/Tapi/ns-tapi-lineaddressstatus)
</dt> <dt>

[**lineForward**](/windows/desktop/api/Tapi/nf-tapi-lineforward)
</dt> <dt>

[**lineGetAddressCaps**](/windows/desktop/api/Tapi/nf-tapi-linegetaddresscaps)
</dt> <dt>

[**lineGetAddressStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetaddressstatus)
</dt> <dt>

[**linePickup**](/windows/desktop/api/Tapi/nf-tapi-linepickup)
</dt> </dl>

 

 




