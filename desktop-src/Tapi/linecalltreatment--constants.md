---
description: As \_ constantes LINECALLTREATMENT listam tratamentos para chamadas que não são respondidas ou estão em espera. Exceto para a validação básica de parâmetros, o tratamento de chamadas é uma passagem direta pela TAPI para o provedor de serviços.
ms.assetid: c28c9200-dd51-48b2-905c-fbe37c83b00f
title: Constantes de LINECALLTREATMENT_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 88c627a89fdf5ab0592c862f09753e0b913eb4b7197a04d4db8cd06478ef10b5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118863834"
---
# <a name="linecalltreatment_-constants"></a>\_Constantes LINECALLTREATMENT

As **constantes \_ LINECALLTREATMENT** listam tratamentos para chamadas que não são respondidas ou estão em espera. Exceto para a validação básica de parâmetros, o tratamento de chamadas é uma passagem direta pela TAPI para o provedor de serviços.

<dl> <dt>

<span id="LINECALLTREATMENT_BUSY"></span><span id="linecalltreatment_busy"></span>**LINECALLTREATMENT \_ ocupado**
</dt> <dd> <dl> <dt>



Quando a chamada não está ativamente conectada a um dispositivo (oferta ou onhold), a parte ouve o sinal ocupado.


</dt> </dl> </dd> <dt>

<span id="LINECALLTREATMENT_MUSIC"></span><span id="linecalltreatment_music"></span>**\_música LINECALLTREATMENT**
</dt> <dd> <dl> <dt>



Quando a chamada não está ativamente conectada a um dispositivo (oferta ou onhold), a parte ouve música.


</dt> </dl> </dd> <dt>

<span id="LINECALLTREATMENT_RINGBACK"></span><span id="linecalltreatment_ringback"></span>**LINECALLTREATMENT de \_ toque**
</dt> <dd> <dl> <dt>



Quando a chamada não está ativamente conectada a um dispositivo (oferta ou onhold), a parte ouve o tom de toque.


</dt> </dl> </dd> <dt>

<span id="LINECALLTREATMENT_SILENCE"></span><span id="linecalltreatment_silence"></span>**\_silêncio LINECALLTREATMENT**
</dt> <dd> <dl> <dt>



Quando a chamada não está ativamente conectada a um dispositivo (oferta ou onhold), a parte ouve silêncio.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Comentários

O valor 0x00000000 é reservado para indicar que o provedor de serviços não dá suporte a tratamentos de chamada. Os valores no intervalo de 0x00000005 a 0x000000FF são reservados para a definição futura. Os valores no intervalo de 0x00000100 a 0xFFFFFFFF são reservados para atribuição por provedores de serviço e podem incluir a identificação de seleções musicais específicas ou anúncios gravados.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|-----------------------------------------------------------------------------------|
| Versão da TAPI<br/> | Requer TAPI 2,0 ou posterior<br/>                                             |
| Cabeçalho<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




