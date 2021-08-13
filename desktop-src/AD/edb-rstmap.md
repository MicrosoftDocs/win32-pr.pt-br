---
title: Estrutura de EDB_RSTMAP (Ntdsbcli. h)
description: Usado com a função DsRestoreRegister para mapear um banco de dados de backup para um novo banco de dados.
ms.assetid: b2c5d30a-3617-4807-82e8-57f7179b817c
ms.tgt_platform: multiple
keywords:
- Estrutura de EDB_RSTMAP Active Directory
- Ponteiro de estrutura de PEDB_RSTMAP Active Directory
topic_type:
- apiref
api_name:
- EDB_RSTMAP
- EDB_RSTMAPA
- EDB_RSTMAPW
api_location:
- Ntdsbcli.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c81fe35d8d41818d279df094a57c041b8ea52212d2ce2f0cdc379628f5d5971
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118191687"
---
# <a name="edb_rstmap-structure"></a>\_Estrutura RSTMAP EDB

A **estrutura \_ RSTMAP do EDB** é usada com a função [**DsRestoreRegister**](dsrestoreregister.md) para mapear um banco de dados de backup para um novo banco de dados.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct {
  LPTSTR szDatabaseName;
  LPTSTR szNewDatabaseName;
} EDB_RSTMAP, *PEDB_RSTMAP;
```



## <a name="members"></a>Membros

<dl> <dt>

**szDatabaseName**
</dt> <dd>

Ponteiro para uma cadeia de caracteres terminada em nulo que contém o nome do banco de dados em que foi feito o backup.

</dd> <dt>

**szNewDatabaseName**
</dt> <dd>

Ponteiro para uma cadeia de caracteres terminada em nulo que contém o novo nome do banco de dados, incluindo seu novo local, quando aplicável.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                              |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                        |
| parâmetro<br/>                   | <dl> <dt>Ntdsbcli. h</dt> </dl> |
| Nomes Unicode e ANSI<br/>   | **EDB \_ RSTMAPW** (Unicode) e **\_ RSTMAPA EDB** (ANSI)<br/>                     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**DsRestoreRegister**](dsrestoreregister.md)
</dt> <dt>

[Estruturas de backup de diretório](directory-backup-structures.md)
</dt> </dl>

 

 





