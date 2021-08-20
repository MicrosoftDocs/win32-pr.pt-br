---
title: MPTHREAT_INFOEX_BEHAVIOR (MpClient.h)
description: Contém informações específicas de modificação de comportamento.
ms.assetid: 762E755F-5BA1-476D-B395-6617093309C5
keywords:
- MPTHREAT_INFOEX_BEHAVIOR estrutura herdada Windows recursos de ambiente
- PMPTHREAT_INFOEX_BEHAVIOR de estrutura herdada Windows recursos de ambiente
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
ms.openlocfilehash: 8d0043b371cf4a77523a3b78bc31c5e56a480f134e87a0ed3853939460fc6a3f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117883189"
---
# <a name="mpthreat_infoex_behavior-structure"></a>Estrutura MPTHREAT \_ INFOEX \_ BEHAVIOR

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

**SignatureID**
</dt> <dd>

Tipo: **ULARGE \_ INTEGER**

</dd> <dd>

ID da assinatura de modificação de comportamento determinada pelo mecanismo no momento da detecção.

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

Versão de assinatura antispyware.

</dd> <dt>

**AVDeltaSignatureVersion**
</dt> <dd>

Tipo: **ULONGLONG**

</dd> <dd>

Versão de assinatura antivírus

</dd> <dt>

**HashType**
</dt> <dd>

Tipo: **[ **TIPO DE \_ HASH do \_ MP**](mp-hash-type.md)**

</dd> <dd>

Tipo de hash usado. Consulte [**MP \_ HASH \_ TYPE**](mp-hash-type.md).

</dd> <dt>

**FidelityValue**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Valor de fidelidade.

</dd> <dt>

**Hashvalue**
</dt> <dd>

Tipo: **MP \_ MIDL STRING \_ LPWSTR**

</dd> <dd>

O hash do arquivo.

</dd> <dt>

**TargetFileName**
</dt> <dd>

Tipo: **MP \_ MIDL STRING \_ LPWSTR**

</dd> <dd>

O caminho e o nome do arquivo de alvo.

</dd> <dt>

**TargetFileHash**
</dt> <dd>

Tipo: **MP \_ MIDL STRING \_ LPWSTR**

</dd> <dd>

O hash do arquivo de alvo.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Windows 8 somente aplicativos da área de trabalho\]<br/>                                            |
| Servidor mínimo com suporte<br/> | \[Windows Server 2012 somente aplicativos da área de trabalho\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>MpClient.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**TIPO \_ DE HASH DO \_ MP**](mp-hash-type.md)
</dt> </dl>

 

 





