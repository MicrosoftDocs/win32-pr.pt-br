---
description: A estrutura informações de tipos de \_ \_ dados 1 contém informações sobre o tipo de dado usado para registrar um trabalho de impressão.
ms.assetid: 6169006c-12d4-4608-865c-732f04107f9f
title: Estrutura de DATATYPES_INFO_1 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DATATYPES_INFO_1
- _DATATYPES_INFO_1A
- _DATATYPES_INFO_1W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 05defe3d8cc6cd66b15b2cacdd3d3d1d56c348e4946a43700278f100ea17da5d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119719666"
---
# <a name="datatypes_info_1-structure"></a>Estrutura de informações de tipos de dados \_ \_ 1

A estrutura informações de tipos de dados **\_ \_ 1** contém informações sobre o tipo de dado usado para registrar um trabalho de impressão.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _DATATYPES_INFO_1 {
  LPTSTR pName;
} DATATYPES_INFO_1, *PDATATYPES_INFO_1;
```



## <a name="members"></a>Membros

<dl> <dt>

**pName**
</dt> <dd>

Ponteiro para uma cadeia de caracteres terminada em nulo que identifica o tipo de dados usado para gravar um trabalho de impressão.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                                |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                      |
| Cabeçalho<br/>                   | <dl> <dt>Winspool. h (incluir Windows. h)</dt> </dl> |
| Nomes Unicode e ANSI<br/>   | Informações de **\_ tipos \_ de \_ 1W** (Unicode) e **\_ informações de tipos de DataType \_ \_ 1a** (ANSI)<br/>                       |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Impressão](printdocs-printing.md)
</dt> <dt>

[Estruturas de API do spooler de impressão](printing-and-print-spooler-structures.md)
</dt> <dt>

[**EnumPrintProcessorDatatypes**](enumprintprocessordatatypes.md)
</dt> </dl>

 

 




