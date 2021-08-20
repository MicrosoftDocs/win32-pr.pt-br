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
ms.openlocfilehash: 6cc130a83aa77021e0be512d9b2ad27914b4c6be382c0290e082e1fbd67b8b22
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119024294"
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

## <a name="return-value"></a>Valor retornado

Esta mensagem não tem nenhum valor de retorno.

## <a name="remarks"></a>Comentários

Ao adicionar páginas ao snap-in do MMC do Active Directory Manager, Active Directory folhas de propriedades do MMC criam os objetos de notificação por uma chamada à função [**ADsPropCreateNotifyObj**](/windows/desktop/api/Adsprop/nf-adsprop-adspropcreatenotifyobj) e, em seguida, passa o identificador do objeto de notificação para cada página de propriedades.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                             |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                       |
| Cabeçalho<br/>                   | <dl> <dt>Adsprop. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ADsPropCreateNotifyObj**](/windows/desktop/api/Adsprop/nf-adsprop-adspropcreatenotifyobj)
</dt> <dt>

[Mensagens em Active Directory Domain Services](messages-in-active-directory-domain-services.md)
</dt> </dl>

 

 





