---
title: Mensagem de LB_GETLOCALE (WinUser. h)
description: Obtém a localidade atual da caixa de listagem. Você pode usar a localidade para determinar a ordem de classificação correta do texto exibido (para caixas de listagem com o \_ estilo de classificação lbs) e o texto adicionado pela mensagem do lb \_ AddString.
ms.assetid: ec814b03-5ce2-4b81-a36c-ab4c115f88be
keywords:
- Controles de LB_GETLOCALE de mensagens do Windows
topic_type:
- apiref
api_name:
- LB_GETLOCALE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 57620b62011dba234710caf1b5d1c429da37ace9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455337"
---
# <a name="lb_getlocale-message"></a>\_Mensagem de GETlocalize do lb

Obtém a localidade atual da caixa de listagem. Você pode usar a localidade para determinar a ordem de classificação correta do texto exibido (para caixas de listagem com o estilo de [**\_ classificação lbs**](list-box-styles.md) ) e o texto adicionado pela mensagem do [**lb \_ AddString**](lb-addstring.md) .

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

O valor de retorno especifica a localidade atual da caixa de listagem. O [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) contém o código de país/região e o [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contém o identificador de idioma.

## <a name="remarks"></a>Comentários

O identificador de idioma consiste em um identificador de subidioma e um identificador de idioma primário. Use a macro [**PRIMARYLANGID**](/windows/desktop/api/winnt/nf-winnt-primarylangid) para extrair o identificador de idioma primário do [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) do valor de retorno e a macro [**SUBLANGID**](/windows/desktop/api/winnt/nf-winnt-sublangid) para extrair o identificador de subidioma.

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

[**seqüência de caracteres de LB \_**](lb-addstring.md)
</dt> <dt>

[**LB \_ SETlocale**](lb-setlocale.md)
</dt> <dt>

**Outros recursos**
</dt> <dt>

[**PRIMARYLANGID**](/windows/desktop/api/winnt/nf-winnt-primarylangid)
</dt> <dt>

[**SUBLANGID**](/windows/desktop/api/winnt/nf-winnt-sublangid)
</dt> </dl>

 

