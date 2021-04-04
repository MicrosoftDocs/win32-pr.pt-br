---
title: Mensagem de BM_SETSTYLE (WinUser. h)
description: Define o estilo de um botão. Você pode enviar essa mensagem explicitamente ou usar a \_ macro SetStyle do botão.
ms.assetid: 6439e68f-87fc-4a4a-8025-facc3c0e03e2
keywords:
- Controles de BM_SETSTYLE de mensagens do Windows
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
ms.openlocfilehash: 3c080e1098d70b17e1e68bbbcd2d5598db79ef8f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918172"
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

## <a name="return-value"></a>Retornar valor

Essa mensagem sempre retorna zero.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                                           |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                                     |
| parâmetro<br/>                   | <dl> <dt>WinUser. h (incluir Windows. h)</dt> </dl> |



 

