---
title: Mensagem de WM_ADSPROP_NOTIFY_APPLY (Adsprop. h)
description: Uma extensão de folha de propriedades do serviço de diretório Active Directory envia a \_ \_ mensagem de aplicação notificar ADSPROP do WM \_ para o objeto de notificação se o manipulador da página de propriedades PSN \_ Apply for executado com sucesso.
ms.assetid: 3536054b-83ee-4cfa-ab54-c0af3a46289e
ms.tgt_platform: multiple
keywords:
- Mensagem de WM_ADSPROP_NOTIFY_APPLY Active Directory
topic_type:
- apiref
api_name:
- WM_ADSPROP_NOTIFY_APPLY
api_location:
- Adsprop.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0ccd5bb95e3f092634d54ba0534e81ded6701bf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105756090"
---
# <a name="wm_adsprop_notify_apply-message"></a>\_Mensagem de \_ aplicação de notificação do WM ADSPROP \_

Uma extensão de folha de propriedades do serviço de diretório Active Directory envia a mensagem de **\_ \_ \_ aplicação notificar ADSPROP do WM** para o objeto de notificação se o manipulador da página de propriedades PSN \_ Apply for executado com sucesso.


```C++
WM_ADSPROP_NOTIFY_APPLY

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

Ao adicionar páginas ao snap-in do MMC do Active Directory Manager, Active Directory folhas de propriedades do MMC criam os objetos de notificação por uma chamada à função [**ADsPropCreateNotifyObj**](/windows/desktop/api/Adsprop/nf-adsprop-adspropcreatenotifyobj) e, em seguida, passa o identificador do objeto de notificação para cada página de propriedades.

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

 

 





