---
title: Mensagem de WM_ADSPROP_NOTIFY_PAGEHWND (Adsprop. h)
description: Uma extensão de folha de propriedades do serviço de diretório Active Directory chama o ADsPropSetHwnd para informar o objeto de notificação do identificador da janela da página de propriedades.
ms.assetid: eb8bf525-cd7f-44d0-a0f9-43178a29c443
ms.tgt_platform: multiple
keywords:
- Mensagem de WM_ADSPROP_NOTIFY_PAGEHWND Active Directory
topic_type:
- apiref
api_name:
- WM_ADSPROP_NOTIFY_PAGEHWND
api_location:
- Adsprop.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d74ef2db993d2a3daf10f69687b8f3525ef80a87
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086201"
---
# <a name="wm_adsprop_notify_pagehwnd-message"></a>\_Mensagem do \_ PAGEHWND de notificação do WM ADSPROP \_

Uma extensão de folha de propriedades do serviço de diretório Active Directory chama o [**ADsPropSetHwnd**](/windows/desktop/api/Adsprop/nf-adsprop-adspropsethwnd) para informar o objeto de notificação do identificador da janela da página de propriedades. A função **ADsPropSetHwnd** envia a mensagem **PAGEHWND do WM \_ ADSPROP \_ Notify \_** para o objeto de notificação, que informa o objeto de notificação do identificador da janela da página de propriedades.


```C++
WM_ADSPROP_NOTIFY_PAGEHWND

    WPARAM hPage
    LPARAM ptzTitle
    
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hNotifyObj* 
</dt> <dd>

O identificador do objeto de notificação. Para obter esse identificador, chame [**ADsPropCreateNotifyObj**](/windows/desktop/api/Adsprop/nf-adsprop-adspropcreatenotifyobj).

</dd> <dt>

*hPage* 
</dt> <dd>

Um identificador de janela da página de propriedades.

</dd> <dt>

*ptzTitle* 
</dt> <dd>

Ponteiro para um buffer **WCHAR** com terminação nula que contém o título da página de propriedades.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esta mensagem não tem nenhum valor de retorno.

## <a name="remarks"></a>Comentários

Uma extensão de folha de propriedades Active Directory normalmente chama a função [**ADsPropSetHwnd**](/windows/desktop/api/Adsprop/nf-adsprop-adspropsethwnd) durante o processamento da mensagem [**\_ INITDIALOG do WM**](../dlgbox/wm-initdialog.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                             |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                       |
| parâmetro<br/>                   | <dl> <dt>Adsprop. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Mensagens em Active Directory Domain Services](messages-in-active-directory-domain-services.md)
</dt> <dt>

[**ADsPropSetHwnd**](/windows/desktop/api/Adsprop/nf-adsprop-adspropsethwnd)
</dt> <dt>

[**ADsPropCreateNotifyObj**](/windows/desktop/api/Adsprop/nf-adsprop-adspropcreatenotifyobj)
</dt> <dt>

[**INITDIALOG do WM \_**](../dlgbox/wm-initdialog.md)
</dt> </dl>

 

