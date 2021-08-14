---
title: '\_ \_ \_ Req de logon de credenciais EAP (Eaptypes. h)'
description: Armazena credenciais de segurança EAP em uma \_ estrutura de matriz de campo de entrada de configuração EAP \_ \_ \_ .
ms.assetid: 1F1A2F77-054D-4FD2-83A5-69C3D77418B3
keywords:
- EAP_CRED_LOGON_REQ
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 719abbed6c16deb6d3bfd61811f3f24253181364fe89f5823ee682bafef001e5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118785619"
---
# <a name="eap_cred_logon_req"></a>Req. de \_ logon de credenciais EAP \_ \_

A estrutura do **\_ \_ \_ req logon** de credenciais EAP armazena as credenciais de segurança EAP em uma estrutura de matriz de campo de entrada de [**\_ configuração \_ \_ \_ EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_array) .


```C++
typedef EAP_CONFIG_INPUT_FIELD_ARRAY EAP_CRED_LOGON_REQ;
```



<dl> <dt>

**Req. de \_ logon de credenciais EAP \_ \_**
</dt> <dd>

A **estrutura \_ \_ \_ req logon** de credenciais EAP armazena as credenciais de segurança EAP apontadas pelo parâmetro *pbUiData* da estrutura de [**\_ \_ \_ dados da interface do usuário interativa do EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_interactive_ui_data) quando o parâmetro *dwDataType* do tipo de [**\_ \_ \_ dados \_ de interface do usuário interativo do EAP**](/windows/desktop/api/eaptypes/ne-eaptypes-eap_interactive_ui_data_type) especifica um tipo de solicitação de credencial. Os campos de entrada nessa estrutura são os mesmos que os campos de entrada retornados por [**EapHostPeerQueryCredentialInputFields**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerquerycredentialinputfields). **EAP \_ O \_ \_ req logon de credenciais** é usado na solicitação de credenciais inicial e o [**\_ \_ req de credenciais EAP**](eap-cred-req.md) é usado na solicitação de repetição de credencial durante uma autenticação.

</dd> </dl>

## <a name="remarks"></a>Comentários

A **estrutura \_ \_ \_ req logon de credenciais EAP** é usada para dar suporte ao SSO (logon único).

A **estrutura \_ \_ \_ req logon de credenciais EAP** é idêntica à estrutura [**\_ \_ \_ resp de logon de credenciais EAP**](eap-cred-logon-resp.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do Server 2008 R2\]<br/>                               |
| parâmetro<br/>                   | <dl> <dt>Eaptypes. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_matriz de \_ campo de entrada de configuração EAP \_ \_**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_array)
</dt> <dt>

[**Req. de \_ credenciais EAP \_**](eap-cred-req.md)
</dt> <dt>

[**\_dados de \_ interface do usuário interativa EAP \_**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_interactive_ui_data)
</dt> <dt>

[**\_tipo de \_ dados de interface do usuário interativa EAP \_ \_**](/windows/desktop/api/eaptypes/ne-eaptypes-eap_interactive_ui_data_type)
</dt> <dt>

[**EapHostPeerQueryCredentialInputFields**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerquerycredentialinputfields)
</dt> </dl>

 

 





