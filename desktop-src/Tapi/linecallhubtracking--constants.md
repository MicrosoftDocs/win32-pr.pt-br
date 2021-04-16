---
description: As \_ constantes de sinalizador de bit LINECALLHUBTRACKING descrevem o tipo de rastreamento de Hub de chamada fornecido.
ms.assetid: ad3c8d2e-f074-4db0-bb72-fb2181cbf687
title: Constantes de LINECALLHUBTRACKING_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9bfae61e36551a7d186408c2c87e0727503540a5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105758402"
---
# <a name="linecallhubtracking_-constants"></a>\_Constantes LINECALLHUBTRACKING

As constantes de sinalizador de bit **LINECALLHUBTRACKING \_** descrevem o tipo de rastreamento de Hub de chamada fornecido.

<dl> <dt>

<span id="LINECALLHUBTRACKING_ALLCALLS"></span><span id="linecallhubtracking_allcalls"></span>**LINECALLHUBTRACKING de \_ chamadas**
</dt> <dd> <dl> <dt>



O controle do hub de chamadas é fornecido no nível de chamada.


</dt> </dl> </dd> <dt>

<span id="LINECALLHUBTRACKING_NONE"></span><span id="linecallhubtracking_none"></span>**LINECALLHUBTRACKING \_ nenhum**
</dt> <dd> <dl> <dt>



Nenhum controle de Hub de chamadas é fornecido.


</dt> </dl> </dd> <dt>

<span id="LINECALLHUBTRACKING_PROVIDERLEVEL"></span><span id="linecallhubtracking_providerlevel"></span>**LINECALLHUBTRACKING \_ PROVIDERLEVEL**
</dt> <dd> <dl> <dt>



Os hubs de chamadas são controlados no nível do provedor de serviço. As alterações de chamada por chamada não são relatadas.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Comentários

Sem extensibilidade. Todos os 32 bits são reservados.

Quando ocorrem alterações nessa estrutura de dados, uma mensagem de [**\_ CALLINFO de linha**](line-callinfo.md) é enviada para o aplicativo. Os parâmetros para essa mensagem são um identificador para a chamada e uma indicação do item de informações que foi alterado. A estrutura de dados [**LINECALLHUBTRACKINGINFO**](/windows/desktop/api/Tapi/ns-tapi-linecallhubtrackinginfo) indica qual tipo de rastreamento é fornecido.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|-----------------------------------------------------------------------------------|
| Versão da TAPI<br/> | Requer TAPI 2,2<br/>                                                      |
| parâmetro<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**CALLINFO de linha \_**](line-callinfo.md)
</dt> <dt>

[**LINECALLHUBTRACKINGINFO**](/windows/desktop/api/Tapi/ns-tapi-linecallhubtrackinginfo)
</dt> <dt>

[**LINECALLINFO**](/windows/desktop/api/Tapi/ns-tapi-linecallinfo)
</dt> </dl>

 

 




