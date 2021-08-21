---
title: Mensagem de SBM_GETSCROLLBARINFO (WinUser. h)
description: Enviado por um aplicativo para recuperar informações sobre a barra de rolagem especificada.
ms.assetid: db6f704f-99ee-448c-ae7a-dd5a23399fb6
keywords:
- controles de Windows de mensagem de SBM_GETSCROLLBARINFO
topic_type:
- apiref
api_name:
- SBM_GETSCROLLBARINFO
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 11f779f237d0ad04fe3e3d8f3348c51c195470280c9b0c20d12c1e245d04a089
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119503976"
---
# <a name="sbm_getscrollbarinfo-message"></a>\_Mensagem SBM GETSCROLLBARINFO

Enviado por um aplicativo para recuperar informações sobre a barra de rolagem especificada.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Não usado; deve ser zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma estrutura [**SCROLLBARINFO**](/windows/win32/api/winuser/ns-winuser-scrollbarinfo) que recebe as informações.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retornará zero, se for bem-sucedido ou zero.

Para obter informações de erro estendidas, chame [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                                           |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                                     |
| Cabeçalho<br/>                   | <dl> <dt>Winuser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[**GetScrollBarInfo**](/windows/desktop/api/Winuser/nf-winuser-getscrollbarinfo)
</dt> <dt>

[**SCROLLBARINFO**](/windows/win32/api/winuser/ns-winuser-scrollbarinfo)
</dt> </dl>

 

