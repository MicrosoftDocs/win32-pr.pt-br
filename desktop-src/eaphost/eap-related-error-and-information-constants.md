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



Windows 7 ou posterior: o método EAP não oferece suporte ao SSO (logon único) para a configuração fornecida.


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

<span id="EAP_E_SERVER_LAST"></span><span id="eap_e_server_last"></span>**EAP \_ E \_ servidor \_ último**
</dt> <dd> <dl> <dt>

0x804202FFL
</dt> <dt>



Define o limite dos relatórios de erros; qualquer erro relacionado ao servidor ocorrerá entre o EAP e o servidor **\_ \_ \_ primeiro** e o **EAP \_ e o \_ servidor \_ por último**.


</dt> </dl> </dd> <dt>

<span id="EAP_E_SERVER_CERT_NOT_FOUND"></span><span id="eap_e_server_cert_not_found"></span>**\_ \_ certificado do servidor EAP E \_ \_ não \_ encontrado**
</dt> <dd> <dl> <dt>

0x80420200
</dt> <dt>



O EAPHost não pôde localizar o certificado do servidor para autenticação.


</dt> </dl> </dd> <dt>

<span id="EAP_E_SERVER_CERT_INVALID"></span><span id="eap_e_server_cert_invalid"></span>**\_ \_ certificado do servidor EAP E \_ \_ inválido**
</dt> <dd> <dl> <dt>

0x80420201
</dt> <dt>



O certificado do servidor sendo o usuário para autenticação não tem um conjunto de EKU (uso estendido de chave) adequado.


</dt> </dl> </dd> <dt>

<span id="EAP_E_SERVER_CERT_EXPIRED"></span><span id="eap_e_server_cert_expired"></span>**\_certificado EAP \_ E \_ servidor \_ expirado**
</dt> <dd> <dl> <dt>

0x80420202
</dt> <dt>



O EAPhost encontrou um certificado de servidor expirado.


</dt> </dl> </dd> <dt>

<span id="EAP_E_SERVER_CERT_REVOKED"></span><span id="eap_e_server_cert_revoked"></span>**\_ \_ certificado do EAP E do servidor \_ \_ revogado**
</dt> <dd> <dl> <dt>

0x80420203
</dt> <dt>



O certificado do servidor que está sendo usado para autenticação foi revogado.


</dt> </dl> </dd> <dt>

<span id="EAP_E_SERVER_CERT_OTHER_ERROR"></span><span id="eap_e_server_cert_other_error"></span>**\_ \_ \_ \_ outro erro de certificado do servidor EAP E \_**
</dt> <dd> <dl> <dt>

0x80420204
</dt> <dt>



Ocorreu um erro desconhecido com o certificado do servidor.


</dt> </dl> </dd> <dt>

<span id="EAP_E_USER_ROOT_CERT_FIRST"></span><span id="eap_e_user_root_cert_first"></span>**EAP \_ E \_ \_ certificado raiz do usuário \_ \_ primeiro**
</dt> <dd> <dl> <dt>

0x80420300L
</dt> <dt>



Define o limite dos relatórios de erros; qualquer erro relacionado ao certificado raiz do usuário ocorrerá entre o EAP e o certificado raiz do **\_ \_ usuário \_ \_ \_ primeiro** e o **\_ \_ \_ certificado raiz do usuário \_ \_ do EAP** e o primeiro.


</dt> </dl> </dd> <dt>

<span id="EAP_E_USER_ROOT_CERT_LAST"></span><span id="eap_e_user_root_cert_last"></span>**EAP \_ E \_ \_ certificado raiz do usuário \_ \_ último**
</dt> <dd> <dl> <dt>

0x804203FFL
</dt> <dt>



Define o limite dos relatórios de erros; qualquer erro relacionado ao certificado raiz do usuário ocorrerá entre o EAP e o certificado raiz do **\_ \_ usuário \_ \_ \_ primeiro** e o **\_ \_ \_ certificado raiz do usuário \_ \_ do EAP** e o primeiro.


</dt> </dl> </dd> <dt>

<span id="EAP_E_USER_ROOT_CERT_NOT_FOUND"></span><span id="eap_e_user_root_cert_not_found"></span>**\_certificado de raiz de usuário E EAP \_ \_ \_ \_ não \_ encontrado**
</dt> <dd> <dl> <dt>

0x80420300
</dt> <dt>



O EAPHost não pôde localizar um certificado em um repositório de certificados raiz confiável para a validação de certificação do usuário.


</dt> </dl> </dd> <dt>

<span id="EAP_E_USER_ROOT_CERT_INVALID"></span><span id="eap_e_user_root_cert_invalid"></span>**EAP \_ E \_ \_ certificado raiz do usuário \_ \_ inválido**
</dt> <dd> <dl> <dt>

0x80420301
</dt> <dt>



A autenticação falhou porque o certificado raiz usado para esta rede é inválido.


</dt> </dl> </dd> <dt>

<span id="EAP_E_USER_ROOT_CERT_EXPIRED"></span><span id="eap_e_user_root_cert_expired"></span>**EAP \_ E \_ \_ certificado raiz de usuário \_ \_ expirados**
</dt> <dd> <dl> <dt>

0x80420302
</dt> <dt>



O certificado raiz confiável necessário para a validação do certificado do usuário expirou.


</dt> </dl> </dd> <dt>

<span id="EAP_E_SERVER_ROOT_CERT_FIRST"></span><span id="eap_e_server_root_cert_first"></span>**\_ \_ certificado raiz do EAP E do servidor \_ \_ \_ primeiro**
</dt> <dd> <dl> <dt>

0x80420400L
</dt> <dt>



Define o limite dos relatórios de erros; qualquer erro relacionado ao certificado raiz do servidor ocorrerá entre o **EAP e o certificado \_ \_ raiz do servidor \_ \_ \_ primeiro** e o **\_ \_ certificado raiz do EAP e do servidor \_ \_ \_ primeiro**.


</dt> </dl> </dd> <dt>

<span id="EAP_E_SERVER_ROOT_CERT_LAST"></span><span id="eap_e_server_root_cert_last"></span>**\_ \_ certificado raiz do EAP E do servidor \_ \_ \_ último**
</dt> <dd> <dl> <dt>

0x804204FFL
</dt> <dt>



Define o limite dos relatórios de erros; qualquer erro relacionado ao certificado raiz do servidor ocorrerá entre o **EAP e o certificado \_ \_ raiz do servidor \_ \_ \_ primeiro** e o **\_ \_ certificado raiz do EAP e do servidor \_ \_ \_ primeiro**.


</dt> </dl> </dd> <dt>

<span id="EAP_E_SERVER_ROOT_CERT_NOT_FOUND"></span><span id="eap_e_server_root_cert_not_found"></span>**\_ \_ certificado raiz do servidor EAP E \_ \_ \_ não \_ encontrado**
</dt> <dd> <dl> <dt>

0x80420400
</dt> <dt>



O EAPHost não pôde localizar um certificado raiz em um repositório de certificados raiz confiável para a validação de certificação do servidor.


</dt> </dl> </dd> <dt>

<span id="EAP_E_SERVER_ROOT_CERT_INVALID__________"></span><span id="eap_e_server_root_cert_invalid__________"></span>**\_ \_ certificado raiz do EAP E do servidor \_ \_ \_ inválido** 
</dt> <dd> <dl> <dt>

0x80420401
</dt> <dt>



A autenticação falhou porque o certificado do servidor necessário para esta rede no computador servidor é inválido.


</dt> </dl> </dd> <dt>

<span id="EAP_E_SERVER_ROOT_CERT_NAME_REQUIRED"></span><span id="eap_e_server_root_cert_name_required"></span>**\_ \_ nome do certificado raiz do EAP E do servidor \_ \_ \_ \_ necessário**
</dt> <dd> <dl> <dt>

0x80420406
</dt> <dt>



A autenticação falhou porque o certificado no computador servidor não tem um nome de servidor especificado.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Comentários

Há nomes alternativos para determinados erros:

-   Outro nome para **o \_ método EAP E \_ EAPHost \_ \_ \_ pacote inválido** é **\_ pacote de método EAP \_ inválido \_**.
-   Outro nome para **EAP \_ E \_ EAPHost \_ remoto \_ \_** é um pacote inválido de **EAP \_ \_**.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                            |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                      |
| parâmetro<br/>                   | <dl> <dt>Eaphosterror. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Constantes do EAPHost comuns](common-eap-host-error-constants.md)
</dt> </dl>

 

