---
description: As constantes de sinalizador de bits LINEANSWERMODE descrevem como uma chamada ativa existente em um dispositivo de linha é afetada respondendo a outra chamada de oferta \_ na mesma linha.
ms.assetid: 35f63d92-970f-4fb8-aba9-179fc7de70f4
title: LINEANSWERMODE_ constantes (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: abfb9d6491864f5be8788575d718e42cc5f5c7c337fd046c110bd5bd82eae110
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117761838"
---
# <a name="lineanswermode_-constants"></a>Constantes LINEANSWERMODE \_

As constantes de sinalizador de bits **LINEANSWERMODE \_** descrevem como uma chamada ativa  existente em um dispositivo de linha é afetada respondendo a outra chamada de oferta na mesma linha.

<dl> <dt>

<span id="LINEANSWERMODE_DROP"></span><span id="lineanswermode_drop"></span>**LINEANSWERMODE \_ DROP**
</dt> <dd> <dl> <dt>



A chamada ativa no momento será automaticamente descartado.


</dt> </dl> </dd> <dt>

<span id="LINEANSWERMODE_HOLD"></span><span id="lineanswermode_hold"></span>**ESPERA \_ LINEANSWERMODE**
</dt> <dd> <dl> <dt>



A chamada ativa no momento será colocada automaticamente em espera.


</dt> </dl> </dd> <dt>

<span id="LINEANSWERMODE_NONE"></span><span id="lineanswermode_none"></span>**LINEANSWERMODE \_ NONE**
</dt> <dd> <dl> <dt>



Responder a outra chamada na mesma linha não tem efeito sobre a chamada ativa existente na linha.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Comentários

Nenhuma extensibilidade. Todos os 32 bits são reservados.

Se uma chamada entrar (é oferecida) no momento em que outra chamada já estiver ativa, a nova chamada será conectada ao invocando [**lineAnswer**](/windows/desktop/api/Tapi/nf-tapi-lineanswer). O efeito que isso tem na chamada ativa existente depende dos recursos do dispositivo da linha. A primeira chamada pode não ser afetada, ela pode ser automaticamente descartado ou pode ser colocada automaticamente em espera.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|-----------------------------------------------------------------------------------|
| Versão do TAPI<br/> | Requer TAPI 2.0 ou posterior<br/>                                             |
| Cabeçalho<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



 

 




