---
description: A \_ estrutura informações da impressora \_ 3 especifica as informações de segurança da impressora.
ms.assetid: 527d635d-2d75-4b56-bab7-e95c9919a8fb
title: Estrutura de PRINTER_INFO_3 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTER_INFO_3
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: aad24e56d43f6fadd3da3f627b2399249a7ff8a6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105812398"
---
# <a name="printer_info_3-structure"></a>Estrutura de informações da impressora \_ \_ 3

A **estrutura \_ informações \_ da impressora 3** especifica as informações de segurança da impressora.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _PRINTER_INFO_3 {
  PSECURITY_DESCRIPTOR pSecurityDescriptor;
} PRINTER_INFO_3, *PPRINTER_INFO_3;
```



## <a name="members"></a>Membros

<dl> <dt>

**pSecurityDescriptor**
</dt> <dd>

Ponteiro para uma estrutura de [**\_ descritor de segurança**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) que especifica as informações de segurança de uma impressora.

</dd> </dl>

## <a name="remarks"></a>Comentários

A **estrutura \_ informações \_ da impressora 3** permite que um aplicativo obtenha e defina o descritor de segurança de uma impressora. O chamador pode fazer isso mesmo que não tenha permissões de impressora específicas, desde que tenha os direitos padrão descritos em [**Setprinter**](setprinter.md) e [**getprinter**](getprinter.md). Assim, um aplicativo pode negar temporariamente todo o acesso a uma impressora, enquanto permite que o proprietário da impressora tenha acesso à ACL discricionária da impressora.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                                |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                      |
| Cabeçalho<br/>                   | <dl> <dt>Winspool. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Impressão](printdocs-printing.md)
</dt> <dt>

[Estruturas de API do spooler de impressão](printing-and-print-spooler-structures.md)
</dt> <dt>

[**Setprinter**](setprinter.md)
</dt> <dt>

[**Getprinter**](getprinter.md)
</dt> <dt>

[**Informações da impressora \_ \_ 1**](printer-info-1.md)
</dt> <dt>

[**Informações da impressora \_ \_ 2**](printer-info-2.md)
</dt> <dt>

[**Informações da impressora \_ \_ 4**](printer-info-4.md)
</dt> <dt>

[**\_descritor de segurança**](/windows/desktop/api/winnt/ns-winnt-security_descriptor)
</dt> </dl>

 

