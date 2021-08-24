---
title: MCIWNDM_NOTIFYMODE mensagem (Vfw.h)
description: A mensagem NOTIFYMODE MCIWNDM notifica a janela pai de um aplicativo de que o modo de operação do \_ dispositivo MCI foi alterado.
ms.assetid: 08adfa8b-4d88-4953-acd8-8a4728f9e1b6
keywords:
- MCIWNDM_NOTIFYMODE mensagem Windows Multimídia
topic_type:
- apiref
api_name:
- MCIWNDM_NOTIFYMODE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c610904512e2b39a5c0f16781c1d9f27155f7826941aebfc66fcd9259f7ee8a8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119525416"
---
# <a name="mciwndm_notifymode-message"></a>Mensagem NOTIFYMODE MCIWNDM \_

A **mensagem \_ NOTIFYMODE MCIWNDM** notifica a janela pai de um aplicativo de que o modo de operação do dispositivo MCI foi alterado.


```C++
MCIWNDM_NOTIFYMODE 
wParam = (WPARAM) (HWND) hwnd; 
lParam = (LPARAM) (LONG) mode; 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="hwnd"></span><span id="HWND"></span>*Hwnd*
</dt> <dd>

Lidar com a janela MCIWnd.

</dd> <dt>

<span id="mode"></span><span id="MODE"></span>*Modo*
</dt> <dd>

Inteiro correspondente ao modo MCI.

</dd> </dl>

## <a name="remarks"></a>Comentários

Você pode habilitar a notificação de alterações de modo de um dispositivo MCI especificando o estilo de janela \_ NOTIFYMODE MCIWNDF.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                       |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                             |
| Cabeçalho<br/>                   | <dl> <dt>Vfw.h</dt> </dl> |



 

 





