---
title: Mensagem de EM_SETMARGINS (WinUser. h)
description: Define as larguras das margens esquerda e direita para um controle de edição. A mensagem redesenha o controle para refletir as novas margens. Você pode enviar essa mensagem para um controle de edição ou um controle de edição rico.
ms.assetid: 23eb6c9e-3cf9-4c90-b33e-8da84034b49b
keywords:
- Controles de EM_SETMARGINS de mensagens do Windows
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
ms.openlocfilehash: 5c68f3394234a6f86b3c5ff69622b86e61afc556
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918622"
---
# <a name="em_setmargins-message"></a>\_Mensagem em SETmargins

Define as larguras das margens esquerda e direita para um controle de edição. A mensagem redesenha o controle para refletir as novas margens. Você pode enviar essa mensagem para um controle de edição ou um controle de edição rico.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

As margens a serem definidas. Esse parâmetro pode ser um ou mais dos valores a seguir.



| Valor                                                                                                                                                            | Significado                                                                                                                                                                                                                                                                                                                                                                                                              |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="EC_LEFTMARGIN"></span><span id="ec_leftmargin"></span><dl> <dt>**LeftMargin do EC \_**</dt> </dl>    | Define a margem esquerda.<br/>                                                                                                                                                                                                                                                                                                                                                                                     |
| <span id="EC_RIGHTMARGIN"></span><span id="ec_rightmargin"></span><dl> <dt>**RIGHTMARGIN do EC \_**</dt> </dl> | Define a margem direita.<br/>                                                                                                                                                                                                                                                                                                                                                                                    |
| <span id="EC_USEFONTINFO"></span><span id="ec_usefontinfo"></span><dl> <dt>**USEFONTINFO do EC \_**</dt> </dl> | **Controles de edição avançados:** Define as margens esquerda e direita com uma largura estreita calculada usando as métricas de texto da fonte atual do controle. Se nenhuma fonte tiver sido definida para o controle, as margens serão definidas como zero. O parâmetro *lParam* é ignorado. <br/> **Controles de edição:** O valor de **\_ USEFONTINFO do EC** não pode ser usado no parâmetro *wParam* . Ele só pode ser usado no parâmetro *lParam* .<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

O [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) especifica a nova largura da margem esquerda, em pixels. Esse valor será ignorado se *wParam* não incluir o **EC \_ LeftMargin**.

**Edite controles e edição avançada 3,0 e posteriores:** O [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) pode especificar o valor de **\_ USEFONTINFO do EC** para definir a margem esquerda com uma largura estreita calculada usando as métricas de texto da fonte atual do controle. Se nenhuma fonte tiver sido definida para o controle, a margem será definida como zero.

O [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) especifica a nova largura da margem direita, em pixels. Esse valor será ignorado se *wParam* não incluir a **\_ margem do EC**.

**Edite controles e edição avançada 3,0 e posteriores:** O [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) pode especificar o valor de **\_ USEFONTINFO do EC** para definir a margem direita com uma largura estreita calculada usando as métricas de texto da fonte atual do controle. Se nenhuma fonte tiver sido definida para o controle, a margem será definida como zero.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa mensagem não retorna um valor.

## <a name="remarks"></a>Comentários

**Controles de edição:** Não é possível usar o **EC \_ USEFONTINFO** no parâmetro *wParam* , mas você pode usá-lo no parâmetro *lParam* .

**Edição avançada:** Com suporte no Microsoft Rich Edit 1,0 e posterior. Todas as versões de edição avançadas dão suporte ao uso do **EC \_ USEFONTINFO** no parâmetro *wParam* . No entanto, somente o Microsoft Rich Edit 3,0 e versões posteriores dão suporte ao uso do **EC \_ USEFONTINFO** no parâmetro *lParam* . Para obter informações sobre a compatibilidade das versões de edição rica com as várias versões do sistema, consulte [sobre controles de edição avançados](about-rich-edit-controls.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                                           |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                                     |
| parâmetro<br/>                   | <dl> <dt>WinUser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**em \_ GETmargins**](em-getmargins.md)
</dt> </dl>

 

