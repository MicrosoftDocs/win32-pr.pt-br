---
title: Estrutura de WINBIO_ACCOUNT_POLICY ( \_ adaptador WINBIO. h)
description: Contém uma política de antifalsificação padrão ou específica da conta.
ms.assetid: 7098FC53-E487-42B2-8B4B-EB7E2D296CB6
keywords:
- API de Windows Biometric Framework de estrutura de WINBIO_ACCOUNT_POLICY
- Ponteiro de estrutura de PWINBIO_ACCOUNT_POLICY Windows Biometric Framework API
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
ms.openlocfilehash: c734fa6d98615b7708a65ebad1dddc47cdc77cc2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918444"
---
# <a name="winbio_account_policy-structure"></a>Estrutura de política de \_ conta do WINBIO \_

A estrutura de **\_ \_ política de conta do WINBIO** contém uma política de antifalsificação padrão ou específica da conta.

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

Uma estrutura de [**\_ identidade WINBIO**](winbio-identity.md) que especifica as informações da conta.

</dd> <dt>

**AntiSpoofBehavior**
</dt> <dd>

Um dos valores de enumeração da [**\_ \_ \_ \_ ação da política antifalsificação WINBIO**](winbio-anti-spoof-policy-action.md) que especifica qual ação de política de antifalsificação deve ser usada para a conta.

</dd> </dl>

## <a name="remarks"></a>Comentários

Consulte a discussão do método [**EngineAdapterSetAccountPolicy**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_set_account_policy_fn) para obter uma descrição de como essa estrutura é usada.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows 10\]<br/>                                                                              |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2016\]<br/>                                                                     |
| parâmetro<br/>                   | <dl> <dt>\_Adaptador WinBio. h (inclui o \_ adaptador WinBio. h)</dt> </dl> |



 

 





