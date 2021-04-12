---
title: Mensagem de EM_GETELLIPSISSTATE (RichEdit. h)
description: Recupera o estado de reticências atual.
ms.assetid: D02AE225-F5BF-401A-9877-55C68946CDBE
keywords:
- Controles de EM_GETELLIPSISSTATE de mensagens do Windows
topic_type:
- apiref
api_name:
- EM_GETELLIPSISSTATE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 905bc8ecc180189f46e896aa0d9aaa3ba88b3f0b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455185"
---
# <a name="em_getellipsisstate-message"></a>\_Mensagem em getreticências

Recupera o estado de reticências atual.


```C++
#define EM_GETELLIPSISSTATE       (WM_USER + 322)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Não usado; deve ser zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Não usado; deve ser zero.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O valor de retorno será TRUE se uma elipse estiver sendo exibida e FALSE caso contrário.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 8\]<br/>                                            |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2012\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**em \_ GETreticênciamode**](em-getellipsismode.md)
</dt> <dt>

[**em \_ setreticências**](em-setellipsismode.md)
</dt> </dl>

 

 





