---
description: As \_ constantes de sinalizador de bit PHONESTATUSFLAGS descrevem uma variedade de informações de status do dispositivo de telefone.
ms.assetid: e94da591-49ab-4932-8621-0a62b8a55dd6
title: Constantes de PHONESTATUSFLAGS_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b42f8e13adfae54c56e44244d04b3961216edb87e29730fec6f689f315380a7e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119060644"
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
| Cabeçalho<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




