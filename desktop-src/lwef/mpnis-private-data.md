---
title: Estrutura de MPNIS_PRIVATE_DATA (MpClient. h)
description: Notificações NIS privadas.
ms.assetid: 19B4928F-BC78-4DEA-A563-1516B6454465
keywords:
- recursos de ambiente de Windows herdado da estrutura de MPNIS_PRIVATE_DATA
- Windows recursos de ambiente herdados do ponteiro de estrutura do PMPNIS_PRIVATE_DATA
topic_type:
- apiref
api_name:
- MPNIS_PRIVATE_DATA
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a50719e4ecc0beff848467023a1c5f941ff06ceb891b05674e199d47a38b8659
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119556136"
---
# <a name="mpnis_private_data-structure"></a>\_Estrutura de dados privada do MPNIS \_

Notificações NIS privadas.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct tagMPNIS_PRIVATE_DATA {
  DWORD dwNotificationType;
  DWORD cbDataSize;
  BYTE  *pbData;
} MPNIS_PRIVATE_DATA, *PMPNIS_PRIVATE_DATA;
```



## <a name="members"></a>Membros

<dl> <dt>

**dwNotificationType**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Tipo de notificação.

</dd> <dt>

**cbDataSize**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Tamanho dos dados reservados, em bytes.

</dd> <dt>

**pbData**
</dt> <dd>

Tipo: **byte \***

</dd> <dd>

Ponteiro para dados reservados.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8 \[ somente aplicativos da área de trabalho\]<br/>                                            |
| Servidor mínimo com suporte<br/> | Windows Server 2012 \[ somente aplicativos da área de trabalho\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>MpClient. h</dt> </dl> |



 

 





