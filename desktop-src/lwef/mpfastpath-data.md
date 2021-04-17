---
title: Estrutura de MPFASTPATH_DATA (MpClient. h)
description: Notificação de atualização do FastPath.
ms.assetid: E19F153D-DD46-4E27-9A4B-33586794DAC2
keywords:
- Recursos do ambiente Windows herdado da estrutura de MPFASTPATH_DATA
- Ponteiro de estrutura de PMPFASTPATH_DATA recursos de ambiente herdados do Windows
topic_type:
- apiref
api_name:
- MPFASTPATH_DATA
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2850a48074fee6984564550683c7fe595d0779ff
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105791591"
---
# <a name="mpfastpath_data-structure"></a>\_Estrutura de dados MPFASTPATH

Notificação de atualização do FastPath.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct tagMPFASTPATH_DATA {
  MP_SIGNATURE_TYPE         SignatureType;
  MP_FASTPATH_TYPE          FastPathSignatureType;
  MP_MIDL_STRING LPWSTR     FastPathSignatureVersion;
  ULARGE_INTEGER            CompilationTimestamp;
  MP_PERSISTENCE_LIMIT_TYPE PersistenceType;
  MP_MIDL_STRING LPWSTR     PersistenceValue;
  MP_MIDL_STRING LPWSTR     PersistencePath;
  MP_REMOVAL_REASON         Reason;
} MPFASTPATH_DATA, *PMPFASTPATH_DATA;
```



## <a name="members"></a>Membros

<dl> <dt>

**SignatureType**
</dt> <dd>

Tipo: **[ **\_ \_ tipo de assinatura MP**](mp-signature-type.md)**

</dd> <dd>

Tipo de assinatura.

</dd> <dt>

**FastPathSignatureType**
</dt> <dd>

Tipo: **[ **\_ \_ tipo de FASTPATH do MP**](mp-fastpath-type.md)**

</dd> <dd>

Tipo de assinatura FastPath.

</dd> <dt>

**FastPathSignatureVersion**
</dt> <dd>

Tipo: **PG \_ MIDL \_ String LPWSTR**

</dd> <dd>

Versão da assinatura FastPath (opcional).

</dd> <dt>

**CompilationTimestamp**
</dt> <dd>

Tipo: **ULARGE \_ inteiro**

</dd> <dd>

Carimbo de data/hora de compilação (UTC).

</dd> <dt>

**PersistenceType**
</dt> <dd>

Tipo: **[ **\_ tipo de \_ limite \_ de persistência MP**](mp-persistence-limit-type.md)**

</dd> <dd>

Tipo de persistência (opcional).

</dd> <dt>

**Persistencevalue**
</dt> <dd>

Tipo: **PG \_ MIDL \_ String LPWSTR**

</dd> <dd>

Valor de persistência (opcional).

</dd> <dt>

**PersistencePath**
</dt> <dd>

Tipo: **PG \_ MIDL \_ String LPWSTR**

</dd> <dd>

Caminho de persistência (opcional).

</dd> <dt>

**Motivo**
</dt> <dd>

Tipo: **[ **\_ \_ motivo da remoção de MP**](mp-removal-reason.md)**

</dd> <dd>

Motivo para remoção de assinatura.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 8\]<br/>                                            |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2012\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>MpClient. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_tipo de FASTPATH MP \_**](mp-fastpath-type.md)
</dt> <dt>

[**\_tipo de \_ limite de persistência MP \_**](mp-persistence-limit-type.md)
</dt> <dt>

[**\_tipo de assinatura MP \_**](mp-signature-type.md)
</dt> </dl>

 

 





