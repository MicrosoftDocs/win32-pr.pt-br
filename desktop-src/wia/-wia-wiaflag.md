---
description: 'Sinalizadores usados pelos métodos IWiaDevMgr:: GetImageDlg, IWiaDevMgr2:: GetImageDlg, IWiaItem::D eviceDlg e IWiaItem2::D eviceDlg para controlar a operação da caixa de diálogo.'
ms.assetid: 468a3c9e-64f8-456d-aad9-fa7c6876fbe6
title: WiaFlag (Wiadef. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WIA_DEVICE_DIALOG_SINGLE_IMAGE
- WIA_DEVICE_DIALOG_USE_COMMON_UI
- WIA_SELECT_DEVICE_NODEFAULT
api_type:
- HeaderDef
api_location:
- wiadef.h
ms.openlocfilehash: bfff3ccab0f8aa73c2ae6e34086c3abc909a4b4d8b9222bf4d6d8a86e0a36c57
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117668959"
---
# <a name="wiaflag"></a>WiaFlag

Sinalizadores usados pelos métodos [**IWiaDevMgr:: GetImageDlg**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-getimagedlg), [**IWiaDevMgr2:: GetImageDlg**](-wia-iwiadevmgr2-getimagedlg.md), [**IWiaItem::D eviceDlg**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-devicedlg)e [**IWiaItem2::D evicedlg**](-wia-iwiaitem2-devicedlg.md) para controlar a operação da caixa de diálogo.



| Constante                                                                                                                                                                                                                | Descrição                                                                                                                                                                                                 |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WIA_DEVICE_DIALOG_SINGLE_IMAGE"></span><span id="wia_device_dialog_single_image"></span><dl> <dt>**\_ \_ imagem única da caixa de diálogo do dispositivo WIA \_ \_**</dt> </dl>     | Restringir a seleção de imagem a uma única imagem na caixa de diálogo aquisição de imagem de dispositivo.<br/>                                                                                                           |
| <span id="WIA_DEVICE_DIALOG_USE_COMMON_UI"></span><span id="wia_device_dialog_use_common_ui"></span><dl> <dt>**\_caixa de \_ diálogo do dispositivo WIA \_ usar \_ \_ interface do usuário comum**</dt> </dl> | Use a interface do usuário do sistema, se disponível, em vez da interface do usuário fornecida pelo fornecedor. Se a interface do usuário do sistema não estiver disponível, a interface do usuário do fornecedor será usada. Se nenhuma interface do usuário estiver disponível, a função retornará E \_ NOTIMPL.<br/>      |
| <span id="WIA_SELECT_DEVICE_NODEFAULT"></span><span id="wia_select_device_nodefault"></span><dl> <dt>**WIA \_ selecionar \_ dispositivo \_ padrão**</dt> </dl>               | Force o método [**IWiaDevMgr:: GetImageDlg**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-getimagedlg) ou [**IWiaDevMgr2:: GetImageDlg**](-wia-iwiadevmgr2-getimagedlg.md) para exibir a caixa de diálogo **selecionar dispositivo** .<br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional, \[ somente aplicativos de área de trabalho do Windows XP\]<br/>              |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                |
| Cabeçalho<br/>                   | <dl> <dt>Wiadef. h</dt> </dl> |



 

 




