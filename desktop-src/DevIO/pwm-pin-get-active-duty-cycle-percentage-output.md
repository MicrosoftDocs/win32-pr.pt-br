---
description: Contém o percentual de ciclo de serviço atual para um pino ou canal em um controlador PWM (Pulse Width Modulartion).
ms.assetid: 09C0232A-DF5C-4A1C-8138-D3D65E45731B
title: PWM_PIN_GET_ACTIVE_DUTY_CYCLE_PERCENTAGE_OUTPUT (Pwm.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PWM_PIN_GET_ACTIVE_DUTY_CYCLE_PERCENTAGE_OUTPUT
api_type:
- HeaderDef
api_location:
- Pwm.h
ms.openlocfilehash: dda05c06ee8c53968647bc29da2febee14abf758d4ad228c16178703c2d1da08
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120053316"
---
# <a name="pwm_pin_get_active_duty_cycle_percentage_output-structure"></a>Estrutura DE SAÍDA DO PERCENTUAL DO CICLO DE \_ \_ \_ \_ \_ TRABALHO \_ \_ ATIVO DO PIN PWM

\[Algumas informações estão relacionadas ao produto pré-lançado, que pode ser substancialmente modificado antes de ser lançado comercialmente. A Microsoft não oferece garantias, expressas ou implícitas, das informações aqui fornecidas.\]

Contém o percentual de ciclo de serviço atual para um pino ou canal em um controlador PWM (Pulse Width Modulartion).

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _PWM_PIN_GET_ACTIVE_DUTY_CYCLE_PERCENTAGE_OUTPUT {
  PWM_PERCENTAGE Percentage;
} PWM_PIN_GET_ACTIVE_DUTY_CYCLE_PERCENTAGE_OUTPUT;
```



## <a name="members"></a>Membros

<dl> <dt>

**Percentual**
</dt> <dd>

O ciclo de serviço de sinal PWM atual, como um PWM \_ PERCENTAGE, que é um valor ULONGLONG.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Windows 10 somente aplicativos da área de trabalho\]<br/>                                                      |
| Servidor mínimo com suporte<br/> | \[Windows Server 2016 somente aplicativos da área de trabalho\]<br/>                                             |
| Versão mínima do KMDF<br/>     | 1,19<br/>                                                                                  |
| Versão mínima do UMDF<br/>     | 2.19<br/>                                                                                  |
| Cabeçalho<br/>                   | <dl> <dt>Pwm.h (inclua Pwm.h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IOCTL \_ PWM \_ PIN \_ GET \_ ACTIVE \_ DUTY \_ CYCLE \_ PERCENTAGE**](https://www.bing.com/search?q=**IOCTL\_PWM\_PIN\_GET\_ACTIVE\_DUTY\_CYCLE\_PERCENTAGE**)
</dt> </dl>

 

 




