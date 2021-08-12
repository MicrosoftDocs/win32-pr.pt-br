---
title: Mensagem de BM_SETSTYLE (WinUser. h)
description: Define o estilo de um botão. Você pode enviar essa mensagem explicitamente ou usar a \_ macro SetStyle do botão.
ms.assetid: 6439e68f-87fc-4a4a-8025-facc3c0e03e2
keywords:
- controles de Windows de mensagem de BM_SETSTYLE
topic_type:
- apiref
api_name:
- BM_SETSTYLE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 17f635a70bf806c6c26f5b236ea939bc453d27bf0fe135f8e2586aeb59021b9b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118674414"
---
# <a name="bm_setstyle-message"></a>BM \_ mensagem SETstyle

Define o estilo de um botão. Você pode enviar essa mensagem explicitamente ou usar a [**macro \_ SetStyle do botão**](/windows/desktop/api/Windowsx/nf-windowsx-button_setstyle) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

O estilo do botão. Esse parâmetro pode ser uma combinação de estilos de botão. Para obter uma tabela de estilos de botão, consulte [estilos de botão](button-styles.md).

</dd> <dt>

*lParam* 
</dt> <dd>

O [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) de *lParam* é um **bool** que especifica se o botão deve ser redesenhado. Um valor de **true** redesenha o botão; um valor **false** não redesenha o botão.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Essa mensagem sempre retorna zero.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                                           |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                                     |
| parâmetro<br/>                   | <dl> <dt>Winuser. h (incluir Windows. h)</dt> </dl> |



 

