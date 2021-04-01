---
title: Mensagem de SBM_GETSCROLLBARINFO (WinUser. h)
description: Enviado por um aplicativo para recuperar informações sobre a barra de rolagem especificada.
ms.assetid: db6f704f-99ee-448c-ae7a-dd5a23399fb6
keywords:
- Controles de SBM_GETSCROLLBARINFO de mensagens do Windows
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
ms.openlocfilehash: b8bdd78eb665bd069d854538bb2bdfae1a946765
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644618"
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

## <a name="return-value"></a>Retornar valor

Retornará zero, se for bem-sucedido ou zero.

Para obter informações de erro estendidas, chame [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                                           |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                                     |
| parâmetro<br/>                   | <dl> <dt>WinUser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[**GetScrollBarInfo**](/windows/desktop/api/Winuser/nf-winuser-getscrollbarinfo)
</dt> <dt>

[**SCROLLBARINFO**](/windows/win32/api/winuser/ns-winuser-scrollbarinfo)
</dt> </dl>

 

