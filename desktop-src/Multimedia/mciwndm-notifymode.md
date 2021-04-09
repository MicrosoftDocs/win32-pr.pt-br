---
title: Mensagem de MCIWNDM_NOTIFYMODE (VFW. h)
description: A \_ mensagem MCIWNDM notifymode notifica a janela pai de um aplicativo de que o modo operacional do dispositivo MCI foi alterado.
ms.assetid: 08adfa8b-4d88-4953-acd8-8a4728f9e1b6
keywords:
- Multimídia do Windows de mensagem MCIWNDM_NOTIFYMODE
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
ms.openlocfilehash: 7fe75048a53023dab67bef4048d6149438ad54d2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104008834"
---
# <a name="mciwndm_notifymode-message"></a>\_Mensagem MCIWNDM notifymode

A mensagem **MCIWNDM \_ notifymode** notifica a janela pai de um aplicativo de que o modo operacional do dispositivo MCI foi alterado.


```C++
MCIWNDM_NOTIFYMODE 
wParam = (WPARAM) (HWND) hwnd; 
lParam = (LPARAM) (LONG) mode; 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="hwnd"></span><span id="HWND"></span>*HWND*
</dt> <dd>

Manipule a janela MCIWnd.

</dd> <dt>

<span id="mode"></span><span id="MODE"></span>*moda*
</dt> <dd>

Inteiro correspondente ao modo MCI.

</dd> </dl>

## <a name="remarks"></a>Comentários

Você pode habilitar a notificação de alterações no modo de um dispositivo MCI especificando o \_ estilo de janela MCIWNDF notifymode.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                       |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                             |
| Cabeçalho<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



 

 





