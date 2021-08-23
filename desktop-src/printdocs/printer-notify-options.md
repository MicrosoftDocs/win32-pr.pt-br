---
description: A estrutura \_ PRINTER NOTIFY OPTIONS especifica opções para um objeto de \_ notificação de alteração que monitora uma impressora ou servidor de impressão.
ms.assetid: 712c546d-dbb3-4f78-b14e-fbb8619b57f9
title: PRINTER_NOTIFY_OPTIONS (Winspool.h)
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
ms.openlocfilehash: 57b95717e7873f0b73b66d450849d92a2c2ed7053d6d387286cc58144c772ba8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118731128"
---
# <a name="printer_notify_options-structure"></a>Estrutura OPÇÕES \_ DE \_ NOTIFICAÇÃO DA IMPRESSORA

A **estrutura PRINTER NOTIFY \_ \_ OPTIONS** especifica opções para um objeto de notificação de alteração que monitora uma impressora ou servidor de impressão.

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

A versão dessa estrutura. De definir esse membro como 2.

</dd> <dt>

**Sinalizadores**
</dt> <dd>

Um sinalizador de bits. Se você definir o sinalizador PRINTER NOTIFY OPTIONS REFRESH em uma chamada para a função \_ \_ \_ [**FindNextPrinterChangeNotification,**](findnextprinterchangenotification.md) a função fornece dados atuais para todos os campos de informações da impressora monitorada. A [**função FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md) ignora o **membro Flags.**

</dd> <dt>

**Count**
</dt> <dd>

O número de elementos na matriz **pTypes.**

</dd> <dt>

**pTypes**
</dt> <dd>

Um ponteiro para uma matriz de [**estruturas TIPO \_ PRINTER NOTIFY \_ \_ OPTIONS.**](printer-notify-options-type.md) Use um elemento dessa matriz para especificar os campos de informações da impressora a monitorar e um elemento para especificar os campos de informações de trabalho a monitorar. Você pode monitorar informações de impressora, informações de trabalho ou ambos.

</dd> </dl>

## <a name="remarks"></a>Comentários

Use essa estrutura com a [**função FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md) para especificar o conjunto de campos de informações de impressora ou trabalho a ser monitorado quanto à alteração.

Use essa estrutura com a [**função FindNextPrinterChangeNotification**](findnextprinterchangenotification.md) para solicitar os dados atuais para todos os campos monitorados de informações de impressora e trabalho. Nesse caso, o **membro Flags** especifica o sinalizador PRINTER NOTIFY OPTIONS REFRESH e a função \_ ignora os outros membros da \_ \_ estrutura.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                                |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                      |
| Cabeçalho<br/>                   | <dl> <dt>Winspool.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Impressão](printdocs-printing.md)
</dt> <dt>

[Imprimir estruturas de API do Spooler](printing-and-print-spooler-structures.md)
</dt> <dt>

[**FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md)
</dt> <dt>

[**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md)
</dt> <dt>

[**TIPO DE \_ OPÇÕES \_ DE NOTIFICAÇÃO DE \_ IMPRESSORA**](printer-notify-options-type.md)
</dt> </dl>

 

 




