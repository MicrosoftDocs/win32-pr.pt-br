---
description: A \_ estrutura informações da impressora \_ 1 especifica informações gerais sobre a impressora.
ms.assetid: 0b0e2d0e-2625-4cab-a8f9-536185479443
title: Estrutura de PRINTER_INFO_1 (winspool. h)
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
ms.openlocfilehash: cbeff42a9125331c45ffd8bbbee5758fd864648c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105814570"
---
# <a name="printer_info_1-structure"></a>Estrutura de informações da impressora \_ \_ 1

A **estrutura \_ informações \_ da impressora 1** especifica informações gerais sobre a impressora.

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
| \_expansão de enumeração de impressora \_    | Um provedor de impressão pode definir esse sinalizador como uma dica para um aplicativo de chamada para enumerar esse objeto posteriormente se a expansão padrão estiver habilitada. Por exemplo, quando os domínios são enumerados, um provedor de impressão pode indicar o domínio do usuário definindo esse sinalizador. |
| \_contêiner de enumeração de impressora \_ | Se esse sinalizador for definido, o objeto de impressora poderá conter objetos enumeráveis. Por exemplo, o objeto pode ser um servidor de impressão que contém impressoras.                                                                                                             |
| \_ICON1 de enumeração de impressora \_     | Indica que, quando apropriado, um aplicativo deve exibir um ícone que identifica o objeto como um nome de rede de nível superior, como a rede do Microsoft Windows.                                                                                           |
| \_ICON2 de enumeração de impressora \_     | Indica que, quando apropriado, um aplicativo deve exibir um ícone que identifica o objeto como um domínio de rede.                                                                                                                                  |
| \_ICON3 de enumeração de impressora \_     | Indica que, quando apropriado, um aplicativo deve exibir um ícone que identifica o objeto como um servidor de impressão.                                                                                                                                    |
| \_ICON4 de enumeração de impressora \_     | Reservado.                                                                                                                                                                                                                                                 |
| \_ICON5 de enumeração de impressora \_     | Reservado.                                                                                                                                                                                                                                                 |
| \_ICON6 de enumeração de impressora \_     | Reservado.                                                                                                                                                                                                                                                 |
| \_ICON7 de enumeração de impressora \_     | Reservado.                                                                                                                                                                                                                                                 |
| \_ICON8 de enumeração de impressora \_     | Indica que, quando apropriado, um aplicativo deve exibir um ícone que identifica o objeto como uma impressora.                                                                                                                                         |



 

</dd> <dt>

**pDescription**
</dt> <dd>

Ponteiro para uma cadeia de caracteres terminada em nulo que descreve o conteúdo da estrutura.

</dd> <dt>

**pName**
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
| Cabeçalho<br/>                   | <dl> <dt>Winspool. h (incluir Windows. h)</dt> </dl> |
| Nomes Unicode e ANSI<br/>   | **\_ Informações de impressora \_ \_ 1W** (Unicode) e **\_ informações de impressora \_ \_ 1a** (ANSI)<br/>                           |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Impressão](printdocs-printing.md)
</dt> <dt>

[Estruturas de API do spooler de impressão](printing-and-print-spooler-structures.md)
</dt> <dt>

[**Getprinter**](getprinter.md)
</dt> <dt>

[**EnumPrinters**](enumprinters.md)
</dt> <dt>

[**Informações da impressora \_ \_ 2**](printer-info-2.md)
</dt> <dt>

[**Informações da impressora \_ \_ 3**](printer-info-3.md)
</dt> <dt>

[**Informações da impressora \_ \_ 4**](printer-info-4.md)
</dt> </dl>

 

 




