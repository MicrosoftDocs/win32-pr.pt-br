---
title: Código de notificação de NM_CUSTOMDRAW (botão) (commctrl. h)
description: Notifica a janela pai de um controle de botão sobre as operações de desenho personalizadas no botão. O controle de botão envia esse código de notificação na forma de uma \_ mensagem de notificação do WM.
ms.assetid: cabe5515-ba64-4c53-8746-7a0559df8989
keywords:
- Código de notificação de NM_CUSTOMDRAW (botão) controles do Windows
topic_type:
- apiref
api_name:
- NM_CUSTOMDRAW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab3cc4eb73c3a0185131bb6ef2198458888ec89d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104456049"
---
# <a name="nm_customdraw-button-notification-code"></a>\_Código de notificação nm CUSTOMDRAW (botão)

Notifica a janela pai de um controle de botão sobre as operações de desenho personalizadas no botão.

O controle de botão envia esse código de notificação na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .


```C++
NM_CUSTOMDRAW

    lpNMCustomDraw = (LPNMCUSTOMDRAW) lParam;
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lParam* 
</dt> <dd>

Um ponteiro para uma estrutura [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) que contém informações sobre a operação de desenho. O membro **dwItemSpec** dessa estrutura contém o índice do item que está sendo desenhado e o membro **lItemlParam** dessa estrutura contém o *lParam* do item.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O valor que seu aplicativo pode retornar depende do estágio de desenho atual. O membro **dwDrawStage** da estrutura [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) associada contém um valor que especifica o estágio de desenho. Você deve retornar um dos valores a seguir.



| Código de retorno                                                                                          | Descrição                                                                                                                                                           |
|------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**CDRF \_ NOTIFYPOSTERASE**</dt> </dl> | O controle notificará o pai depois de apagar um item. Isso só poderá ser usado se **dwDrawStage** for igual a CDDs \_ preerase.<br/>                                  |
| <dl> <dt>**CDRF \_ NOTIFYPOSTPAINT**</dt> </dl> | O controle notificará o pai depois de pintar um item. Isso pode ser usado somente se **dwDrawStage** for igual a CDDs \_ PrePaint.<br/>                                 |
| <dl> <dt>**CDRF \_ SKIPDEFAULT**</dt> </dl>     | O aplicativo desenhou o item manualmente. O controle não vai desenhar o item. Isso pode ser usado quando **dwDrawStage** é igual a CDDs \_ PREerase ou CDDs \_ PrePaint.<br/> |



 

## <a name="remarks"></a>Comentários

Se o controle de botão estiver marcado como OwnerDraw (BS \_ OwnerDraw), o \_ código de notificação nm CUSTOMDRAW não será enviado.

Consulte [usando o desenho personalizado](custom-draw.md) para mais discussões.

> [!Note]  
> Para usar esse código de notificação, você deve fornecer um manifesto especificando Comclt32.dll versão 6,0. Para obter mais informações sobre manifestos, consulte [habilitando estilos visuais](cookbook-overview.md).

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                                            |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                                      |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h (incluir Windows. h)</dt> </dl> |



 

 





