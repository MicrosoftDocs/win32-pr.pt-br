---
description: As \_ constantes de sinalizador de bit LINEADDRESSSTATE descrevem vários itens de status de endereço.
ms.assetid: f06140d0-f41a-4228-93c5-21d609af5473
title: Constantes de LINEADDRESSSTATE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 483ac665c41989c65b43419442601dfb70667dc2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105788052"
---
# <a name="lineaddressstate_-constants"></a>\_Constantes LINEADDRESSSTATE

As constantes de sinalizador de bit **LINEADDRESSSTATE \_** descrevem vários itens de status de endereço.

<dl> <dt>

<span id="LINEADDRESSSTATE_CAPSCHANGE"></span><span id="lineaddressstate_capschange"></span>**LINEADDRESSSTATE \_ CAPSCHANGE**
</dt> <dd> <dl> <dt>



Indica que, devido a alterações de configuração feitas pelo usuário ou outras circunstâncias, um ou mais dos membros na estrutura [**LINEADDRESSCAPS**](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps) para o endereço foram alterados. O aplicativo deve usar [**lineGetAddressCaps**](/windows/desktop/api/Tapi/nf-tapi-linegetaddresscaps) para ler a estrutura atualizada. Se um provedor de serviços enviar uma mensagem [**\_ addressstate de linha**](line-addressstate.md) que contém esse valor para TAPI, a TAPI a passará para aplicativos que negociaram a TAPI versão 1,4 ou posterior; os aplicativos que negociam uma versão de API anterior receberão mensagens [**\_ LINEDEVSTATE de linha**](line-linedevstate.md) especificando LINEDEVSTATE \_ REINIT, exigindo que eles desliguem e reinicialize sua conexão com a TAPI para obter as informações atualizadas


</dt> </dl> </dd> <dt>

<span id="LINEADDRESSSTATE_DEVSPECIFIC"></span><span id="lineaddressstate_devspecific"></span>**LINEADDRESSSTATE \_ DEVSPECIFIC**
</dt> <dd> <dl> <dt>



O item específico do dispositivo do status do endereço foi alterado.


</dt> </dl> </dd> <dt>

<span id="LINEADDRESSSTATE_FORWARD"></span><span id="lineaddressstate_forward"></span>**encaminhar LINEADDRESSSTATE \_**
</dt> <dd> <dl> <dt>



O status de encaminhamento do endereço foi alterado, incluindo possivelmente o número de anéis para determinar uma condição de não resposta. O aplicativo deve verificar o status do endereço para determinar os detalhes sobre o status de encaminhamento atual do endereço.


</dt> </dl> </dd> <dt>

<span id="LINEADDRESSSTATE_INUSEMANY"></span><span id="lineaddressstate_inusemany"></span>**LINEADDRESSSTATE \_ INUSEMANY**
</dt> <dd> <dl> <dt>



O endereço monitorado ou com ponte mudou de sendo usado por uma estação para estar em uso por mais de uma estação.


</dt> </dl> </dd> <dt>

<span id="LINEADDRESSSTATE_INUSEONE"></span><span id="lineaddressstate_inuseone"></span>**LINEADDRESSSTATE \_ INUSEONE**
</dt> <dd> <dl> <dt>



O endereço mudou de ocioso ou em uso por muitas estações de ponte para estar em uso por apenas uma estação.


</dt> </dl> </dd> <dt>

<span id="LINEADDRESSSTATE_INUSEZERO"></span><span id="lineaddressstate_inusezero"></span>**LINEADDRESSSTATE \_ INUSEZERO**
</dt> <dd> <dl> <dt>



O endereço foi alterado para ocioso (ele não está em uso por nenhuma estação).


</dt> </dl> </dd> <dt>

<span id="LINEADDRESSSTATE_NUMCALLS"></span><span id="lineaddressstate_numcalls"></span>**LINEADDRESSSTATE \_ NUMCALLS**
</dt> <dd> <dl> <dt>



O número de chamadas no endereço foi alterado. Esse é o resultado de eventos como uma nova chamada de entrada, uma chamada de saída no endereço ou uma chamada que altera seu status de espera. Esse sinalizador aborda as alterações em qualquer um dos membros **dwNumActiveCalls**, **dwNumOnHoldCalls** e **dwNumOnHoldPendingCalls** na estrutura [**LINEADDRESSSTATUS**](/windows/desktop/api/Tapi/ns-tapi-lineaddressstatus) . O aplicativo deve verificar todos esses três membros ao receber uma mensagem de [**\_ endereço de linhastate**](line-addressstate.md) (numCalls).


</dt> </dl> </dd> <dt>

<span id="LINEADDRESSSTATE_OTHER"></span><span id="lineaddressstate_other"></span>**LINEADDRESSSTATE \_ outros**
</dt> <dd> <dl> <dt>



Os itens de status de endereço diferentes daqueles listados abaixo foram alterados. O aplicativo deve verificar o status do endereço atual para determinar quais itens foram alterados.


</dt> </dl> </dd> <dt>

<span id="LINEADDRESSSTATE_TERMINALS"></span><span id="lineaddressstate_terminals"></span>**\_terminais LINEADDRESSSTATE**
</dt> <dd> <dl> <dt>



As configurações de terminal para o endereço foram alteradas.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Comentários

Sem extensibilidade. Todos os 32 bits são reservados.

Um aplicativo é notificado sobre alterações nesses itens de status na [**mensagem \_ addressstate de linha**](line-addressstate.md) . Os recursos do dispositivo do endereço indicam quais alterações de estado de endereço podem possivelmente ser relatadas para esse endereço.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|-----------------------------------------------------------------------------------|
| Versão da TAPI<br/> | Requer TAPI 2,0 ou posterior<br/>                                             |
| parâmetro<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Endereço de LINHAstate \_**](line-addressstate.md)
</dt> <dt>

[**LINEDEVSTATE de linha \_**](line-linedevstate.md)
</dt> <dt>

[**LINEADDRESSCAPS**](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps)
</dt> <dt>

[**LINEADDRESSSTATUS**](/windows/desktop/api/Tapi/ns-tapi-lineaddressstatus)
</dt> <dt>

[**lineGetAddressCaps**](/windows/desktop/api/Tapi/nf-tapi-linegetaddresscaps)
</dt> </dl>

 

 




