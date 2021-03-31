---
title: Mensagem de MCIWNDM_PUT_DEST (VFW. h)
description: O MCIWNDM \_ colocar \_ mensagem de destino redefine as coordenadas do retângulo de destino usado para ampliar ou alongar as imagens de um arquivo AVI durante a reprodução. Você pode enviar essa mensagem explicitamente ou usando a macro MCIWndPutDest.
ms.assetid: 0b13d473-ef93-41a2-bbb2-09fbf264493e
keywords:
- Multimídia do Windows de mensagem MCIWNDM_PUT_DEST
topic_type:
- apiref
api_name:
- MCIWNDM_PUT_DEST
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba150f450f71c3593976f98c9935233918becd70
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103645012"
---
# <a name="mciwndm_put_dest-message"></a>MCIWNDM \_ colocar \_ mensagem de dest

O **MCIWNDM \_ colocar \_** mensagem de destino redefine as coordenadas do retângulo de destino usado para ampliar ou alongar as imagens de um arquivo AVI durante a reprodução. Você pode enviar essa mensagem explicitamente ou usando a macro [**MCIWndPutDest**](/windows/desktop/api/Vfw/nf-vfw-mciwndputdest) .


```C++
MCIWNDM_PUT_DEST 
wParam = 0; 
lParam = (LPARAM) (LPRECT) prc; 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="prc"></span><span id="PRC"></span>*popular*
</dt> <dd>

Ponteiro para uma estrutura [**Rect**](/previous-versions//dd162897(v=vs.85)) que contém as coordenadas do retângulo de destino.

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retornará zero se for bem-sucedido ou um erro de outra forma.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                       |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                             |
| Cabeçalho<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[**MCIWndPutDest**](/windows/desktop/api/Vfw/nf-vfw-mciwndputdest)
</dt> </dl>

 

