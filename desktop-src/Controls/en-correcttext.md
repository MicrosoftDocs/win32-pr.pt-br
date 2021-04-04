---
title: EN_CORRECTTEXT código de notificação (RichEdit. h)
description: Notifica uma janela pai do controle de edição rico que ocorreu um gesto de SYV \_ correto, dando à janela pai a oportunidade de cancelar a correção do texto. Um controle de edição rico envia esse código de notificação na forma de uma \_ mensagem de notificação do WM.
ms.assetid: d6f6278f-ff63-4f6a-a352-2b4d70df3e1a
keywords:
- EN_CORRECTTEXT de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- EN_CORRECTTEXT
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e5d1339513a94967ab60bdab2b9ee39172b19e76
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085214"
---
# <a name="en_correcttext-notification-code"></a>\_Código de notificação en CORRECTTEXT

Notifica uma janela pai do controle de edição rico que ocorreu um gesto de SYV \_ correto, dando à janela pai a oportunidade de cancelar a correção do texto. Um controle de edição rico envia esse código de notificação na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .


```C++
EN_CORRECTTEXT

    penCorrectText = (ENCORRECTTEXT *) lParam; 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lParam* 
</dt> <dd>

Uma estrutura [**ENCORRECTTEXT**](/windows/desktop/api/Richedit/ns-richedit-encorrecttext) que especifica a seleção a ser corrigida.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retornar zero para ignorar a ação.

Retorna um valor diferente de zero para processar a ação.

## <a name="remarks"></a>Comentários

Esse código de notificação será enviado somente se os recursos de caneta estiverem disponíveis.

Para receber \_ códigos de notificação do en CORRECTTEXT, especifique [**enm \_ CORRECTTEXT**](rich-edit-control-event-mask-flags.md) na máscara enviada com a mensagem em [**\_ SETEVENTMASK**](em-seteventmask.md) .

> [!Note]  
> O \_ código de notificação en CORRECTTEXT só tem suporte na versão de edição avançada 1,0. Não há suporte para ele em versões posteriores do rich edit. Para obter informações sobre a compatibilidade das versões de edição rica com as várias versões do sistema, consulte [sobre controles de edição avançados](about-rich-edit-controls.md).

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[**ENCORRECTTEXT**](/windows/desktop/api/Richedit/ns-richedit-encorrecttext)
</dt> </dl>

 

 





