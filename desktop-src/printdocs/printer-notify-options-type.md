---
description: A \_ estrutura do \_ tipo de opções de notificação de impressora \_ especifica o conjunto de campos de informações de impressora ou trabalho a ser monitorado por um objeto de notificação de alteração de impressora. Uma chamada para a função FindFirstPrinterChangeNotification especifica uma \_ \_ estrutura de opções de notificação de impressora, que contém uma matriz de estruturas de tipo de opções de notificação de impressora \_ \_ \_ .
ms.assetid: 1009f892-d3a8-4887-99b4-a35d1268eeb4
title: Estrutura de PRINTER_NOTIFY_OPTIONS_TYPE (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTER_NOTIFY_OPTIONS_TYPE
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 2b593a502a668345cdd0206b4f1363cf160074b6c9aa26696427b5b42a0fbdc9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118056273"
---
# <a name="printer_notify_options_type-structure"></a>\_Estrutura do \_ tipo de opções de notificação de impressora \_

A estrutura do tipo de opções de notificação de impressora especifica o conjunto de campos de informações de impressora ou trabalho a ser monitorado por um objeto de notificação de alteração de impressora. **\_ \_ \_**

Uma chamada para a função [**FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md) especifica uma estrutura de [**\_ \_ Opções de notificação de impressora**](printer-notify-options.md) , que contém uma matriz de estruturas de **\_ \_ \_ tipo de opções de notificação de impressora** .

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _PRINTER_NOTIFY_OPTIONS_TYPE {
  WORD  Type;
  WORD  Reserved0;
  DWORD Reserved1;
  DWORD Reserved2;
  DWORD Count;
  PWORD pFields;
} PRINTER_NOTIFY_OPTIONS_TYPE, *PPRINTER_NOTIFY_OPTIONS_TYPE;
```



## <a name="members"></a>Membros

<dl> <dt>

**Tipo**
</dt> <dd>

O tipo a ser observado. Esse membro pode ser um dos valores a seguir.



| Valor                                                                                                                                                                                                                                      | Significado                                                                                                           |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| <span id="JOB_NOTIFY_TYPE"></span><span id="job_notify_type"></span><dl> <dt>**Trabalho \_ do NOTIFICAr \_ tipo**</dt> <dt>0x01</dt> </dl>             | Indica que os campos especificados na matriz **pFields** são constantes de \_ campo de notificação de trabalho \_ \_ \* .<br/>     |
| <span id="PRINTER_NOTIFY_TYPE"></span><span id="printer_notify_type"></span><dl> <dt>**Impressora \_ NOTIFICAr \_ tipo**</dt> <dt>0x00</dt> </dl> | Indica que os campos especificados na matriz **pFields** são constantes de \_ campo de notificação de impressora \_ \_ \* .<br/> |



 

</dd> <dt>

**Reserved0**
</dt> <dd>

Reservado.

</dd> <dt>

**Reserved1**
</dt> <dd>

Reservado.

</dd> <dt>

**Reserved2**
</dt> <dd>

Reservado.

</dd> <dt>

**Count**
</dt> <dd>

O número de elementos na matriz **pFields** .

</dd> <dt>

**pFields**
</dt> <dd>

Um ponteiro para uma matriz de valores. Cada elemento da matriz Especifica um campo de informações de trabalho ou de impressora de interesse. Para obter uma lista de campos de informações de impressora e de trabalho com suporte, consulte a estrutura de [**\_ \_ \_ dados informações de notificação de impressora**](printer-notify-info-data.md) .

</dd> </dl>

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

[**FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md)
</dt> <dt>

[**\_dados de \_ informações de notificação da impressora \_**](printer-notify-info-data.md)
</dt> <dt>

[**\_Opções de notificação de impressora \_**](printer-notify-options.md)
</dt> </dl>

 

 




