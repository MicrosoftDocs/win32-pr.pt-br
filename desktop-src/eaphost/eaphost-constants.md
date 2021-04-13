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
# <a name="eaphost-constants"></a><span data-ttu-id="540d7-103">Constantes do EAPHost</span><span class="sxs-lookup"><span data-stu-id="540d7-103">EAPHost Constants</span></span>

<span data-ttu-id="540d7-104">As constantes usadas pelos métodos EAPHost.</span><span class="sxs-lookup"><span data-stu-id="540d7-104">The constants used by EAPHost methods.</span></span>

<dl> <dt>

<span data-ttu-id="540d7-105"><span id="EAP_INTERACTIVE_UI_DATA_VERSION"></span><span id="eap_interactive_ui_data_version"></span>**\_versão de \_ dados da interface do usuário interativa EAP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="540d7-105"><span id="EAP_INTERACTIVE_UI_DATA_VERSION"></span><span id="eap_interactive_ui_data_version"></span>**EAP\_INTERACTIVE\_UI\_DATA\_VERSION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="540d7-106">0</span><span class="sxs-lookup"><span data-stu-id="540d7-106">0</span></span>
</dt> <dt>



<span data-ttu-id="540d7-107">A versão dos dados de interface do usuário interativa do EAP.</span><span class="sxs-lookup"><span data-stu-id="540d7-107">The version of the EAP interactive UI data.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="540d7-108"><span id="EAP_CREDENTIAL_VERSION"></span><span id="eap_credential_version"></span>**\_versão da credencial EAP \_**</span><span class="sxs-lookup"><span data-stu-id="540d7-108"><span id="EAP_CREDENTIAL_VERSION"></span><span id="eap_credential_version"></span>**EAP\_CREDENTIAL\_VERSION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="540d7-109">1</span><span class="sxs-lookup"><span data-stu-id="540d7-109">1</span></span>
</dt> <dt>



<span data-ttu-id="540d7-110">A versão das credenciais EAP fornecidas pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="540d7-110">The version of the EAP credentials supplied by the user.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="540d7-111"><span id="EAPHOST_PEER_API_VERSION"></span><span id="eaphost_peer_api_version"></span>**\_versão da API de mesmo nível do EAPHost \_ \_**</span><span class="sxs-lookup"><span data-stu-id="540d7-111"><span id="EAPHOST_PEER_API_VERSION"></span><span id="eaphost_peer_api_version"></span>**EAPHOST\_PEER\_API\_VERSION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="540d7-112">1</span><span class="sxs-lookup"><span data-stu-id="540d7-112">1</span></span>
</dt> <dt>



<span data-ttu-id="540d7-113">A versão da API de mesmo nível do EAPHost.</span><span class="sxs-lookup"><span data-stu-id="540d7-113">The version of the EAPHost peer API.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="540d7-114"><span id="CERTIFICATE_HASH_LENGTH"></span><span id="certificate_hash_length"></span>**\_comprimento do hash do certificado \_**</span><span class="sxs-lookup"><span data-stu-id="540d7-114"><span id="CERTIFICATE_HASH_LENGTH"></span><span id="certificate_hash_length"></span>**CERTIFICATE\_HASH\_LENGTH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="540d7-115">20</span><span class="sxs-lookup"><span data-stu-id="540d7-115">20</span></span>
</dt> <dt>



<span data-ttu-id="540d7-116">Comprimento do hash SHA1 do certificado.</span><span class="sxs-lookup"><span data-stu-id="540d7-116">Length of the SHA1 hash of the certificate.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="540d7-117"><span id="MAX_EAP_CONFIG_INPUT_FIELD_LENGTH"></span><span id="max_eap_config_input_field_length"></span>**comprimento máximo do \_ \_ campo de entrada de configuração EAP \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="540d7-117"><span id="MAX_EAP_CONFIG_INPUT_FIELD_LENGTH"></span><span id="max_eap_config_input_field_length"></span>**MAX\_EAP\_CONFIG\_INPUT\_FIELD\_LENGTH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="540d7-118">256</span><span class="sxs-lookup"><span data-stu-id="540d7-118">256</span></span>
</dt> <dt>



<span data-ttu-id="540d7-119">Especifica o comprimento máximo com suporte de um campo de entrada.</span><span class="sxs-lookup"><span data-stu-id="540d7-119">Specifies the maximum supported length of an input field.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="540d7-120"><span id="MAX_EAP_CONFIG_INPUT_FIELD_VALUE_LENGTH"></span><span id="max_eap_config_input_field_value_length"></span>**comprimento máximo do \_ valor do campo de \_ entrada de configuração EAP \_ \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="540d7-120"><span id="MAX_EAP_CONFIG_INPUT_FIELD_VALUE_LENGTH"></span><span id="max_eap_config_input_field_value_length"></span>**MAX\_EAP\_CONFIG\_INPUT\_FIELD\_VALUE\_LENGTH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="540d7-121">1024</span><span class="sxs-lookup"><span data-stu-id="540d7-121">1024</span></span>
</dt> <dt>



<span data-ttu-id="540d7-122">Especifica o comprimento máximo com suporte de um campo de entrada.</span><span class="sxs-lookup"><span data-stu-id="540d7-122">Specifies the maximum supported length of an input field.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="540d7-123"><span id="EAP_UI_INPUT_FIELD_PROPS_DEFAULT"></span><span id="eap_ui_input_field_props_default"></span>**\_padrão de \_ Propriedades do campo de entrada da interface do usuário do EAP \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="540d7-123"><span id="EAP_UI_INPUT_FIELD_PROPS_DEFAULT"></span><span id="eap_ui_input_field_props_default"></span>**EAP\_UI\_INPUT\_FIELD\_PROPS\_DEFAULT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="540d7-124">0X00000000</span><span class="sxs-lookup"><span data-stu-id="540d7-124">0X00000000</span></span> 
</dt> <dt>



<span data-ttu-id="540d7-125">Windows Vista com SP1 ou posterior: representa o valor da propriedade padrão para entradas de campo de entrada exibidas na interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="540d7-125">Windows Vista with SP1 or later: Represents the default property value for input field entries displayed in the UI.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="540d7-126"><span id="EAP_CONFIG_INPUT_FIELD_PROPS_DEFAULT"></span><span id="eap_config_input_field_props_default"></span>**\_padrão de \_ Propriedades do campo de entrada de configuração EAP \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="540d7-126"><span id="EAP_CONFIG_INPUT_FIELD_PROPS_DEFAULT"></span><span id="eap_config_input_field_props_default"></span>**EAP\_CONFIG\_INPUT\_FIELD\_PROPS\_DEFAULT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="540d7-127">0X00000000</span><span class="sxs-lookup"><span data-stu-id="540d7-127">0X00000000</span></span> 
</dt> <dt>



<span data-ttu-id="540d7-128">Representa o valor da propriedade padrão para entradas de campo de entrada de configuração exibidas na interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="540d7-128">Represents the default property value for configuration input field entries displayed in the UI.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="540d7-129"><span id="EAP_UI_INPUT_FIELD_PROPS_NON_DISPLAYABLE"></span><span id="eap_ui_input_field_props_non_displayable"></span>**\_Propriedades do campo de entrada da interface do usuário EAP \_ \_ \_ \_ não \_ exibíveis**</span><span class="sxs-lookup"><span data-stu-id="540d7-129"><span id="EAP_UI_INPUT_FIELD_PROPS_NON_DISPLAYABLE"></span><span id="eap_ui_input_field_props_non_displayable"></span>**EAP\_UI\_INPUT\_FIELD\_PROPS\_NON\_DISPLAYABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="540d7-130">0X00000001</span><span class="sxs-lookup"><span data-stu-id="540d7-130">0X00000001</span></span> 
</dt> <dt>



<span data-ttu-id="540d7-131">Windows Vista com SP1 ou posterior: Especifica que as entradas de campo de entrada não serão exibidas na interface do usuário (uma senha ou número de PIN, por exemplo).</span><span class="sxs-lookup"><span data-stu-id="540d7-131">Windows Vista with SP1 or later: Specifies that input field entries will not be displayed in the UI (a password or PIN number, for example).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="540d7-132"><span id="EAP_CONFIG_INPUT_FIELD_PROPS_NON_DISPLAYABLE"></span><span id="eap_config_input_field_props_non_displayable"></span>**\_Propriedades do campo de entrada de configuração EAP \_ \_ \_ \_ não \_ exibíveis**</span><span class="sxs-lookup"><span data-stu-id="540d7-132"><span id="EAP_CONFIG_INPUT_FIELD_PROPS_NON_DISPLAYABLE"></span><span id="eap_config_input_field_props_non_displayable"></span>**EAP\_CONFIG\_INPUT\_FIELD\_PROPS\_NON\_DISPLAYABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="540d7-133">0X00000001</span><span class="sxs-lookup"><span data-stu-id="540d7-133">0X00000001</span></span> 
</dt> <dt>



<span data-ttu-id="540d7-134">Especifica que as entradas de campo de entrada de configuração não serão exibidas na interface do usuário (uma senha ou um número PIN, por exemplo).</span><span class="sxs-lookup"><span data-stu-id="540d7-134">Specifies that configuration input field entries will not be displayed in the UI (a password or PIN number, for example).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="540d7-135"><span id="EAP_UI_INPUT_FIELD_PROPS_NON_PERSIST"></span><span id="eap_ui_input_field_props_non_persist"></span>**\_Propriedades do campo de entrada da interface do usuário EAP \_ \_ \_ \_ não \_ persistentes**</span><span class="sxs-lookup"><span data-stu-id="540d7-135"><span id="EAP_UI_INPUT_FIELD_PROPS_NON_PERSIST"></span><span id="eap_ui_input_field_props_non_persist"></span>**EAP\_UI\_INPUT\_FIELD\_PROPS\_NON\_PERSIST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="540d7-136">0X00000002</span><span class="sxs-lookup"><span data-stu-id="540d7-136">0X00000002</span></span> 
</dt> <dt>



<span data-ttu-id="540d7-137">Windows Vista com SP1 ou posterior: indica que o método EAP não armazenará em cache os dados do campo; o suplicante deve armazenar em cache os dados de campo para roaming.</span><span class="sxs-lookup"><span data-stu-id="540d7-137">Windows Vista with SP1 or later: Indicates that the EAP method will not cache the field data; the supplicant must cache the field data for roaming.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="540d7-138"><span id="EAP_UI_INPUT_FIELD_PROPS_READ_ONLY"></span><span id="eap_ui_input_field_props_read_only"></span>**\_Propriedades do campo de entrada da interface do usuário do EAP \_ \_ \_ \_ \_ somente leitura**</span><span class="sxs-lookup"><span data-stu-id="540d7-138"><span id="EAP_UI_INPUT_FIELD_PROPS_READ_ONLY"></span><span id="eap_ui_input_field_props_read_only"></span>**EAP\_UI\_INPUT\_FIELD\_PROPS\_READ\_ONLY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="540d7-139">0x00000004</span><span class="sxs-lookup"><span data-stu-id="540d7-139">0x00000004</span></span>
</dt> <dt>



<span data-ttu-id="540d7-140">Windows Vista com SP1 ou posterior: indica que o campo de entrada é somente leitura e não pode ser editado.</span><span class="sxs-lookup"><span data-stu-id="540d7-140">Windows Vista with SP1 or later: Indicates that the input field is read-only and cannot be edited.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="540d7-141">Requisitos</span><span class="sxs-lookup"><span data-stu-id="540d7-141">Requirements</span></span>



| <span data-ttu-id="540d7-142">Função</span><span class="sxs-lookup"><span data-stu-id="540d7-142">Role</span></span> | <span data-ttu-id="540d7-143">Versão mínima do sistema operacional com suporte</span><span class="sxs-lookup"><span data-stu-id="540d7-143">Minimum supported OS version</span></span> |
|------|------------------------------|
| <span data-ttu-id="540d7-144">Cliente</span><span class="sxs-lookup"><span data-stu-id="540d7-144">Client</span></span><br/> | <span data-ttu-id="540d7-145">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="540d7-145">Windows 8 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="540d7-146">Servidor</span><span class="sxs-lookup"><span data-stu-id="540d7-146">Server</span></span><br/> | <span data-ttu-id="540d7-147">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="540d7-147">Windows Server 2012 \[desktop apps only\]</span></span><br/> |



 

 





