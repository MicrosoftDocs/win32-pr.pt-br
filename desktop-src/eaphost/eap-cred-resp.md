---
title: '\_ \_ Resp de credenciais EAP (Eaptypes. h)'
description: Armazena credenciais de segurança EAP em uma \_ estrutura de matriz de campo de entrada de configuração EAP \_ \_ \_ . | \_ \_ Resp de credenciais EAP (Eaptypes. h)
ms.assetid: 714c75d8-71c7-4c3f-802a-a5e4f6ca65c2
keywords:
- EAP_CRED_RESP
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e5c2176377dbde0f7c02d2a7d8083ad1bcff9e71
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "105771347"
---
# <a name="eap_cred_resp"></a>\_resp de credenciais EAP \_

A **estrutura \_ \_ resp** de credenciais de EAP armazena as credenciais de segurança EAP em uma estrutura de [**matriz de campo de \_ entrada de configuração \_ \_ \_ EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_array) .


```C++
typedef EAP_CONFIG_INPUT_FIELD_ARRAY EAP_CRED_RESP;
```



<dl> <dt>

**\_resp de credenciais EAP \_**
</dt> <dd>

A **estrutura \_ \_ resp de credenciais do EAP** armazena as credenciais de segurança EAP novas e antigas apontadas pelo parâmetro *pbUiData* da estrutura de [**\_ \_ \_ dados da interface do usuário interativa do EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_interactive_ui_data) quando o parâmetro *dwDataType* do [**\_ \_ \_ \_ tipo de dados da interface do usuário interativa do EAP**](/windows/desktop/api/eaptypes/ne-eaptypes-eap_interactive_ui_data_type) especifica um tipo de resposta de credencial.

</dd> </dl>

## <a name="remarks"></a>Comentários

A **estrutura \_ \_ resp de credenciais de EAP** é usada para dar suporte ao SSO (logon único).

A **estrutura \_ \_ resp de credenciais de EAP** é idêntica à estrutura req. de [**\_ credenciais \_ EAP**](eap-cred-req.md) .

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

[**Req. de \_ credenciais EAP \_**](eap-cred-req.md)
</dt> <dt>

[**Req. de \_ expiração de credenciais EAP \_ \_**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_cred_expiry_req)
</dt> <dt>

[**\_resp de \_ expiração de credenciais EAP \_**](/previous-versions/windows/desktop/legacy/bb530539(v=vs.85))
</dt> <dt>

[**\_dados de \_ interface do usuário interativa EAP \_**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_interactive_ui_data)
</dt> <dt>

[SSO e PLAP](understanding-sso-and-plap.md)
</dt> </dl>

 

