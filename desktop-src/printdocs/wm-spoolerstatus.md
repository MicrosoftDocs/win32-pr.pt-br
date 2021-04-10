---
description: A mensagem do WM \_ SPOOLERSTATUS é enviada do Gerenciador de impressão sempre que um trabalho é adicionado ou removido da fila do Gerenciador de impressão.
ms.assetid: 6140c9d8-0e5b-49f2-a4a6-cc1f2a0bed0a
title: Mensagem de WM_SPOOLERSTATUS (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 460e36e44f219bcbe6f514d7d368accddae46b83
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104091697"
---
# <a name="wm_spoolerstatus-message"></a>Mensagem do WM \_ SPOOLERSTATUS

A mensagem do **WM \_ SPOOLERSTATUS** é enviada do Gerenciador de impressão sempre que um trabalho é adicionado ou removido da fila do Gerenciador de impressão.

Uma janela recebe essa mensagem por meio de sua função [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
LRESULT CALLBACK WindowProc(
  HWND hwnd, 
  UINT  uMsg, 
  WPARAM wParam, 
  LPARAM lParam     
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

O \_ sinalizador PR JOBSTATUS.

</dd> <dt>

*lParam* 
</dt> <dd>

A palavra de ordem inferior Especifica o número de trabalhos restantes na fila do Gerenciador de impressão.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Um aplicativo deve retornar zero se ele processar essa mensagem.

## <a name="remarks"></a>Comentários

Esta mensagem é apenas para fins informativos. Esta mensagem é consultoria e não tem semântica de entrega garantida. Os aplicativos não devem pressupor que receberão uma \_ mensagem do WM SPOOLERSTATUS para cada alteração no status do spooler.

A mensagem do WM \_ SPOOLERSTATUS não tem suporte após o Windows XP. Para ser notificado sobre alterações no status da fila de impressão, você pode usar [**FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md) e [**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                               |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                     |
| Cabeçalho<br/>                   | <dl> <dt>WinUser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Impressão](printdocs-printing.md)
</dt> <dt>

[Mensagens da API do spooler de impressão](printing-and-print-spooler-messages.md)
</dt> <dt>

[**FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md)
</dt> <dt>

[**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md)
</dt> </dl>

 

