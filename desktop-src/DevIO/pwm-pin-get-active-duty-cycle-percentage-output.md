---
description: Contém a porcentagem de ciclo de serviço atual para um PIN ou canal em um controlador de modulação de pulso de pulsação (PWM).
ms.assetid: 09C0232A-DF5C-4A1C-8138-D3D65E45731B
title: Estrutura de PWM_PIN_GET_ACTIVE_DUTY_CYCLE_PERCENTAGE_OUTPUT (PWM. h)
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
ms.openlocfilehash: 607fcb1ab429e7cbe9aee593f75d48f0f9d308bd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089195"
---
# <a name="pwm_pin_get_active_duty_cycle_percentage_output-structure"></a>PWM \_ PIN \_ obter \_ a \_ \_ estrutura de \_ saída percentual do ciclo de imposto ativo \_

\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente. A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]

Contém a porcentagem de ciclo de serviço atual para um PIN ou canal em um controlador de modulação de pulso de pulsação (PWM).

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

O ciclo de serviço de sinal de PWM atual, como um percentual de PWM \_ , que é um valor de ULONGLONG.

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

[**IOCTL \_ PWM \_ PIN \_ obter \_ \_ percentual de \_ ciclo de imposto ativo \_**](https://www.bing.com/search?q=**IOCTL\_PWM\_PIN\_GET\_ACTIVE\_DUTY\_CYCLE\_PERCENTAGE**)
</dt> </dl>

 

 




