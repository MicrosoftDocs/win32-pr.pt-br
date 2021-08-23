---
title: LB_GETLOCALE mensagem (Winuser.h)
description: Obtém a localidade atual da caixa de listagem. Você pode usar a localidade para determinar a ordem de classificação correta do texto exibido (para caixas de listagem com o estilo SORT LBS) e do texto adicionado pela mensagem \_ \_ ADDSTRING do LB.
ms.assetid: ec814b03-5ce2-4b81-a36c-ab4c115f88be
keywords:
- LB_GETLOCALE controles de Windows mensagem
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
ms.openlocfilehash: 732bfac72502c38265f7c1651667dc235c440293c8435f16088eaee775a874f2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119544516"
---
# <a name="lb_getlocale-message"></a>Mensagem \_ GETLOCALE do LB

Obtém a localidade atual da caixa de listagem. Você pode usar a localidade para determinar a ordem de classificação correta do texto exibido (para caixas de listagem com o estilo [**SORT \_ LBS)**](list-box-styles.md) e do texto adicionado pela mensagem [**\_ ADDSTRING do LB.**](lb-addstring.md)

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

## <a name="return-value"></a>Valor retornado

O valor de retorno especifica a localidade atual da caixa de listagem. O [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) contém o código de país/região e [**o LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contém o identificador de idioma.

## <a name="remarks"></a>Comentários

O identificador de idioma consiste em um identificador de sublângua e um identificador de idioma primário. Use a macro [**PRIMARYLANGID**](/windows/desktop/api/winnt/nf-winnt-primarylangid) para extrair o identificador de idioma primário da [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) do valor de retorno e a [**macro SUBLANGID**](/windows/desktop/api/winnt/nf-winnt-sublangid) para extrair o identificador de sublanguagem.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                                           |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                                     |
| Cabeçalho<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[**LB \_ ADDSTRING**](lb-addstring.md)
</dt> <dt>

[**LB \_ SETLOCALE**](lb-setlocale.md)
</dt> <dt>

**Outros recursos**
</dt> <dt>

[**PRIMARYLANGID**](/windows/desktop/api/winnt/nf-winnt-primarylangid)
</dt> <dt>

[**SUBLANGID**](/windows/desktop/api/winnt/nf-winnt-sublangid)
</dt> </dl>

 

