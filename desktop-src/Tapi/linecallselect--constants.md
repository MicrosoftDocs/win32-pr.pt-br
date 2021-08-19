---
description: As \_ constantes de sinalizador de bit LINECALLSELECT descrevem quais chamadas devem ser selecionadas.
ms.assetid: f19a41bc-403a-4d4b-ab85-240a73514ebb
title: Constantes de LINECALLSELECT_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: feaa76ea5b421b8090f9289431bfee65be61a6b47abd170569beff73a9846533
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119003144"
---
# <a name="linecallselect_-constants"></a>\_Constantes LINECALLSELECT

As constantes de sinalizador de bit **LINECALLSELECT \_** descrevem quais chamadas devem ser selecionadas.

<dl> <dt>

<span id="LINECALLSELECT_ADDRESS"></span><span id="linecallselect_address"></span>**\_endereço LINECALLSELECT**
</dt> <dd> <dl> <dt>



Seleciona a chamada no endereço especificado.


</dt> </dl> </dd> <dt>

<span id="LINECALLSELECT_CALL"></span><span id="linecallselect_call"></span>**\_chamada LINECALLSELECT**
</dt> <dd> <dl> <dt>



Seleciona chamadas relacionadas à chamada especificada. Por exemplo, as partes em uma chamada de conferência.


</dt> </dl> </dd> <dt>

<span id="LINECALLSELECT_CALLID"></span><span id="linecallselect_callid"></span>**\_callid LINECALLSELECT**
</dt> <dd> <dl> <dt>



Seleciona chamadas relacionadas ao identificador de chamada especificado. Esse sinalizador é exposto somente a aplicativos que negociam uma versão de TAPI 3,0 ou superior.


</dt> </dl> </dd> <dt>

<span id="LINECALLSELECT_DEVICEID"></span><span id="linecallselect_deviceid"></span>**LINECALLSELECT \_ DeviceID**
</dt> <dd> <dl> <dt>



Seleciona chamadas no identificador de dispositivo especificado. Esse sinalizador é exposto somente a aplicativos que negociam uma versão de TAPI 2,1 ou superior. Os aplicativos devem considerar o uso da \_ constante de linha LINECALLSELECT em vez deste.


</dt> </dl> </dd> <dt>

<span id="LINECALLSELECT_LINE"></span><span id="linecallselect_line"></span>**LINECALLSELECT \_ linha**
</dt> <dd> <dl> <dt>



Seleciona as chamadas no dispositivo de linha especificado.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Comentários

Sem extensibilidade. Todos os 32 bits são reservados.

Essa constante é usada em [**lineGetNewCalls**](/windows/desktop/api/Tapi/nf-tapi-linegetnewcalls) e para especificar uma seleção (escopo) das chamadas que são solicitadas.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|-----------------------------------------------------------------------------------|
| Versão da TAPI<br/> | Requer TAPI 2,0 ou posterior<br/>                                             |
| Cabeçalho<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




