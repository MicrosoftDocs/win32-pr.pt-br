---
title: Estrutura de MPCONFIGURATION_DATA (MpClient. h)
description: Contém dados sobre alterações de configuração, incluindo os valores novos e antigos.
ms.assetid: AB70B1C0-C148-44BC-8C0E-CC5D2A66BCA5
keywords:
- Recursos do ambiente Windows herdado da estrutura de MPCONFIGURATION_DATA
- Ponteiro de estrutura de PMPCONFIGURATION_DATA recursos de ambiente herdados do Windows
topic_type:
- apiref
api_name:
- MPCONFIGURATION_DATA
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7bb54ae4e323f2144dd25c52005d8484b0a207e6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009219"
---
# <a name="mpconfiguration_data-structure"></a>\_Estrutura de dados MPCONFIGURATION

Contém dados sobre alterações de configuração, incluindo os valores novos e antigos.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct tagMPCONFIGURATION_DATA {
  MP_MIDL_STRING LPWSTR ConfigurationName;
  DWORD                 DataType;
  DWORD                 PreviousDataSize;
  BYTE                  *pPreviousData;
  DWORD                 CurrentDataSize;
  BYTE                  *pCurrentData;
} MPCONFIGURATION_DATA, *PMPCONFIGURATION_DATA;
```



## <a name="members"></a>Membros

<dl> <dt>

**ConfigurationName**
</dt> <dd>

Tipo: **PG \_ MIDL \_ String LPWSTR**

</dd> <dd>

Nome da configuração que foi alterada.

</dd> <dt>

**DataType**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

O tipo de dados usados.

</dd> <dt>

**PreviousDataSize**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Tamanho dos dados anteriores, em bytes.

</dd> <dt>

**pPreviousData**
</dt> <dd>

Tipo: **byte \** _

</dd> <dd>

Ponteiro para dados anteriores.

</dd> <dt>

_ *CurrentDataSize**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Tamanho dos novos dados, em bytes.

</dd> <dt>

**pCurrentData**
</dt> <dd>

Tipo: **byte \***

</dd> <dd>

Ponteiro para novos dados.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 8\]<br/>                                            |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2012\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>MpClient. h</dt> </dl> |



 

 





