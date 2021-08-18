---
description: A \_ estrutura padrões da impressora especifica o tipo de dados padrão, o ambiente, os dados de inicialização e os direitos de acesso de uma impressora.
ms.assetid: df29c3a6-b1d1-4d40-887d-5ffc032a5871
title: Estrutura de PRINTER_DEFAULTS (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTER_DEFAULTS
- _PRINTER_DEFAULTSA
- _PRINTER_DEFAULTSW
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: f1419948dddcd579e559ed084ce0af092cec373a7cd7f6d4b05d41f104f6666b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118731684"
---
# <a name="printer_defaults-structure"></a>Estrutura de padrões de impressora \_

A **estrutura \_ padrões da impressora** especifica o tipo de dados padrão, o ambiente, os dados de inicialização e os direitos de acesso de uma impressora.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _PRINTER_DEFAULTS {
  LPTSTR      pDatatype;
  LPDEVMODE   pDevMode;
  ACCESS_MASK DesiredAccess;
} PRINTER_DEFAULTS, *PPRINTER_DEFAULTS;
```



## <a name="members"></a>Membros

<dl> <dt>

**pDatatype**
</dt> <dd>

Ponteiro para uma cadeia de caracteres terminada em nulo que especifica o tipo de dados padrão para uma impressora.

</dd> <dt>

**pDevMode**
</dt> <dd>

Ponteiro para uma estrutura [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) que identifica o ambiente padrão e os dados de inicialização para uma impressora.

</dd> <dt>

**DesiredAccess**
</dt> <dd>

Especifica os direitos de acesso desejados para uma impressora. A função [**OpenPrinter**](openprinter.md) usa esse membro para definir direitos de acesso à impressora. Esses direitos podem afetar a operação das funções [**Setprinter**](setprinter.md) e [**DeletePrinter**](deleteprinter.md) . Os direitos de acesso podem ser um dos seguintes.



| Valor                                       | Significado                                                                                                                                                                                      |
|---------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| acesso de impressora \_ \_ administrar                 | Para executar tarefas administrativas, como as fornecidas pelo [**Setprinter**](setprinter.md).                                                                                                 |
| \_uso de acesso à impressora \_                        | Para executar operações básicas de impressão.                                                                                                                                                        |
| \_Gerenciamento de acesso à impressora \_ \_ limitado            | Para executar tarefas administrativas, como as fornecidas por [**Setprinter**](setprinter.md) e [**SetPrinterData**](setprinterdata.md). Esse valor está disponível a partir de Windows 8.1. |
| \_todos os \_ acessos à impressora                        | Para executar todas as tarefas administrativas e operações básicas de impressão, exceto para sincronizar (consulte [direitos de acesso padrão](/windows/desktop/SecAuthZ/standard-access-rights) ).                                   |
| valores de segurança genéricos, como gravar \_ DAC | Para permitir direitos de acesso de controle específico. Consulte [direitos de acesso padrão](/windows/desktop/SecAuthZ/standard-access-rights).                                                                                      |



 

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                                |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                      |
| Cabeçalho<br/>                   | <dl> <dt>Winspool. h (incluir Windows. h)</dt> </dl> |
| Nomes Unicode e ANSI<br/>   | **\_ \_ DEFAULTSW de impressora** (Unicode) e **\_ \_ DEFAULTSA de impressora** (ANSI)<br/>                         |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Impressão](printdocs-printing.md)
</dt> <dt>

[Estruturas de API do spooler de impressão](printing-and-print-spooler-structures.md)
</dt> <dt>

[**DeletePrinter**](deleteprinter.md)
</dt> <dt>

[**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea)
</dt> <dt>

[**OpenPrinter**](openprinter.md)
</dt> <dt>

[**Setprinter**](setprinter.md)
</dt> </dl>

 

