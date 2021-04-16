---
title: '\_ \_ Req de credenciais EAP (Eaptypes. h)'
description: Armazena credenciais de segurança EAP em uma \_ estrutura de matriz de campo de entrada de configuração EAP \_ \_ \_ . | \_ \_ Req de credenciais EAP (Eaptypes. h)
ms.assetid: 537a90fc-4dd2-44d4-93da-949f31130ac4
keywords:
- EAP_CRED_REQ
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 20da4e6aa8b1ab24dfd9cd791236d1f9b26304f6
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "105794589"
---
# <a name="eap_cred_req"></a>Req. de \_ credenciais EAP \_

A **estrutura \_ \_ req. de credenciais EAP** armazena as credenciais de segurança EAP em uma estrutura de matriz de [**\_ campo de entrada de configuração \_ \_ \_ EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_array) .


```C++
typedef EAP_CONFIG_INPUT_FIELD_ARRAY EAP_CRED_REQ;
```



<dl> <dt>

**Req. de \_ credenciais EAP \_**
</dt> <dd>

A estrutura do req. de **\_ credenciais \_ EAP** armazena as credenciais de segurança EAP novas e antigas apontadas pelo parâmetro *pbUiData* da estrutura de [**\_ \_ \_ dados da interface do usuário interativa do EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_interactive_ui_data) quando o parâmetro *dwDataType* do tipo de [**\_ \_ \_ dados \_ de interface do usuário interativo do EAP**](/windows/desktop/api/eaptypes/ne-eaptypes-eap_interactive_ui_data_type) especifica um tipo de solicitação de credencial.

</dd> </dl>

## <a name="remarks"></a>Comentários

A estrutura de **\_ \_ req. de credenciais EAP** é usada para dar suporte ao SSO (logon único).

A estrutura de req. de **\_ credenciais \_ EAP** é idêntica à estrutura [**resp de \_ credenciais \_ de EAP**](eap-cred-resp.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Eaptypes. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Estruturas do suplicante EAPHost](eap-host-supplicant-structures.md)
</dt> <dt>

[**\_resp de credenciais EAP \_**](eap-cred-resp.md)
</dt> <dt>

[**Req. de \_ expiração de credenciais EAP \_ \_**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_cred_expiry_req)
</dt> <dt>

[**\_resp de \_ expiração de credenciais EAP \_**](/previous-versions/windows/desktop/legacy/bb530539(v=vs.85))
</dt> <dt>

[**\_dados de \_ interface do usuário interativa EAP \_**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_interactive_ui_data)
</dt> <dt>

[SSO e PLAP](understanding-sso-and-plap.md)
</dt> </dl>

 

