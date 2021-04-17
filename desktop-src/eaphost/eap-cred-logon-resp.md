---
title: '\_ \_ \_ Resp de logon de credenciais EAP (Eaptypes. h)'
description: Armazena credenciais de segurança EAP em uma \_ estrutura de matriz de campo de entrada de configuração EAP \_ \_ \_ . | \_ \_ \_ Resp de logon de credenciais EAP (Eaptypes. h)
ms.assetid: 1244A40F-6999-4053-97C4-1C4FB107B2F5
keywords:
- EAP_CRED_LOGON_RESP
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0e1bbabc30918efaed0e286b5df231537ed5543
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "105763450"
---
# <a name="eap_cred_logon_resp"></a>\_resp de \_ logon de credenciais EAP \_

A **estrutura \_ \_ \_ resp de logon de credenciais EAP** armazena as credenciais de segurança EAP em uma estrutura de [**\_ \_ \_ \_ matriz de campo de entrada de configuração EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_array) .


```C++
typedef EAP_CONFIG_INPUT_FIELD_ARRAY EAP_CRED_LOGON_RESP;
```



<dl> <dt>

**\_resp de \_ logon de credenciais EAP \_**
</dt> <dd>

A **estrutura \_ \_ \_ resp de logon de credenciais do EAP** armazena as credenciais de segurança EAP apontadas pelo parâmetro *pbUiData* da estrutura de [**\_ \_ \_ dados da interface do usuário interativa EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_interactive_ui_data) quando o parâmetro *dwDataType* do [**tipo de \_ \_ \_ dados \_ da interface do usuário interativa do EAP**](/windows/desktop/api/eaptypes/ne-eaptypes-eap_interactive_ui_data_type) especifica um tipo de solicitação de credencial. Os campos de entrada nessa estrutura serão os mesmos dos campos de entrada retornados por [**EapHostPeerQueryCredentialInputFields**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerquerycredentialinputfields). **EAP \_ O \_ logon \_ de credenciais resp** é usado na solicitação de credencial inicial e o [**\_ \_ resp de credenciais de EAP**](eap-cred-resp.md) é usado na solicitação de repetição de credencial durante uma autenticação.

</dd> </dl>

## <a name="remarks"></a>Comentários

A **estrutura \_ \_ \_ resp de logon de credenciais EAP** é usada para dar suporte ao SSO (logon único).

A estrutura de **\_ resp de \_ logon \_ de credenciais EAP** é idêntica à estrutura [**\_ \_ \_ req logon de credenciais EAP**](eap-cred-logon-req.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]<br/>                               |
| parâmetro<br/>                   | <dl> <dt>Eaptypes. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**EapHostPeerQueryCredentialInputFields**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerquerycredentialinputfields)
</dt> <dt>

[**\_matriz de \_ campo de entrada de configuração EAP \_ \_**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_array)
</dt> <dt>

[**Req. de \_ logon de credenciais EAP \_ \_**](eap-cred-logon-req.md)
</dt> <dt>

[**\_dados de \_ interface do usuário interativa EAP \_**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_interactive_ui_data)
</dt> <dt>

[**\_tipo de \_ dados de interface do usuário interativa EAP \_ \_**](/windows/desktop/api/eaptypes/ne-eaptypes-eap_interactive_ui_data_type)
</dt> </dl>

 

 





