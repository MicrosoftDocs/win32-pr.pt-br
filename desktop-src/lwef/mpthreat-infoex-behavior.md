---
title: Estrutura de MPTHREAT_INFOEX_BEHAVIOR (MpClient. h)
description: Contém informações específicas de modificação de comportamento.
ms.assetid: 762E755F-5BA1-476D-B395-6617093309C5
keywords:
- Recursos do ambiente Windows herdado da estrutura de MPTHREAT_INFOEX_BEHAVIOR
- Ponteiro de estrutura de PMPTHREAT_INFOEX_BEHAVIOR recursos de ambiente herdados do Windows
topic_type:
- apiref
api_name:
- MPTHREAT_INFOEX_BEHAVIOR
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4cb0bc00aeb56aec38b88f2590211c705079834f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103645068"
---
# <a name="mpthreat_infoex_behavior-structure"></a>Estrutura de comportamento do MPTHREAT \_ INFOEX \_

Contém informações específicas de modificação de comportamento.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct tagMPTHREAT_INFOEX_BEHAVIOR {
  ULARGE_INTEGER         SignatureID;
  ULONGLONG              EngineVersion;
  ULONGLONG              ASDeltaSignatureVersion;
  ULONGLONG              AVDeltaSignatureVersion;
  MP_HASH_TYPE           HashType;
  DWORD                  FidelityValue;
  MP_MIDL_STRING  LPWSTR HashValue;
  MP_MIDL_STRING  LPWSTR TargetFileName;
  MP_MIDL_STRING  LPWSTR TargetFileHash;
} MPTHREAT_INFOEX_BEHAVIOR, *PMPTHREAT_INFOEX_BEHAVIOR;
```



## <a name="members"></a>Membros

<dl> <dt>

**SignatureId**
</dt> <dd>

Tipo: **ULARGE \_ inteiro**

</dd> <dd>

ID de assinatura de modificação de comportamento fornecida pelo mecanismo no momento da detecção.

</dd> <dt>

**EngineVersion**
</dt> <dd>

Tipo: **ULONGLONG**

</dd> <dd>

Versão do módulo do mecanismo.

</dd> <dt>

**ASDeltaSignatureVersion**
</dt> <dd>

Tipo: **ULONGLONG**

</dd> <dd>

Versão da assinatura de AntiSpyware.

</dd> <dt>

**AVDeltaSignatureVersion**
</dt> <dd>

Tipo: **ULONGLONG**

</dd> <dd>

Versão da assinatura antivírus

</dd> <dt>

**Hashtype**
</dt> <dd>

Tipo: **[ **\_ \_ tipo de hash do MP**](mp-hash-type.md)**

</dd> <dd>

Tipo de hash usado. Consulte [**\_ \_ tipo de hash MP**](mp-hash-type.md).

</dd> <dt>

**Fidelidadevalue**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Valor de fidelidade.

</dd> <dt>

**HashValue**
</dt> <dd>

Tipo: **PG \_ MIDL \_ String LPWSTR**

</dd> <dd>

O hash do arquivo.

</dd> <dt>

**TargetFileName**
</dt> <dd>

Tipo: **PG \_ MIDL \_ String LPWSTR**

</dd> <dd>

O caminho e o nome do arquivo de destino.

</dd> <dt>

**TargetFileHash**
</dt> <dd>

Tipo: **PG \_ MIDL \_ String LPWSTR**

</dd> <dd>

O hash do arquivo de destino.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 8\]<br/>                                            |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2012\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>MpClient. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_tipo de hash MP \_**](mp-hash-type.md)
</dt> </dl>

 

 





