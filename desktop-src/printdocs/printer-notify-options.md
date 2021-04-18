---
description: A \_ \_ estrutura opções de notificação de impressora especifica opções para um objeto de notificação de alteração que monitora uma impressora ou um servidor de impressão.
ms.assetid: 712c546d-dbb3-4f78-b14e-fbb8619b57f9
title: Estrutura de PRINTER_NOTIFY_OPTIONS (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTER_NOTIFY_OPTIONS
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: af1aeaa1138145c5df18ea4fd5babaa1a9e60416
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105785964"
---
# <a name="printer_notify_options-structure"></a>Estrutura de opções de \_ notificação de impressora \_

A **estrutura \_ \_ Opções** de notificação de impressora especifica opções para um objeto de notificação de alteração que monitora uma impressora ou um servidor de impressão.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _PRINTER_NOTIFY_OPTIONS {
  DWORD                        Version;
  DWORD                        Flags;
  DWORD                        Count;
  PPRINTER_NOTIFY_OPTIONS_TYPE pTypes;
} PRINTER_NOTIFY_OPTIONS, *PPRINTER_NOTIFY_OPTIONS;
```



## <a name="members"></a>Membros

<dl> <dt>

**Versão**
</dt> <dd>

A versão desta estrutura. Defina esse membro como 2.

</dd> <dt>

**Sinalizadores**
</dt> <dd>

Um sinalizador de bits. Se você definir o \_ sinalizador de atualização de opções de notificação de impressora \_ \_ em uma chamada para a função [**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md) , a função fornecerá dados atuais para todos os campos de informações de impressora monitorados. A função [**FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md) ignora o membro **flags** .

</dd> <dt>

**Count**
</dt> <dd>

O número de elementos na matriz **pTypes** .

</dd> <dt>

**pTypes**
</dt> <dd>

Um ponteiro para uma matriz de [**Opções de notificação de impressora \_ \_ \_ tipo**](printer-notify-options-type.md) estruturas. Use um elemento dessa matriz para especificar os campos de informações da impressora a serem monitorados e um elemento para especificar os campos de informações do trabalho a serem monitorados. Você pode monitorar as informações da impressora, as informações do trabalho ou ambas.

</dd> </dl>

## <a name="remarks"></a>Comentários

Use essa estrutura com a função [**FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md) para especificar o conjunto de campos de informações da impressora ou do trabalho a ser monitorado para alteração.

Use essa estrutura com a função [**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md) para solicitar os dados atuais de todos os campos de impressora e de informações de trabalho monitorados. Nesse caso, o membro **flags** especifica o sinalizador de \_ atualização de opções de notificação de impressora \_ \_ e a função ignora os outros membros da estrutura.

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

[**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md)
</dt> <dt>

[**\_tipo de \_ Opções de notificação de impressora \_**](printer-notify-options-type.md)
</dt> </dl>

 

 




