---
title: Mensagem de WM_ADSPROP_NOTIFY_EXIT (Adsprop. h)
description: Uma Active Directory extensão de folha de propriedades envia a mensagem de saída de notificação do WM \_ ADSPROP \_ \_ para o objeto de notificação quando o objeto de notificação não é mais necessário.
ms.assetid: b0f58c73-8953-412d-b801-bf34967fe0b4
ms.tgt_platform: multiple
keywords:
- Mensagem de WM_ADSPROP_NOTIFY_EXIT Active Directory
topic_type:
- apiref
api_name:
- WM_ADSPROP_NOTIFY_EXIT
api_location:
- Adsprop.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 32d74ef4b7dfa525cfb77a6d89499837cbfac8f9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918993"
---
# <a name="wm_adsprop_notify_exit-message"></a>\_Mensagem de \_ saída de notificação do WM ADSPROP \_

Uma Active Directory extensão de folha de propriedades envia a mensagem de **\_ saída de \_ notificação \_ do WM ADSPROP** para o objeto de notificação quando o objeto de notificação não é mais necessário.


```C++
WM_ADSPROP_NOTIFY_EXIT

    WPARAM wParam
    LPARAM lParam
    
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*HWND* 
</dt> <dd>

O identificador do objeto de notificação. Para obter esse identificador, chame [**ADsPropCreateNotifyObj**](/windows/desktop/api/Adsprop/nf-adsprop-adspropcreatenotifyobj).

</dd> <dt>

*wParam* 
</dt> <dd>

Não usado.

</dd> <dt>

*lParam* 
</dt> <dd>

Não usado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esta mensagem não tem nenhum valor de retorno.

## <a name="remarks"></a>Comentários

O objeto de notificação será excluído em resposta a esta mensagem. Quando essa mensagem é enviada, o identificador do objeto de notificação deve ser considerado inválido.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                             |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                       |
| parâmetro<br/>                   | <dl> <dt>Adsprop. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ADsPropCreateNotifyObj**](/windows/desktop/api/Adsprop/nf-adsprop-adspropcreatenotifyobj)
</dt> <dt>

[Mensagens em Active Directory Domain Services](messages-in-active-directory-domain-services.md)
</dt> </dl>

 

 





