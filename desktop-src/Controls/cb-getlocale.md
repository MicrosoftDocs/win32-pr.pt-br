---
title: Mensagem de CB_GETLOCALE (WinUser. h)
description: Obtém a localidade atual da caixa de combinação. A localidade é usada para determinar a ordem de classificação correta do texto exibido para caixas de combinação com o \_ estilo de classificação CBS e o texto adicionado usando a \_ mensagem createstring CB.
ms.assetid: 57c77ce2-bad0-43f3-8325-f2a7227994ec
keywords:
- Controles de CB_GETLOCALE de mensagens do Windows
topic_type:
- apiref
api_name:
- CB_GETLOCALE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 847d9f73e8bf0b1d533d0b79ba86d939bee0e9b4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009359"
---
# <a name="cb_getlocale-message"></a>\_Mensagem de GETlocalização CB

Obtém a localidade atual da caixa de combinação. A localidade é usada para determinar a ordem de classificação correta do texto exibido para caixas de combinação com o estilo de [**\_ classificação CBS**](combo-box-styles.md) e o texto adicionado usando a mensagem [**\_ createstring CB**](cb-addstring.md) .

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

O valor de retorno especifica a localidade atual da caixa de combinação. O [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) contém o código de país/região e o [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contém o identificador de idioma.

## <a name="remarks"></a>Comentários

O identificador de idioma é composto por um identificador de subidioma e um identificador de idioma primário. A macro [**PRIMARYLANGID**](/windows/desktop/api/winnt/nf-winnt-primarylangid) Obtém o identificador de idioma primário e a macro [**SUBLANGID**](/windows/desktop/api/winnt/nf-winnt-sublangid) Obtém o identificador do subidioma.

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

[**AddString CB \_**](cb-addstring.md)
</dt> <dt>

[**setlocalar do CB \_**](cb-setlocale.md)
</dt> <dt>

**Outros recursos**
</dt> <dt>

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))
</dt> <dt>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))
</dt> <dt>

[**PRIMARYLANGID**](/windows/desktop/api/winnt/nf-winnt-primarylangid)
</dt> <dt>

[**SUBLANGID**](/windows/desktop/api/winnt/nf-winnt-sublangid)
</dt> </dl>

 

