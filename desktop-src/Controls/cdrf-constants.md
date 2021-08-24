---
title: Constantes de RF (CommCtrl.h)
description: Essas constantes são usadas como valores de retorno por um controle em resposta a um código de notificação \_ CUSTOMDRAW NM.
ms.assetid: 6b05e27e-5d18-46f2-b326-2a5148597852
topic_type:
- apiref
api_name:
- CDRF_DODEFAULT
- CDRF_NEWFONT
- CDRF_SKIPDEFAULT
- CDRF_DOERASE
- CDRF_NOTIFYPOSTPAINT
- CDRF_NOTIFYITEMDRAW
- CDRF_NOTIFYSUBITEMDRAW
- CDRF_NOTIFYPOSTERASE
- CDRF_SKIPPOSTPAINT
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 817bab7c2ec41134d71c92ada94c62475b01cc2db96a9f8c74ecb2c7b9274451
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119770376"
---
# <a name="rf-constants"></a>Constantes de RF

Essas constantes são usadas como valores de retorno por um controle em resposta a um código de notificação [ \_ CUSTOMDRAW NM.](nm-customdraw.md)



| Constante/valor                                                                                                                                                                                                                                           | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                           |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CDRF_DODEFAULT"></span><span id="cdrf_dodefault"></span><dl> <dt>**CDRF \_ DODEFAULT**</dt> <dt>0x00000000</dt> </dl>                         | O controle se desenhará. Ele não enviará nenhum código de [notificação \_ CUSTOMDRAW de NM](nm-customdraw.md) adicional para esse ciclo de pintura. Isso ocorre quando **dwDrawStage da** estrutura [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) é igual a CDDS \_ PREPAINT.<br/>                                                                                                                                                               |
| <span id="CDRF_NEWFONT"></span><span id="cdrf_newfont"></span><dl> <dt>**CDRF \_ NEWFONT**</dt> <dt>0x00000002</dt> </dl>                               | O aplicativo especificou uma nova fonte para o item; o controle usará a nova fonte. Para obter mais informações sobre como alterar fontes, consulte Alterando fontes e cores. Isso ocorre quando **dwDrawStage da** estrutura [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) é igual a CDDS \_ ITEMPREPAINT.<br/>                                                                                                                                      |
| <span id="CDRF_SKIPDEFAULT"></span><span id="cdrf_skipdefault"></span><dl> <dt>**CDRF \_ SKIPDEFAULT**</dt> <dt>0x00000004</dt> </dl>                   | O aplicativo extraia o item manualmente. O controle não desenhará o item. Isso ocorre quando **dwDrawStage da** estrutura [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) é igual a CDDS \_ ITEMPREPAINT.<br/>                                                                                                                                                                                                                          |
| <span id="CDRF_DOERASE"></span><span id="cdrf_doerase"></span><dl> <dt>**CDRF \_ DOERASE**</dt> <dt>0x00000008</dt> </dl>                               | **Windows Vista e posterior.** O controle desenhará a plano de fundo.<br/>                                                                                                                                                                                                                                                                                                                                                         |
| <span id="CDRF_NOTIFYPOSTPAINT"></span><span id="cdrf_notifypostpaint"></span><dl> <dt>**CDRF \_ NOTIFYPOSTPAINT**</dt> <dt>0x00000010</dt> </dl>       | O controle notificará o pai depois de pintar um item. Isso ocorre quando **dwDrawStage da** estrutura [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) é igual a CDDS \_ PREPAINT.<br/>                                                                                                                                                                                                                                               |
| <span id="CDRF_NOTIFYITEMDRAW"></span><span id="cdrf_notifyitemdraw"></span><dl> <dt>**CDRF \_ NOTIFYITEMDRAW**</dt> <dt>0x00000020</dt> </dl>          | O controle notificará o pai de todas as operações de desenho relacionadas ao item. Ele enviará códigos [de \_ notificação CUSTOMDRAW de NM](nm-customdraw.md) antes e depois de desenhar itens. Isso ocorre quando **dwDrawStage da** estrutura [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) é igual a CDDS \_ PREPAINT.<br/>                                                                                                                           |
| <span id="CDRF_NOTIFYSUBITEMDRAW"></span><span id="cdrf_notifysubitemdraw"></span><dl> <dt>**CDRF \_ NOTIFYSUBITEMDRAW**</dt> <dt>0x00000020</dt> </dl> | **Internet Explorer 4.0 e posterior.** O controle notificará o pai de todas as operações de desenho relacionadas ao item. Ele enviará códigos [de \_ notificação CUSTOMDRAW de NM](nm-customdraw.md) antes e depois de desenhar itens. Isso ocorre quando **dwDrawStage da** estrutura [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) é igual a CDDS \_ PREPAINT. Esse sinalizador é idêntico ao **CDRF \_ NOTIFYITEMDRAW** e seu uso depende do contexto.<br/> |
| <span id="CDRF_NOTIFYPOSTERASE"></span><span id="cdrf_notifyposterase"></span><dl> <dt>**CDRF \_ NOTIFYPOSTERASE**</dt> <dt>0x00000040</dt> </dl>       | O controle notificará o pai depois de apagar um item. Isso ocorre quando **dwDrawStage da** estrutura [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) é igual a CDDS \_ PREPAINT.<br/>                                                                                                                                                                                                                                                |
| <span id="CDRF_SKIPPOSTPAINT"></span><span id="cdrf_skippostpaint"></span><dl> <dt>**CDRF \_ SKIPPOSTPAINT**</dt> <dt>0x00000100</dt> </dl>             | **Windows Vista e posterior.** O controle não desenhará o retângulo de foco.<br/>                                                                                                                                                                                                                                                                                                                                                |



## <a name="remarks"></a>Comentários

Essas constantes são definidas em Commctrl.h.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>CommCtrl.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Personalização da aparência de um controle usando desenho personalizado](custom-draw.md)
</dt> </dl>

 

 





