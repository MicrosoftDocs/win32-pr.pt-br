---
title: Tipo de privacidade (Wininet. h)
description: Especifica que as configurações de privacidade são para cookies primários ou de terceiros.
ms.assetid: 7d0846d4-fd81-4af9-b7e6-05c4c1438770
topic_type:
- apiref
api_name:
- PRIVACY_TYPE_FIRST_PARTY
- PRIVACY_TYPE_THIRD_PARTY
api_location:
- Wininet.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af6f29461f57a2209fde00b30bce7914c207958f27e28062e2c3bd3d94d442e1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117743723"
---
# <a name="privacy-type"></a>Tipo de privacidade

Especifica que as configurações de privacidade são para cookies primários ou de terceiros.

<dl> <dt>

<span id="PRIVACY_TYPE_FIRST_PARTY"></span><span id="privacy_type_first_party"></span>**tipo de privacidade- \_ \_ primeira \_ entidade**
</dt> <dd> <dl> <dt>

0
</dt> <dt>



Refere-se às configurações de privacidade para cookies de primeira entidade.


</dt> </dl> </dd> <dt>

<span id="PRIVACY_TYPE_THIRD_PARTY"></span><span id="privacy_type_third_party"></span>**tipo de privacidade de \_ \_ terceiros \_**
</dt> <dd> <dl> <dt>

1
</dt> <dt>



Refere-se às configurações de privacidade para cookies de terceiros.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Comentários

Os cookies são categorizados como primários e de terceiros. Um cookie primário é aquele originado do domínio do host. Se " https://www.blueyonderairlines.com " for encontrado na barra de endereços do Microsoft Internet Explorer, "www.blueyonderairlines.com" será o domínio do host. Ao visitar essa página, se um cookie for definido de um domínio diferente de "www.blueyonderairlines.com", como "www.fourthcoffee.com", esse cookie será considerado um cookie de terceiros.

> [!Note]  
> O WinINet não oferece suporte a implementações de servidor. Além disso, ele não deve ser usado de um serviço. para implementações de servidor ou serviços, use [o Microsoft Windows HTTP services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                           |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                 |
| Cabeçalho<br/>                   | <dl> <dt>WinInet. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**PrivacyGetZonePreferenceW**](/windows/win32/api/winineti/nf-winineti-privacygetzonepreferencew)
</dt> <dt>

[**PrivacySetZonePreferenceW**](/windows/win32/api/winineti/nf-winineti-privacysetzonepreferencew)
</dt> </dl>

 

