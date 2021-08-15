---
title: WM_ADSPROP_NOTIFY_APPLY mensagem (Adsprop.h)
description: Uma extensão de folha de propriedades do serviço de diretório do Active Directory enviará a mensagem WM ADSPROP NOTIFY APPLY para o objeto de notificação se o manipulador PSN APPLY da página de propriedades \_ \_ for \_ \_ bem-sucedido.
ms.assetid: 3536054b-83ee-4cfa-ab54-c0af3a46289e
ms.tgt_platform: multiple
keywords:
- WM_ADSPROP_NOTIFY_APPLY mensagem do Active Directory
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
# <a name="wm_adsprop_notify_apply-message"></a>Mensagem WM \_ ADSPROP \_ NOTIFY \_ APPLY

Uma extensão de folha de propriedades do serviço de diretório do Active Directory enviará a mensagem **WM \_ ADSPROP \_ NOTIFY \_ APPLY** para o objeto de notificação se o manipulador PSN APPLY da página de propriedades \_ for bem-sucedido.


```C++
WM_ADSPROP_NOTIFY_APPLY

    WPARAM wParam
    LPARAM lParam
    
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Hwnd* 
</dt> <dd>

O identificador do objeto de notificação. Para obter esse handle, chame [**ADsPropCreateNotifyObj.**](/windows/desktop/api/Adsprop/nf-adsprop-adspropcreatenotifyobj)

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

Essa mensagem não tem nenhum valor de retorno.

## <a name="remarks"></a>Comentários

Ao adicionar páginas ao snap-in do MMC do Active Directory Manager, as folhas de propriedades do MMC do Active Directory criam os objetos de notificação por meio de uma chamada para a [**função ADsPropCreateNotifyObj**](/windows/desktop/api/Adsprop/nf-adsprop-adspropcreatenotifyobj) e, em seguida, passa o identificador de objeto de notificação para cada página de propriedades.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                             |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                       |
| Cabeçalho<br/>                   | <dl> <dt>Adsprop.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ADsPropCreateNotifyObj**](/windows/desktop/api/Adsprop/nf-adsprop-adspropcreatenotifyobj)
</dt> <dt>

[Mensagens em Active Directory Domain Services](messages-in-active-directory-domain-services.md)
</dt> </dl>

 

 





