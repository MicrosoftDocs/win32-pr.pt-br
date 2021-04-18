---
description: As \_ constantes de sinalizador de bit LINEANSWERMODE descrevem como uma chamada ativa existente em um dispositivo de linha é afetada respondendo a outra chamada de oferta na mesma linha.
ms.assetid: 35f63d92-970f-4fb8-aba9-179fc7de70f4
title: Constantes de LINEANSWERMODE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 658d5b1265d28f8cb719719e4303fde97d3fff3e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105757220"
---
# <a name="lineanswermode_-constants"></a>\_Constantes LINEANSWERMODE

As constantes de sinalizador de bit **LINEANSWERMODE \_** descrevem como uma chamada ativa existente em um dispositivo de linha é afetada respondendo a outra chamada de *oferta* na mesma linha.

<dl> <dt>

<span id="LINEANSWERMODE_DROP"></span><span id="lineanswermode_drop"></span>**\_descartar LINEANSWERMODE**
</dt> <dd> <dl> <dt>



A chamada ativa no momento será automaticamente descartada.


</dt> </dl> </dd> <dt>

<span id="LINEANSWERMODE_HOLD"></span><span id="lineanswermode_hold"></span>**LINEANSWERMODE \_ reter**
</dt> <dd> <dl> <dt>



A chamada ativa no momento será automaticamente colocada em espera.


</dt> </dl> </dd> <dt>

<span id="LINEANSWERMODE_NONE"></span><span id="lineanswermode_none"></span>**LINEANSWERMODE \_ nenhum**
</dt> <dd> <dl> <dt>



Responder a outra chamada na mesma linha não tem nenhum efeito sobre a chamada ativa existente na linha.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Comentários

Sem extensibilidade. Todos os 32 bits são reservados.

Se uma chamada chegar (é oferecida) no momento em que outra chamada já estiver ativa, a nova chamada será conectada invocando [**lineAnswer**](/windows/desktop/api/Tapi/nf-tapi-lineanswer). O efeito que isso tem na chamada ativa existente depende dos recursos do dispositivo da linha. A primeira chamada pode não ser afetada, pode ser descartada automaticamente ou pode ser automaticamente colocada em espera.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|-----------------------------------------------------------------------------------|
| Versão da TAPI<br/> | Requer TAPI 2,0 ou posterior<br/>                                             |
| parâmetro<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




