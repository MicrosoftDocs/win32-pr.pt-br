---
title: Mensagem de MCIWNDM_OPENINTERFACE (VFW. h)
description: A \_ mensagem MCIWNDM OPENINTERFACE anexa o fluxo de dados ou o arquivo associado à interface especificada a uma janela MCIWnd. Você pode enviar essa mensagem explicitamente ou usando a macro MCIWndOpenInterface.
ms.assetid: 73cbd637-d315-4b39-a978-2b72aed1f303
keywords:
- mensagem de MCIWNDM_OPENINTERFACE Windows multimídia
topic_type:
- apiref
api_name:
- MCIWNDM_OPENINTERFACE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 83097ad6301dbfdb4636a8478c2df8e544207df334efd27fe9695f15e0693533
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118373448"
---
# <a name="mciwndm_openinterface-message"></a>\_Mensagem MCIWNDM OPENINTERFACE

A mensagem **MCIWNDM \_ OPENINTERFACE** anexa o fluxo de dados ou o arquivo associado à interface especificada a uma janela MCIWnd. Você pode enviar essa mensagem explicitamente ou usando a macro [**MCIWndOpenInterface**](/windows/desktop/api/Vfw/nf-vfw-mciwndopeninterface) .


```C++
MCIWNDM_OPENINTERFACE 
wParam = 0; 
lParam = (LPARAM) (LPUNKNOWN) pUnk; 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="pUnk"></span><span id="punk"></span><span id="PUNK"></span>*pUnk*
</dt> <dd>

Ponteiro para uma interface IAVI que aponta para um arquivo ou um fluxo de dados em um arquivo.

</dd> </dl>

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

[**MCIWndOpenInterface**](/windows/desktop/api/Vfw/nf-vfw-mciwndopeninterface)
</dt> </dl>

 

 





