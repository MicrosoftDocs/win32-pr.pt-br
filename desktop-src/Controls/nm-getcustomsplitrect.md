---
title: NM_GETCUSTOMSPLITRECT código de notificação (commctrl. h)
description: Enviado por um controle de botão para seu pai para obter medidas para os dois retângulos do botão de divisão. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: ce72778d-3cca-46a4-9d05-40954a18681d
keywords:
- NM_GETCUSTOMSPLITRECT de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- NM_GETCUSTOMSPLITRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 97b839540da7e07069fdf56ed656ed8772d029eb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085163"
---
# <a name="nm_getcustomsplitrect-notification-code"></a>\_Código de notificação nm GETCUSTOMSPLITRECT

Enviado por um controle de botão para seu pai para obter medidas para os dois retângulos do botão de divisão. Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .


```C++
NM_GETCUSTOMSPLITRECT
        
    nmCustomSplit = (NMCUSTOMSPLITRECTINFO *) lParam;
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lParam* 
</dt> <dd>

Um ponteiro para um [**NMCUSTOMSPLITRECTINFO**](/windows/win32/api/commctrl/ns-commctrl-nmcustomsplitrectinfo) para receber informações de retângulos delimitadores. A estrutura **NMCUSTOMSPLITRECTINFO** é enviada com o código de notificação como uma solicitação para que o pai forneça medidas para os retângulos do botão de divisão.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorne [**CDRF \_ SKIPDEFAULT**](cdrf-constants.md) para instruir o controle de botão a usar os valores retornados na estrutura [**NMCUSTOMSPLITRECTINFO**](/windows/win32/api/commctrl/ns-commctrl-nmcustomsplitrectinfo) ; caso contrário, retornará [**CDRF \_ dopadrão**](cdrf-constants.md).

## <a name="remarks"></a>Comentários

Esse código de notificação é enviado por um controle de botão antes de ser desenhado. O botão deve ser do estilo [**BS \_ SPLITBUTTON**](button-styles.md) ou [**BS \_ DEFSPLITBUTTON**](button-styles.md). Se os retângulos retornados ao controle em *lParam* não forem válidos, eles serão ignorados.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





