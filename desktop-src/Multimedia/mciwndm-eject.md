---
title: Mensagem de MCIWNDM_EJECT (VFW. h)
description: A \_ mensagem de ejeção MCIWNDM envia um comando para um dispositivo MCI para ejetar sua mídia. Você pode enviar essa mensagem explicitamente ou usando a macro MCIWndEject.
ms.assetid: a492f504-8b58-480e-9766-bc2878466c44
keywords:
- Multimídia do Windows de mensagem MCIWNDM_EJECT
topic_type:
- apiref
api_name:
- MCIWNDM_EJECT
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e41686ce41b82dc48ee6c22ac556606c79c5b24a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369348"
---
# <a name="mciwndm_eject-message"></a>Mensagem de ejeção de MCIWNDM \_

A mensagem de **\_ ejeção MCIWNDM** envia um comando para um dispositivo MCI para ejetar sua mídia. Você pode enviar essa mensagem explicitamente ou usando a macro [**MCIWndEject**](/windows/desktop/api/Vfw/nf-vfw-mciwndeject) .


```C++
MCIWNDM_EJECT 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>Valor Retornado

Retornará zero se for bem-sucedido ou um erro de outra forma.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                       |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                             |
| Cabeçalho<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**MCIWndEject**](/windows/desktop/api/Vfw/nf-vfw-mciwndeject)
</dt> </dl>

 

 





