---
title: MCIWNDM_GET_DEST mensagem (Vfw.h)
description: A mensagem GET DEST MCIWNDM recupera as coordenadas do retângulo de destino usadas para ampliar ou ampliar as imagens de um arquivo AVI durante \_ \_ a reprodução. Você pode enviar essa mensagem explicitamente ou usando a macro MCIWndGetDest.
ms.assetid: d4d8a3eb-aad4-4435-a23b-7a9c55fc194d
keywords:
- MCIWNDM_GET_DEST mensagem Windows Multimídia
topic_type:
- apiref
api_name:
- MCIWNDM_GET_DEST
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b4a6326485bece572b03ceeca687ca4468b6d866c25c738c32d13763fd0931a9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117802900"
---
# <a name="mciwndm_get_dest-message"></a>Mensagem GET \_ DEST MCIWNDM \_

A **mensagem GET \_ \_ DEST MCIWNDM** recupera as coordenadas do retângulo de destino usadas para ampliar ou ampliar as imagens de um arquivo AVI durante a reprodução. Você pode enviar essa mensagem explicitamente ou usando a macro [**MCIWndGetDest.**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetdest)


```C++
MCIWNDM_GET_DEST 
wParam = 0; 
lParam = (LPARAM) (LPRECT) prc; 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="prc"></span><span id="PRC"></span>*Prc*
</dt> <dd>

Ponteiro para uma [**estrutura RECT**](/previous-versions//dd162897(v=vs.85)) para retornar as coordenadas do retângulo de destino.

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retornará zero se for bem-sucedido ou um erro, caso contrário.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                       |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                             |
| Cabeçalho<br/>                   | <dl> <dt>Vfw.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**MCIWndGetDest**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetdest)
</dt> </dl>

 

