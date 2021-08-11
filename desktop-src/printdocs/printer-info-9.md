---
description: A \_ estrutura informações da impressora \_ 9 especifica as configurações de impressora padrão por usuário.
ms.assetid: 8bafb995-f31c-46e3-a950-45e240c678aa
title: Estrutura de PRINTER_INFO_9 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTER_INFO_9
- _PRINTER_INFO_9A
- _PRINTER_INFO_9W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 684ffc6ccfc4f94c036bde42faec9458c8bb60911fc8c9398006f58631baa791
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118234231"
---
# <a name="printer_info_9-structure"></a>Estrutura de informações da impressora \_ \_ 9

A **estrutura \_ informações \_ da impressora 9** especifica as configurações de impressora padrão por usuário.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _PRINTER_INFO_9 {
  LPDEVMODE pDevMode;
} PRINTER_INFO_9, *PPRINTER_INFO_9;
```



## <a name="members"></a>Membros

<dl> <dt>

**pDevMode**
</dt> <dd>

Um ponteiro para uma estrutura [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) que define os dados de impressora padrão por usuário, como a orientação do papel e a resolução. O **DEVMODE** é armazenado no registro do usuário.

</dd> </dl>

## <a name="remarks"></a>Comentários

Os padrões por usuário afetarão apenas um usuário específico ou qualquer pessoa que use o perfil. Por outro lado, os padrões globais são definidos pelo administrador de uma impressora que pode ser usada por qualquer pessoa. Para padrões globais, use as [**informações da impressora \_ \_ 8**](printer-info-8.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                                |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                      |
| Cabeçalho<br/>                   | <dl> <dt>Winspool. h (incluir Windows. h)</dt> </dl> |
| Nomes Unicode e ANSI<br/>   | **\_ Informações de impressora \_ \_ 9W** (Unicode) e **\_ informações de impressora \_ \_ 9a** (ANSI)<br/>                           |



## <a name="see-also"></a>Veja também

<dl> <dt>

[Impressão](printdocs-printing.md)
</dt> <dt>

[Estruturas de API do spooler de impressão](printing-and-print-spooler-structures.md)
</dt> <dt>

[**Getprinter**](getprinter.md)
</dt> <dt>

[**Setprinter**](setprinter.md)
</dt> <dt>

[**Informações da impressora \_ \_ 8**](printer-info-8.md)
</dt> </dl>

 

 




