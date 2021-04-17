---
description: As \_ constantes LINECALLORIGIN descrevem a origem de uma chamada.
ms.assetid: b830a40e-62d9-4a6c-b43f-8318f30a7cd4
title: Constantes de LINECALLORIGIN_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f00495d67dcff56ef7ee34cd85600a281e006ec3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105766216"
---
# <a name="linecallorigin_-constants"></a>\_Constantes LINECALLORIGIN

As **constantes \_ LINECALLORIGIN** descrevem a origem de uma chamada.

<dl> <dt>

<span id="LINECALLORIGIN_CONFERENCE"></span><span id="linecallorigin_conference"></span>**\_conferência LINECALLORIGIN**
</dt> <dd> <dl> <dt>



O identificador de chamada é para uma chamada de conferência, ou seja, a conexão do aplicativo com a ponte de conferência no comutador.


</dt> </dl> </dd> <dt>

<span id="LINECALLORIGIN_EXTERNAL"></span><span id="linecallorigin_external"></span>**LINECALLORIGIN \_ externo**
</dt> <dd> <dl> <dt>



A chamada foi originada como uma chamada de entrada em uma linha externa.


</dt> </dl> </dd> <dt>

<span id="LINECALLORIGIN_INBOUND"></span><span id="linecallorigin_inbound"></span>**LINECALLORIGIN de \_ entrada**
</dt> <dd> <dl> <dt>



A chamada foi originada como uma chamada de entrada, mas o provedor de serviços não pode determinar se ele veio de outra estação no mesmo comutador ou de uma linha externa. Os provedores de serviço podem usar essa constante somente quando a TAPI versão 1,4 ou posterior tiver sido negociada. Caso contrário, o provedor de serviços pode substituir LINECALLORIGIN não \_ disp.


</dt> </dl> </dd> <dt>

<span id="LINECALLORIGIN_INTERNAL"></span><span id="linecallorigin_internal"></span>**LINECALLORIGIN \_ interno**
</dt> <dd> <dl> <dt>



A chamada foi originada como uma chamada de entrada em uma estação interna para o mesmo ambiente de comutação.


</dt> </dl> </dd> <dt>

<span id="LINECALLORIGIN_OUTBOUND"></span><span id="linecallorigin_outbound"></span>**LINECALLORIGIN de \_ saída**
</dt> <dd> <dl> <dt>



A chamada foi originada desta estação como uma chamada de saída.


</dt> </dl> </dd> <dt>

<span id="LINECALLORIGIN_UNAVAIL"></span><span id="linecallorigin_unavail"></span>**LINECALLORIGIN não \_ disp.**
</dt> <dd> <dl> <dt>



A origem da chamada não está disponível e nunca se tornará conhecida para essa chamada.


</dt> </dl> </dd> <dt>

<span id="LINECALLORIGIN_UNKNOWN"></span><span id="linecallorigin_unknown"></span>**LINECALLORIGIN \_ desconhecido**
</dt> <dd> <dl> <dt>



A origem da chamada é desconhecida no momento, mas pode ser conhecida mais tarde.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Comentários

Sem extensibilidade. Todos os 32 bits são reservados.

A origem de uma chamada é armazenada no membro **dwOrigin** da estrutura [**LINECALLINFO**](/windows/desktop/api/Tapi/ns-tapi-linecallinfo) da chamada.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|-----------------------------------------------------------------------------------|
| Versão da TAPI<br/> | Requer TAPI 2,0 ou posterior<br/>                                             |
| parâmetro<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




