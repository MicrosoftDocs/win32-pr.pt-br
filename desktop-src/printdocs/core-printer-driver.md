---
description: Representa um driver de impressora do qual outros drivers de impressora dependem.
ms.assetid: b03f9ac1-7ad2-4aee-b496-e1ee15ba7d38
title: CORE_PRINTER_DRIVER (Winspool.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CORE_PRINTER_DRIVER
- _CORE_PRINTER_DRIVERA
- _CORE_PRINTER_DRIVERW
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 18ac3dba88d9cf781393b01b6594777426b7195e6f68afa0fd00a5bddb01f129
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119950396"
---
# <a name="core_printer_driver-structure"></a>Estrutura \_ CORE PRINTER \_ DRIVER

Representa um driver de impressora do qual outros drivers de impressora dependem.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _CORE_PRINTER_DRIVER {
  GUID      CoreDriverGUID;
  FILETIME  ftDriverDate;
  DWORDLONG dwlDriverVersion;
  TCHAR     szPackageID[MAX_PATH];
} CORE_PRINTER_DRIVER, *PCORE_PRINTER_DRIVER;
```



## <a name="members"></a>Membros

<dl> <dt>

**CoreDriverGUID**
</dt> <dd>

O GUID do driver de impressora principal.

</dd> <dt>

**ftDriverDate**
</dt> <dd>

A data e a hora da versão mais recente do driver de impressora principal.

</dd> <dt>

**dwlDriverVersion**
</dt> <dd>

A ID da versão mais recente do driver de impressora principal.

</dd> <dt>

**szPackageID \[ MAX \_ PATH\]**
</dt> <dd>

O caminho para o pacote de driver que contém o driver de impressora principal.

</dd> </dl>

## <a name="remarks"></a>Comentários

Essa estrutura pode representar o driver base de um fabricante no qual os drivers para vários modelos de impressora dependem.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                                            |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                                                      |
| Cabeçalho<br/>                   | <dl> <dt>Winspool.h (incluir Windows.h)</dt> </dl> |
| Nomes Unicode e ANSI<br/>   | **\_ CORE \_ PRINTER \_ DRIVERW** (Unicode) e **\_ CORE PRINTER \_ \_ DRIVERA** (ANSI)<br/>                 |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Impressão](printdocs-printing.md)
</dt> <dt>

[Imprimir estruturas de API do Spooler](printing-and-print-spooler-structures.md)
</dt> </dl>

 

 




