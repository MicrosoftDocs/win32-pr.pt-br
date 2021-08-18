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
ms.openlocfilehash: bc4140444d1b5c3ae99c90c2447e165a4143b042dcc7567104e4b5f0063b645b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118984236"
---
# <a name="eap-related-error-and-information-constants"></a>Constantes de erro e informações relacionadas a EAP

Grupos individuais de erros e constantes de informações relacionadas a EAP comuns a todas as tecnologias de API do EAPHost.

<dl> <dt>

<span id="EAP_E_EAPHOST_FIRST"></span><span id="eap_e_eaphost_first"></span>**EAP \_ E \_ EAPHost \_ primeiro**
</dt> <dd> <dl> <dt>

0x80420000L
</dt> <dt>



Define o limite dos relatórios de erros; qualquer erro relacionado ao EAPHost ocorrerá entre o **EAP \_ e o \_ EAPHost \_ primeiro** e o **EAP \_ e o \_ EAPHost \_ por último**.


</dt> </dl> </dd> <dt>

<span id="EAP_E_EAPHOST_LAST___"></span><span id="eap_e_eaphost_last___"></span>**EAP \_ E \_ EAPHost \_ por último** 
</dt> <dd> <dl> <dt>

0x804200FFL
</dt> <dt>



Define o limite dos relatórios de erros; qualquer erro relacionado ao EAPHost ocorrerá entre o **EAP \_ e o \_ EAPHost \_ primeiro** e o **EAP \_ e o \_ EAPHost \_ por último**.


</dt> </dl> </dd> <dt>

<span id="EAP_I_EAPHOST_FIRST_"></span><span id="eap_i_eaphost_first_"></span>**EAP \_ I \_ EAPHost \_ primeiro** 
</dt> <dd> <dl> <dt>

0x80420000L
</dt> <dt>



Define o limite de relatórios de informações; qualquer log de eventos informativo relacionado ao EAPHost ocorrerá entre o **EAP \_ i \_ EAPHost \_ primeiro** e o **EAP \_ i \_ EAPHost \_ por último**.


</dt> </dl> </dd> <dt>

<span id="EAP_I_EAPHOST_LAST"></span><span id="eap_i_eaphost_last"></span>**EAP \_ I \_ EAPHost \_ por último**
</dt> <dd> <dl> <dt>

0x804200FFL
</dt> <dt>



Define o limite de relatórios de informações; qualquer log de eventos informativo relacionado ao EAPHost ocorrerá entre o **EAP \_ i \_ EAPHost \_ primeiro** e o **EAP \_ i \_ EAPHost \_ por último**.


</dt> </dl> </dd> <dt>

<span id="EAP_E_CERT_STORE_INACCESSIBLE"></span><span id="eap_e_cert_store_inaccessible"></span>**\_repositório de certificados EAP E \_ \_ \_ inacessível**
</dt> <dd> <dl> <dt>

0x80420011
</dt> <dt>



Nem o autenticador ou o ponto pode acessar o repositório de certificados.


</dt> </dl> </dd> <dt>

<span id="EAP_E_EAPHOST_METHOD_NOT_INSTALLED"></span><span id="eap_e_eaphost_method_not_installed"></span>**\_método EAP \_ E \_ EAPHost \_ não \_ instalado**
</dt> <dd> <dl> <dt>

0x80420011
</dt> <dt>



O método EAP solicitado não está instalado.


</dt> </dl> </dd> <dt>

<span id="EAP_E_EAPHOST_THIRDPARTY_METHOD_HOST_RESET"></span><span id="eap_e_eaphost_thirdparty_method_host_reset"></span>**redefinição do \_ host do método EAP E \_ EAPHost \_ THIRDPARTY \_ \_ \_**
</dt> <dd> <dl> <dt>

0x80420012
</dt> <dt>



O host do método de terceiros não está respondendo e foi reiniciado automaticamente.


</dt> </dl> </dd> <dt>

<span id="EAP_E_EAPHOST_EAPQEC_INACCESSIBLE"></span><span id="eap_e_eaphost_eapqec_inaccessible"></span>**EAP \_ E \_ EAPHost \_ EAPQEC \_ inacessíveis**
</dt> <dd> <dl> <dt>

0x80420013
</dt> <dt>



O EAPHost não é capaz de se comunicar com o [cliente de imposição de quarentena](/windows/desktop/NAP/nap-client-architecture) EAP (QEC) em um cliente habilitado para NAP ( [proteção de acesso à rede](/windows/desktop/NAP/network-access-protection-start-page) ).


</dt> </dl> </dd> <dt>

<span id="EAP_E_EAPHOST_IDENTITY_UNKNOWN"></span><span id="eap_e_eaphost_identity_unknown"></span>**\_ \_ \_ identidade desconhecida de EAP E EAPHost \_**
</dt> <dd> <dl> <dt>

0x80420014
</dt> <dt>



O EAPHost retornará esse erro se o autenticador falhar na autenticação após o envio da identidade do par.


</dt> </dl> </dd> <dt>

<span id="EAP_E_AUTHENTICATION_FAILED"></span><span id="eap_e_authentication_failed"></span>**\_ \_ falha na autenticação de EAP E \_**
</dt> <dd> <dl> <dt>

0x80420015 
</dt> <dt>



O EAPHost retorna esse erro em caso de falha de autenticação.


</dt> </dl> </dd> <dt>

<span id="EAP_I_EAPHOST_EAP_NEGOTIATION_FAILED"></span><span id="eap_i_eaphost_eap_negotiation_failed"></span>**\_ \_ \_ \_ \_ falha na negociação EAP de EAP-EAPHost**
</dt> <dd> <dl> <dt>

0x40420016
</dt> <dt>



O EAPHost registra esse evento de informações quando o cliente e o servidor não estão configurados com tipos EAP compatíveis.


</dt> </dl> </dd> <dt>

<span id="EAP_E_EAPHOST_METHOD_INVALID_PACKET"></span><span id="eap_e_eaphost_method_invalid_packet"></span>**\_pacote de método EAP E \_ EAPHost \_ \_ inválido \_**
</dt> <dd> <dl> <dt>

0x80420017
</dt> <dt>



Um método EAP recebeu um pacote EAP que não pode ser processado. Outro nome para **o \_ método EAP E \_ EAPHost \_ \_ \_ pacote inválido** é **\_ pacote de método EAP \_ inválido \_**.


</dt> </dl> </dd> <dt>

<span id="EAP_E_EAPHOST_REMOTE_INVALID_PACKET"></span><span id="eap_e_eaphost_remote_invalid_packet"></span>**\_pacote inválido de EAP E \_ EAPHost \_ remoto \_ \_**
</dt> <dd> <dl> <dt>

0x80420018
</dt> <dt>



O EAPHost recebeu um pacote que não pode ser processado. Outro nome para **EAP \_ E \_ EAPHost \_ remoto \_ \_** é um pacote inválido de **EAP \_ \_**.


</dt> </dl> </dd> <dt>

<span id="EAP_E_EAPHOST_XML_MALFORMED_"></span><span id="eap_e_eaphost_xml_malformed_"></span>**XML do EAP \_ E \_ EAPHost \_ \_ malformado** 
</dt> <dd> <dl> <dt>

0x80420019
</dt> <dt>



Falha na validação do esquema de configuração EAPHost.


</dt> </dl> </dd> <dt>

<span id="EAP_E_METHOD_CONFIG_DOES_NOT_SUPPORT_SSO"></span><span id="eap_e_method_config_does_not_support_sso"></span>**a \_ configuração do método EAP E \_ \_ \_ \_ não \_ oferece suporte a \_ SSO**
</dt> <dd> <dl> <dt>

0x8042001A
</dt> <dt>



Windows 7 ou posterior: o método EAP não oferece suporte ao sso (logon único) para a configuração fornecida.


</dt> </dl> </dd> <dt>

<span id="EAP_E_EAPHOST_METHOD_OPERATION_NOT_SUPPORTED"></span><span id="eap_e_eaphost_method_operation_not_supported"></span>**\_ \_ \_ \_ \_ não \_ há suporte para a operação do método EAP E EAPHost**
</dt> <dd> <dl> <dt>

0x80420020
</dt> <dt>



O EAPHost retorna esse erro quando um método EAP configurado não dá suporte a uma operação solicitada (chamada de procedimento).


</dt> </dl> </dd> <dt>

<span id="EAP_E_USER_FIRST"></span><span id="eap_e_user_first"></span>**EAP \_ E \_ usuário \_ primeiro**
</dt> <dd> <dl> <dt>

0x80420100L
</dt> <dt>



Define o limite dos relatórios de erros; qualquer erro relacionado ao usuário ocorrerá entre o EAP e o usuário **\_ \_ \_ primeiro** e o **EAP \_ e o \_ usuário \_ por último**.


</dt> </dl> </dd> <dt>

<span id="EAP_E_USER_LAST_"></span><span id="eap_e_user_last_"></span>**EAP \_ E \_ usuário \_ último** 
</dt> <dd> <dl> <dt>

0x804201FFL
</dt> <dt>



Define o limite dos relatórios de erros; qualquer erro relacionado ao usuário ocorrerá entre o EAP e o usuário **\_ \_ \_ primeiro** e o **EAP \_ e o \_ usuário \_ por último**.


</dt> </dl> </dd> <dt>

<span id="EAP_I_USER_FIRST"></span><span id="eap_i_user_first"></span>**EAP \_ I \_ usuário \_ primeiro**
</dt> <dd> <dl> <dt>

0x40420100L
</dt> <dt>



Define o limite de relatórios de informações; qualquer log de eventos informativo relacionado ao EAP ocorrerá entre o **usuário do EAP \_ i \_ \_ primeiro** e o **EAP \_ i \_ user \_ Last**.


</dt> </dl> </dd> <dt>

<span id="EAP_I_USER_LAST"></span><span id="eap_i_user_last"></span>**EAP \_ I \_ usuário \_ último**
</dt> <dd> <dl> <dt>

0x404201FFL
</dt> <dt>



Define o limite de relatórios de informações; qualquer log de eventos informativo relacionado ao EAP ocorrerá entre o **usuário do EAP \_ i \_ \_ primeiro** e o **EAP \_ i \_ user \_ Last**.


</dt> </dl> </dd> <dt>

<span id="EAP_E_USER_CERT_NOT_FOUND"></span><span id="eap_e_user_cert_not_found"></span>**\_certificado EAP E de \_ usuário \_ \_ não \_ encontrado**
</dt> <dd> <dl> <dt>

0x80420100
</dt> <dt>



O EAPHost não pôde localizar um certificado de usuário para autenticação.


</dt> </dl> </dd> <dt>

<span id="EAP_E_USER_CERT_INVALID"></span><span id="eap_e_user_cert_invalid"></span>**EAP \_ E \_ certificado de usuário \_ \_ inválido**
</dt> <dd> <dl> <dt>

0x80420101
</dt> <dt>



O certificado de usuário que está sendo o usuário para autenticação não tem o conjunto de EKU (uso estendido de chave) adequado.


</dt> </dl> </dd> <dt>

<span id="EAP_E_USER_CERT_EXPIRED"></span><span id="eap_e_user_cert_expired"></span>**EAP \_ E \_ certificado de usuário \_ \_ expirados**
</dt> <dd> <dl> <dt>

0x80420102
</dt> <dt>



O EAPhost encontrou um certificado de usuário expirado.


</dt> </dl> </dd> <dt>

<span id="EAP_E_USER_CERT_REVOKED"></span><span id="eap_e_user_cert_revoked"></span>**certificado de usuário do EAP \_ E \_ \_ \_ revogado**
</dt> <dd> <dl> <dt>

0x80420103
</dt> <dt>



O certificado de usuário que está sendo usado para autenticação foi revogado.


</dt> </dl> </dd> <dt>

<span id="EAP_E_USER_CERT_OTHER_ERROR"></span><span id="eap_e_user_cert_other_error"></span>**\_erro de \_ \_ outro certificado \_ de usuário EAP E \_**
</dt> <dd> <dl> <dt>

0x80420104
</dt> <dt>



Ocorreu um erro desconhecido com a certificação de usuário que está sendo usada para autenticação.


</dt> </dl> </dd> <dt>

<span id="EAP_E_USER_CERT_REJECTED_"></span><span id="eap_e_user_cert_rejected_"></span>**EAP \_ E \_ certificado de usuário \_ \_ rejeitados** 
</dt> <dd> <dl> <dt>

0x80420105
</dt> <dt>



O autenticador rejeitou a certificação de usuário.


</dt> </dl> </dd> <dt>

<span id="EAP_I_USER_ACCOUNT_OTHER_ERROR"></span><span id="eap_i_user_account_other_error"></span>**\_erro de \_ \_ outra conta \_ de \_ usuário do EAP**
</dt> <dd> <dl> <dt>

0x40420110
</dt> <dt>



Uma falha de EAP foi recebida após uma troca de identidade, indicando a probabilidade de um problema com a conta do usuário de autenticação.


</dt> </dl> </dd> <dt>

<span id="EAP_E_USER_CREDENTIALS_REJECTED"></span><span id="eap_e_user_credentials_rejected"></span>**\_credenciais de usuário EAP E \_ \_ \_ rejeitadas**
</dt> <dd> <dl> <dt>

0x80420111
</dt> <dt>



O autenticador rejeitou as credenciais de usuário para autenticação.


</dt> </dl> </dd> <dt>

<span id="EAP_E_USER_NAME_PASSWORD_REJECTED"></span><span id="eap_e_user_name_password_rejected"></span>**senha do EAP \_ E do \_ nome de usuário \_ \_ \_ rejeitada**
</dt> <dd> <dl> <dt>

0x80420112
</dt> <dt>



Windows 7 ou posterior: falha na autenticação. O autenticador rejeitou as credenciais do usuário.


</dt> </dl> </dd> <dt>

<span id="EAP_E_NO_SMART_CARD_READER"></span><span id="eap_e_no_smart_card_reader"></span>**EAP \_ E \_ sem \_ \_ leitor de cartão inteligente \_**
</dt> <dd> <dl> <dt>

0x80420113
</dt> <dt>



Windows 7 ou posterior: nenhum leitor de cartão inteligente encontrado.


</dt> </dl> </dd> <dt>

<span id="EAP_E_SERVER_FIRST"></span><span id="eap_e_server_first"></span>**EAP \_ E \_ Server \_ primeiro**
</dt> <dd> <dl> <dt>

0x80420200L
</dt> <dt>



Define o limite dos relatórios de erros; qualquer erro relacionado ao servidor ocorrerá entre o EAP e o servidor **\_ \_ \_ primeiro** e o **EAP \_ e o \_ servidor \_ por último**.


</dt> </dl> </dd> <dt>

<span id="EAP_E_SERVER_LAST"></span><span id="eap_e_server_last"></span>**EAP \_ E \_ SERVER \_ LAST**
</dt> <dd> <dl> <dt>

0x804202FFL
</dt> <dt>



Define o limite de relatórios de erro; qualquer erro relacionado ao servidor ocorrerá entre **EAP \_ E SERVER \_ \_ FIRST** **e EAP E SERVER \_ \_ \_ LAST.**


</dt> </dl> </dd> <dt>

<span id="EAP_E_SERVER_CERT_NOT_FOUND"></span><span id="eap_e_server_cert_not_found"></span>**CERTIFICADO DO \_ SERVIDOR EAP \_ NÃO \_ \_ \_ ENCONTRADO**
</dt> <dd> <dl> <dt>

0x80420200
</dt> <dt>



EAPHost não pôde encontrar o certificado do servidor para autenticação.


</dt> </dl> </dd> <dt>

<span id="EAP_E_SERVER_CERT_INVALID"></span><span id="eap_e_server_cert_invalid"></span>**EAP \_ E \_ SERVER \_ CERT \_ INVALID**
</dt> <dd> <dl> <dt>

0x80420201
</dt> <dt>



O certificado do servidor que está sendo usuário para autenticação não tem um EKU (uso de chave estendido) adequado definido.


</dt> </dl> </dd> <dt>

<span id="EAP_E_SERVER_CERT_EXPIRED"></span><span id="eap_e_server_cert_expired"></span>**CERTIFICADO DO \_ SERVIDOR EAP \_ \_ \_ EXPIRADO**
</dt> <dd> <dl> <dt>

0x80420202
</dt> <dt>



O EAPhost encontrou um certificado de servidor expirado.


</dt> </dl> </dd> <dt>

<span id="EAP_E_SERVER_CERT_REVOKED"></span><span id="eap_e_server_cert_revoked"></span>**EAP \_ E SERVER CERT \_ \_ \_ REVOGADO**
</dt> <dd> <dl> <dt>

0x80420203
</dt> <dt>



O certificado do servidor que está sendo usado para autenticação foi revogado.


</dt> </dl> </dd> <dt>

<span id="EAP_E_SERVER_CERT_OTHER_ERROR"></span><span id="eap_e_server_cert_other_error"></span>**EAP \_ E \_ SERVER \_ CERT \_ OTHER \_ ERROR**
</dt> <dd> <dl> <dt>

0x80420204
</dt> <dt>



Ocorreu um erro desconhecido com o certificado do servidor.


</dt> </dl> </dd> <dt>

<span id="EAP_E_USER_ROOT_CERT_FIRST"></span><span id="eap_e_user_root_cert_first"></span>**EAP \_ E CERTIFICADO RAIZ DO USUÁRIO \_ \_ \_ \_ PRIMEIRO**
</dt> <dd> <dl> <dt>

0x80420300L
</dt> <dt>



Define o limite de relatórios de erro; qualquer erro relacionado ao certificado raiz do usuário ocorrerá entre **EAP \_ E USER ROOT CERT \_ \_ \_ \_ FIRST** e **EAP E USER \_ ROOT CERT \_ \_ \_ \_ FIRST.**


</dt> </dl> </dd> <dt>

<span id="EAP_E_USER_ROOT_CERT_LAST"></span><span id="eap_e_user_root_cert_last"></span>**EAP \_ E CERTIFICADO RAIZ DO USUÁRIO POR \_ \_ \_ \_ ÚLTIMO**
</dt> <dd> <dl> <dt>

0x804203FFL
</dt> <dt>



Define o limite de relatórios de erro; qualquer erro relacionado ao certificado raiz do usuário ocorrerá entre **EAP \_ E USER ROOT CERT \_ \_ \_ \_ FIRST** e **EAP E USER \_ ROOT CERT \_ \_ \_ \_ FIRST.**


</dt> </dl> </dd> <dt>

<span id="EAP_E_USER_ROOT_CERT_NOT_FOUND"></span><span id="eap_e_user_root_cert_not_found"></span>**EAP \_ E CERTIFICADO RAIZ DO USUÁRIO NÃO \_ \_ \_ \_ \_ ENCONTRADO**
</dt> <dd> <dl> <dt>

0x80420300
</dt> <dt>



O EAPHost não pôde encontrar um certificado em um armazenamento de certificados raiz confiável para validação de certificação do usuário.


</dt> </dl> </dd> <dt>

<span id="EAP_E_USER_ROOT_CERT_INVALID"></span><span id="eap_e_user_root_cert_invalid"></span>**EAP \_ E CERTIFICADO RAIZ DO USUÁRIO \_ \_ \_ \_ INVÁLIDO**
</dt> <dd> <dl> <dt>

0x80420301
</dt> <dt>



A autenticação falhou porque o certificado raiz usado para essa rede é inválido.


</dt> </dl> </dd> <dt>

<span id="EAP_E_USER_ROOT_CERT_EXPIRED"></span><span id="eap_e_user_root_cert_expired"></span>**O CERTIFICADO RAIZ DO USUÁRIO DO EAP \_ \_ \_ \_ \_ EXPIROU**
</dt> <dd> <dl> <dt>

0x80420302
</dt> <dt>



O certificado raiz confiável necessário para validação de certificado de usuário expirou.


</dt> </dl> </dd> <dt>

<span id="EAP_E_SERVER_ROOT_CERT_FIRST"></span><span id="eap_e_server_root_cert_first"></span>**CERTIFICADO RAIZ \_ DO SERVIDOR EAP \_ \_ \_ \_ PRIMEIRO**
</dt> <dd> <dl> <dt>

0x80420400L
</dt> <dt>



Define o limite de relatórios de erro; qualquer erro relacionado ao certificado raiz do servidor ocorrerá entre **EAP \_ E SERVER ROOT CERT \_ \_ \_ \_ FIRST** e **EAP E SERVER ROOT \_ \_ CERT \_ \_ \_ FIRST.**


</dt> </dl> </dd> <dt>

<span id="EAP_E_SERVER_ROOT_CERT_LAST"></span><span id="eap_e_server_root_cert_last"></span>**EAP \_ E \_ SERVER \_ ROOT \_ CERT \_ LAST**
</dt> <dd> <dl> <dt>

0x804204FFL
</dt> <dt>



Define o limite de relatórios de erro; qualquer erro relacionado ao certificado raiz do servidor ocorrerá entre **EAP \_ E SERVER ROOT CERT \_ \_ \_ \_ FIRST** e **EAP E SERVER ROOT \_ \_ CERT \_ \_ \_ FIRST.**


</dt> </dl> </dd> <dt>

<span id="EAP_E_SERVER_ROOT_CERT_NOT_FOUND"></span><span id="eap_e_server_root_cert_not_found"></span>**CERTIFICADO RAIZ DO SERVIDOR EAP \_ \_ NÃO \_ \_ \_ \_ ENCONTRADO**
</dt> <dd> <dl> <dt>

0x80420400
</dt> <dt>



O EAPHost não pôde encontrar um certificado raiz em um armazenamento de certificados raiz confiável para a validação de certificação do servidor.


</dt> </dl> </dd> <dt>

<span id="EAP_E_SERVER_ROOT_CERT_INVALID__________"></span><span id="eap_e_server_root_cert_invalid__________"></span>**CERTIFICADO RAIZ \_ DO SERVIDOR EAP \_ \_ \_ \_ INVÁLIDO** 
</dt> <dd> <dl> <dt>

0x80420401
</dt> <dt>



A autenticação falhou porque o certificado do servidor necessário para essa rede no computador servidor é inválido.


</dt> </dl> </dd> <dt>

<span id="EAP_E_SERVER_ROOT_CERT_NAME_REQUIRED"></span><span id="eap_e_server_root_cert_name_required"></span>**EAP \_ E NOME DO CERTIFICADO RAIZ DO SERVIDOR \_ \_ \_ \_ \_ NECESSÁRIO**
</dt> <dd> <dl> <dt>

0x80420406
</dt> <dt>



A autenticação falhou porque o certificado no computador do servidor não tem um nome de servidor especificado.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Comentários

Há nomes alternativos para determinados erros:

-   Outro nome para **O PACOTE INVÁLIDO DO MÉTODO \_ \_ EAPHOST EAPHOST \_ \_ \_** **É EAP METHOD INVALID \_ \_ \_ PACKET**.
-   Outro nome para **EAP \_ \_ EAPHOST \_ REMOTE INVALID PACKET \_ \_ é** **EAP INVALID \_ \_ PACKET**.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                            |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                                      |
| Cabeçalho<br/>                   | <dl> <dt>Eaphosterror.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Constantes comuns de EAPHost](common-eap-host-error-constants.md)
</dt> </dl>

 

