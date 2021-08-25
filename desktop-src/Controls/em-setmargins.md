---
title: EM_SETMARGINS mensagem (Winuser.h)
description: Define as larguras das margens esquerda e direita para um controle de edição. A mensagem redesenha o controle para refletir as novas margens. Você pode enviar essa mensagem para um controle de edição ou um controle de edição rico.
ms.assetid: 23eb6c9e-3cf9-4c90-b33e-8da84034b49b
keywords:
- EM_SETMARGINS controles Windows mensagem
topic_type:
- apiref
api_name:
- EM_SETMARGINS
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 396bba6dda0f6dbd132b9f67fa5a1ef012758bbf7cf8fa9517b656dcf164c94c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120048356"
---
# <a name="em_setmargins-message"></a>Mensagem EM \_ SETMARGINS

Define as larguras das margens esquerda e direita para um controle de edição. A mensagem redesenha o controle para refletir as novas margens. Você pode enviar essa mensagem para um controle de edição ou um controle de edição rico.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

As margens a definir. Esse parâmetro pode ser um ou mais dos valores a seguir.



| Valor                                                                                                                                                            | Significado                                                                                                                                                                                                                                                                                                                                                                                                              |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="EC_LEFTMARGIN"></span><span id="ec_leftmargin"></span><dl> <dt>**EC \_ LEFTMARGIN**</dt> </dl>    | Define a margem esquerda.<br/>                                                                                                                                                                                                                                                                                                                                                                                     |
| <span id="EC_RIGHTMARGIN"></span><span id="ec_rightmargin"></span><dl> <dt>**EC \_ RIGHTMARGIN**</dt> </dl> | Define a margem direita.<br/>                                                                                                                                                                                                                                                                                                                                                                                    |
| <span id="EC_USEFONTINFO"></span><span id="ec_usefontinfo"></span><dl> <dt>**EC \_ USEFONTINFO**</dt> </dl> | **Controles de edição rich:** Define as margens esquerda e direita para uma largura estreita calculada usando as métricas de texto da fonte atual do controle. Se nenhuma fonte tiver sido definida para o controle, as margens serão definidas como zero. O *parâmetro lParam* é ignorado. <br/> **Editar controles:** O **valor \_ EC USEFONTINFO** não pode ser usado no *parâmetro wParam.* Ele só pode ser usado no *parâmetro lParam.*<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

A [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) especifica a nova largura da margem esquerda, em pixels. Esse valor será ignorado se *wParam* não incluir **EC \_ LEFTMARGIN.**

**Editar controles e Edição 3.0 e posteriores:** A [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) pode especificar o valor **EC \_ USEFONTINFO** para definir a margem esquerda para uma largura estreita calculada usando as métricas de texto da fonte atual do controle. Se nenhuma fonte tiver sido definida para o controle, a margem será definida como zero.

O [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) especifica a nova largura da margem direita, em pixels. Esse valor será ignorado se *wParam* não incluir **EC \_ RIGHTMARGIN.**

**Editar controles e Edição 3.0 e posteriores:** O [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) pode especificar o valor **EC \_ USEFONTINFO** para definir a margem direita para uma largura estreita calculada usando as métricas de texto da fonte atual do controle. Se nenhuma fonte tiver sido definida para o controle, a margem será definida como zero.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Essa mensagem não retorna um valor.

## <a name="remarks"></a>Comentários

**Editar controles:** Você não pode **usar EC \_ USEFONTINFO** no *parâmetro wParam,* mas pode usá-lo no *parâmetro lParam.*

**Edição rica:** Com suporte no Microsoft Rich Edit 1.0 e posterior. Todas as versões de edição rich suportam o uso **de EC \_ USEFONTINFO** no *parâmetro wParam.* No entanto, somente o Microsoft Rich Edit 3.0 e posteriores são suportados pelo uso de **EC \_ USEFONTINFO** no *parâmetro lParam.* Para obter informações sobre a compatibilidade de versões de edição rich com as várias versões do sistema, consulte [Sobre controles de edição rich](about-rich-edit-controls.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                                           |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                                     |
| Cabeçalho<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**EM \_ GETMARGINS**](em-getmargins.md)
</dt> </dl>

 

