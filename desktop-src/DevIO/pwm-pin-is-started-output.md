---
description: Contém o estado atual de geração de sinal de um PIN.
ms.assetid: 07D76F8D-C5B5-4500-BFA2-452989868027
title: Estrutura de PWM_PIN_IS_STARTED_OUTPUT (PWM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PWM_PIN_IS_STARTED_OUTPUT
api_type:
- HeaderDef
api_location:
- Pwm.h
ms.openlocfilehash: 11350c3bb0fbec0f05ab3153c339f8fa30baeed5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105755817"
---
# <a name="pwm_pin_is_started_output-structure"></a>A \_ estrutura de saída do PIN PWM \_ é \_ iniciada \_

\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente. A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]

Contém o estado atual de geração de sinal de um PIN.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _PWM_PIN_IS_STARTED_OUTPUT {
  BOOLEAN IsStarted;
} PWM_PIN_IS_STARTED_OUTPUT;
```



## <a name="members"></a>Membros

<dl> <dt>

**IsStarted**
</dt> <dd>

O estado de geração de sinal atual do PIN. Um valor de true significa que o PIN é iniciado. Um valor false significa que o PIN foi interrompido.

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

[**o \_ PIN PWM do IOCTL \_ \_ foi \_ iniciado**](https://www.bing.com/search?q=**IOCTL\_PWM\_PIN\_IS\_STARTED**)
</dt> </dl>

 

 




