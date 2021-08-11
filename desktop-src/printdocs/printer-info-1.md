---
description: A estrutura PRINTER \_ INFO \_ 1 especifica informações gerais da impressora.
ms.assetid: 0b0e2d0e-2625-4cab-a8f9-536185479443
title: PRINTER_INFO_1 (Winspool.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTER_INFO_1
- _PRINTER_INFO_1A
- _PRINTER_INFO_1W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: ab70662371ef4ebe80b1d10f7f61700c97e979959c337bb5e81b3bc688e8c36b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118234203"
---
# <a name="printer_info_1-structure"></a>Estrutura INFORMAÇÕES \_ \_ DA IMPRESSORA 1

A **estrutura PRINTER INFO \_ \_ 1** especifica informações gerais da impressora.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _PRINTER_INFO_1 {
  DWORD  Flags;
  LPTSTR pDescription;
  LPTSTR pName;
  LPTSTR pComment;
} PRINTER_INFO_1, *PPRINTER_INFO_1;
```



## <a name="members"></a>Membros

<dl> <dt>

**Sinalizadores**
</dt> <dd>

Especifica informações sobre os dados retornados. A seguir estão os valores para esse membro.



| Valor                    | Significado                                                                                                                                                                                                                                                   |
|--------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| PRINTER \_ ENUM \_ EXPAND    | Um provedor de impressão pode definir esse sinalizador como uma dica para um aplicativo de chamada para enumerar esse objeto ainda mais se a expansão padrão estiver habilitada. Por exemplo, quando os domínios são enumerados, um provedor de impressão pode indicar o domínio do usuário definindo esse sinalizador. |
| CONTÊINER \_ ENUM DA \_ IMPRESSORA | Se esse sinalizador for definido, o objeto de impressora poderá conter objetos enumeráveis. Por exemplo, o objeto pode ser um servidor de impressão que contém impressoras.                                                                                                             |
| ÍCONE \_ DE ENUM \_ DA IMPRESSORA1     | Indica que, quando apropriado, um aplicativo deve exibir um ícone que identifica o objeto como um nome de rede de nível superior, como Microsoft Windows Network.                                                                                           |
| ÍCONE \_ DE ENUM \_ DA IMPRESSORA2     | Indica que, quando apropriado, um aplicativo deve exibir um ícone que identifica o objeto como um domínio de rede.                                                                                                                                  |
| ÍCONE \_ DE ENUM \_ DA IMPRESSORA3     | Indica que, quando apropriado, um aplicativo deve exibir um ícone que identifica o objeto como um servidor de impressão.                                                                                                                                    |
| ÍCONE \_ DE ENUM \_ DA IMPRESSORA4     | Reservado.                                                                                                                                                                                                                                                 |
| ÍCONE \_ DE ENUM \_ DA IMPRESSORA5     | Reservado.                                                                                                                                                                                                                                                 |
| ÍCONE \_ DE ENUM \_ DA IMPRESSORA6     | Reservado.                                                                                                                                                                                                                                                 |
| ÍCONE \_ DE ENUM \_ DA IMPRESSORA7     | Reservado.                                                                                                                                                                                                                                                 |
| ÍCONE \_ DE ENUM \_ DA IMPRESSORA8     | Indica que, quando apropriado, um aplicativo deve exibir um ícone que identifica o objeto como uma impressora.                                                                                                                                         |



 

</dd> <dt>

**pDescription**
</dt> <dd>

Ponteiro para uma cadeia de caracteres terminada em nulo que descreve o conteúdo da estrutura.

</dd> <dt>

**Pname**
</dt> <dd>

Ponteiro para uma cadeia de caracteres terminada em nulo que nomeia o conteúdo da estrutura.

</dd> <dt>

**pComment**
</dt> <dd>

Ponteiro para uma cadeia de caracteres terminada em nulo que contém dados adicionais que descrevem a estrutura.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                                |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                      |
| Cabeçalho<br/>                   | <dl> <dt>Winspool.h (incluir Windows.h)</dt> </dl> |
| Nomes Unicode e ANSI<br/>   | **\_ INFORMAÇÕES \_ DA IMPRESSORA \_ 1W** (Unicode) e INFORMAÇÕES DA IMPRESSORA **\_ \_ \_ 1A** (ANSI)<br/>                           |



## <a name="see-also"></a>Veja também

<dl> <dt>

[Impressão](printdocs-printing.md)
</dt> <dt>

[Imprimir estruturas de API do Spooler](printing-and-print-spooler-structures.md)
</dt> <dt>

[**GetPrinter**](getprinter.md)
</dt> <dt>

[**EnumPrinters**](enumprinters.md)
</dt> <dt>

[**INFORMAÇÕES \_ DA IMPRESSORA \_ 2**](printer-info-2.md)
</dt> <dt>

[**INFORMAÇÕES \_ DA IMPRESSORA \_ 3**](printer-info-3.md)
</dt> <dt>

[**INFORMAÇÕES \_ DA IMPRESSORA \_ 4**](printer-info-4.md)
</dt> </dl>

 

 




