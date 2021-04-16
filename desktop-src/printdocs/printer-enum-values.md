---
description: A estrutura de valores de enumeração da impressora \_ \_ especifica o nome do valor, o tipo e os dados para um valor de configuração de impressora retornado pela função EnumPrinterDataEx.
ms.assetid: 87eb1452-0d9d-46bd-8af8-0542a11a929b
title: Estrutura de PRINTER_ENUM_VALUES (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTER_ENUM_VALUES
- _PRINTER_ENUM_VALUESA
- _PRINTER_ENUM_VALUESW
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: ea73318db7a91fa4d422624b1c3c0c6f09d97cb0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105772541"
---
# <a name="printer_enum_values-structure"></a>Estrutura de valores de \_ enumeração de impressora \_

A estrutura de **\_ \_ valores de enumeração da impressora** especifica o nome do valor, o tipo e os dados para um valor de configuração de impressora retornado pela função [**EnumPrinterDataEx**](enumprinterdataex.md) .

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _PRINTER_ENUM_VALUES {
  LPTSTR pValueName;
  DWORD  cbValueName;
  DWORD  dwType;
  LPBYTE pData;
  DWORD  cbData;
} PRINTER_ENUM_VALUES, *PPRINTER_ENUM_VALUES;
```



## <a name="members"></a>Membros

<dl> <dt>

**Valores principais**
</dt> <dd>

Ponteiro para uma cadeia de caracteres terminada em nulo que especifica o nome do valor recuperado.

</dd> <dt>

**cbValueName**
</dt> <dd>

O número de bytes **no membro de valor de espaço** , incluindo o caractere nulo de terminação.

</dd> <dt>

**dwType**
</dt> <dd>

Um código que indica o tipo de dados apontado pelo membro **pData** . Para obter uma lista dos possíveis códigos de tipo, consulte [tipos de valor do registro](/windows/desktop/SysInfo/registry-value-types).

</dd> <dt>

**pData**
</dt> <dd>

Ponteiro para um buffer que contém os dados para o valor recuperado.

</dd> <dt>

**cbData**
</dt> <dd>

O número de bytes recuperados no buffer **pData** .

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                                |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                      |
| Cabeçalho<br/>                   | <dl> <dt>Winspool. h (incluir Windows. h)</dt> </dl> |
| Nomes Unicode e ANSI<br/>   | **\_ \_ \_ VALUESW de enumeração de impressora** (Unicode) e **\_ \_ \_ valores de enum de impressora** (ANSI)<br/>                 |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Impressão](printdocs-printing.md)
</dt> <dt>

[Estruturas de API do spooler de impressão](printing-and-print-spooler-structures.md)
</dt> <dt>

[**EnumPrinterDataEx**](enumprinterdataex.md)
</dt> </dl>

 

