---
description: Contém uma matriz de BLOBs.
ms.assetid: e87f493b-f160-4316-b369-75d20c735213
title: Estrutura de BLOB_TABLE (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- BLOB_TABLE
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 32bacc925381f1c7ed30aa66247671b67e31b7e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104169381"
---
# <a name="blob_table-structure"></a>Estrutura da tabela de BLOBs \_

A estrutura da **\_ tabela de BLOBs** contém uma matriz de BLOBs.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct {
  DWORD dwNumBlobs;
  HBLOB hBlobs[];
} BLOB_TABLE, *PBLOB_TABLE;
```



## <a name="members"></a>Membros

<dl> <dt>

**dwNumBlobs**
</dt> <dd>

Indicador de que muitos BLOBs seguem.

</dd> <dt>

**hBlobs**
</dt> <dd>

Identificador para a matriz de BLOBs.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                          |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                |
| Cabeçalho<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



 

 




