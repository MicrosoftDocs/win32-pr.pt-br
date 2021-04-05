---
title: Mensagem de MCIWNDM_GETEND (VFW. h)
description: A \_ mensagem MCIWNDM GETEND recupera o local do final do conteúdo de um dispositivo ou arquivo MCI. Você pode enviar essa mensagem explicitamente ou usando a macro MCIWndGetEnd.
ms.assetid: 3fa45928-af63-4f87-835d-f409011a797e
keywords:
- Multimídia do Windows de mensagem MCIWNDM_GETEND
topic_type:
- apiref
api_name:
- MCIWNDM_GETEND
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 00d18057619e31fa9b22d7f6354527c394c02798
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824734"
---
# <a name="mciwndm_getend-message"></a>\_Mensagem MCIWNDM GETEND

A mensagem **MCIWNDM \_ GETEND** recupera o local do final do conteúdo de um dispositivo ou arquivo MCI. Você pode enviar essa mensagem explicitamente ou usando a macro [**MCIWndGetEnd**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetend) .


```C++
MCIWNDM_GETEND 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>Valor Retornado

Retorna o local no formato de hora atual.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                       |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                             |
| Cabeçalho<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**MCIWndGetEnd**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetend)
</dt> </dl>

 

 





