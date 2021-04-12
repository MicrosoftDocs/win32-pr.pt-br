---
description: A \_ estrutura info \_ 1 do PROVIDOR identifica um provedor de impressão.
ms.assetid: 0eff115a-b3d2-4c8f-b820-46e7f62dd295
title: Estrutura de PROVIDOR_INFO_1 (winspool. h)
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
ms.openlocfilehash: 2eabc00009b76247af71b06ea877ca0bf738c1d5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297146"
---
# <a name="providor_info_1-structure"></a>Estrutura de informações de PROVIDOR \_ \_ 1

A **estrutura \_ info \_ 1 do PROVIDOR** identifica um provedor de impressão.

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

**pName**
</dt> <dd>

Ponteiro para uma cadeia de caracteres terminada em nulo que é o nome do provedor de impressão.

</dd> <dt>

**pEnvironment**
</dt> <dd>

Ponteiro para uma cadeia de caracteres de ambiente terminada em nulo que especifica o ambiente no qual a DLL (biblioteca de vínculo dinâmico) do provedor foi projetada para ser executada.

</dd> <dt>

**pDLLName**
</dt> <dd>

Ponteiro para uma cadeia de caracteres terminada em nulo que é o nome do Provider. dll.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                                |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                      |
| Cabeçalho<br/>                   | <dl> <dt>Winspool. h (incluir Windows. h)</dt> </dl> |
| Nomes Unicode e ANSI<br/>   | **\_ PROVIDOR \_ info \_ 1W** (Unicode) e **\_ PROVIDOR \_ info \_ 1a** (ANSI)<br/>                         |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Impressão](printdocs-printing.md)
</dt> <dt>

[Estruturas de API do spooler de impressão](printing-and-print-spooler-structures.md)
</dt> <dt>

[**AddPrintProvidor**](addprintprovidor.md)
</dt> </dl>

 

 




