---
description: As \_ constantes LINEDIGITMODE descrevem tipos diferentes de geração de dígitos de inband.
ms.assetid: d603ea28-2b93-4548-bb16-78e93087f828
title: Constantes de LINEDIGITMODE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 50bedd7f508368a84ab2fa70fac37c316dcc6c85
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105753537"
---
# <a name="linedigitmode_-constants"></a>\_Constantes LINEDIGITMODE

As **constantes \_ LINEDIGITMODE** descrevem tipos diferentes de geração de dígitos de inband.

<dl> <dt>

<span id="LINEDIGITMODE_DTMF"></span><span id="linedigitmode_dtmf"></span>**\_DTMF LINEDIGITMODE**
</dt> <dd> <dl> <dt>



Usa tons DTMF para sinalizar dígitos. Os dígitos válidos são de 0 a 9, ' \* ', ' \# ', ' A ', ' B ', ' C' e ' d'.


</dt> </dl> </dd> <dt>

<span id="LINEDIGITMODE_DTMFEND"></span><span id="linedigitmode_dtmfend"></span>**LINEDIGITMODE \_ DTMFEND**
</dt> <dd> <dl> <dt>



Usa tons DTMF para sinalizar dígitos e detectar as bordas inativas. Os dígitos válidos são de 0 a 9, ' \* ', ' \# ', ' A ', ' B ', ' C' e ' d'.


</dt> </dl> </dd> <dt>

<span id="LINEDIGITMODE_PULSE"></span><span id="linedigitmode_pulse"></span>**pulso de LINEDIGITMODE \_**
</dt> <dd> <dl> <dt>



Usa sequências de pulsos de rota para indicar dígitos. Os dígitos válidos são de 0 a 9.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Comentários

Sem extensibilidade. Todos os 32 bits são reservados.

Um modo de dígito pode ser especificado ao gerar ou detectar dígitos. Observe que os dígitos de pulso são gerados pela criação e interrupção do circuito de loop local. Esses pulsos são absorvidos pelo comutador. A extremidade remota simplesmente observa isso como uma série de cliques de áudio de banda. A detecção de dígitos enviados como pulsos deve, portanto, ser capaz de detectar essas sequências de 1 a 10 cliques audíveis.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|-----------------------------------------------------------------------------------|
| Versão da TAPI<br/> | Requer TAPI 2,0 ou posterior<br/>                                             |
| parâmetro<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




