---
description: Contém um valor de polaridade a ser retornado.
ms.assetid: 432C10EF-AC08-4781-9BCA-A31E0DF12704
title: Estrutura de PWM_PIN_GET_POLARITY_OUTPUT (PWM. h)
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
ms.openlocfilehash: 81cf7b658a0024c3280db1523af34aaf2ef17262
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920314"
---
# <a name="pwm_pin_get_polarity_output-structure"></a>PWM \_ PIN \_ obter a \_ estrutura de saída de polaridade \_

\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente. A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]

Contém um valor de polaridade a ser retornado.

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

A polaridade do PIN ou canal como um valor de [**\_ polaridade PWM**](/windows/desktop/api/Pwm/ne-pwm-pwm_polarity) . A polaridade é ativo alto ou ativo baixo.

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

[**IOCTL \_ PWM \_ PIN \_ obter \_ polaridade**](https://www.bing.com/search?q=**IOCTL\_PWM\_PIN\_GET\_POLARITY**)
</dt> <dt>

[**\_polaridade PWM**](/windows/win32/api/pwm/ne-pwm-pwm_polarity)
</dt> </dl>

 

