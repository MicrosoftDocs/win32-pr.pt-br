---
description: A estrutura \_ PRINTER NOTIFY INFO contém informações de impressora \_ retornadas pela função FindNextPrinterChangeNotification. A função retorna essas informações depois que uma operação de espera em um objeto de notificação de alteração de impressora foi atendida.
ms.assetid: c104fabe-edf5-426e-859b-694811975623
title: PRINTER_NOTIFY_INFO (Winspool.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTER_NOTIFY_INFO
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 26c7fca07eda8638bf657055691d72c78bccdbec6ef2b9a8c76ee7cf830bc767
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120091846"
---
# <a name="printer_notify_info-structure"></a>Estrutura DE \_ INFORMAÇÕES DE \_ NOTIFICAÇÃO DA IMPRESSORA

A **estrutura PRINTER NOTIFY \_ \_ INFO** contém informações de impressora retornadas pela [**função FindNextPrinterChangeNotification.**](findnextprinterchangenotification.md) A função retorna essas informações depois que uma operação de espera em um objeto de notificação de alteração de impressora foi atendida.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _PRINTER_NOTIFY_INFO {
  DWORD                    Version;
  DWORD                    Flags;
  DWORD                    Count;
  PRINTER_NOTIFY_INFO_DATA aData[1];
} PRINTER_NOTIFY_INFO, *PPRINTER_NOTIFY_INFO;
```



## <a name="members"></a>Membros

<dl> <dt>

**Versão**
</dt> <dd>

A versão dessa estrutura. De definir esse membro como 2.

</dd> <dt>

**Sinalizadores**
</dt> <dd>

Um sinalizador de bit que indica o estado da estrutura de notificação. Se o bit PRINTER NOTIFY INFO DISCARDED estiver definido, isso indicará que algumas \_ notificações tiveram que ser \_ \_ descartadas.

</dd> <dt>

**Count**
</dt> <dd>

O número de elementos [**PRINTER \_ NOTIFY INFO \_ \_ DATA**](printer-notify-info-data.md) na **matriz aData.**

</dd> <dt>

**Adata**
</dt> <dd>

Uma matriz de [**estruturas PRINTER \_ NOTIFY INFO \_ \_ DATA.**](printer-notify-info-data.md) Cada elemento da matriz identifica um único campo de informações de trabalho ou impressora e fornece os dados atuais para esse campo.

</dd> </dl>

## <a name="remarks"></a>Comentários

Se o **membro Sinalizadores** tiver o bit PRINTER NOTIFY INFO DISCARDED definido, isso indicará que ocorreu um estouro ou erro e que as notificações \_ podem ter sido \_ \_ perdidas. Nesse caso, você deve chamar [**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md) e especificar o sinalizador PRINTER NOTIFY OPTIONS REFRESH para recuperar todas \_ as informações \_ \_ atuais. Até que você solicite essa operação de atualização, o sistema não enviará notificações adicionais para esse objeto de notificação de alteração.

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

[**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md)
</dt> <dt>

[**DADOS DE \_ INFORMAÇÕES \_ DE NOTIFICAÇÃO DA \_ IMPRESSORA**](printer-notify-info-data.md)
</dt> </dl>

 

 




