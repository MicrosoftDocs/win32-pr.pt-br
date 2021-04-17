---
description: A estrutura de informações de notificação de impressora \_ \_ contém informações de impressora retornadas pela função FindNextPrinterChangeNotification. A função retorna essas informações depois que uma operação de espera em um objeto de notificação de alteração de impressora é satisfeita.
ms.assetid: c104fabe-edf5-426e-859b-694811975623
title: Estrutura de PRINTER_NOTIFY_INFO (winspool. h)
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
ms.openlocfilehash: 631169cfcdabd6a87459ebb777adb6842d09089b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105761302"
---
# <a name="printer_notify_info-structure"></a>Estrutura de informações de \_ notificação de impressora \_

A estrutura de **\_ \_ informações de notificação de impressora** contém informações de impressora retornadas pela função [**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md) . A função retorna essas informações depois que uma operação de espera em um objeto de notificação de alteração de impressora é satisfeita.

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

A versão desta estrutura. Defina esse membro como 2.

</dd> <dt>

**Sinalizadores**
</dt> <dd>

Um sinalizador de bits que indica o estado da estrutura de notificação. Se o bit de notificação de informação de impressora \_ \_ \_ descartada estiver definido, isso indica que algumas notificações precisaram ser descartadas.

</dd> <dt>

**Count**
</dt> <dd>

O número de elementos de dados de informações de notificação de impressora na matriz **aData** . [**\_ \_ \_**](printer-notify-info-data.md)

</dd> <dt>

**aData**
</dt> <dd>

Uma matriz de estruturas de [**dados de informações de notificação de impressora \_ \_ \_**](printer-notify-info-data.md) . Cada elemento da matriz identifica um único trabalho ou campo de informações de impressora e fornece os dados atuais para esse campo.

</dd> </dl>

## <a name="remarks"></a>Comentários

Se o membro **flags** tiver o conjunto de bits de informações de notificação de impressora \_ \_ \_ descartado, isso indicará que ocorreu um estouro ou erro, e as notificações podem ter sido perdidas. Nesse caso, você deve chamar [**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md) e especificar o sinalizador de \_ atualização de opções de notificação de impressora \_ \_ para recuperar todas as informações atuais. Até que você solicite essa operação de atualização, o sistema não enviará notificações adicionais para esse objeto de notificação de alteração.

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

[**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md)
</dt> <dt>

[**\_dados de \_ informações de notificação da impressora \_**](printer-notify-info-data.md)
</dt> </dl>

 

 




