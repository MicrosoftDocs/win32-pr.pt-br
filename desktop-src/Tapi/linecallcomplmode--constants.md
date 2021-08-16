---
description: As \_ constantes de sinalizador de bit LINECALLCOMPLMODE descrevem diferentes maneiras em que uma chamada pode ser concluída.
ms.assetid: 68f755a1-586b-4c5b-b8e8-c8b40eb71685
title: Constantes de LINECALLCOMPLMODE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d43f76c9b8012f9ecb60c6b0ffd787d5a0bad87794eb833cc4095c276ba983f9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117761750"
---
# <a name="linecallcomplmode_-constants"></a>\_Constantes LINECALLCOMPLMODE

As constantes de sinalizador de bit **LINECALLCOMPLMODE \_** descrevem diferentes maneiras em que uma chamada pode ser concluída.

<dl> <dt>

<span id="LINECALLCOMPLMODE_CALLBACK"></span><span id="linecallcomplmode_callback"></span>**\_retorno de chamada LINECALLCOMPLMODE**
</dt> <dd> <dl> <dt>



Solicita que a estação chamada retorne a chamada quando ela retornar para ocioso.


</dt> </dl> </dd> <dt>

<span id="LINECALLCOMPLMODE_CAMPON"></span><span id="linecallcomplmode_campon"></span>**LINECALLCOMPLMODE \_ Camp**
</dt> <dd> <dl> <dt>



Enfileira a chamada até que a chamada possa ser concluída.


</dt> </dl> </dd> <dt>

<span id="LINECALLCOMPLMODE_INTRUDE"></span><span id="linecallcomplmode_intrude"></span>**intrusão LINECALLCOMPLMODE \_**
</dt> <dd> <dl> <dt>



Adiciona o aplicativo à chamada existente na estação chamada (Barge).


</dt> </dl> </dd> <dt>

<span id="LINECALLCOMPLMODE_MESSAGE"></span><span id="linecallcomplmode_message"></span>**\_mensagem LINECALLCOMPLMODE**
</dt> <dd> <dl> <dt>



Deixa uma mensagem predefinida curta para a estação chamada (Deixe o Word chamar). A mensagem a ser enviada é especificada separadamente.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Comentários

Sem extensibilidade. Todos os 32 bits são reservados.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|-----------------------------------------------------------------------------------|
| Versão da TAPI<br/> | Requer TAPI 2,0 ou posterior<br/>                                             |
| Cabeçalho<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




