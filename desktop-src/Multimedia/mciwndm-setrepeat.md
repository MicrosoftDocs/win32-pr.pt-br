---
title: Mensagem de MCIWNDM_SETREPEAT (VFW. h)
description: A \_ mensagem MCIWNDM setrepetir define o sinalizador de repetição associado à reprodução contínua.
ms.assetid: 9a8da201-9ce8-4b6c-8b76-cd9e1356c75d
keywords:
- Multimídia do Windows de mensagem MCIWNDM_SETREPEAT
topic_type:
- apiref
api_name:
- MCIWNDM_SETREPEAT
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aeae2ac3cb57f8ddbb2343ee3f42d30fa8def370
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824578"
---
# <a name="mciwndm_setrepeat-message"></a>MCIWNDM \_ AutoRepetir mensagem

A mensagem **MCIWNDM \_ setrepetir** define o sinalizador de repetição associado à reprodução contínua. A mensagem **MCIWNDM \_ setrepetir** funciona em conjunto com o comando [MCI \_ Play](mci-play.md) para fornecer um loop de reprodução contínua. Você pode enviar essa mensagem explicitamente ou usando a macro [**MCIWndSetRepeat**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetrepeat) .


```C++
MCIWNDM_SETREPEAT 
wParam = 0; 
lParam = (LPARAM) (BOOL) f; 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="f"></span><span id="F"></span>*fixo*
</dt> <dd>

Novo estado do sinalizador de repetição. Especifique **true** para ativar a reprodução contínua.

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retorna zero.

## <a name="remarks"></a>Comentários

Atualmente, MCIAVI é o único dispositivo que dá suporte à reprodução contínua.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                       |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                             |
| Cabeçalho<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[\_reprodução MCI](mci-play.md)
</dt> <dt>

[**MCIWndSetRepeat**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetrepeat)
</dt> </dl>

 

 





