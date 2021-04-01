---
title: Constantes de TF_LBI_STATUS_ (Ctfutb. h)
description: As \_ constantes TF bin \_ status \_ \ Constants indicam o status de um item de barra de idiomas. Esses valores são usados com o método GetStatus ITfLangBarItem.
ms.assetid: 5f2c0e61-f7e5-4dcc-86a3-7bd1c994b8bc
topic_type:
- apiref
api_name:
- TF_LBI_STATUS_HIDDEN
- TF_LBI_STATUS_DISABLED
- TF_LBI_STATUS_BTN_TOGGLED
api_location:
- Ctfutb.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7de9dcf0272eaf79fd001461aa555d78c9d6ae30
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103645005"
---
# <a name="tf_lbi_status_-constants"></a>Constantes de status de TF \_ ICB \_ \_ \*

As constantes ** \_ TF \_ bin \_ \* status* _ indicam o status de um item da barra de idiomas. Esses valores são usados com o método [ITfLangBarItem:: GetStatus](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritem-getstatus) .



| Constante/valor                                                                                                                                                                                                                                                       | Descrição                                                                                                                                       |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TF_LBI_STATUS_HIDDEN"></span><span id="tf_lbi_status_hidden"></span><dl> <dt>_ * TF \_ STATUS do ICB \_ \_ oculto * *</dt> <dt>0x00000001</dt> </dl>                 | O item está oculto. Esse estilo será ignorado se o item não incluir o estilo de \_ HIDDENSTATUSCONTROL do estilo de TF bin \_ \_ .<br/>                  |
| <span id="TF_LBI_STATUS_DISABLED"></span><span id="tf_lbi_status_disabled"></span><dl> <dt>**TF \_ STATUS de ICB \_ \_ desabilitado**</dt> <dt>0x00000002</dt> </dl>           | O item está desabilitado.<br/>                                                                                                                  |
| <span id="TF_LBI_STATUS_BTN_TOGGLED"></span><span id="tf_lbi_status_btn_toggled"></span><dl> <dt>**TF \_ BIN \_ status \_ BTN \_ toggleu**</dt> <dt>0x00010000</dt> </dl> | O item está no estado alternado ou pressionado. Esse estilo será ignorado se o item não incluir o estilo de \_ alternância TF bin \_ Style \_ BTN \_ .<br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                            |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                  |
| Redistribuível<br/>          | TSF 1,0 no Windows 2000 Professional<br/>                                       |
| parâmetro<br/>                   | <dl> <dt>Ctfutb. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>Ctfutb. idl</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ITfLangBarItem:: GetStatus](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritem-getstatus)
</dt> </dl>

 

 





