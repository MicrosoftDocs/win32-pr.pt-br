---
description: Contém uma porcentagem de ciclo de serviço desejado para um PIN ou canal em um controlador de modulação de largura de pulso (PWM).
ms.assetid: CA699703-2D9B-4841-99AD-9C27FF428394
title: Estrutura de PWM_PIN_SET_ACTIVE_DUTY_CYCLE_PERCENTAGE_INPUT (PWM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PWM_PIN_SET_ACTIVE_DUTY_CYCLE_PERCENTAGE_INPUT
api_type:
- HeaderDef
api_location:
- Pwm.h
ms.openlocfilehash: ca6b2ee6aa4d4d2da3f94aa7cc471de12c1f8040b597edf568bf061c8e392aa1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119758846"
---
# <a name="pwm_pin_set_active_duty_cycle_percentage_input-structure"></a>\_Estrutura de \_ \_ entrada de \_ \_ percentual de ciclo de serviço ativo da \_ definição \_ de PIN PWM

\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente. A Microsoft não oferece garantias, expressas ou implícitas, das informações aqui fornecidas.\]

Contém uma porcentagem de ciclo de serviço desejado para um PIN ou canal em um controlador de modulação de largura de pulso (PWM).

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _PWM_PIN_SET_ACTIVE_DUTY_CYCLE_PERCENTAGE_INPUT {
  PWM_PERCENTAGE Percentage;
} PWM_PIN_SET_ACTIVE_DUTY_CYCLE_PERCENTAGE_INPUT;
```



## <a name="members"></a>Membros

<dl> <dt>

**Percentual**
</dt> <dd>

O ciclo de serviço de sinal de PWM desejado, como um percentual de PWM \_ , que é um valor de ULONGLONG.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 10 \[ somente aplicativos da área de trabalho\]<br/>                                                      |
| Servidor mínimo com suporte<br/> | Windows Server 2016 \[ somente aplicativos da área de trabalho\]<br/>                                             |
| Versão mínima do KMDF<br/>     | 1,19<br/>                                                                                  |
| Versão mínima do UMDF<br/>     | 2.19<br/>                                                                                  |
| Cabeçalho<br/>                   | <dl> <dt>PWM. h (incluir PWM. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IOCTL \_ PWM \_ PIN \_ definir \_ o \_ \_ percentual do ciclo de imposto ativo \_**](https://www.bing.com/search?q=**IOCTL\_PWM\_PIN\_SET\_ACTIVE\_DUTY\_CYCLE\_PERCENTAGE**)
</dt> </dl>

 

 




