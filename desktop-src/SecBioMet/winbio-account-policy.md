---
title: WINBIO_ACCOUNT_POLICY (adaptador \_ Winbio.h)
description: Contém uma política antispoofing padrão ou específica da conta.
ms.assetid: 7098FC53-E487-42B2-8B4B-EB7E2D296CB6
keywords:
- WINBIO_ACCOUNT_POLICY estrutura Windows API do Biometric Framework
- PWINBIO_ACCOUNT_POLICY de estrutura Windows API do Biometric Framework
topic_type:
- apiref
api_name:
- WINBIO_ACCOUNT_POLICY
api_location:
- Winbio_adapter.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c30241f0e13528c8427367c61362b803caaa9fc8c0a15a0eefad72689517d40f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120035246"
---
# <a name="winbio_account_policy-structure"></a>Estrutura DA \_ POLÍTICA DE CONTA DO WINBIO \_

A **estrutura DE POLÍTICA DE CONTA \_ \_ WINBIO** contém uma política antifalsagem padrão ou específica da conta.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _WINBIO_ACCOUNT_POLICY {
  WINBIO_IDENTITY                 Identity;
  WINBIO_ANTI_SPOOF_POLICY_ACTION AntiSpoofBehavior;
} WINBIO_ACCOUNT_POLICY, *PWINBIO_ACCOUNT_POLICY;
```



## <a name="members"></a>Membros

<dl> <dt>

**Identidade**
</dt> <dd>

Uma [**estrutura WINBIO \_ IDENTITY**](winbio-identity.md) que especifica as informações da conta.

</dd> <dt>

**AntiSpoofBehavior**
</dt> <dd>

Um dos valores [**de enumeração \_ WINBIO ANTI \_ SPOOF \_ POLICY \_ ACTION**](winbio-anti-spoof-policy-action.md) que especifica qual ação de política antipoofing usar para a conta.

</dd> </dl>

## <a name="remarks"></a>Comentários

Confira a discussão sobre o [**método EngineAdapterSetAccountPolicy**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_set_account_policy_fn) para ver uma descrição de como essa estrutura é usada.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Windows 10 somente aplicativos da área de trabalho\]<br/>                                                                              |
| Servidor mínimo com suporte<br/> | \[Windows Server 2016 somente aplicativos da área de trabalho\]<br/>                                                                     |
| Cabeçalho<br/>                   | <dl> <dt>Winbio \_ adapter.h (inclua Adaptador \_ winbio.h)</dt> </dl> |



 

 





