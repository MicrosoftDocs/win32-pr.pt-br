---
description: As constantes de sinalizador de bits LINECALLCOMPLMODE descrevem diferentes maneiras \_ pelas quais uma chamada pode ser concluída.
ms.assetid: 68f755a1-586b-4c5b-b8e8-c8b40eb71685
title: LINECALLCOMPLMODE_ constantes (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d43f76c9b8012f9ecb60c6b0ffd787d5a0bad87794eb833cc4095c276ba983f9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117761750"
---
# <a name="linecallcomplmode_-constants"></a>Constantes LINECALLCOMPLMODE \_

As constantes de sinalizador de bits **LINECALLCOMPLMODE \_** descrevem diferentes maneiras pelas quais uma chamada pode ser concluída.

<dl> <dt>

<span id="LINECALLCOMPLMODE_CALLBACK"></span><span id="linecallcomplmode_callback"></span>**RETORNO DE CHAMADA LINECALLCOMPLMODE \_**
</dt> <dd> <dl> <dt>



Solicita que a estação chamada retorne a chamada quando ela retornar para ociosa.


</dt> </dl> </dd> <dt>

<span id="LINECALLCOMPLMODE_CAMPON"></span><span id="linecallcomplmode_campon"></span>**LINECALLCOMPLMODE \_ CAMPON**
</dt> <dd> <dl> <dt>



Enfile a chamada até que a chamada possa ser concluída.


</dt> </dl> </dd> <dt>

<span id="LINECALLCOMPLMODE_INTRUDE"></span><span id="linecallcomplmode_intrude"></span>**LINECALLCOMPLMODE \_ INTRUDE**
</dt> <dd> <dl> <dt>



Adiciona o aplicativo à chamada existente na estação chamada (em que se chama ).


</dt> </dl> </dd> <dt>

<span id="LINECALLCOMPLMODE_MESSAGE"></span><span id="linecallcomplmode_message"></span>**MENSAGEM LINECALLCOMPLMODE \_**
</dt> <dd> <dl> <dt>



Deixa uma mensagem predefinida curta para a estação chamada (Deixe Chamada de Palavra). A mensagem a ser enviada é especificada separadamente.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Comentários

Nenhuma extensibilidade. Todos os 32 bits são reservados.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|-----------------------------------------------------------------------------------|
| Versão do TAPI<br/> | Requer TAPI 2.0 ou posterior<br/>                                             |
| Cabeçalho<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



 

 




