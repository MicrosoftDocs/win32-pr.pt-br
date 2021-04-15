---
title: Mensagem de MCIWNDM_GETLENGTH (VFW. h)
description: A \_ mensagem MCIWNDM GETLENGTH recupera o tamanho do conteúdo ou arquivo usado atualmente por um dispositivo MCI. Você pode enviar essa mensagem explicitamente ou usando a macro MCIWndGetLength.
ms.assetid: bee4d9fc-78eb-4577-98bb-d6c2d9acbb7f
keywords:
- Multimídia do Windows de mensagem MCIWNDM_GETLENGTH
topic_type:
- apiref
api_name:
- MCIWNDM_GETLENGTH
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2347647fcff0beb87be12b7f6a05790b97f36d51
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454750"
---
# <a name="mciwndm_getlength-message"></a>\_Mensagem MCIWNDM GETLENGTH

A mensagem **MCIWNDM \_ GETLENGTH** recupera o tamanho do conteúdo ou arquivo usado atualmente por um dispositivo MCI. Você pode enviar essa mensagem explicitamente ou usando a macro [**MCIWndGetLength**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetlength) .


```C++
MCIWNDM_GETLENGTH 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>Valor Retornado

Retorna o comprimento. As unidades para o comprimento dependem do formato de hora atual.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                       |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                             |
| Cabeçalho<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**MCIWndGetLength**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetlength)
</dt> </dl>

 

 





