---
description: Representa um driver de impressora no qual dependem outros drivers de impressora.
ms.assetid: b03f9ac1-7ad2-4aee-b496-e1ee15ba7d38
title: Estrutura de CORE_PRINTER_DRIVER (winspool. h)
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
ms.openlocfilehash: 786fa3491919659fca60700cfb086023c3fdef3f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105751940"
---
# <a name="core_printer_driver-structure"></a>Estrutura de driver de \_ impressora principal \_

Representa um driver de impressora no qual dependem outros drivers de impressora.

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

**\[caminho máximo de szPackageID \_\]**
</dt> <dd>

O caminho para o pacote de driver que contém o driver de impressora principal.

</dd> </dl>

## <a name="remarks"></a>Comentários

Essa estrutura pode representar o driver base de um fabricante no qual os drivers para vários modelos de impressora são dependentes.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                                            |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                                      |
| parâmetro<br/>                   | <dl> <dt>Winspool. h (incluir Windows. h)</dt> </dl> |
| Nomes Unicode e ANSI<br/>   | **\_ \_ \_ DRIVERW de impressora principal** (Unicode) e **\_ \_ \_ Driver de impressora de núcleo** (ANSI)<br/>                 |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Impressão](printdocs-printing.md)
</dt> <dt>

[Estruturas de API do spooler de impressão](printing-and-print-spooler-structures.md)
</dt> </dl>

 

 




