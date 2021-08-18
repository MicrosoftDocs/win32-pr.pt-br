---
description: A \_ estrutura informações sobre a impressora \_ 8 especifica as configurações de impressora padrão globais.
ms.assetid: 98f26a45-5302-4358-bed6-691d9bc37554
title: Estrutura de PRINTER_INFO_8 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTER_INFO_8
- _PRINTER_INFO_8A
- _PRINTER_INFO_8W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 0aa5d516dd099caeba5699a8328fa52add64f14ea970e6ccec28ea8bfbe87271
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119947666"
---
# <a name="printer_info_8-structure"></a>Estrutura de informações da impressora \_ \_ 8

A **estrutura \_ informações \_ sobre a impressora 8** especifica as configurações de impressora padrão globais.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _PRINTER_INFO_8 {
  LPDEVMODE pDevMode;
} PRINTER_INFO_8, *PPRINTER_INFO_8;
```



## <a name="members"></a>Membros

<dl> <dt>

**pDevMode**
</dt> <dd>

Um ponteiro para uma estrutura [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) que define os dados de impressora padrão globais, como a orientação do papel e a resolução.

</dd> </dl>

## <a name="remarks"></a>Comentários

Os padrões globais são definidos pelo administrador de uma impressora que pode ser usada por qualquer pessoa. Por outro lado, os padrões por usuário afetarão um usuário específico ou qualquer outra pessoa que use o perfil. Para padrões por usuário, use as [**informações da \_ impressora \_ 9**](printer-info-9.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                                |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                      |
| Cabeçalho<br/>                   | <dl> <dt>Winspool. h (incluir Windows. h)</dt> </dl> |
| Nomes Unicode e ANSI<br/>   | **\_ Informações de impressora \_ \_ 8W** (Unicode) e **\_ informações de impressora \_ \_ 8a** (ANSI)<br/>                           |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Impressão](printdocs-printing.md)
</dt> <dt>

[Estruturas de API do spooler de impressão](printing-and-print-spooler-structures.md)
</dt> <dt>

[**Getprinter**](getprinter.md)
</dt> <dt>

[**Setprinter**](setprinter.md)
</dt> <dt>

[**Informações da impressora \_ \_ 9**](printer-info-9.md)
</dt> </dl>

 

 




