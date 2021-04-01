---
title: Enumeração de WINBIO_ANTI_SPOOF_POLICY_ACTION (WinBio \_ Types. h)
description: Especifica os tipos de ações que você assume para a política de antifalsificação de um usuário.
ms.assetid: 846C0725-1796-49E4-883C-44AC7D618317
keywords:
- API de Windows Biometric Framework de enumeração de WINBIO_ANTI_SPOOF_POLICY_ACTION
- PWINBIO_ANTI_SPOOF_POLICY Windows Biometric Framework API do ponteiro de enumeração
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
ms.openlocfilehash: 5905624bad252475cdde12c003f31a734e64dd2e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918672"
---
# <a name="winbio_anti_spoof_policy_action-enumeration"></a>\_Enumeração de \_ ação de política de antifalsificação WINBIO \_ \_

Especifica os tipos de ações que você assume para a política de antifalsificação de um usuário.

## <a name="syntax"></a>Syntax


```C++
typedef enum _WINBIO_ANTI_SPOOF_POLICY_ACTION { 
  WINBIO_ANTI_SPOOF_DISABLE  = 0x00000000,
  WINBIO_ANTI_SPOOF_ENABLE   = 0x00000001,
  WINBIO_ANTI_SPOOF_REMOVE   = 0x00000002
} WINBIO_ANTI_SPOOF_POLICY_ACTION, *PWINBIO_ANTI_SPOOF_POLICY;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="WINBIO_ANTI_SPOOF_DISABLE"></span><span id="winbio_anti_spoof_disable"></span>**\_ \_ desabilitar antifalsificação do WINBIO \_**
</dt> <dd>

Desativa a detecção de falsificação para um fator biométrico.

</dd> <dt>

<span id="WINBIO_ANTI_SPOOF_ENABLE"></span><span id="winbio_anti_spoof_enable"></span>**\_ \_ habilitar antifalsificação do WINBIO \_**
</dt> <dd>

Ativa a detecção de falsificação para um fator biométrico.

</dd> <dt>

<span id="WINBIO_ANTI_SPOOF_REMOVE"></span><span id="winbio_anti_spoof_remove"></span>**\_remoção de \_ antifalsificação do WINBIO \_**
</dt> <dd>

Remove toda a política antifalsificação para o fator biométrico da conta.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows 10\]<br/>                                                                                                                              |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2016\]<br/>                                                                                                                     |
| parâmetro<br/>                   | <dl> <dt>WinBio \_ Types. h (inclui WinBio. h para aplicativos cliente ou WinBio \_ Adapters. h para adaptadores)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_ação da \_ política antifalsificação do \_ WINBIO \_**](winbio-anti-spoof-policy-action.md)
</dt> <dt>

[**\_origem da política de WINBIO \_**](winbio-policy-source.md)
</dt> </dl>

 

 





