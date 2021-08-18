---
title: WINBIO_ANTI_SPOOF_POLICY_ACTION enumeração (Tipos \_ Winbio.h)
description: Especifica os tipos de ações que você toma para a política antispoofing de um usuário.
ms.assetid: 846C0725-1796-49E4-883C-44AC7D618317
keywords:
- WINBIO_ANTI_SPOOF_POLICY_ACTION enumeração Windows API do Biometric Framework
- PWINBIO_ANTI_SPOOF_POLICY de enumeração Windows API do Biometric Framework
topic_type:
- apiref
api_name:
- WINBIO_ANTI_SPOOF_POLICY_ACTION
api_location:
- winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f65fec198a0784bf076eb90224318bd36a88ba3ed96258ffd2014a27da5c8f8d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118911265"
---
# <a name="winbio_anti_spoof_policy_action-enumeration"></a>Enumeração WINBIO \_ ANTI \_ SPOOF \_ POLICY \_ ACTION

Especifica os tipos de ações que você toma para a política antispoofing de um usuário.

## <a name="syntax"></a>Sintaxe


```C++
typedef enum _WINBIO_ANTI_SPOOF_POLICY_ACTION { 
  WINBIO_ANTI_SPOOF_DISABLE  = 0x00000000,
  WINBIO_ANTI_SPOOF_ENABLE   = 0x00000001,
  WINBIO_ANTI_SPOOF_REMOVE   = 0x00000002
} WINBIO_ANTI_SPOOF_POLICY_ACTION, *PWINBIO_ANTI_SPOOF_POLICY;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="WINBIO_ANTI_SPOOF_DISABLE"></span><span id="winbio_anti_spoof_disable"></span>**WINBIO \_ ANTI \_ SPOOF \_ DISABLE**
</dt> <dd>

Desliga a detecção de fraudes para um fator biométrico.

</dd> <dt>

<span id="WINBIO_ANTI_SPOOF_ENABLE"></span><span id="winbio_anti_spoof_enable"></span>**WINBIO \_ ANTI \_ SPOOF \_ ENABLE**
</dt> <dd>

Liga a detecção de fraudes para um fator biométrico.

</dd> <dt>

<span id="WINBIO_ANTI_SPOOF_REMOVE"></span><span id="winbio_anti_spoof_remove"></span>**WINBIO \_ ANTI \_ SPOOF \_ REMOVE**
</dt> <dd>

Remove toda a política antispoofing do fator biométrico da conta.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Windows 10 somente aplicativos da área de trabalho\]<br/>                                                                                                                              |
| Servidor mínimo com suporte<br/> | \[Windows Server 2016 somente aplicativos da área de trabalho\]<br/>                                                                                                                     |
| parâmetro<br/>                   | <dl> <dt>Winbio \_ types.h (inclua Winbio.h para aplicativos cliente ou \_ adaptadores Winbio.h para adaptadores)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**AÇÃO DE POLÍTICA \_ WINBIO ANTI \_ \_ SPOOF \_**](winbio-anti-spoof-policy-action.md)
</dt> <dt>

[**FONTE DE POLÍTICA DO WINBIO \_ \_**](winbio-policy-source.md)
</dt> </dl>

 

 





