---
title: Estrutura de MPCONFIGURATION_DATA (MpClient. h)
description: Contém dados sobre alterações de configuração, incluindo os valores novos e antigos.
ms.assetid: AB70B1C0-C148-44BC-8C0E-CC5D2A66BCA5
keywords:
- recursos de ambiente de Windows herdado da estrutura de MPCONFIGURATION_DATA
- Windows recursos de ambiente herdados do ponteiro de estrutura do PMPCONFIGURATION_DATA
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
ms.openlocfilehash: 192cb4d2e35d1b471ef92fb976535bb1e6ed733e2f29ebf86d357f722904514c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120114576"
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

Tipo: **byte \***

</dd> <dd>

Ponteiro para dados anteriores.

</dd> <dt>

**CurrentDataSize**
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
| Cliente mínimo com suporte<br/> | Windows 8 \[ somente aplicativos da área de trabalho\]<br/>                                            |
| Servidor mínimo com suporte<br/> | Windows Server 2012 \[ somente aplicativos da área de trabalho\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>MpClient. h</dt> </dl> |



 

 





