---
description: Associa um nome de grupo e seu identificador.
ms.assetid: 76f3fe37-cf85-42ab-8f9e-3ab2c6053dcd
title: Estrutura GROUPINFO (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GROUPINFO
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 5152b0a621a34e49d6f1024a81b7e91aed94a06b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105787483"
---
# <a name="groupinfo-structure"></a>Estrutura GROUPINFO

A estrutura **GROUPINFO** associa um nome de grupo e seu identificador.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct {
  char   szGroupName[EXPERTGROUPNAMELENGTH+1];
  HGROUP hGroup;
} GROUPINFO, *PGROUPINFO;
```



## <a name="members"></a>Membros

<dl> <dt>

**szGroupName**
</dt> <dd>

Valor incrementado de uma matriz na estrutura **GroupName** .

</dd> <dt>

**hGroup**
</dt> <dd>

Identificador para um grupo.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                          |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                |
| Cabeçalho<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



 

 




