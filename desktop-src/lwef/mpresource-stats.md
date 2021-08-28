---
title: MPRESOURCE_STATS estrutura (MpClient.h)
description: Estatísticas relacionadas a recursos.
ms.assetid: D1DC4BC9-911D-448C-A421-11D2F51F0A61
keywords:
- MPRESOURCE_STATS estrutura herdada Windows recursos de ambiente
- PMPRESOURCE_STATS de estrutura herdado Windows recursos de ambiente
topic_type:
- apiref
api_name:
- MPRESOURCE_STATS
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b72a21bf0ec020c1fc2cf5ba1394b4cd5ed04dc32721a4aac9f8349034907b49
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119848466"
---
# <a name="mpresource_stats-structure"></a>Estrutura MPRESOURCE \_ STATS

Estatísticas relacionadas a recursos.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct tagMPRESOURCE_STATS {
  DWORD  PPMProgress;
  UINT64 ProcessCount;
  UINT64 FileCount;
  UINT64 FileBytesCount;
  UINT64 RegKeyCount;
  UINT64 Reserved[4];
} MPRESOURCE_STATS, *PMPRESOURCE_STATS;
```



## <a name="members"></a>Membros

<dl> <dt>

**PPMProgress**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Progresso aproximado para verificação em ppm (partes por milhão). Definido como **MPPROGRESS \_ INVALID se** as informações de progresso não estão disponíveis.

</dd> <dt>

**ProcessCount**
</dt> <dd>

Tipo: **UINT64**

</dd> <dd>

Número de processos verificados.

</dd> <dt>

**FileCount**
</dt> <dd>

Tipo: **UINT64**

</dd> <dd>

Número de arquivos verificados.

</dd> <dt>

**FileBytesCount**
</dt> <dd>

Tipo: **UINT64**

</dd> <dd>

Número de bytes verificados para arquivos.

</dd> <dt>

**RegKeyCount**
</dt> <dd>

Tipo: **UINT64**

</dd> <dd>

Número de RegKeys digitalizados.

</dd> <dt>

**Reserved**
</dt> <dd>

Tipo: **UINT64 \[ 4 \]**

</dd> <dd>

Campos reservados para uso futuro.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Windows 8 somente aplicativos da área de trabalho\]<br/>                                            |
| Servidor mínimo com suporte<br/> | \[Windows Server 2012 somente aplicativos da área de trabalho\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>MpClient.h</dt> </dl> |



 

 





