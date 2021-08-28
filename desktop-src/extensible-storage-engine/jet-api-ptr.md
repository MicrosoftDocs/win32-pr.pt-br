---
description: 'Saiba mais sobre: JET_API_PTR'
title: JET_API_PTR
TOCTitle: JET_API_PTR
ms:assetid: 27b1eeec-1707-4edb-a4b2-2619190c21e7
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269209(v=EXCHG.10)
ms:contentKeyID: 32765512
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ddf50b5bb5e65ca60677f5578170b84f744016e9
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122985299"
---
# <a name="jet_api_ptr"></a>JET_API_PTR


_**Aplica-se a:** Windows | Windows Servidor_

## <a name="jet_api_ptr"></a>JET_API_PTR

O **JET_API_PTR** tipo de dados contém um inteiro ou um valor de ponteiro.

```cpp
    #if defined(_WIN64)
        typedef unsigned __int64 JET_API_PTR;
    #elif !defined(__midl) && (defined(_X86_) || defined(_M_IX86)) && _MSC_VER >= 1300
        typedef __w64 unsigned long JET_API_PTR;
    #else
        typedef unsigned long JET_API_PTR;
    #endif
```

### <a name="data-types"></a>Tipos de dados

JET_API_PTR

Como um **DWORD_PTR** de dados, o **tipo de** dados JET_API_PTR é definido como 4 bytes em um computador de 32 bits e 8 bytes em um computador de 64 bits.

### <a name="remarks"></a>Comentários

O **JET_API_PTR** de dados é usado para definir os seguintes tipos de dados:

  - [JET_HANDLE](./jet-handle.md)

  - [JET_INSTANCE](./jet-instance.md)

  - [JET_SESID](./jet-sesid.md)

  - [JET_TABLEID](./jet-tableid.md)

  - [JET_LS](./jet-ls.md)

### <a name="requirements"></a>Requisitos


| Requisito | Valor |
|------------|----------|
| <p><strong>Cliente</strong></p> | <p>Requer Windows Vista, Windows XP ou Windows 2000 Professional.</p> | 
| <p><strong>Servidor</strong></p> | <p>Requer Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</p> | 
| <p><strong>Cabeçalho</strong></p> | <p>Declarado em Esent.h.</p> | 

