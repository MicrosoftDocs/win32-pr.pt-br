---
description: As \_ constantes de sinalizador de bit LINEBUSYMODE descrevem sinais ocupados diferentes que o comutador ou a rede pode gerar. Esses sinais ocupados normalmente indicam que um recurso diferente necessário para fazer uma chamada está em uso no momento.
ms.assetid: 4a3fa79f-7a7a-4f9b-9353-e6c5ca4fcb4e
title: Constantes de LINEBUSYMODE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 54563567944a2e5164717f7d64ff7026a0045ea735405a7bcad159969f07514a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119681986"
---
# <a name="linebusymode_-constants"></a>\_Constantes LINEBUSYMODE

As constantes de sinalizador de bit **LINEBUSYMODE \_** descrevem sinais ocupados diferentes que o comutador ou a rede pode gerar. Esses sinais ocupados normalmente indicam que um recurso diferente necessário para fazer uma chamada está em uso no momento.

<dl> <dt>

<span id="LINEBUSYMODE_STATION"></span><span id="linebusymode_station"></span>**\_estação LINEBUSYMODE**
</dt> <dd> <dl> <dt>



O sinal de ocupado indica que a estação da parte chamada está ocupada. Isso geralmente é sinalizado com um tom ocupado *normal* .


</dt> </dl> </dd> <dt>

<span id="LINEBUSYMODE_TRUNK"></span><span id="linebusymode_trunk"></span>**\_tronco LINEBUSYMODE**
</dt> <dd> <dl> <dt>



O sinal Busy indica que um tronco ou circuito está ocupado. Em geral, isso é sinalizado com um tom de ocupado *rápido* .


</dt> </dl> </dd> <dt>

<span id="LINEBUSYMODE_UNKNOWN"></span><span id="linebusymode_unknown"></span>**LINEBUSYMODE \_ desconhecido**
</dt> <dd> <dl> <dt>



O modo específico do sinal Busy é desconhecido no momento, mas pode ser conhecido mais tarde.


</dt> </dl> </dd> <dt>

<span id="LINEBUSYMODE_UNAVAIL"></span><span id="linebusymode_unavail"></span>**LINEBUSYMODE não \_ disp.**
</dt> <dd> <dl> <dt>



O modo específico do sinal de ocupado não está disponível e não se tornará conhecido.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Comentários

Os 16 bits de ordem superior podem ser atribuídos para extensões específicas do dispositivo. Os 16 bits de ordem inferior são reservados.

> [!Note]  
> Sinais ocupados podem ser enviados como tons de inband ou mensagens fora de banda. A TAPI não faz suposições sobre o mecanismo de sinalização específico.

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|-----------------------------------------------------------------------------------|
| Versão da TAPI<br/> | Requer TAPI 2,0 ou posterior<br/>                                             |
| Cabeçalho<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




