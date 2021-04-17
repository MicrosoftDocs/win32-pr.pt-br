---
description: As \_ constantes de sinalizador de bit PHONESTATUSFLAGS descrevem uma variedade de informações de status do dispositivo de telefone.
ms.assetid: e94da591-49ab-4932-8621-0a62b8a55dd6
title: Constantes de PHONESTATUSFLAGS_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 969c2553274037797bdf9abea3e8bdbc1cd8d018
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105811922"
---
# <a name="phonestatusflags_-constants"></a>\_Constantes PHONESTATUSFLAGS

As constantes de sinalizador de bit **PHONESTATUSFLAGS \_** descrevem uma variedade de informações de status do dispositivo de telefone.

<dl> <dt>

<span id="PHONESTATUSFLAGS_CONNECTED"></span><span id="phonestatusflags_connected"></span>**PHONESTATUSFLAGS \_ conectado**
</dt> <dd> <dl> <dt>



Especifica se o telefone está atualmente conectado à TAPI. **True** se conectado; caso contrário, **false** .


</dt> </dl> </dd> <dt>

<span id="PHONESTATUSFLAGS_SUSPENDED"></span><span id="phonestatusflags_suspended"></span>**PHONESTATUSFLAGS \_ suspensa**
</dt> <dd> <dl> <dt>



Especifica se a manipulação da TAPI do dispositivo de telefone está suspensa. **True** se suspenso; caso contrário, **false** . O uso do aplicativo de um dispositivo telefônico pode ser temporariamente suspenso quando o comutador deseja manipular o telefone de forma que não possa tolerar a interferência do aplicativo.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Comentários

Sem extensibilidade. Todos os 32 bits são reservados.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|-----------------------------------------------------------------------------------|
| Versão da TAPI<br/> | Requer TAPI 2,0 ou posterior<br/>                                             |
| parâmetro<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




