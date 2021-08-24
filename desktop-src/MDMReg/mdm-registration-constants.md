---
title: Valores de erro de registro do MDM (MDMRegistration. h)
description: Os seguintes valores de erro são com o registro do MDM.
ms.assetid: 1f42ed5e-e221-47ec-a019-ed06c05d55d0
topic_type:
- apiref
api_name:
- E_DATATYPE_MISMATCH
- MREGISTER_E_DEVICE_MESSAGE_FORMAT_ERROR
- MENROLL_E_DEVICE_MESSAGE_FORMAT_ERROR
- MREGISTER_E_DEVICE_AUTHENTICATION_ERROR
- MENROLL_E_DEVICE_AUTHENTICATION_ERROR
- MREGISTER_E_DEVICE_AUTHORIZATION_ERROR
- MENROLL_E_DEVICE_AUTHORIZATION_ERROR
- MREGISTER_E_DEVICE_CERTIFCATEREQUEST_ERROR
- MENROLL_E_DEVICE_CERTIFCATEREQUEST_ERROR
- MREGISTER_E_DEVICE_CONFIGMGRSERVER_ERROR
- MENROLL_E_DEVICE_CONFIGMGRSERVER_ERROR
- MREGISTER_E_DEVICE_INTERNALSERVICE_ERROR
- MENROLL_E_DEVICE_INTERNALSERVICE_ERROR
- MREGISTER_E_DEVICE_INVALIDSECURITY_ERROR
- MENROLL_E_DEVICE_INVALIDSECURITY_ERROR
- MREGISTER_E_DEVICE_UNKNOWN_ERROR
- MENROLL_E_DEVICE_UNKNOWN_ERROR
- MREGISTER_E_REGISTRATION_IN_PROGRESS
- MENROLL_E_ENROLLMENT_IN_PROGRESS
- MREGISTER_E_DEVICE_ALREADY_REGISTERED
- MENROLL_E_DEVICE_ALREADY_ENROLLED
- MREGISTER_E_DEVICE_NOT_REGISTERED
- MENROLL_E_DEVICE_NOT_ENROLLED
- MREGISTER_E_DISCOVERY_REDIRECTED
- MREGISTER_E_DEVICE_NOT_AD_REGISTERED_ERROR
- MENROLL_E_DISCOVERY_SEC_CERT_DATE_INVALID
- MREGISTER_E_DISCOVERY_FAILED
- MENROLL_E_PASSWORD_NEEDED
- MENROLL_E_WAB_ERROR
- MENROLL_E_CONNECTIVITY
- MENROLL_S_ENROLLMENT_SUSPENDED
- MENROLL_E_INVALIDSSLCERT
- MENROLL_E_DEVICECAPREACHED
- MENROLL_E_DEVICENOTSUPPORTED
- MENROLL_E_NOTSUPPORTED
- MREGISTER_E_NOTELIGIBLETORENEW
- MENROLL_E_INMAINTENANCE
- MENROLL_E_USERLICENSE
- MENROLL_E_ENROLLMENTDATAINVALID
- MENROLL_E_INSECUREREDIRECT
- MENROLL_E_PLATFORM_WRONG_STATE
- MENROLL_E_PLATFORM_LICENSE_ERROR
- MENROLL_E_PLATFORM_UNKNOWN_ERROR
- MENROLL_E_PROV_CSP_CERTSTORE
- MENROLL_E_PROV_CSP_W7
- MENROLL_E_PROV_CSP_DMCLIENT
- MENROLL_E_PROV_CSP_PFW
- MENROLL_E_PROV_CSP_MISC
- MENROLL_E_PROV_UNKNOWN
- MENROLL_E_PROV_SSLCERTNOTFOUND
- MENROLL_E_PROV_CSP_APPMGMT
- MENROLL_E_DEVICE_MANAGEMENT_BLOCKED
- MENROLL_E_CERTPOLICY_PRIVATEKEYCREATION_FAILED
- MENROLL_E_CERTAUTH_FAILED_TO_FIND_CERT
- MENROLL_E_EMPTY_MESSAGE
- MENROLL_E_USER_CANCELED
- MENROLL_E_MDM_NOT_CONFIGURED
api_location:
- MDMRegistration.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ff5c73941b0235788772522f5551f73faea30d06e91e582dcdbe97433ca85c2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119638456"
---
# <a name="mdm-registration-error-values"></a>Valores de erro de registro do MDM

Os seguintes valores de erro são com o registro do MDM.

<dl> <dt>

<span id="E_DATATYPE_MISMATCH"></span><span id="e_datatype_mismatch"></span>**E \_ DataType não \_ coincide**
</dt> <dd> <dl> <dt>

0x8007065d
</dt> <dt>



O tipo de dados não corresponde ao tipo de dados esperado.


</dt> </dl> </dd> <dt>

<span id="MREGISTER_E_DEVICE_MESSAGE_FORMAT_ERROR"></span><span id="mregister_e_device_message_format_error"></span>**\_erro de \_ formato de mensagem de dispositivo \_ \_ MREGISTER \_**
</dt> <dd> <dl> <dt>

0x80190001
</dt> <dt>



Esquema inválido, erro de formato de mensagem do servidor.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_DEVICE_MESSAGE_FORMAT_ERROR"></span><span id="menroll_e_device_message_format_error"></span>**\_erro de \_ formato de mensagem de dispositivo \_ \_ MENROLL \_**
</dt> <dd> <dl> <dt>

0x80180001
</dt> <dt>



Esquema inválido, erro de formato de mensagem do servidor.

**Windows 8.1:** Essa constante não está disponível antes de Windows 10.


</dt> </dl> </dd> <dt>

<span id="MREGISTER_E_DEVICE_AUTHENTICATION_ERROR"></span><span id="mregister_e_device_authentication_error"></span>**MREGISTER \_ E \_ \_ erro de autenticação de dispositivo \_**
</dt> <dd> <dl> <dt>

0x80190002
</dt> <dt>



Falha do servidor ao autenticar o usuário.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_DEVICE_AUTHENTICATION_ERROR"></span><span id="menroll_e_device_authentication_error"></span>**MENROLL \_ E \_ \_ erro de autenticação de dispositivo \_**
</dt> <dd> <dl> <dt>

0x80180002
</dt> <dt>



Falha do servidor ao autenticar o usuário.

**Windows 8.1:** Essa constante não está disponível antes de Windows 10.


</dt> </dl> </dd> <dt>

<span id="MREGISTER_E_DEVICE_AUTHORIZATION_ERROR"></span><span id="mregister_e_device_authorization_error"></span>**\_erro de \_ autorização do dispositivo \_ \_ MREGISTER**
</dt> <dd> <dl> <dt>

0x80190003
</dt> <dt>



O usuário não está autorizado a se registrar.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_DEVICE_AUTHORIZATION_ERROR"></span><span id="menroll_e_device_authorization_error"></span>**\_erro de \_ autorização do dispositivo \_ \_ MENROLL**
</dt> <dd> <dl> <dt>

0x80180003
</dt> <dt>



O usuário não está autorizado a se registrar.

**Windows 8.1:** Essa constante não está disponível antes de Windows 10.


</dt> </dl> </dd> <dt>

<span id="MREGISTER_E_DEVICE_CERTIFCATEREQUEST_ERROR"></span><span id="mregister_e_device_certifcaterequest_error"></span>**\_erro MREGISTER E \_ dispositivo \_ CERTIFCATEREQUEST \_**
</dt> <dd> <dl> <dt>

0x80190004
</dt> <dt>



O usuário não tem permissão para o modelo de certificado ou a autoridade de certificação está inacessível.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_DEVICE_CERTIFCATEREQUEST_ERROR"></span><span id="menroll_e_device_certifcaterequest_error"></span>**\_erro MENROLL E \_ dispositivo \_ CERTIFCATEREQUEST \_**
</dt> <dd> <dl> <dt>

0x80180004
</dt> <dt>



O usuário não tem permissão para o modelo de certificado ou a autoridade de certificação está inacessível.

**Windows 8.1:** Essa constante não está disponível antes de Windows 10.


</dt> </dl> </dd> <dt>

<span id="MREGISTER_E_DEVICE_CONFIGMGRSERVER_ERROR"></span><span id="mregister_e_device_configmgrserver_error"></span>**\_erro MREGISTER E \_ dispositivo \_ CONFIGMGRSERVER \_**
</dt> <dd> <dl> <dt>

0x80190005
</dt> <dt>



Houve uma falha no servidor de gerenciamento, como um erro de acesso ao banco de dados.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_DEVICE_CONFIGMGRSERVER_ERROR"></span><span id="menroll_e_device_configmgrserver_error"></span>**\_erro MENROLL E \_ dispositivo \_ CONFIGMGRSERVER \_**
</dt> <dd> <dl> <dt>

0x80180005
</dt> <dt>



Houve uma falha no servidor de gerenciamento, como um erro de acesso ao banco de dados.

**Windows 8.1:** Essa constante não está disponível antes de Windows 10.


</dt> </dl> </dd> <dt>

<span id="MREGISTER_E_DEVICE_INTERNALSERVICE_ERROR"></span><span id="mregister_e_device_internalservice_error"></span>**\_erro MREGISTER E \_ dispositivo \_ INTERNALSERVICE \_**
</dt> <dd> <dl> <dt>

0x80190006
</dt> <dt>



Houve uma exceção sem tratamento no servidor.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_DEVICE_INTERNALSERVICE_ERROR"></span><span id="menroll_e_device_internalservice_error"></span>**\_erro MENROLL E \_ dispositivo \_ INTERNALSERVICE \_**
</dt> <dd> <dl> <dt>

0x80180006
</dt> <dt>



Houve uma exceção sem tratamento no servidor.

**Windows 8.1:** Essa constante não está disponível antes de Windows 10.


</dt> </dl> </dd> <dt>

<span id="MREGISTER_E_DEVICE_INVALIDSECURITY_ERROR"></span><span id="mregister_e_device_invalidsecurity_error"></span>**\_erro MREGISTER E \_ dispositivo \_ INVALIDSECURITY \_**
</dt> <dd> <dl> <dt>

0x80190007
</dt> <dt>



Houve uma exceção sem tratamento no servidor.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_DEVICE_INVALIDSECURITY_ERROR"></span><span id="menroll_e_device_invalidsecurity_error"></span>**\_erro MENROLL E \_ dispositivo \_ INVALIDSECURITY \_**
</dt> <dd> <dl> <dt>

0x80180007
</dt> <dt>



Houve uma exceção sem tratamento no servidor.

**Windows 8.1:** Essa constante não está disponível antes de Windows 10.


</dt> </dl> </dd> <dt>

<span id="MREGISTER_E_DEVICE_UNKNOWN_ERROR"></span><span id="mregister_e_device_unknown_error"></span>**\_ \_ erro desconhecido de dispositivo MREGISTER E \_ \_**
</dt> <dd> <dl> <dt>

0x80190008
</dt> <dt>



Erro de servidor desconhecido.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_DEVICE_UNKNOWN_ERROR"></span><span id="menroll_e_device_unknown_error"></span>**\_ \_ erro desconhecido de dispositivo MENROLL E \_ \_**
</dt> <dd> <dl> <dt>

0x80180008
</dt> <dt>



Erro de servidor desconhecido.

**Windows 8.1:** Essa constante não está disponível antes de Windows 10.


</dt> </dl> </dd> <dt>

<span id="MREGISTER_E_REGISTRATION_IN_PROGRESS"></span><span id="mregister_e_registration_in_progress"></span>**MREGISTER \_ E \_ registro \_ em \_ andamento**
</dt> <dd> <dl> <dt>

0x80190009
</dt> <dt>



Outra operação de registro está em andamento.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_ENROLLMENT_IN_PROGRESS"></span><span id="menroll_e_enrollment_in_progress"></span>**\_ \_ registro do MENROLL E \_ em \_ andamento**
</dt> <dd> <dl> <dt>

0x80180009
</dt> <dt>



Outra operação de registro está em andamento.

**Windows 8.1:** Essa constante não está disponível antes de Windows 10.


</dt> </dl> </dd> <dt>

<span id="MREGISTER_E_DEVICE_ALREADY_REGISTERED"></span><span id="mregister_e_device_already_registered"></span>**\_dispositivo MREGISTER \_ E \_ já \_ registrado**
</dt> <dd> <dl> <dt>

0x8019000A
</dt> <dt>



Não se usa mais.

**Windows 8.1:** O dispositivo já está registrado.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_DEVICE_ALREADY_ENROLLED"></span><span id="menroll_e_device_already_enrolled"></span>**MENROLL \_ E \_ dispositivo \_ já \_ registrado**
</dt> <dd> <dl> <dt>

0x8018000A
</dt> <dt>



O dispositivo já está registrado.

**Windows 8.1:** Essa constante não está disponível antes de Windows 10.


</dt> </dl> </dd> <dt>

<span id="MREGISTER_E_DEVICE_NOT_REGISTERED"></span><span id="mregister_e_device_not_registered"></span>**\_dispositivo MREGISTER \_ E \_ não \_ registrado**
</dt> <dd> <dl> <dt>

0x8019000B
</dt> <dt>



Não se usa mais.

**Windows 8.1:** O dispositivo não está registrado.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_DEVICE_NOT_ENROLLED"></span><span id="menroll_e_device_not_enrolled"></span>**\_dispositivo MENROLL \_ E \_ não \_ registrado**
</dt> <dd> <dl> <dt>

0x8018000B
</dt> <dt>



O dispositivo não está registrado.

**Windows 8.1:** Essa constante não está disponível antes de Windows 10.


</dt> </dl> </dd> <dt>

<span id="MREGISTER_E_DISCOVERY_REDIRECTED"></span><span id="mregister_e_discovery_redirected"></span>**descoberta de MREGISTER \_ E \_ \_ redirecionada**
</dt> <dd> <dl> <dt>

0x8019000C
</dt> <dt>



Não se usa mais.

**Windows 8.1:** O redirecionamento é necessário.


</dt> </dl> </dd> <dt>

<span id="MREGISTER_E_DEVICE_NOT_AD_REGISTERED_ERROR"></span><span id="mregister_e_device_not_ad_registered_error"></span>**\_erro MREGISTER E \_ dispositivo \_ não \_ registrado no AD \_ \_**
</dt> <dd> <dl> <dt>

0x8019000D
</dt> <dt>



Não se usa mais.

**Windows 8.1:** O dispositivo não está registrado com Active Directory.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_DISCOVERY_SEC_CERT_DATE_INVALID"></span><span id="menroll_e_discovery_sec_cert_date_invalid"></span>**MENROLL \_ E \_ \_ data de CERT SEC de descoberta \_ \_ \_ inválida**
</dt> <dd> <dl> <dt>

0x8018000D
</dt> <dt>



Durante a descoberta, a data de CERT SEC era inválida.

**Windows 8.1:** Essa constante não está disponível antes de Windows 10.


</dt> </dl> </dd> <dt>

<span id="MREGISTER_E_DISCOVERY_FAILED"></span><span id="mregister_e_discovery_failed"></span>**\_ \_ falha na descoberta do MREGISTER \_**
</dt> <dd> <dl> <dt>

0x8019000E
</dt> <dt>



Não se usa mais.

**Windows 8.1:** Falha na descoberta; O redirecionamento é necessário.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_PASSWORD_NEEDED"></span><span id="menroll_e_password_needed"></span>**MENROLL \_ E \_ PASSWORD \_ NEEDED**
</dt> <dd> <dl> <dt>

0x8018000E
</dt> <dt>



Uma senha é necessária, mas não foi fornecida.

**Windows 8.1:** Essa constante não está disponível antes Windows 10.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_WAB_ERROR"></span><span id="menroll_e_wab_error"></span>**ERRO DE \_ MENROLL E \_ \_ WAB**
</dt> <dd> <dl> <dt>

0x8018000F
</dt> <dt>



Ocorreu um erro durante o registro de WAB.

**Windows 8.1:** Essa constante não está disponível antes Windows 10.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_CONNECTIVITY"></span><span id="menroll_e_connectivity"></span>**MENROLL \_ E \_ CONNECTIVITY**
</dt> <dd> <dl> <dt>

0x80180010
</dt> <dt>



Ocorreu um erro de rede, como DNS ou um tempo de vida de rede.

**Windows 8.1:** Essa constante não está disponível antes Windows 10.


</dt> </dl> </dd> <dt>

<span id="MENROLL_S_ENROLLMENT_SUSPENDED"></span><span id="menroll_s_enrollment_suspended"></span>**REGISTRO DO MENROLL \_ \_ \_ SUSPENSO**
</dt> <dd> <dl> <dt>

0x00180011
</dt> <dt>



O registro foi suspenso. Não tem mais suporte.

**Windows 8.1:** Essa constante não está disponível antes Windows 10.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_INVALIDSSLCERT"></span><span id="menroll_e_invalidsslcert"></span>**MENROLL \_ E \_ INVALIDSSLCERT**
</dt> <dd> <dl> <dt>

0x80180012
</dt> <dt>



O certificado SSL não era válido.

**Windows 8.1:** Essa constante não está disponível antes Windows 10.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_DEVICECAPREACHED"></span><span id="menroll_e_devicecapreached"></span>**MENROLL \_ E \_ DEVICECAPREACHED**
</dt> <dd> <dl> <dt>

0x80180013
</dt> <dt>



O usuário já registrou muitos dispositivos. Exclua ou desinclua os antigos para corrigir esse erro. Observe que o usuário pode resolver esse erro sem assistência do administrador.

**Windows 8.1:** Essa constante não está disponível antes Windows 10.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_DEVICENOTSUPPORTED"></span><span id="menroll_e_devicenotsupported"></span>**MENROLL \_ E \_ DEVICENOTSUPPORTED**
</dt> <dd> <dl> <dt>

0x80180014
</dt> <dt>



Não há suporte para uma plataforma específica (por exemplo, Windows) ou versão. A correção geral para esse erro é atualizar o dispositivo.

**Windows 8.1:** Essa constante não está disponível antes Windows 10.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_NOTSUPPORTED"></span><span id="menroll_e_notsupported"></span>**MENROLL \_ E \_ NOTSUPPORTED**
</dt> <dd> <dl> <dt>

0x80180015
</dt> <dt>



O gerenciamento de dispositivo móvel geralmente não tem suporte para esse dispositivo – o usuário pode chamar o administrador, mas será improvável resolver esse problema.

**Windows 8.1:** Essa constante não está disponível antes Windows 10.


</dt> </dl> </dd> <dt>

<span id="MREGISTER_E_NOTELIGIBLETORENEW"></span><span id="mregister_e_noteligibletorenew"></span>**MREGISTER \_ E \_ NOTELIGIBLETORENEW**
</dt> <dd> <dl> <dt>

0x80180016
</dt> <dt>



O dispositivo está tentando renovar, mas o servidor rejeitou a solicitação. Verifique a hora no dispositivo. O usuário pode ser capaz de resolver esse erro registrando-se.

**Windows 8.1:** Essa constante não está disponível antes Windows 10.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_INMAINTENANCE"></span><span id="menroll_e_inmaintenance"></span>**MENROLL \_ E \_ INMAINTENANCE**
</dt> <dd> <dl> <dt>

0x80180017
</dt> <dt>



A conta está em manutenção; tentar novamente mais tarde. O usuário pode tentar novamente mais tarde. No entanto, o usuário pode optar por chamar o administrador para determinar o agendamento de manutenção.

**Windows 8.1:** Essa constante não está disponível antes Windows 10.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_USERLICENSE"></span><span id="menroll_e_userlicense"></span>**MENROLL \_ E \_ USERLICENSE**
</dt> <dd> <dl> <dt>

0x80180018
</dt> <dt>



A licença do usuário está em estado ruim bloqueando o registro; o usuário precisará chamar o administrador.

**Windows 8.1:** Essa constante não está disponível antes Windows 10.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_ENROLLMENTDATAINVALID"></span><span id="menroll_e_enrollmentdatainvalid"></span>**MENROLL \_ E \_ ENROLLMENTDATAINVALID**
</dt> <dd> <dl> <dt>

0x80180019
</dt> <dt>



O servidor rejeitou os dados de registro; O servidor pode não estar configurado corretamente.

**Windows 8.1:** Essa constante não está disponível antes Windows 10.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_INSECUREREDIRECT"></span><span id="menroll_e_insecureredirect"></span>**MENROLL \_ E \_ INSECUREREDIRECT**
</dt> <dd> <dl> <dt>

0x8018001A
</dt> <dt>



O servidor solicitou HTTP em vez de HTTPS, mas não foi aceito.

**Windows 8.1:** Essa constante não está disponível antes Windows 10.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_PLATFORM_WRONG_STATE"></span><span id="menroll_e_platform_wrong_state"></span>**MENROLL \_ E \_ PLATFORM \_ WRONG \_ STATE**
</dt> <dd> <dl> <dt>

0x8018001B
</dt> <dt>



Foi tentada uma operação inválida, como tentar registrar o mesmo dispositivo duas vezes ou não registrar um dispositivo desconhecido.

**Windows 8.1:** Essa constante não está disponível antes Windows 10.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_PLATFORM_LICENSE_ERROR"></span><span id="menroll_e_platform_license_error"></span>**ERRO DE LICENÇA DA PLATAFORMA MENROLL \_ E \_ \_ \_**
</dt> <dd> <dl> <dt>

0x8018001C
</dt> <dt>



A versão do Windows instalada no cliente não dá suporte a esse tipo de registro.

**Windows 8.1:** Essa constante não está disponível antes Windows 10.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_PLATFORM_UNKNOWN_ERROR"></span><span id="menroll_e_platform_unknown_error"></span>**ERRO DESCONHECIDO DA PLATAFORMA MENROLL \_ E \_ \_ \_**
</dt> <dd> <dl> <dt>

0x8018001D
</dt> <dt>



Ocorreu um erro desconhecido no cliente.

**Windows 8.1:** Essa constante não está disponível antes Windows 10.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_PROV_CSP_CERTSTORE"></span><span id="menroll_e_prov_csp_certstore"></span>**MENROLL \_ E \_ PROV \_ CSP \_ CERTSTORE**
</dt> <dd> <dl> <dt>

0x8018001E
</dt> <dt>



Falha no provisionamento no CSP do armazenamento de certificados.

**Windows 8.1:** Essa constante não está disponível antes Windows 10.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_PROV_CSP_W7"></span><span id="menroll_e_prov_csp_w7"></span>**MENROLL \_ E \_ PROV \_ CSP \_ W7**
</dt> <dd> <dl> <dt>

0x8018001F
</dt> <dt>



Falha no provisionamento em um CPP W7/DMAcc.

**Windows 8.1:** Essa constante não está disponível antes Windows 10.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_PROV_CSP_DMCLIENT"></span><span id="menroll_e_prov_csp_dmclient"></span>**MENROLL \_ E \_ PROV \_ CSP \_ DMCLIENT**
</dt> <dd> <dl> <dt>

0x80180020
</dt> <dt>



Falha no provisionamento em um CSP cliente DM.

**Windows 8.1:** Essa constante não está disponível antes Windows 10.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_PROV_CSP_PFW"></span><span id="menroll_e_prov_csp_pfw"></span>**MENROLL \_ E \_ PROV \_ CSP \_ PFW**
</dt> <dd> <dl> <dt>

0x80180021
</dt> <dt>



Falha no provisionamento em um CSP do Passport for Work.

**Windows 8.1:** Essa constante não está disponível antes Windows 10.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_PROV_CSP_MISC"></span><span id="menroll_e_prov_csp_misc"></span>**MENROLL \_ E \_ PROV \_ CSP \_ MISC**
</dt> <dd> <dl> <dt>

0x80180022
</dt> <dt>



Falha no provisionamento em um CSP não listado acima.

**Windows 8.1:** Essa constante não está disponível antes Windows 10.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_PROV_UNKNOWN"></span><span id="menroll_e_prov_unknown"></span>**MENROLL \_ E \_ PROV \_ UNKNOWN**
</dt> <dd> <dl> <dt>

0x80180023
</dt> <dt>



Falha no provisionamento, mas um CSP específico não é indicado.

**Windows 8.1:** Essa constante não está disponível antes Windows 10.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_PROV_SSLCERTNOTFOUND"></span><span id="menroll_e_prov_sslcertnotfound"></span>**MENROLL \_ E \_ PROV \_ SSLCERTNOTFOUND**
</dt> <dd> <dl> <dt>

0x80180024
</dt> <dt>



Ao tentar associar o certificado público/chave privada, o certificado público não foi encontrado: ao tentar associar a chave pública de certificado/privado, ou ao examinar a carga de provisionamento (talvez direcionando o repositório errado).

**Windows 8.1:** Essa constante não está disponível antes de Windows 10.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_PROV_CSP_APPMGMT"></span><span id="menroll_e_prov_csp_appmgmt"></span>**MENROLL \_ E \_ Prov \_ CSP \_ APPMGMT**
</dt> <dd> <dl> <dt>

0x80180025
</dt> <dt>



O provisionamento falhou no CSP EnterpriseAppManagement.

> [!Note]  
> essa constante não está disponível antes de Windows 10, versão 1709.

 


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_DEVICE_MANAGEMENT_BLOCKED"></span><span id="menroll_e_device_management_blocked"></span>**MENROLL \_ E \_ Gerenciamento de dispositivo \_ \_ bloqueado**
</dt> <dd> <dl> <dt>

0x80180026
</dt> <dt>



O MDM (gerenciamento de dispositivo móvel) foi bloqueado, possivelmente por Política de Grupo ou pela função [**SetManagedExternally**](/windows/desktop/api/MDMRegistration/nf-mdmregistration-setmanagedexternally) .

> [!Note]  
> essa constante não está disponível antes de Windows 10, versão 1709.

 


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_CERTPOLICY_PRIVATEKEYCREATION_FAILED"></span><span id="menroll_e_certpolicy_privatekeycreation_failed"></span>**falha de MENROLL \_ E \_ CERTPOLICY \_ PRIVATEKEYCREATION \_**
</dt> <dd> <dl> <dt>

0x80180027
</dt> <dt>



Falha ao criar a chave privada.

> [!Note]  
> essa constante não está disponível antes de Windows 10, versão 1709.

 


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_CERTAUTH_FAILED_TO_FIND_CERT"></span><span id="menroll_e_certauth_failed_to_find_cert"></span>**MENROLL \_ E \_ CERTAUTH \_ falhou \_ ao \_ localizar o \_ certificado**
</dt> <dd> <dl> <dt>

0x80180028
</dt> <dt>



A autenticação do certificado foi solicitada, mas falhou ao localizar um certificado a ser usado.

> [!Note]  
> essa constante não está disponível antes de Windows 10, versão 1709.

 


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_EMPTY_MESSAGE"></span><span id="menroll_e_empty_message"></span>**MENROLL \_ E \_ \_ mensagem vazia**
</dt> <dd> <dl> <dt>

0x80180029
</dt> <dt>



O servidor respondeu com HTTP 200, mas a mensagem estava vazia.

> [!Note]  
> essa constante não está disponível antes de Windows 10, versão 1709.

 


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_USER_CANCELED_"></span><span id="menroll_e_user_canceled_"></span>**MENROLL \_ E \_ usuário \_ cancelado** 
</dt> <dd> <dl> <dt>

0x80180030
</dt> <dt>



O usuário cancelou a operação.

> [!Note]  
> essa constante não está disponível antes de Windows 10, versão 1709.

 


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_MDM_NOT_CONFIGURED"></span><span id="menroll_e_mdm_not_configured"></span>**MENROLL \_ E \_ MDM \_ não \_ configurado**
</dt> <dd> <dl> <dt>

0x80180031
</dt> <dt>



O MDM (gerenciamento de dispositivo móvel) não está configurado.

> [!Note]  
> essa constante não está disponível antes de Windows 10, versão 1709.

 


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos

| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8.1<br/>                                                                       |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                    |
| Cabeçalho<br/>                   | <dl> <dt>MDMRegistration. h</dt> </dl> |



 

 





