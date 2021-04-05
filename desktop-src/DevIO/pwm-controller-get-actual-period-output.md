---
description: Contém o período de sinal de saída efetivo para um controlador de modulação de pulsos (PWM).
ms.assetid: 280F564F-FF7F-4121-B726-9F9AF9E98EB7
title: Estrutura de PWM_CONTROLLER_GET_ACTUAL_PERIOD_OUTPUT (PWM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PWM_CONTROLLER_GET_ACTUAL_PERIOD_OUTPUT
api_type:
- HeaderDef
api_location:
- Pwm.h
ms.openlocfilehash: f63057299a8ef37ed1b38151958d2e0061ad2727
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646360"
---
# <a name="pwm_controller_get_actual_period_output-structure"></a>\_Controlador PWM \_ obter a estrutura de \_ saída do \_ período real \_

\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente. A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]

Contém o período de sinal de saída efetivo para um controlador de modulação de pulsos (PWM).

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _PWM_CONTROLLER_GET_ACTUAL_PERIOD_OUTPUT {
  PWM_PERIOD ActualPeriod;
} PWM_CONTROLLER_GET_ACTUAL_PERIOD_OUTPUT;
```



## <a name="members"></a>Membros

<dl> <dt>

**ActualPeriod**
</dt> <dd>

O período de sinal de saída efetivo como seria medido nos canais de saída do controlador.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows 10\]<br/>                                                      |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2016\]<br/>                                             |
| Versão mínima do KMDF<br/>     | 1,19<br/>                                                                                  |
| Versão mínima do UMDF<br/>     | 2.19<br/>                                                                                  |
| parâmetro<br/>                   | <dl> <dt>PWM. h (incluir PWM. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_controlador PWM \_ IOCTL \_ obter \_ \_ período real**](https://www.bing.com/search?q=**IOCTL\_PWM\_CONTROLLER\_GET\_ACTUAL\_PERIOD**)
</dt> </dl>

 

 




