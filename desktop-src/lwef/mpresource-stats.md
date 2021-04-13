---
title: Estrutura de MPRESOURCE_STATS (MpClient. h)
description: Estatísticas relacionadas a recursos.
ms.assetid: D1DC4BC9-911D-448C-A421-11D2F51F0A61
keywords:
- Recursos do ambiente Windows herdado da estrutura de MPRESOURCE_STATS
- Ponteiro de estrutura de PMPRESOURCE_STATS recursos de ambiente herdados do Windows
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
ms.openlocfilehash: afbe1ce6734aabd1093f7acd886af757c51ed83e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455460"
---
# <a name="mpresource_stats-structure"></a>\_Estrutura de estatísticas MPRESOURCE

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

Progresso aproximado para verificação em ppm (partes por milhão). Defina como **MPPROGRESS \_ inválido** se as informações de progresso não estiverem disponíveis.

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

Número de bytes verificados em busca de arquivos.

</dd> <dt>

**RegKeyCount**
</dt> <dd>

Tipo: **UINT64**

</dd> <dd>

Número de RegKeys verificados.

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
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 8\]<br/>                                            |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2012\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>MpClient. h</dt> </dl> |



 

 





