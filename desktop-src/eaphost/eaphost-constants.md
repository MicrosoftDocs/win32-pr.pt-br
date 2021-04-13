---
title: Constantes do EAPHost (Eaptypes. h)
description: Exiba uma lista de constantes do EAPHost (Eaptypes. h) usadas pelos métodos do EAPHost e veja os requisitos para seu uso.
ms.assetid: 56338B98-06E3-4CD3-B1CA-F8F45AA39566
topic_type:
- apiref
api_name:
- EAP_INTERACTIVE_UI_DATA_VERSION
- EAP_CREDENTIAL_VERSION
- EAPHOST_PEER_API_VERSION
- CERTIFICATE_HASH_LENGTH
- MAX_EAP_CONFIG_INPUT_FIELD_LENGTH
- MAX_EAP_CONFIG_INPUT_FIELD_VALUE_LENGTH
- EAP_UI_INPUT_FIELD_PROPS_DEFAULT
- EAP_CONFIG_INPUT_FIELD_PROPS_DEFAULT
- EAP_UI_INPUT_FIELD_PROPS_NON_DISPLAYABLE
- EAP_CONFIG_INPUT_FIELD_PROPS_NON_DISPLAYABLE
- EAP_UI_INPUT_FIELD_PROPS_NON_PERSIST
- EAP_UI_INPUT_FIELD_PROPS_READ_ONLY
api_location:
- eaptypes.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 84704e59ed43466c47435f4804cb4dedc9c3a92d
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104366697"
---
# <a name="eaphost-constants"></a>Constantes do EAPHost

As constantes usadas pelos métodos EAPHost.

<dl> <dt>

<span id="EAP_INTERACTIVE_UI_DATA_VERSION"></span><span id="eap_interactive_ui_data_version"></span>**\_versão de \_ dados da interface do usuário interativa EAP \_ \_**
</dt> <dd> <dl> <dt>

0
</dt> <dt>



A versão dos dados de interface do usuário interativa do EAP.


</dt> </dl> </dd> <dt>

<span id="EAP_CREDENTIAL_VERSION"></span><span id="eap_credential_version"></span>**\_versão da credencial EAP \_**
</dt> <dd> <dl> <dt>

1
</dt> <dt>



A versão das credenciais EAP fornecidas pelo usuário.


</dt> </dl> </dd> <dt>

<span id="EAPHOST_PEER_API_VERSION"></span><span id="eaphost_peer_api_version"></span>**\_versão da API de mesmo nível do EAPHost \_ \_**
</dt> <dd> <dl> <dt>

1
</dt> <dt>



A versão da API de mesmo nível do EAPHost.


</dt> </dl> </dd> <dt>

<span id="CERTIFICATE_HASH_LENGTH"></span><span id="certificate_hash_length"></span>**\_comprimento do hash do certificado \_**
</dt> <dd> <dl> <dt>

20
</dt> <dt>



Comprimento do hash SHA1 do certificado.


</dt> </dl> </dd> <dt>

<span id="MAX_EAP_CONFIG_INPUT_FIELD_LENGTH"></span><span id="max_eap_config_input_field_length"></span>**comprimento máximo do \_ \_ campo de entrada de configuração EAP \_ \_ \_**
</dt> <dd> <dl> <dt>

256
</dt> <dt>



Especifica o comprimento máximo com suporte de um campo de entrada.


</dt> </dl> </dd> <dt>

<span id="MAX_EAP_CONFIG_INPUT_FIELD_VALUE_LENGTH"></span><span id="max_eap_config_input_field_value_length"></span>**comprimento máximo do \_ valor do campo de \_ entrada de configuração EAP \_ \_ \_ \_**
</dt> <dd> <dl> <dt>

1024
</dt> <dt>



Especifica o comprimento máximo com suporte de um campo de entrada.


</dt> </dl> </dd> <dt>

<span id="EAP_UI_INPUT_FIELD_PROPS_DEFAULT"></span><span id="eap_ui_input_field_props_default"></span>**\_padrão de \_ Propriedades do campo de entrada da interface do usuário do EAP \_ \_ \_**
</dt> <dd> <dl> <dt>

0X00000000 
</dt> <dt>



Windows Vista com SP1 ou posterior: representa o valor da propriedade padrão para entradas de campo de entrada exibidas na interface do usuário.


</dt> </dl> </dd> <dt>

<span id="EAP_CONFIG_INPUT_FIELD_PROPS_DEFAULT"></span><span id="eap_config_input_field_props_default"></span>**\_padrão de \_ Propriedades do campo de entrada de configuração EAP \_ \_ \_**
</dt> <dd> <dl> <dt>

0X00000000 
</dt> <dt>



Representa o valor da propriedade padrão para entradas de campo de entrada de configuração exibidas na interface do usuário.


</dt> </dl> </dd> <dt>

<span id="EAP_UI_INPUT_FIELD_PROPS_NON_DISPLAYABLE"></span><span id="eap_ui_input_field_props_non_displayable"></span>**\_Propriedades do campo de entrada da interface do usuário EAP \_ \_ \_ \_ não \_ exibíveis**
</dt> <dd> <dl> <dt>

0X00000001 
</dt> <dt>



Windows Vista com SP1 ou posterior: Especifica que as entradas de campo de entrada não serão exibidas na interface do usuário (uma senha ou número de PIN, por exemplo).


</dt> </dl> </dd> <dt>

<span id="EAP_CONFIG_INPUT_FIELD_PROPS_NON_DISPLAYABLE"></span><span id="eap_config_input_field_props_non_displayable"></span>**\_Propriedades do campo de entrada de configuração EAP \_ \_ \_ \_ não \_ exibíveis**
</dt> <dd> <dl> <dt>

0X00000001 
</dt> <dt>



Especifica que as entradas de campo de entrada de configuração não serão exibidas na interface do usuário (uma senha ou um número PIN, por exemplo).


</dt> </dl> </dd> <dt>

<span id="EAP_UI_INPUT_FIELD_PROPS_NON_PERSIST"></span><span id="eap_ui_input_field_props_non_persist"></span>**\_Propriedades do campo de entrada da interface do usuário EAP \_ \_ \_ \_ não \_ persistentes**
</dt> <dd> <dl> <dt>

0X00000002 
</dt> <dt>



Windows Vista com SP1 ou posterior: indica que o método EAP não armazenará em cache os dados do campo; o suplicante deve armazenar em cache os dados de campo para roaming.


</dt> </dl> </dd> <dt>

<span id="EAP_UI_INPUT_FIELD_PROPS_READ_ONLY"></span><span id="eap_ui_input_field_props_read_only"></span>**\_Propriedades do campo de entrada da interface do usuário do EAP \_ \_ \_ \_ \_ somente leitura**
</dt> <dd> <dl> <dt>

0x00000004
</dt> <dt>



Windows Vista com SP1 ou posterior: indica que o campo de entrada é somente leitura e não pode ser editado.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Função | Versão mínima do sistema operacional com suporte |
|------|------------------------------|
| Cliente<br/> | \[Somente aplicativos de área de trabalho do Windows 8\]<br/> |
| Servidor<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2012\]<br/> |



 

 





