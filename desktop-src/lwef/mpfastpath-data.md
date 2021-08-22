---
title: Estrutura de MPFASTPATH_DATA (MpClient. h)
description: Notificação de atualização do FastPath.
ms.assetid: E19F153D-DD46-4E27-9A4B-33586794DAC2
keywords:
- recursos de ambiente de Windows herdado da estrutura de MPFASTPATH_DATA
- Windows recursos de ambiente herdados do ponteiro de estrutura do PMPFASTPATH_DATA
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
ms.openlocfilehash: e138e9c45657cfc4ebeba1d1dbeed38070b6e07d09c512ec96835a04702d0c8a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119556146"
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
| Cliente mínimo com suporte<br/> | Windows 8 \[ somente aplicativos da área de trabalho\]<br/>                                            |
| Servidor mínimo com suporte<br/> | Windows Server 2012 \[ somente aplicativos da área de trabalho\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>MpClient. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_tipo de FASTPATH MP \_**](mp-fastpath-type.md)
</dt> <dt>

[**\_tipo de \_ limite de persistência MP \_**](mp-persistence-limit-type.md)
</dt> <dt>

[**\_tipo de assinatura MP \_**](mp-signature-type.md)
</dt> </dl>

 

 





