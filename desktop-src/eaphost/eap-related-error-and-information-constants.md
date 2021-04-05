---
title: Constantes de erro e informações relacionadas a EAP (Eaphosterror. h)
description: Grupos individuais de erros e constantes de informações relacionadas a EAP comuns a todas as tecnologias de API do EAPHost.
ms.assetid: 081b7a72-abe3-4cbb-9b6c-07bb6717fbfe
topic_type:
- apiref
api_name:
- EAP_E_EAPHOST_FIRST
- EAP_E_EAPHOST_LAST
- EAP_I_EAPHOST_FIRST
- EAP_I_EAPHOST_LAST
- EAP_E_CERT_STORE_INACCESSIBLE
- EAP_E_EAPHOST_METHOD_NOT_INSTALLED
- EAP_E_EAPHOST_THIRDPARTY_METHOD_HOST_RESET
- EAP_E_EAPHOST_EAPQEC_INACCESSIBLE
- EAP_E_EAPHOST_IDENTITY_UNKNOWN
- EAP_E_AUTHENTICATION_FAILED
- EAP_I_EAPHOST_EAP_NEGOTIATION_FAILED
- EAP_E_EAPHOST_METHOD_INVALID_PACKET
- EAP_E_EAPHOST_REMOTE_INVALID_PACKET
- EAP_E_EAPHOST_XML_MALFORMED
- EAP_E_METHOD_CONFIG_DOES_NOT_SUPPORT_SSO
- EAP_E_EAPHOST_METHOD_OPERATION_NOT_SUPPORTED
- EAP_E_USER_FIRST
- EAP_E_USER_LAST
- EAP_I_USER_FIRST
- EAP_I_USER_LAST
- EAP_E_USER_CERT_NOT_FOUND
- EAP_E_USER_CERT_INVALID
- EAP_E_USER_CERT_EXPIRED
- EAP_E_USER_CERT_REVOKED
- EAP_E_USER_CERT_OTHER_ERROR
- EAP_E_USER_CERT_REJECTED
- EAP_I_USER_ACCOUNT_OTHER_ERROR
- EAP_E_USER_CREDENTIALS_REJECTED
- EAP_E_USER_NAME_PASSWORD_REJECTED
- EAP_E_NO_SMART_CARD_READER
- EAP_E_SERVER_FIRST
- EAP_E_SERVER_LAST
- EAP_E_SERVER_CERT_NOT_FOUND
- EAP_E_SERVER_CERT_INVALID
- EAP_E_SERVER_CERT_EXPIRED
- EAP_E_SERVER_CERT_REVOKED
- EAP_E_SERVER_CERT_OTHER_ERROR
- EAP_E_USER_ROOT_CERT_FIRST
- EAP_E_USER_ROOT_CERT_LAST
- EAP_E_USER_ROOT_CERT_NOT_FOUND
- EAP_E_USER_ROOT_CERT_INVALID
- EAP_E_USER_ROOT_CERT_EXPIRED
- EAP_E_SERVER_ROOT_CERT_FIRST
- EAP_E_SERVER_ROOT_CERT_LAST
- EAP_E_SERVER_ROOT_CERT_NOT_FOUND
- EAP_E_SERVER_ROOT_CERT_INVALID
- EAP_E_SERVER_ROOT_CERT_NAME_REQUIRED
api_location:
- eaphosterror.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8bd7b829cd4c5ba550fd88242ffb8c34572648d9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009458"
---
# <a name="eap-related-error-and-information-constants"></a><span data-ttu-id="45543-103">Constantes de erro e informações relacionadas a EAP</span><span class="sxs-lookup"><span data-stu-id="45543-103">EAP Related Error and Information Constants</span></span>

<span data-ttu-id="45543-104">Grupos individuais de erros e constantes de informações relacionadas a EAP comuns a todas as tecnologias de API do EAPHost.</span><span class="sxs-lookup"><span data-stu-id="45543-104">Individual groups of EAP related error and information constants common to all EAPHost API technologies.</span></span>

<dl> <dt>

<span data-ttu-id="45543-105"><span id="EAP_E_EAPHOST_FIRST"></span><span id="eap_e_eaphost_first"></span>**EAP \_ E \_ EAPHost \_ primeiro**</span><span class="sxs-lookup"><span data-stu-id="45543-105"><span id="EAP_E_EAPHOST_FIRST"></span><span id="eap_e_eaphost_first"></span>**EAP\_E\_EAPHOST\_FIRST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45543-106">0x80420000L</span><span class="sxs-lookup"><span data-stu-id="45543-106">0x80420000L</span></span>
</dt> <dt>



<span data-ttu-id="45543-107">Define o limite dos relatórios de erros; qualquer erro relacionado ao EAPHost ocorrerá entre o **EAP \_ e o \_ EAPHost \_ primeiro** e o **EAP \_ e o \_ EAPHost \_ por último**.</span><span class="sxs-lookup"><span data-stu-id="45543-107">Defines the boundary of error reports; any EAPHost related error will occur between **EAP\_E\_EAPHOST\_FIRST** and **EAP\_E\_EAPHOST\_LAST**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="45543-108"><span id="EAP_E_EAPHOST_LAST___"></span><span id="eap_e_eaphost_last___"></span>**EAP \_ E \_ EAPHost \_ por último**</span><span class="sxs-lookup"><span data-stu-id="45543-108"><span id="EAP_E_EAPHOST_LAST___"></span><span id="eap_e_eaphost_last___"></span>**EAP\_E\_EAPHOST\_LAST**</span></span> 
</dt> <dd> <dl> <dt>

<span data-ttu-id="45543-109">0x804200FFL</span><span class="sxs-lookup"><span data-stu-id="45543-109">0x804200FFL</span></span>
</dt> <dt>



<span data-ttu-id="45543-110">Define o limite dos relatórios de erros; qualquer erro relacionado ao EAPHost ocorrerá entre o **EAP \_ e o \_ EAPHost \_ primeiro** e o **EAP \_ e o \_ EAPHost \_ por último**.</span><span class="sxs-lookup"><span data-stu-id="45543-110">Defines the boundary of error reports; any EAPHost related error will occur between **EAP\_E\_EAPHOST\_FIRST** and **EAP\_E\_EAPHOST\_LAST**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="45543-111"><span id="EAP_I_EAPHOST_FIRST_"></span><span id="eap_i_eaphost_first_"></span>**EAP \_ I \_ EAPHost \_ primeiro**</span><span class="sxs-lookup"><span data-stu-id="45543-111"><span id="EAP_I_EAPHOST_FIRST_"></span><span id="eap_i_eaphost_first_"></span>**EAP\_I\_EAPHOST\_FIRST**</span></span> 
</dt> <dd> <dl> <dt>

<span data-ttu-id="45543-112">0x80420000L</span><span class="sxs-lookup"><span data-stu-id="45543-112">0x80420000L</span></span>
</dt> <dt>



<span data-ttu-id="45543-113">Define o limite de relatórios de informações; qualquer log de eventos informativo relacionado ao EAPHost ocorrerá entre o **EAP \_ i \_ EAPHost \_ primeiro** e o **EAP \_ i \_ EAPHost \_ por último**.</span><span class="sxs-lookup"><span data-stu-id="45543-113">Defines the boundary of information reports; any EAPHost related informational event logging will occur between **EAP\_I\_EAPHOST\_FIRST** and **EAP\_I\_EAPHOST\_LAST**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="45543-114"><span id="EAP_I_EAPHOST_LAST"></span><span id="eap_i_eaphost_last"></span>**EAP \_ I \_ EAPHost \_ por último**</span><span class="sxs-lookup"><span data-stu-id="45543-114"><span id="EAP_I_EAPHOST_LAST"></span><span id="eap_i_eaphost_last"></span>**EAP\_I\_EAPHOST\_LAST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45543-115">0x804200FFL</span><span class="sxs-lookup"><span data-stu-id="45543-115">0x804200FFL</span></span>
</dt> <dt>



<span data-ttu-id="45543-116">Define o limite de relatórios de informações; qualquer log de eventos informativo relacionado ao EAPHost ocorrerá entre o **EAP \_ i \_ EAPHost \_ primeiro** e o **EAP \_ i \_ EAPHost \_ por último**.</span><span class="sxs-lookup"><span data-stu-id="45543-116">Defines the boundary of information reports; any EAPHost related informational event logging will occur between **EAP\_I\_EAPHOST\_FIRST** and **EAP\_I\_EAPHOST\_LAST**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="45543-117"><span id="EAP_E_CERT_STORE_INACCESSIBLE"></span><span id="eap_e_cert_store_inaccessible"></span>**\_repositório de certificados EAP E \_ \_ \_ inacessível**</span><span class="sxs-lookup"><span data-stu-id="45543-117"><span id="EAP_E_CERT_STORE_INACCESSIBLE"></span><span id="eap_e_cert_store_inaccessible"></span>**EAP\_E\_CERT\_STORE\_INACCESSIBLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45543-118">0x80420011</span><span class="sxs-lookup"><span data-stu-id="45543-118">0x80420011</span></span>
</dt> <dt>



<span data-ttu-id="45543-119">Nem o autenticador ou o ponto pode acessar o repositório de certificados.</span><span class="sxs-lookup"><span data-stu-id="45543-119">Neither the authenticator or peer can access the certificate store.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="45543-120"><span id="EAP_E_EAPHOST_METHOD_NOT_INSTALLED"></span><span id="eap_e_eaphost_method_not_installed"></span>**\_método EAP \_ E \_ EAPHost \_ não \_ instalado**</span><span class="sxs-lookup"><span data-stu-id="45543-120"><span id="EAP_E_EAPHOST_METHOD_NOT_INSTALLED"></span><span id="eap_e_eaphost_method_not_installed"></span>**EAP\_E\_EAPHOST\_METHOD\_NOT\_INSTALLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45543-121">0x80420011</span><span class="sxs-lookup"><span data-stu-id="45543-121">0x80420011</span></span>
</dt> <dt>



<span data-ttu-id="45543-122">O método EAP solicitado não está instalado.</span><span class="sxs-lookup"><span data-stu-id="45543-122">The requested EAP method is not installed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="45543-123"><span id="EAP_E_EAPHOST_THIRDPARTY_METHOD_HOST_RESET"></span><span id="eap_e_eaphost_thirdparty_method_host_reset"></span>**redefinição do \_ host do método EAP E \_ EAPHost \_ THIRDPARTY \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="45543-123"><span id="EAP_E_EAPHOST_THIRDPARTY_METHOD_HOST_RESET"></span><span id="eap_e_eaphost_thirdparty_method_host_reset"></span>**EAP\_E\_EAPHOST\_THIRDPARTY\_METHOD\_HOST\_RESET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45543-124">0x80420012</span><span class="sxs-lookup"><span data-stu-id="45543-124">0x80420012</span></span>
</dt> <dt>



<span data-ttu-id="45543-125">O host do método de terceiros não está respondendo e foi reiniciado automaticamente.</span><span class="sxs-lookup"><span data-stu-id="45543-125">The host of the third party method is not responding and was restarted automatically.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="45543-126"><span id="EAP_E_EAPHOST_EAPQEC_INACCESSIBLE"></span><span id="eap_e_eaphost_eapqec_inaccessible"></span>**EAP \_ E \_ EAPHost \_ EAPQEC \_ inacessíveis**</span><span class="sxs-lookup"><span data-stu-id="45543-126"><span id="EAP_E_EAPHOST_EAPQEC_INACCESSIBLE"></span><span id="eap_e_eaphost_eapqec_inaccessible"></span>**EAP\_E\_EAPHOST\_EAPQEC\_INACCESSIBLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45543-127">0x80420013</span><span class="sxs-lookup"><span data-stu-id="45543-127">0x80420013</span></span>
</dt> <dt>



<span data-ttu-id="45543-128">O EAPHost não é capaz de se comunicar com o [cliente de imposição de quarentena](/windows/desktop/NAP/nap-client-architecture) EAP (QEC) em um cliente habilitado para NAP ( [proteção de acesso à rede](/windows/desktop/NAP/network-access-protection-start-page) ).</span><span class="sxs-lookup"><span data-stu-id="45543-128">EAPHost not able to communicate with EAP [quarantine enforcement client](/windows/desktop/NAP/nap-client-architecture) (QEC) on a [Network Access Protection](/windows/desktop/NAP/network-access-protection-start-page) (NAP) enabled client.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="45543-129"><span id="EAP_E_EAPHOST_IDENTITY_UNKNOWN"></span><span id="eap_e_eaphost_identity_unknown"></span>**\_ \_ \_ identidade desconhecida de EAP E EAPHost \_**</span><span class="sxs-lookup"><span data-stu-id="45543-129"><span id="EAP_E_EAPHOST_IDENTITY_UNKNOWN"></span><span id="eap_e_eaphost_identity_unknown"></span>**EAP\_E\_EAPHOST\_IDENTITY\_UNKNOWN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45543-130">0x80420014</span><span class="sxs-lookup"><span data-stu-id="45543-130">0x80420014</span></span>
</dt> <dt>



<span data-ttu-id="45543-131">O EAPHost retornará esse erro se o autenticador falhar na autenticação após o envio da identidade do par.</span><span class="sxs-lookup"><span data-stu-id="45543-131">EAPHost returns this error if the authenticator fails the authentication after the peer identity was submitted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="45543-132"><span id="EAP_E_AUTHENTICATION_FAILED"></span><span id="eap_e_authentication_failed"></span>**\_ \_ falha na autenticação de EAP E \_**</span><span class="sxs-lookup"><span data-stu-id="45543-132"><span id="EAP_E_AUTHENTICATION_FAILED"></span><span id="eap_e_authentication_failed"></span>**EAP\_E\_AUTHENTICATION\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45543-133">0x80420015</span><span class="sxs-lookup"><span data-stu-id="45543-133">0x80420015</span></span> 
</dt> <dt>



<span data-ttu-id="45543-134">O EAPHost retorna esse erro em caso de falha de autenticação.</span><span class="sxs-lookup"><span data-stu-id="45543-134">EAPHost returns this error on authentication failure.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="45543-135"><span id="EAP_I_EAPHOST_EAP_NEGOTIATION_FAILED"></span><span id="eap_i_eaphost_eap_negotiation_failed"></span>**\_ \_ \_ \_ \_ falha na negociação EAP de EAP-EAPHost**</span><span class="sxs-lookup"><span data-stu-id="45543-135"><span id="EAP_I_EAPHOST_EAP_NEGOTIATION_FAILED"></span><span id="eap_i_eaphost_eap_negotiation_failed"></span>**EAP\_I\_EAPHOST\_EAP\_NEGOTIATION\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45543-136">0x40420016</span><span class="sxs-lookup"><span data-stu-id="45543-136">0x40420016</span></span>
</dt> <dt>



<span data-ttu-id="45543-137">O EAPHost registra esse evento de informações quando o cliente e o servidor não estão configurados com tipos EAP compatíveis.</span><span class="sxs-lookup"><span data-stu-id="45543-137">EAPHost logs this information event when the client and server aren't configured with compatible EAP types.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="45543-138"><span id="EAP_E_EAPHOST_METHOD_INVALID_PACKET"></span><span id="eap_e_eaphost_method_invalid_packet"></span>**\_pacote de método EAP E \_ EAPHost \_ \_ inválido \_**</span><span class="sxs-lookup"><span data-stu-id="45543-138"><span id="EAP_E_EAPHOST_METHOD_INVALID_PACKET"></span><span id="eap_e_eaphost_method_invalid_packet"></span>**EAP\_E\_EAPHOST\_METHOD\_INVALID\_PACKET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45543-139">0x80420017</span><span class="sxs-lookup"><span data-stu-id="45543-139">0x80420017</span></span>
</dt> <dt>



<span data-ttu-id="45543-140">Um método EAP recebeu um pacote EAP que não pode ser processado.</span><span class="sxs-lookup"><span data-stu-id="45543-140">An EAP method received an EAP packet that cannot be processed.</span></span> <span data-ttu-id="45543-141">Outro nome para **o \_ método EAP E \_ EAPHost \_ \_ \_ pacote inválido** é **\_ pacote de método EAP \_ inválido \_**.</span><span class="sxs-lookup"><span data-stu-id="45543-141">Another name for **EAP\_E\_EAPHOST\_METHOD\_INVALID\_PACKET** is **EAP\_METHOD\_INVALID\_PACKET**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="45543-142"><span id="EAP_E_EAPHOST_REMOTE_INVALID_PACKET"></span><span id="eap_e_eaphost_remote_invalid_packet"></span>**\_pacote inválido de EAP E \_ EAPHost \_ remoto \_ \_**</span><span class="sxs-lookup"><span data-stu-id="45543-142"><span id="EAP_E_EAPHOST_REMOTE_INVALID_PACKET"></span><span id="eap_e_eaphost_remote_invalid_packet"></span>**EAP\_E\_EAPHOST\_REMOTE\_INVALID\_PACKET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45543-143">0x80420018</span><span class="sxs-lookup"><span data-stu-id="45543-143">0x80420018</span></span>
</dt> <dt>



<span data-ttu-id="45543-144">O EAPHost recebeu um pacote que não pode ser processado.</span><span class="sxs-lookup"><span data-stu-id="45543-144">EAPHost received a packet that cannot be processed.</span></span> <span data-ttu-id="45543-145">Outro nome para **EAP \_ E \_ EAPHost \_ remoto \_ \_** é um pacote inválido de **EAP \_ \_**.</span><span class="sxs-lookup"><span data-stu-id="45543-145">Another name for **EAP\_E\_EAPHOST\_REMOTE\_INVALID\_PACKET** is **EAP\_INVALID\_PACKET**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="45543-146"><span id="EAP_E_EAPHOST_XML_MALFORMED_"></span><span id="eap_e_eaphost_xml_malformed_"></span>**XML do EAP \_ E \_ EAPHost \_ \_ malformado**</span><span class="sxs-lookup"><span data-stu-id="45543-146"><span id="EAP_E_EAPHOST_XML_MALFORMED_"></span><span id="eap_e_eaphost_xml_malformed_"></span>**EAP\_E\_EAPHOST\_XML\_MALFORMED**</span></span> 
</dt> <dd> <dl> <dt>

<span data-ttu-id="45543-147">0x80420019</span><span class="sxs-lookup"><span data-stu-id="45543-147">0x80420019</span></span>
</dt> <dt>



<span data-ttu-id="45543-148">Falha na validação do esquema de configuração EAPHost.</span><span class="sxs-lookup"><span data-stu-id="45543-148">The EAPHost configuration schema validation failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="45543-149"><span id="EAP_E_METHOD_CONFIG_DOES_NOT_SUPPORT_SSO"></span><span id="eap_e_method_config_does_not_support_sso"></span>**a \_ configuração do método EAP E \_ \_ \_ \_ não \_ oferece suporte a \_ SSO**</span><span class="sxs-lookup"><span data-stu-id="45543-149"><span id="EAP_E_METHOD_CONFIG_DOES_NOT_SUPPORT_SSO"></span><span id="eap_e_method_config_does_not_support_sso"></span>**EAP\_E\_METHOD\_CONFIG\_DOES\_NOT\_SUPPORT\_SSO**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45543-150">0x8042001A</span><span class="sxs-lookup"><span data-stu-id="45543-150">0x8042001A</span></span>
</dt> <dt>



<span data-ttu-id="45543-151">Windows 7 ou posterior: o método EAP não oferece suporte ao SSO (logon único) para a configuração fornecida.</span><span class="sxs-lookup"><span data-stu-id="45543-151">Windows 7 or later: The EAP method does not support single sign on (SSO) for the provided configuration.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="45543-152"><span id="EAP_E_EAPHOST_METHOD_OPERATION_NOT_SUPPORTED"></span><span id="eap_e_eaphost_method_operation_not_supported"></span>**\_ \_ \_ \_ \_ não \_ há suporte para a operação do método EAP E EAPHost**</span><span class="sxs-lookup"><span data-stu-id="45543-152"><span id="EAP_E_EAPHOST_METHOD_OPERATION_NOT_SUPPORTED"></span><span id="eap_e_eaphost_method_operation_not_supported"></span>**EAP\_E\_EAPHOST\_METHOD\_OPERATION\_NOT\_SUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45543-153">0x80420020</span><span class="sxs-lookup"><span data-stu-id="45543-153">0x80420020</span></span>
</dt> <dt>



<span data-ttu-id="45543-154">O EAPHost retorna esse erro quando um método EAP configurado não dá suporte a uma operação solicitada (chamada de procedimento).</span><span class="sxs-lookup"><span data-stu-id="45543-154">EAPHost returns this error when a configured EAP method does not support a requested operation (procedure call).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="45543-155"><span id="EAP_E_USER_FIRST"></span><span id="eap_e_user_first"></span>**EAP \_ E \_ usuário \_ primeiro**</span><span class="sxs-lookup"><span data-stu-id="45543-155"><span id="EAP_E_USER_FIRST"></span><span id="eap_e_user_first"></span>**EAP\_E\_USER\_FIRST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45543-156">0x80420100L</span><span class="sxs-lookup"><span data-stu-id="45543-156">0x80420100L</span></span>
</dt> <dt>



<span data-ttu-id="45543-157">Define o limite dos relatórios de erros; qualquer erro relacionado ao usuário ocorrerá entre o EAP e o usuário **\_ \_ \_ primeiro** e o **EAP \_ e o \_ usuário \_ por último**.</span><span class="sxs-lookup"><span data-stu-id="45543-157">Defines the boundary of error reports; any user related error will occur between **EAP\_E\_USER\_FIRST** and **EAP\_E\_USER\_LAST**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="45543-158"><span id="EAP_E_USER_LAST_"></span><span id="eap_e_user_last_"></span>**EAP \_ E \_ usuário \_ último**</span><span class="sxs-lookup"><span data-stu-id="45543-158"><span id="EAP_E_USER_LAST_"></span><span id="eap_e_user_last_"></span>**EAP\_E\_USER\_LAST**</span></span> 
</dt> <dd> <dl> <dt>

<span data-ttu-id="45543-159">0x804201FFL</span><span class="sxs-lookup"><span data-stu-id="45543-159">0x804201FFL</span></span>
</dt> <dt>



<span data-ttu-id="45543-160">Define o limite dos relatórios de erros; qualquer erro relacionado ao usuário ocorrerá entre o EAP e o usuário **\_ \_ \_ primeiro** e o **EAP \_ e o \_ usuário \_ por último**.</span><span class="sxs-lookup"><span data-stu-id="45543-160">Defines the boundary of error reports; any user related error will occur between **EAP\_E\_USER\_FIRST** and **EAP\_E\_USER\_LAST**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="45543-161"><span id="EAP_I_USER_FIRST"></span><span id="eap_i_user_first"></span>**EAP \_ I \_ usuário \_ primeiro**</span><span class="sxs-lookup"><span data-stu-id="45543-161"><span id="EAP_I_USER_FIRST"></span><span id="eap_i_user_first"></span>**EAP\_I\_USER\_FIRST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45543-162">0x40420100L</span><span class="sxs-lookup"><span data-stu-id="45543-162">0x40420100L</span></span>
</dt> <dt>



<span data-ttu-id="45543-163">Define o limite de relatórios de informações; qualquer log de eventos informativo relacionado ao EAP ocorrerá entre o **usuário do EAP \_ i \_ \_ primeiro** e o **EAP \_ i \_ user \_ Last**.</span><span class="sxs-lookup"><span data-stu-id="45543-163">Defines the boundary of information reports; any EAP related informational event logging will occur between **EAP\_I\_USER\_FIRST** and **EAP\_I\_USER\_LAST**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="45543-164"><span id="EAP_I_USER_LAST"></span><span id="eap_i_user_last"></span>**EAP \_ I \_ usuário \_ último**</span><span class="sxs-lookup"><span data-stu-id="45543-164"><span id="EAP_I_USER_LAST"></span><span id="eap_i_user_last"></span>**EAP\_I\_USER\_LAST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45543-165">0x404201FFL</span><span class="sxs-lookup"><span data-stu-id="45543-165">0x404201FFL</span></span>
</dt> <dt>



<span data-ttu-id="45543-166">Define o limite de relatórios de informações; qualquer log de eventos informativo relacionado ao EAP ocorrerá entre o **usuário do EAP \_ i \_ \_ primeiro** e o **EAP \_ i \_ user \_ Last**.</span><span class="sxs-lookup"><span data-stu-id="45543-166">Defines the boundary of information reports; any EAP related informational event logging will occur between **EAP\_I\_USER\_FIRST** and **EAP\_I\_USER\_LAST**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="45543-167"><span id="EAP_E_USER_CERT_NOT_FOUND"></span><span id="eap_e_user_cert_not_found"></span>**\_certificado EAP E de \_ usuário \_ \_ não \_ encontrado**</span><span class="sxs-lookup"><span data-stu-id="45543-167"><span id="EAP_E_USER_CERT_NOT_FOUND"></span><span id="eap_e_user_cert_not_found"></span>**EAP\_E\_USER\_CERT\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45543-168">0x80420100</span><span class="sxs-lookup"><span data-stu-id="45543-168">0x80420100</span></span>
</dt> <dt>



<span data-ttu-id="45543-169">O EAPHost não pôde localizar um certificado de usuário para autenticação.</span><span class="sxs-lookup"><span data-stu-id="45543-169">EAPHost could not find a user certificate for authentication.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="45543-170"><span id="EAP_E_USER_CERT_INVALID"></span><span id="eap_e_user_cert_invalid"></span>**EAP \_ E \_ certificado de usuário \_ \_ inválido**</span><span class="sxs-lookup"><span data-stu-id="45543-170"><span id="EAP_E_USER_CERT_INVALID"></span><span id="eap_e_user_cert_invalid"></span>**EAP\_E\_USER\_CERT\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45543-171">0x80420101</span><span class="sxs-lookup"><span data-stu-id="45543-171">0x80420101</span></span>
</dt> <dt>



<span data-ttu-id="45543-172">O certificado de usuário que está sendo o usuário para autenticação não tem o conjunto de EKU (uso estendido de chave) adequado.</span><span class="sxs-lookup"><span data-stu-id="45543-172">The user certificate being user for authentication does not have proper extended key usage (EKU) set.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="45543-173"><span id="EAP_E_USER_CERT_EXPIRED"></span><span id="eap_e_user_cert_expired"></span>**EAP \_ E \_ certificado de usuário \_ \_ expirados**</span><span class="sxs-lookup"><span data-stu-id="45543-173"><span id="EAP_E_USER_CERT_EXPIRED"></span><span id="eap_e_user_cert_expired"></span>**EAP\_E\_USER\_CERT\_EXPIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45543-174">0x80420102</span><span class="sxs-lookup"><span data-stu-id="45543-174">0x80420102</span></span>
</dt> <dt>



<span data-ttu-id="45543-175">O EAPhost encontrou um certificado de usuário expirado.</span><span class="sxs-lookup"><span data-stu-id="45543-175">EAPhost found an expired user certificate.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="45543-176"><span id="EAP_E_USER_CERT_REVOKED"></span><span id="eap_e_user_cert_revoked"></span>**certificado de usuário do EAP \_ E \_ \_ \_ revogado**</span><span class="sxs-lookup"><span data-stu-id="45543-176"><span id="EAP_E_USER_CERT_REVOKED"></span><span id="eap_e_user_cert_revoked"></span>**EAP\_E\_USER\_CERT\_REVOKED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45543-177">0x80420103</span><span class="sxs-lookup"><span data-stu-id="45543-177">0x80420103</span></span>
</dt> <dt>



<span data-ttu-id="45543-178">O certificado de usuário que está sendo usado para autenticação foi revogado.</span><span class="sxs-lookup"><span data-stu-id="45543-178">The user certificate being used for authentication has been revoked.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="45543-179"><span id="EAP_E_USER_CERT_OTHER_ERROR"></span><span id="eap_e_user_cert_other_error"></span>**\_erro de \_ \_ outro certificado \_ de usuário EAP E \_**</span><span class="sxs-lookup"><span data-stu-id="45543-179"><span id="EAP_E_USER_CERT_OTHER_ERROR"></span><span id="eap_e_user_cert_other_error"></span>**EAP\_E\_USER\_CERT\_OTHER\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45543-180">0x80420104</span><span class="sxs-lookup"><span data-stu-id="45543-180">0x80420104</span></span>
</dt> <dt>



<span data-ttu-id="45543-181">Ocorreu um erro desconhecido com a certificação de usuário que está sendo usada para autenticação.</span><span class="sxs-lookup"><span data-stu-id="45543-181">An unknown error occurred with the user certification being used for authentication.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="45543-182"><span id="EAP_E_USER_CERT_REJECTED_"></span><span id="eap_e_user_cert_rejected_"></span>**EAP \_ E \_ certificado de usuário \_ \_ rejeitados**</span><span class="sxs-lookup"><span data-stu-id="45543-182"><span id="EAP_E_USER_CERT_REJECTED_"></span><span id="eap_e_user_cert_rejected_"></span>**EAP\_E\_USER\_CERT\_REJECTED**</span></span> 
</dt> <dd> <dl> <dt>

<span data-ttu-id="45543-183">0x80420105</span><span class="sxs-lookup"><span data-stu-id="45543-183">0x80420105</span></span>
</dt> <dt>



<span data-ttu-id="45543-184">O autenticador rejeitou a certificação de usuário.</span><span class="sxs-lookup"><span data-stu-id="45543-184">The authenticator rejected the user certification.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="45543-185"><span id="EAP_I_USER_ACCOUNT_OTHER_ERROR"></span><span id="eap_i_user_account_other_error"></span>**\_erro de \_ \_ outra conta \_ de \_ usuário do EAP**</span><span class="sxs-lookup"><span data-stu-id="45543-185"><span id="EAP_I_USER_ACCOUNT_OTHER_ERROR"></span><span id="eap_i_user_account_other_error"></span>**EAP\_I\_USER\_ACCOUNT\_OTHER\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45543-186">0x40420110</span><span class="sxs-lookup"><span data-stu-id="45543-186">0x40420110</span></span>
</dt> <dt>



<span data-ttu-id="45543-187">Uma falha de EAP foi recebida após uma troca de identidade, indicando a probabilidade de um problema com a conta do usuário de autenticação.</span><span class="sxs-lookup"><span data-stu-id="45543-187">An EAP failure was received after an identity exchange, indicating the likelihood of a problem with the authenticating user's account.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="45543-188"><span id="EAP_E_USER_CREDENTIALS_REJECTED"></span><span id="eap_e_user_credentials_rejected"></span>**\_credenciais de usuário EAP E \_ \_ \_ rejeitadas**</span><span class="sxs-lookup"><span data-stu-id="45543-188"><span id="EAP_E_USER_CREDENTIALS_REJECTED"></span><span id="eap_e_user_credentials_rejected"></span>**EAP\_E\_USER\_CREDENTIALS\_REJECTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45543-189">0x80420111</span><span class="sxs-lookup"><span data-stu-id="45543-189">0x80420111</span></span>
</dt> <dt>



<span data-ttu-id="45543-190">O autenticador rejeitou as credenciais de usuário para autenticação.</span><span class="sxs-lookup"><span data-stu-id="45543-190">The authenticator rejected user credentials for authentication.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="45543-191"><span id="EAP_E_USER_NAME_PASSWORD_REJECTED"></span><span id="eap_e_user_name_password_rejected"></span>**senha do EAP \_ E do \_ nome de usuário \_ \_ \_ rejeitada**</span><span class="sxs-lookup"><span data-stu-id="45543-191"><span id="EAP_E_USER_NAME_PASSWORD_REJECTED"></span><span id="eap_e_user_name_password_rejected"></span>**EAP\_E\_USER\_NAME\_PASSWORD\_REJECTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45543-192">0x80420112</span><span class="sxs-lookup"><span data-stu-id="45543-192">0x80420112</span></span>
</dt> <dt>



<span data-ttu-id="45543-193">Windows 7 ou posterior: falha na autenticação.</span><span class="sxs-lookup"><span data-stu-id="45543-193">Windows 7 or later: Authentication failed.</span></span> <span data-ttu-id="45543-194">O autenticador rejeitou as credenciais do usuário.</span><span class="sxs-lookup"><span data-stu-id="45543-194">The authenticator rejected the user credentials.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="45543-195"><span id="EAP_E_NO_SMART_CARD_READER"></span><span id="eap_e_no_smart_card_reader"></span>**EAP \_ E \_ sem \_ \_ leitor de cartão inteligente \_**</span><span class="sxs-lookup"><span data-stu-id="45543-195"><span id="EAP_E_NO_SMART_CARD_READER"></span><span id="eap_e_no_smart_card_reader"></span>**EAP\_E\_NO\_SMART\_CARD\_READER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45543-196">0x80420113</span><span class="sxs-lookup"><span data-stu-id="45543-196">0x80420113</span></span>
</dt> <dt>



<span data-ttu-id="45543-197">Windows 7 ou posterior: nenhum leitor de cartão inteligente encontrado.</span><span class="sxs-lookup"><span data-stu-id="45543-197">Windows 7 or later: No smart card reader found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="45543-198"><span id="EAP_E_SERVER_FIRST"></span><span id="eap_e_server_first"></span>**EAP \_ E \_ Server \_ primeiro**</span><span class="sxs-lookup"><span data-stu-id="45543-198"><span id="EAP_E_SERVER_FIRST"></span><span id="eap_e_server_first"></span>**EAP\_E\_SERVER\_FIRST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45543-199">0x80420200L</span><span class="sxs-lookup"><span data-stu-id="45543-199">0x80420200L</span></span>
</dt> <dt>



<span data-ttu-id="45543-200">Define o limite dos relatórios de erros; qualquer erro relacionado ao servidor ocorrerá entre o EAP e o servidor **\_ \_ \_ primeiro** e o **EAP \_ e o \_ servidor \_ por último**.</span><span class="sxs-lookup"><span data-stu-id="45543-200">Defines the boundary of error reports; any server related error will occur between **EAP\_E\_SERVER\_FIRST** and **EAP\_E\_SERVER\_LAST**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="45543-201"><span id="EAP_E_SERVER_LAST"></span><span id="eap_e_server_last"></span>**EAP \_ E \_ servidor \_ último**</span><span class="sxs-lookup"><span data-stu-id="45543-201"><span id="EAP_E_SERVER_LAST"></span><span id="eap_e_server_last"></span>**EAP\_E\_SERVER\_LAST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45543-202">0x804202FFL</span><span class="sxs-lookup"><span data-stu-id="45543-202">0x804202FFL</span></span>
</dt> <dt>



<span data-ttu-id="45543-203">Define o limite dos relatórios de erros; qualquer erro relacionado ao servidor ocorrerá entre o EAP e o servidor **\_ \_ \_ primeiro** e o **EAP \_ e o \_ servidor \_ por último**.</span><span class="sxs-lookup"><span data-stu-id="45543-203">Defines the boundary of error reports; any server related error will occur between **EAP\_E\_SERVER\_FIRST** and **EAP\_E\_SERVER\_LAST**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="45543-204"><span id="EAP_E_SERVER_CERT_NOT_FOUND"></span><span id="eap_e_server_cert_not_found"></span>**\_ \_ certificado do servidor EAP E \_ \_ não \_ encontrado**</span><span class="sxs-lookup"><span data-stu-id="45543-204"><span id="EAP_E_SERVER_CERT_NOT_FOUND"></span><span id="eap_e_server_cert_not_found"></span>**EAP\_E\_SERVER\_CERT\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45543-205">0x80420200</span><span class="sxs-lookup"><span data-stu-id="45543-205">0x80420200</span></span>
</dt> <dt>



<span data-ttu-id="45543-206">O EAPHost não pôde localizar o certificado do servidor para autenticação.</span><span class="sxs-lookup"><span data-stu-id="45543-206">EAPHost could not find the server certificate for authentication.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="45543-207"><span id="EAP_E_SERVER_CERT_INVALID"></span><span id="eap_e_server_cert_invalid"></span>**\_ \_ certificado do servidor EAP E \_ \_ inválido**</span><span class="sxs-lookup"><span data-stu-id="45543-207"><span id="EAP_E_SERVER_CERT_INVALID"></span><span id="eap_e_server_cert_invalid"></span>**EAP\_E\_SERVER\_CERT\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45543-208">0x80420201</span><span class="sxs-lookup"><span data-stu-id="45543-208">0x80420201</span></span>
</dt> <dt>



<span data-ttu-id="45543-209">O certificado do servidor sendo o usuário para autenticação não tem um conjunto de EKU (uso estendido de chave) adequado.</span><span class="sxs-lookup"><span data-stu-id="45543-209">The server certificate being user for authentication does not have a proper extended key usage (EKU) set.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="45543-210"><span id="EAP_E_SERVER_CERT_EXPIRED"></span><span id="eap_e_server_cert_expired"></span>**\_certificado EAP \_ E \_ servidor \_ expirado**</span><span class="sxs-lookup"><span data-stu-id="45543-210"><span id="EAP_E_SERVER_CERT_EXPIRED"></span><span id="eap_e_server_cert_expired"></span>**EAP\_E\_SERVER\_CERT\_EXPIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45543-211">0x80420202</span><span class="sxs-lookup"><span data-stu-id="45543-211">0x80420202</span></span>
</dt> <dt>



<span data-ttu-id="45543-212">O EAPhost encontrou um certificado de servidor expirado.</span><span class="sxs-lookup"><span data-stu-id="45543-212">EAPhost found an expired server certificate.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="45543-213"><span id="EAP_E_SERVER_CERT_REVOKED"></span><span id="eap_e_server_cert_revoked"></span>**\_ \_ certificado do EAP E do servidor \_ \_ revogado**</span><span class="sxs-lookup"><span data-stu-id="45543-213"><span id="EAP_E_SERVER_CERT_REVOKED"></span><span id="eap_e_server_cert_revoked"></span>**EAP\_E\_SERVER\_CERT\_REVOKED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45543-214">0x80420203</span><span class="sxs-lookup"><span data-stu-id="45543-214">0x80420203</span></span>
</dt> <dt>



<span data-ttu-id="45543-215">O certificado do servidor que está sendo usado para autenticação foi revogado.</span><span class="sxs-lookup"><span data-stu-id="45543-215">The server certificate being used for authentication has been revoked.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="45543-216"><span id="EAP_E_SERVER_CERT_OTHER_ERROR"></span><span id="eap_e_server_cert_other_error"></span>**\_ \_ \_ \_ outro erro de certificado do servidor EAP E \_**</span><span class="sxs-lookup"><span data-stu-id="45543-216"><span id="EAP_E_SERVER_CERT_OTHER_ERROR"></span><span id="eap_e_server_cert_other_error"></span>**EAP\_E\_SERVER\_CERT\_OTHER\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45543-217">0x80420204</span><span class="sxs-lookup"><span data-stu-id="45543-217">0x80420204</span></span>
</dt> <dt>



<span data-ttu-id="45543-218">Ocorreu um erro desconhecido com o certificado do servidor.</span><span class="sxs-lookup"><span data-stu-id="45543-218">An unknown error occurred with the server certificate.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="45543-219"><span id="EAP_E_USER_ROOT_CERT_FIRST"></span><span id="eap_e_user_root_cert_first"></span>**EAP \_ E \_ \_ certificado raiz do usuário \_ \_ primeiro**</span><span class="sxs-lookup"><span data-stu-id="45543-219"><span id="EAP_E_USER_ROOT_CERT_FIRST"></span><span id="eap_e_user_root_cert_first"></span>**EAP\_E\_USER\_ROOT\_CERT\_FIRST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45543-220">0x80420300L</span><span class="sxs-lookup"><span data-stu-id="45543-220">0x80420300L</span></span>
</dt> <dt>



<span data-ttu-id="45543-221">Define o limite dos relatórios de erros; qualquer erro relacionado ao certificado raiz do usuário ocorrerá entre o EAP e o certificado raiz do **\_ \_ usuário \_ \_ \_ primeiro** e o **\_ \_ \_ certificado raiz do usuário \_ \_ do EAP** e o primeiro.</span><span class="sxs-lookup"><span data-stu-id="45543-221">Defines the boundary of error reports; any user root certificate related error will occur between **EAP\_E\_USER\_ROOT\_CERT\_FIRST** and **EAP\_E\_USER\_ROOT\_CERT\_FIRST**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="45543-222"><span id="EAP_E_USER_ROOT_CERT_LAST"></span><span id="eap_e_user_root_cert_last"></span>**EAP \_ E \_ \_ certificado raiz do usuário \_ \_ último**</span><span class="sxs-lookup"><span data-stu-id="45543-222"><span id="EAP_E_USER_ROOT_CERT_LAST"></span><span id="eap_e_user_root_cert_last"></span>**EAP\_E\_USER\_ROOT\_CERT\_LAST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45543-223">0x804203FFL</span><span class="sxs-lookup"><span data-stu-id="45543-223">0x804203FFL</span></span>
</dt> <dt>



<span data-ttu-id="45543-224">Define o limite dos relatórios de erros; qualquer erro relacionado ao certificado raiz do usuário ocorrerá entre o EAP e o certificado raiz do **\_ \_ usuário \_ \_ \_ primeiro** e o **\_ \_ \_ certificado raiz do usuário \_ \_ do EAP** e o primeiro.</span><span class="sxs-lookup"><span data-stu-id="45543-224">Defines the boundary of error reports; any user root certificate related error will occur between **EAP\_E\_USER\_ROOT\_CERT\_FIRST** and **EAP\_E\_USER\_ROOT\_CERT\_FIRST**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="45543-225"><span id="EAP_E_USER_ROOT_CERT_NOT_FOUND"></span><span id="eap_e_user_root_cert_not_found"></span>**\_certificado de raiz de usuário E EAP \_ \_ \_ \_ não \_ encontrado**</span><span class="sxs-lookup"><span data-stu-id="45543-225"><span id="EAP_E_USER_ROOT_CERT_NOT_FOUND"></span><span id="eap_e_user_root_cert_not_found"></span>**EAP\_E\_USER\_ROOT\_CERT\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45543-226">0x80420300</span><span class="sxs-lookup"><span data-stu-id="45543-226">0x80420300</span></span>
</dt> <dt>



<span data-ttu-id="45543-227">O EAPHost não pôde localizar um certificado em um repositório de certificados raiz confiável para a validação de certificação do usuário.</span><span class="sxs-lookup"><span data-stu-id="45543-227">EAPHost could not find a certificate in a trusted root certificate store for user certification validation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="45543-228"><span id="EAP_E_USER_ROOT_CERT_INVALID"></span><span id="eap_e_user_root_cert_invalid"></span>**EAP \_ E \_ \_ certificado raiz do usuário \_ \_ inválido**</span><span class="sxs-lookup"><span data-stu-id="45543-228"><span id="EAP_E_USER_ROOT_CERT_INVALID"></span><span id="eap_e_user_root_cert_invalid"></span>**EAP\_E\_USER\_ROOT\_CERT\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45543-229">0x80420301</span><span class="sxs-lookup"><span data-stu-id="45543-229">0x80420301</span></span>
</dt> <dt>



<span data-ttu-id="45543-230">A autenticação falhou porque o certificado raiz usado para esta rede é inválido.</span><span class="sxs-lookup"><span data-stu-id="45543-230">The authentication failed because the root certificate used for this network is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="45543-231"><span id="EAP_E_USER_ROOT_CERT_EXPIRED"></span><span id="eap_e_user_root_cert_expired"></span>**EAP \_ E \_ \_ certificado raiz de usuário \_ \_ expirados**</span><span class="sxs-lookup"><span data-stu-id="45543-231"><span id="EAP_E_USER_ROOT_CERT_EXPIRED"></span><span id="eap_e_user_root_cert_expired"></span>**EAP\_E\_USER\_ROOT\_CERT\_EXPIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45543-232">0x80420302</span><span class="sxs-lookup"><span data-stu-id="45543-232">0x80420302</span></span>
</dt> <dt>



<span data-ttu-id="45543-233">O certificado raiz confiável necessário para a validação do certificado do usuário expirou.</span><span class="sxs-lookup"><span data-stu-id="45543-233">The trusted root certificate needed for user certificate validation has expired.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="45543-234"><span id="EAP_E_SERVER_ROOT_CERT_FIRST"></span><span id="eap_e_server_root_cert_first"></span>**\_ \_ certificado raiz do EAP E do servidor \_ \_ \_ primeiro**</span><span class="sxs-lookup"><span data-stu-id="45543-234"><span id="EAP_E_SERVER_ROOT_CERT_FIRST"></span><span id="eap_e_server_root_cert_first"></span>**EAP\_E\_SERVER\_ROOT\_CERT\_FIRST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45543-235">0x80420400L</span><span class="sxs-lookup"><span data-stu-id="45543-235">0x80420400L</span></span>
</dt> <dt>



<span data-ttu-id="45543-236">Define o limite dos relatórios de erros; qualquer erro relacionado ao certificado raiz do servidor ocorrerá entre o **EAP e o certificado \_ \_ raiz do servidor \_ \_ \_ primeiro** e o **\_ \_ certificado raiz do EAP e do servidor \_ \_ \_ primeiro**.</span><span class="sxs-lookup"><span data-stu-id="45543-236">Defines the boundary of error reports; any server root certificate related error will occur between **EAP\_E\_SERVER\_ROOT\_CERT\_FIRST** and **EAP\_E\_SERVER\_ROOT\_CERT\_FIRST**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="45543-237"><span id="EAP_E_SERVER_ROOT_CERT_LAST"></span><span id="eap_e_server_root_cert_last"></span>**\_ \_ certificado raiz do EAP E do servidor \_ \_ \_ último**</span><span class="sxs-lookup"><span data-stu-id="45543-237"><span id="EAP_E_SERVER_ROOT_CERT_LAST"></span><span id="eap_e_server_root_cert_last"></span>**EAP\_E\_SERVER\_ROOT\_CERT\_LAST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45543-238">0x804204FFL</span><span class="sxs-lookup"><span data-stu-id="45543-238">0x804204FFL</span></span>
</dt> <dt>



<span data-ttu-id="45543-239">Define o limite dos relatórios de erros; qualquer erro relacionado ao certificado raiz do servidor ocorrerá entre o **EAP e o certificado \_ \_ raiz do servidor \_ \_ \_ primeiro** e o **\_ \_ certificado raiz do EAP e do servidor \_ \_ \_ primeiro**.</span><span class="sxs-lookup"><span data-stu-id="45543-239">Defines the boundary of error reports; any server root certificate related error will occur between **EAP\_E\_SERVER\_ROOT\_CERT\_FIRST** and **EAP\_E\_SERVER\_ROOT\_CERT\_FIRST**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="45543-240"><span id="EAP_E_SERVER_ROOT_CERT_NOT_FOUND"></span><span id="eap_e_server_root_cert_not_found"></span>**\_ \_ certificado raiz do servidor EAP E \_ \_ \_ não \_ encontrado**</span><span class="sxs-lookup"><span data-stu-id="45543-240"><span id="EAP_E_SERVER_ROOT_CERT_NOT_FOUND"></span><span id="eap_e_server_root_cert_not_found"></span>**EAP\_E\_SERVER\_ROOT\_CERT\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45543-241">0x80420400</span><span class="sxs-lookup"><span data-stu-id="45543-241">0x80420400</span></span>
</dt> <dt>



<span data-ttu-id="45543-242">O EAPHost não pôde localizar um certificado raiz em um repositório de certificados raiz confiável para a validação de certificação do servidor.</span><span class="sxs-lookup"><span data-stu-id="45543-242">EAPHost could not find a root certificate in a trusted root certificate store for the server certification validation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="45543-243"><span id="EAP_E_SERVER_ROOT_CERT_INVALID__________"></span><span id="eap_e_server_root_cert_invalid__________"></span>**\_ \_ certificado raiz do EAP E do servidor \_ \_ \_ inválido**</span><span class="sxs-lookup"><span data-stu-id="45543-243"><span id="EAP_E_SERVER_ROOT_CERT_INVALID__________"></span><span id="eap_e_server_root_cert_invalid__________"></span>**EAP\_E\_SERVER\_ROOT\_CERT\_INVALID**</span></span> 
</dt> <dd> <dl> <dt>

<span data-ttu-id="45543-244">0x80420401</span><span class="sxs-lookup"><span data-stu-id="45543-244">0x80420401</span></span>
</dt> <dt>



<span data-ttu-id="45543-245">A autenticação falhou porque o certificado do servidor necessário para esta rede no computador servidor é inválido.</span><span class="sxs-lookup"><span data-stu-id="45543-245">The authentication failed because the server certificate required for this network on the server computer is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="45543-246"><span id="EAP_E_SERVER_ROOT_CERT_NAME_REQUIRED"></span><span id="eap_e_server_root_cert_name_required"></span>**\_ \_ nome do certificado raiz do EAP E do servidor \_ \_ \_ \_ necessário**</span><span class="sxs-lookup"><span data-stu-id="45543-246"><span id="EAP_E_SERVER_ROOT_CERT_NAME_REQUIRED"></span><span id="eap_e_server_root_cert_name_required"></span>**EAP\_E\_SERVER\_ROOT\_CERT\_NAME\_REQUIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45543-247">0x80420406</span><span class="sxs-lookup"><span data-stu-id="45543-247">0x80420406</span></span>
</dt> <dt>



<span data-ttu-id="45543-248">A autenticação falhou porque o certificado no computador servidor não tem um nome de servidor especificado.</span><span class="sxs-lookup"><span data-stu-id="45543-248">The authentication failed because the certificate on the server computer does not have a server name specified.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="45543-249">Comentários</span><span class="sxs-lookup"><span data-stu-id="45543-249">Remarks</span></span>

<span data-ttu-id="45543-250">Há nomes alternativos para determinados erros:</span><span class="sxs-lookup"><span data-stu-id="45543-250">There are alternate names for certain errors:</span></span>

-   <span data-ttu-id="45543-251">Outro nome para **o \_ método EAP E \_ EAPHost \_ \_ \_ pacote inválido** é **\_ pacote de método EAP \_ inválido \_**.</span><span class="sxs-lookup"><span data-stu-id="45543-251">Another name for **EAP\_E\_EAPHOST\_METHOD\_INVALID\_PACKET** is **EAP\_METHOD\_INVALID\_PACKET**.</span></span>
-   <span data-ttu-id="45543-252">Outro nome para **EAP \_ E \_ EAPHost \_ remoto \_ \_** é um pacote inválido de **EAP \_ \_**.</span><span class="sxs-lookup"><span data-stu-id="45543-252">Another name for **EAP\_E\_EAPHOST\_REMOTE\_INVALID\_PACKET** is **EAP\_INVALID\_PACKET**.</span></span>

## <a name="requirements"></a><span data-ttu-id="45543-253">Requisitos</span><span class="sxs-lookup"><span data-stu-id="45543-253">Requirements</span></span>



| <span data-ttu-id="45543-254">Requisito</span><span class="sxs-lookup"><span data-stu-id="45543-254">Requirement</span></span> | <span data-ttu-id="45543-255">Valor</span><span class="sxs-lookup"><span data-stu-id="45543-255">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="45543-256">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="45543-256">Minimum supported client</span></span><br/> | <span data-ttu-id="45543-257">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="45543-257">Windows Vista \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="45543-258">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="45543-258">Minimum supported server</span></span><br/> | <span data-ttu-id="45543-259">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="45543-259">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="45543-260">parâmetro</span><span class="sxs-lookup"><span data-stu-id="45543-260">Header</span></span><br/>                   | <dl> <span data-ttu-id="45543-261"><dt>Eaphosterror. h</dt></span><span class="sxs-lookup"><span data-stu-id="45543-261"><dt>Eaphosterror.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="45543-262">Confira também</span><span class="sxs-lookup"><span data-stu-id="45543-262">See also</span></span>

<dl> <dt>

[<span data-ttu-id="45543-263">Constantes do EAPHost comuns</span><span class="sxs-lookup"><span data-stu-id="45543-263">Common EAPHost Constants</span></span>](common-eap-host-error-constants.md)
</dt> </dl>

 

