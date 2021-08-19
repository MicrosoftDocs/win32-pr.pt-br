---
description: Estatísticas de recursos coletadas pelo ResourceManager D3DDEVINFO ao usar o mecanismo de consulta \_ assíncrona.
ms.assetid: f4d9c6db-4002-439c-9a88-485763badc82
title: Estrutura D3DRESOURCESTATS (D3D9Types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DRESOURCESTATS
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: dc992c5b8246ce302cda8924b8521c923575c8914c83b35c8c1e789e4bc1c826
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118527468"
---
# <a name="d3dresourcestats-structure"></a>Estrutura D3DRESOURCESTATS

Estatísticas de recursos coletadas pelo [**\_ ResourceManager D3DDEVINFO**](d3ddevinfo-resourcemanager.md) ao usar o mecanismo de consulta assíncrona.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct D3DRESOURCESTATS {
  BOOL  bThrashing;
  DWORD ApproxBytesDownloaded;
  DWORD NumEvicts;
  DWORD NumVidCreates;
  DWORD LastPri;
  DWORD NumUsed;
  DWORD NumUsedInVidMem;
  DWORD WorkingSet;
  DWORD WorkingSetBytes;
  DWORD TotalManaged;
  DWORD TotalBytes;
} D3DRESOURCESTATS, *LPD3DRESOURCESTATS;
```



## <a name="members"></a>Membros

<dl> <dt>

**bThrashing**
</dt> <dd>

Tipo: **[ **BOOL**](../winprog/windows-data-types.md)**

</dd> <dd>

Indica se a reação está ocorrendo.

</dd> <dt>

**ApproxBytesDownloaded**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Número aproximado de bytes baixados pelo gerenciador de recursos.

</dd> <dt>

**NumEvicts**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Número de objetos despejados.

</dd> <dt>

**NumVidCreates**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Número de objetos criados na memória de vídeo.

</dd> <dt>

**LastPri**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Prioridade do último objeto desalojado.

</dd> <dt>

**NumUsed**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Número de objetos definidos para o dispositivo.

</dd> <dt>

**NumUsedInVidMem**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Número de objetos definidos para o dispositivo, que já estão na memória de vídeo.

</dd> <dt>

**Workingset**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Número de objetos na memória de vídeo.

</dd> <dt>

**WorkingSetBytes**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Número de bytes na memória de vídeo.

</dd> <dt>

**TotalManaged**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Número total de objetos gerenciados.

</dd> <dt>

**TotalBytes**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Número total de bytes de objetos gerenciados.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3D9Types.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Estruturas Direct3D](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[Notificação assíncrona (Direct3D 9)](asynchronous-notification.md)
</dt> </dl>

 

 
