---
description: A estrutura PROVIDOR \_ INFO \_ 1 identifica um provedor de impressão.
ms.assetid: 0eff115a-b3d2-4c8f-b820-46e7f62dd295
title: PROVIDOR_INFO_1 (Winspool.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PROVIDOR_INFO_1
- _PROVIDOR_INFO_1A
- _PROVIDOR_INFO_1W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 4f9e7015382ef34f4582c4772e148059c4ed01de9e81da5af71bc0849df26f15
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120091696"
---
# <a name="providor_info_1-structure"></a>Estrutura PROVIDOR \_ INFO \_ 1

A **estrutura PROVIDOR \_ INFO \_ 1** identifica um provedor de impressão.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _PROVIDOR_INFO_1 {
  LPTSTR pName;
  LPTSTR pEnvironment;
  LPTSTR pDLLName;
} PROVIDOR_INFO_1, *PPROVIDOR_INFO_1;
```



## <a name="members"></a>Membros

<dl> <dt>

**Pname**
</dt> <dd>

Ponteiro para uma cadeia de caracteres terminada em nulo que é o nome do provedor de impressão.

</dd> <dt>

**pEnvironment**
</dt> <dd>

Ponteiro para uma cadeia de caracteres de ambiente terminada em nulo especificando o ambiente em que a DLL (biblioteca de vínculo dinâmico) do provedor foi projetada para ser executado.

</dd> <dt>

**pDLLName**
</dt> <dd>

Ponteiro para uma cadeia de caracteres terminada em nulo que é o nome do provedor .dll.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                                |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                      |
| Cabeçalho<br/>                   | <dl> <dt>Winspool.h (incluir Windows.h)</dt> </dl> |
| Nomes Unicode e ANSI<br/>   | **\_ PROVIDOR \_ INFO \_ 1W** (Unicode) e **\_ PROVIDOR \_ INFO \_ 1A** (ANSI)<br/>                         |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Impressão](printdocs-printing.md)
</dt> <dt>

[Imprimir estruturas de API do Spooler](printing-and-print-spooler-structures.md)
</dt> <dt>

[**AddPrintProvidor**](addprintprovidor.md)
</dt> </dl>

 

 




