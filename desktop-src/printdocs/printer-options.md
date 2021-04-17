---
description: Representa opções de impressora.
ms.assetid: 7cc3d10c-8bc2-4899-b083-63d802ee16e7
title: Estrutura de PRINTER_OPTIONS (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTER_OPTIONS
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 37c45277f0a7e30bc94b2d23ffa27de0092a7164
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105770652"
---
# <a name="printer_options-structure"></a>Estrutura de opções de impressora \_

Representa opções de impressora.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _PRINTER_OPTIONS {
  UINT  cbSize;
  DWORD dwFlags;
} PRINTER_OPTIONS, *PPRINTER_OPTIONS;
```



## <a name="members"></a>Membros

<dl> <dt>

**cbSize**
</dt> <dd>

O tamanho da estrutura **de \_ Opções da impressora** .

</dd> <dt>

**dwFlags**
</dt> <dd>

Um conjunto de [**\_ \_ sinalizadores de opção de impressora**](printer-option-flags.md) que especifica como o identificador para uma impressora retornada por [**OpenPrinter2**](openprinter2.md) será usado por outras funções.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                                            |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                                      |
| parâmetro<br/>                   | <dl> <dt>Winspool. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Impressão](printdocs-printing.md)
</dt> <dt>

[Estruturas de API do spooler de impressão](printing-and-print-spooler-structures.md)
</dt> <dt>

[**OpenPrinter2**](openprinter2.md)
</dt> <dt>

[**\_sinalizadores de opção de impressora \_**](printer-option-flags.md)
</dt> </dl>

 

 




