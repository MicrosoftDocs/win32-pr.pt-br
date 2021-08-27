---
title: Estrutura de WINBIO_ANTI_SPOOF_POLICY (WinBio \_ Types. h)
description: Representa a política de antifalsificação para um usuário.
ms.assetid: 2B433AE8-21A0-4AF1-853C-9074527DB2E4
keywords:
- API de Windows Biometric Framework de estrutura de WINBIO_ANTI_SPOOF_POLICY
- ponteiro de estrutura de PWINBIO_ANTI_SPOOF_POLICY Windows Biometric Framework API
topic_type:
- apiref
api_name:
- WINBIO_ANTI_SPOOF_POLICY
api_location:
- winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 28ade20749b105cc3c7f8a92e0904aff1cea860f9175c8b3c6adb113f273f0fd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120073246"
---
# <a name="winbio_anti_spoof_policy-structure"></a>\_Estrutura de \_ política antifalsificação do WINBIO \_

Representa a política de antifalsificação para um usuário.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _WINBIO_ANTI_SPOOF_POLICY {
  WINBIO_ANTI_SPOOF_POLICY_ACTION Action;
  WINBIO_POLICY_SOURCE            Source;
} WINBIO_ANTI_SPOOF_POLICY, *PWINBIO_ANTI_SPOOF_POLICY;
```



## <a name="members"></a>Membros

<dl> <dt>

**Ação**
</dt> <dd>

O tipo de ação a ser tomada para a política de antifalsificação.

</dd> <dt>

**Origem**
</dt> <dd>

A origem da política de antifalsificação.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 10 \[ somente aplicativos da área de trabalho\]<br/>                                                                                                                              |
| Servidor mínimo com suporte<br/> | Windows Server 2016 \[ somente aplicativos da área de trabalho\]<br/>                                                                                                                     |
| Cabeçalho<br/>                   | <dl> <dt>WinBio \_ Types. h (inclui WinBio. h para aplicativos cliente ou WinBio \_ Adapters. h para adaptadores)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_ação da \_ política antifalsificação do \_ WINBIO \_**](winbio-anti-spoof-policy-action.md)
</dt> <dt>

[**\_origem da política de WINBIO \_**](winbio-policy-source.md)
</dt> <dt>

[**\_resultado assíncrono do WINBIO \_**](/windows/desktop/api/Winbio/ns-winbio-winbio_async_result)
</dt> <dt>

[**WinBioGetProperty**](/windows/desktop/api/Winbio/nf-winbio-winbiogetproperty)
</dt> <dt>

[**WinBioSetProperty**](/windows/desktop/api/winbio/nf-winbio-winbiosetproperty)
</dt> </dl>

 

 





