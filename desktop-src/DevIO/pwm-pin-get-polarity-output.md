---
description: Contém um valor de polaridade a ser retornada.
ms.assetid: 432C10EF-AC08-4781-9BCA-A31E0DF12704
title: PWM_PIN_GET_POLARITY_OUTPUT (Pwm.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PWM_PIN_GET_POLARITY_OUTPUT
api_type:
- HeaderDef
api_location:
- Pwm.h
ms.openlocfilehash: 7d4c3103663ceac65deff7744b0cf45a21a787959cc6e866bde5ac8673f7f64a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119984426"
---
# <a name="pwm_pin_get_polarity_output-structure"></a>Estrutura DE SAÍDA \_ \_ GET \_ POLARITY DO PIN PWM \_

\[Algumas informações estão relacionadas ao produto pré-lançado, que pode ser substancialmente modificado antes de ser lançado comercialmente. A Microsoft não oferece garantias, expressas ou implícitas, das informações aqui fornecidas.\]

Contém um valor de polaridade a ser retornada.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _PWM_PIN_GET_POLARITY_OUTPUT {
  PWM_POLARITY Polarity;
} PWM_PIN_GET_POLARITY_OUTPUT;
```



## <a name="members"></a>Membros

<dl> <dt>

**Polaridade**
</dt> <dd>

A polaridade do pino ou canal como um [**valor de \_ POLARIDADE PWM.**](/windows/desktop/api/Pwm/ne-pwm-pwm_polarity) A polaridade é Alta Ativa ou Baixa Ativa.

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

[**IOCTL \_ PWM \_ PIN \_ GET \_ POLARITY**](https://www.bing.com/search?q=**IOCTL\_PWM\_PIN\_GET\_POLARITY**)
</dt> <dt>

[**POLARIDADE \_ PWM**](/windows/win32/api/pwm/ne-pwm-pwm_polarity)
</dt> </dl>

 

