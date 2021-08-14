---
title: EN_OBJECTPOSITIONS código de notificação (RichEdit. h)
description: Notifica uma janela pai do controle de edição rico quando o controle lê em objetos. Um controle de edição rico envia esse código de notificação na forma de uma \_ mensagem de notificação do WM.
ms.assetid: 1965185f-8a13-4989-8574-af8b9b30f6b0
keywords:
- EN_OBJECTPOSITIONS código de notificação Windows controles
topic_type:
- apiref
api_name:
- EN_OBJECTPOSITIONS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f3be6f3f41877a56396ef021e97130f4c174516160d7243144f10ea1dfd3951b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119436686"
---
# <a name="en_objectpositions-notification-code"></a>\_Código de notificação de OBJECTPOSIÇÕES en

Notifica uma janela pai do controle de edição rico quando o controle lê em objetos. Um controle de edição rico envia esse código de notificação na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .


```C++
EN_OBJECTPOSITIONS

    pOjectPositions = (OBJECTPOSITIONS *) lParam; 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lParam* 
</dt> <dd>

Uma estrutura de [**objectposições**](/windows/desktop/api/Richedit/ns-richedit-objectpositions) .

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retornar zero para continuar a operação de **leitura** .

Retornar um valor diferente de zero para interromper a operação de **leitura** .

## <a name="remarks"></a>Comentários

Para receber um \_ código de notificação en objectposições, especifique o sinalizador [**enm \_ objectpositiones**](rich-edit-control-event-mask-flags.md) na máscara enviada com a mensagem em [**\_ SETEVENTMASK**](em-seteventmask.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[**em \_ SETEVENTMASK**](em-seteventmask.md)
</dt> <dt>

[**Objectposições**](/windows/desktop/api/Richedit/ns-richedit-objectpositions)
</dt> <dt>

[**notificação do WM \_**](wm-notify.md)
</dt> <dt>

**Outros recursos**
</dt> <dt>

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))
</dt> <dt>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))
</dt> </dl>

 

