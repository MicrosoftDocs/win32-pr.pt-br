---
title: MCIWNDM_SETREPEAT mensagem (Vfw.h)
description: A mensagem SETREPEAT MCIWNDM define o sinalizador de repetição \_ associado à reprodução contínua.
ms.assetid: 9a8da201-9ce8-4b6c-8b76-cd9e1356c75d
keywords:
- MCIWNDM_SETREPEAT mensagem Windows Multimídia
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
ms.openlocfilehash: 158e0b52f01431886fd8a70e89efadfdd7335258c0808cdb6780bf06071e3280
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119807586"
---
# <a name="mciwndm_setrepeat-message"></a>Mensagem MCIWNDM \_ SETREPEAT

A **mensagem \_ SETREPEAT MCIWNDM** define o sinalizador de repetição associado à reprodução contínua. A **mensagem MCIWNDM \_ SETREPEAT** funciona em conjunto com o comando [MCI \_ PLAY](mci-play.md) para fornecer um loop de reprodução contínua. Você pode enviar essa mensagem explicitamente ou usando a macro [**MCIWndSetRepeat.**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetrepeat)


```C++
MCIWNDM_SETREPEAT 
wParam = 0; 
lParam = (LPARAM) (BOOL) f; 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="f"></span><span id="F"></span>*F*
</dt> <dd>

Novo estado do sinalizador de repetição. **Especifique TRUE** para ativar a reprodução contínua.

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retorna zero.

## <a name="remarks"></a>Comentários

Atualmente, o MCIAVI é o único dispositivo que dá suporte à reprodução contínua.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                       |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                             |
| Cabeçalho<br/>                   | <dl> <dt>Vfw.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[MCI \_ PLAY](mci-play.md)
</dt> <dt>

[**MCIWndSetRepeat**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetrepeat)
</dt> </dl>

 

 





