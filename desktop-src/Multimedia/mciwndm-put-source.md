---
title: Mensagem de MCIWNDM_PUT_SOURCE (VFW. h)
description: A \_ mensagem de origem MCIWNDM Put \_ define as coordenadas do retângulo de origem usado para cortar as imagens de um arquivo AVI durante a reprodução. Você pode enviar essa mensagem explicitamente ou usando a macro MCIWndPutSource.
ms.assetid: cff95139-0302-4db3-bf2e-559e75257e85
keywords:
- Multimídia do Windows de mensagem MCIWNDM_PUT_SOURCE
topic_type:
- apiref
api_name:
- MCIWNDM_PUT_SOURCE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5407f420b8def6dda9795e87eb68943c9373b143
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644228"
---
# <a name="mciwndm_put_source-message"></a>MCIWNDM \_ colocar \_ mensagem de origem

A mensagem de **\_ \_ origem MCIWNDM Put** define as coordenadas do retângulo de origem usado para cortar as imagens de um arquivo AVI durante a reprodução. Você pode enviar essa mensagem explicitamente ou usando a macro [**MCIWndPutSource**](/windows/desktop/api/Vfw/nf-vfw-mciwndputsource) .


```C++
MCIWNDM_PUT_SOURCE 
wParam = 0; 
lParam = (LPARAM) (LPRECT) prc; 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="prc"></span><span id="PRC"></span>*popular*
</dt> <dd>

Ponteiro para uma estrutura [Rect](/previous-versions//ms536136(v=vs.85)) que contém as coordenadas do retângulo de origem.

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retornará zero se for bem-sucedido ou um erro de outra forma.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                       |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                             |
| Cabeçalho<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



 

