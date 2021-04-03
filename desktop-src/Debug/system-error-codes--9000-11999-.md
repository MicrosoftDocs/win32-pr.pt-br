---
description: Descreve os códigos de erro 9000-11999 definidos no arquivo de cabeçalho WinError. h e destina-se a desenvolvedores.
ms.assetid: 27fe3fee-4ae3-43f1-a1f2-91c935e9851b
title: Códigos de erro do sistema (9000-11999) (WinError. h)
ms.topic: reference
ms.date: 07/18/2019
ms.openlocfilehash: 01eb071962d8d0f5beb801067ce1d72adc796bad
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646369"
---
# <a name="system-error-codes-9000-11999"></a>Códigos de erro do sistema (9000-11999)

> [!NOTE]
> Essas informações destinam-se a desenvolvedores Depurando erros do sistema. Para outros erros, como problemas com Windows Update, há uma lista de recursos na página códigos de [erro](system-error-codes.md) .

A lista a seguir descreve os [códigos de erro do sistema](system-error-codes.md) (erros 9000 a 11999). Elas são retornadas pela função [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) quando muitas funções falham. Para recuperar o texto de descrição do erro em seu aplicativo, use a função [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) com a **mensagem de formato \_ \_ do sinalizador do \_ sistema** .

<dl> <dt>

<span id="DNS_ERROR_RCODE_FORMAT_ERROR"></span><span id="dns_error_rcode_format_error"></span>**erro \_ de \_ RCODE de \_ formato de \_ erro DNS**
</dt> <dd> <dl> <dt>

9001 (0x2329)
</dt> <dt>



O servidor DNS não pode interpretar o formato.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_RCODE_SERVER_FAILURE"></span><span id="dns_error_rcode_server_failure"></span>**erro de DNS \_ \_ RCODE \_ falha do servidor \_**
</dt> <dd> <dl> <dt>

9002 (0x232A)
</dt> <dt>



Falha do servidor DNS.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_RCODE_NAME_ERROR"></span><span id="dns_error_rcode_name_error"></span>**erro \_ DNS \_ RCODE \_ nome \_ do erro**
</dt> <dd> <dl> <dt>

9003 (0x232B)
</dt> <dt>



O nome do DNS não existe.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_RCODE_NOT_IMPLEMENTED"></span><span id="dns_error_rcode_not_implemented"></span>**\_RCODE de erro DNS \_ \_ não \_ implementado**
</dt> <dd> <dl> <dt>

9004 (0x232C)
</dt> <dt>



O servidor de nomes não dá suporte à solicitação DNS.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_RCODE_REFUSED"></span><span id="dns_error_rcode_refused"></span>**erro de DNS \_ \_ RCODE \_ recusado**
</dt> <dd> <dl> <dt>

9005 (0x232D)
</dt> <dt>



Operação DNS recusada.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_RCODE_YXDOMAIN"></span><span id="dns_error_rcode_yxdomain"></span>**erro de DNS \_ \_ RCODE \_ YXDOMAIN**
</dt> <dd> <dl> <dt>

9006 (0x232E)
</dt> <dt>



O nome DNS que não deveria existir, existe.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_RCODE_YXRRSET"></span><span id="dns_error_rcode_yxrrset"></span>**erro de DNS \_ \_ RCODE \_ YXRRSET**
</dt> <dd> <dl> <dt>

9007 (0x232F)
</dt> <dt>



O conjunto de RR DNS que não deveria existir, existe.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_RCODE_NXRRSET"></span><span id="dns_error_rcode_nxrrset"></span>**erro de DNS \_ \_ RCODE \_ NXRRSET**
</dt> <dd> <dl> <dt>

9008 (0x2330)
</dt> <dt>



O conjunto de RR do DNS que deveria existir não existe.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_RCODE_NOTAUTH"></span><span id="dns_error_rcode_notauth"></span>**erro de DNS \_ \_ RCODE não \_ auth**
</dt> <dd> <dl> <dt>

9009 (0x2331)
</dt> <dt>



O servidor DNS não é autoritativo para a zona.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_RCODE_NOTZONE"></span><span id="dns_error_rcode_notzone"></span>**erro de DNS \_ \_ RCODE não \_ zona**
</dt> <dd> <dl> <dt>

9010 (0x2332)
</dt> <dt>



O nome DNS na atualização ou pré-requisito não está na zona.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_RCODE_BADSIG"></span><span id="dns_error_rcode_badsig"></span>**erro de DNS \_ \_ RCODE \_ BADSIG**
</dt> <dd> <dl> <dt>

9016 (0x2338)
</dt> <dt>



Falha na verificação da assinatura DNS.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_RCODE_BADKEY"></span><span id="dns_error_rcode_badkey"></span>**erro de DNS \_ \_ RCODE \_ BADKEY**
</dt> <dd> <dl> <dt>

9017 (0x2339)
</dt> <dt>



Chave inadequada do DNS.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_RCODE_BADTIME"></span><span id="dns_error_rcode_badtime"></span>**erro de DNS \_ \_ RCODE \_ Badtime**
</dt> <dd> <dl> <dt>

9018 (0x233A)
</dt> <dt>



Validade da assinatura DNS expirada.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_KEYMASTER_REQUIRED"></span><span id="dns_error_keymaster_required"></span>**o mestre de erro de DNS é \_ \_ \_ necessário**
</dt> <dd> <dl> <dt>

9101 (0x238D)
</dt> <dt>



Somente o servidor DNS que atua como mestre de chave para a zona pode executar esta operação.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_NOT_ALLOWED_ON_SIGNED_ZONE"></span><span id="dns_error_not_allowed_on_signed_zone"></span>**\_erro \_ de DNS não \_ permitido \_ em \_ zona assinada \_**
</dt> <dd> <dl> <dt>

9102 (0x238E)
</dt> <dt>



Esta operação não é permitida em uma zona assinada ou tem chaves de assinatura.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_NSEC3_INCOMPATIBLE_WITH_RSA_SHA1"></span><span id="dns_error_nsec3_incompatible_with_rsa_sha1"></span>**DNS \_ \_ de erro \_ de NSEC3 incompatível \_ com \_ RSA \_ SHA1**
</dt> <dd> <dl> <dt>

9103 (0x238F)
</dt> <dt>



O NSEC3 não é compatível com o algoritmo RSA-SHA-1. Escolha um algoritmo diferente ou use NSEC.

Esse valor também foi nomeado **DNS \_ erro \_ \_ \_ parâmetros de NSEC3 inválido**


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_NOT_ENOUGH_SIGNING_KEY_DESCRIPTORS"></span><span id="dns_error_not_enough_signing_key_descriptors"></span>**erro de DNS \_ \_ não \_ há \_ \_ descritores de chave de assinatura suficientes \_**
</dt> <dd> <dl> <dt>

9104 (0x2390)
</dt> <dt>



A zona não tem chaves de assinatura suficientes. Deve haver pelo menos uma KSK (chave de assinatura de chave) e pelo menos uma ZSK (chave de assinatura de zona).


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_UNSUPPORTED_ALGORITHM"></span><span id="dns_error_unsupported_algorithm"></span>**algoritmo de erro de DNS \_ \_ sem suporte \_**
</dt> <dd> <dl> <dt>

9105 (0x2391)
</dt> <dt>



Não há suporte para o algoritmo especificado.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_INVALID_KEY_SIZE"></span><span id="dns_error_invalid_key_size"></span>**\_tamanho de \_ \_ chave inválido do erro \_ DNS**
</dt> <dd> <dl> <dt>

9106 (0x2392)
</dt> <dt>



Não há suporte para o tamanho de chave especificado.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_SIGNING_KEY_NOT_ACCESSIBLE"></span><span id="dns_error_signing_key_not_accessible"></span>**\_chave de assinatura de erro DNS \_ \_ \_ não \_ acessível**
</dt> <dd> <dl> <dt>

9107 (0x2393)
</dt> <dt>



Uma ou mais das chaves de assinatura de uma zona não podem ser acessadas pelo servidor DNS. A assinatura de zona não estará operacional até que esse erro seja resolvido.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_KSP_DOES_NOT_SUPPORT_PROTECTION"></span><span id="dns_error_ksp_does_not_support_protection"></span>**\_o KSP de erro DNS não \_ \_ \_ \_ oferece suporte à \_ proteção**
</dt> <dd> <dl> <dt>

9108 (0x2394)
</dt> <dt>



O provedor de armazenamento de chaves especificado não dá suporte à proteção de dados DPAPI + +. A assinatura de zona não estará operacional até que esse erro seja resolvido.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_UNEXPECTED_DATA_PROTECTION_ERROR"></span><span id="dns_error_unexpected_data_protection_error"></span>**erro \_ de \_ \_ proteção de dados inesperada \_ \_ do DNS**
</dt> <dd> <dl> <dt>

9109 (0x2395)
</dt> <dt>



Foi encontrado um erro não esperado DPAPI + +. A assinatura de zona não estará operacional até que esse erro seja resolvido.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_UNEXPECTED_CNG_ERROR"></span><span id="dns_error_unexpected_cng_error"></span>**erro \_ de \_ CNG inesperado de erro DNS \_ \_**
</dt> <dd> <dl> <dt>

9110 (0x2396)
</dt> <dt>



Foi encontrado um erro de criptografia inesperado. A assinatura de zona pode não estar operacional até que esse erro seja resolvido.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_UNKNOWN_SIGNING_PARAMETER_VERSION"></span><span id="dns_error_unknown_signing_parameter_version"></span>**\_erro DNS \_ versão desconhecida do \_ parâmetro de assinatura \_ \_**
</dt> <dd> <dl> <dt>

9111 (0x2397)
</dt> <dt>



O servidor DNS encontrou uma chave de assinatura com uma versão desconhecida. A assinatura de zona não estará operacional até que esse erro seja resolvido.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_KSP_NOT_ACCESSIBLE"></span><span id="dns_error_ksp_not_accessible"></span>**\_KSP de erro DNS \_ \_ não \_ acessível**
</dt> <dd> <dl> <dt>

9112 (0x2398)
</dt> <dt>



O provedor de serviços de chave especificado não pode ser aberto pelo servidor DNS.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_TOO_MANY_SKDS"></span><span id="dns_error_too_many_skds"></span>**erro de DNS em excesso de \_ \_ \_ \_ SKDS**
</dt> <dd> <dl> <dt>

9113 (0x2399)
</dt> <dt>



O servidor DNS não pode aceitar mais chaves de assinatura com o algoritmo especificado e o valor do sinalizador KSK para essa zona.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_INVALID_ROLLOVER_PERIOD"></span><span id="dns_error_invalid_rollover_period"></span>**erro de DNS \_ \_ \_ período de substituição inválido \_**
</dt> <dd> <dl> <dt>

9114 (0x239A)
</dt> <dt>



O período de substituição especificado é inválido.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_INVALID_INITIAL_ROLLOVER_OFFSET"></span><span id="dns_error_invalid_initial_rollover_offset"></span>**erro de DNS \_ \_ \_ deslocamento de substituição inicial inválido \_ \_**
</dt> <dd> <dl> <dt>

9115 (0x239B)
</dt> <dt>



O deslocamento de substituição inicial especificado é inválido.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_ROLLOVER_IN_PROGRESS"></span><span id="dns_error_rollover_in_progress"></span>**\_ \_ substituição de erro \_ de DNS em \_ andamento**
</dt> <dd> <dl> <dt>

9116 (0x239C)
</dt> <dt>



A chave de assinatura especificada já está em processo de substituição de chaves.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_STANDBY_KEY_NOT_PRESENT"></span><span id="dns_error_standby_key_not_present"></span>**a \_ chave de espera de erro DNS \_ \_ \_ não \_ está presente**
</dt> <dd> <dl> <dt>

9117 (0x239D)
</dt> <dt>



A chave de assinatura especificada não tem uma chave em espera para revogar.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_NOT_ALLOWED_ON_ZSK"></span><span id="dns_error_not_allowed_on_zsk"></span>**\_erro \_ de DNS não \_ permitido \_ em \_ ZSK**
</dt> <dd> <dl> <dt>

9118 (0x239E)
</dt> <dt>



Esta operação não é permitida em uma ZSK (chave de assinatura de zona).


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_NOT_ALLOWED_ON_ACTIVE_SKD"></span><span id="dns_error_not_allowed_on_active_skd"></span>**\_erro \_ de DNS não \_ permitido \_ no \_ \_ SKD ativo**
</dt> <dd> <dl> <dt>

9119 (0x239F)
</dt> <dt>



Esta operação não é permitida em uma chave de assinatura ativa.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_ROLLOVER_ALREADY_QUEUED"></span><span id="dns_error_rollover_already_queued"></span>**\_substituição de erro DNS \_ \_ já \_ colocada na fila**
</dt> <dd> <dl> <dt>

9120 (0x23A0)
</dt> <dt>



A chave de assinatura especificada já está na fila para substituição.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_NOT_ALLOWED_ON_UNSIGNED_ZONE"></span><span id="dns_error_not_allowed_on_unsigned_zone"></span>**\_erro \_ de DNS não \_ permitido \_ em \_ zona não assinada \_**
</dt> <dd> <dl> <dt>

9121 (0x23A1)
</dt> <dt>



Esta operação não é permitida em uma zona não assinada.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_BAD_KEYMASTER"></span><span id="dns_error_bad_keymaster"></span>**erro de DNS- \_ \_ mestre inadequado \_**
</dt> <dd> <dl> <dt>

9122 (0x23A2)
</dt> <dt>



Esta operação não pôde ser concluída porque o servidor DNS listado como o mestre de chave atual para esta zona está inoperante ou configurado incorretamente. Resolva o problema no mestre de chave atual dessa zona ou use outro servidor DNS para executar a função mestre de chave.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_INVALID_SIGNATURE_VALIDITY_PERIOD"></span><span id="dns_error_invalid_signature_validity_period"></span>**erro de DNS \_ \_ período de \_ validade de assinatura inválido \_ \_**
</dt> <dd> <dl> <dt>

9123 (0x23A3)
</dt> <dt>



O período de validade da assinatura especificado é inválido.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_INVALID_NSEC3_ITERATION_COUNT"></span><span id="dns_error_invalid_nsec3_iteration_count"></span>**\_Erro DNS \_ \_ contagem de \_ iteração NSEC3 inválida \_**
</dt> <dd> <dl> <dt>

9124 (0x23A4)
</dt> <dt>



A contagem de iteração NSEC3 especificada é maior do que a permitida pelo comprimento mínimo de chave usado na zona.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_DNSSEC_IS_DISABLED"></span><span id="dns_error_dnssec_is_disabled"></span>**erro DNS o \_ \_ DNSSEC \_ está \_ desabilitado**
</dt> <dd> <dl> <dt>

9125 (0x23A5)
</dt> <dt>



Esta operação não pôde ser concluída porque o servidor DNS foi configurado com recursos de DNSSEC desabilitados. Habilite o DNSSEC no servidor DNS.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_INVALID_XML"></span><span id="dns_error_invalid_xml"></span>**\_ \_ XML inválido de erro DNS \_**
</dt> <dd> <dl> <dt>

9126 (0x23A6)
</dt> <dt>



Esta operação não pôde ser concluída porque o fluxo XML recebido está vazio ou é sintaticamente inválido.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_NO_VALID_TRUST_ANCHORS"></span><span id="dns_error_no_valid_trust_anchors"></span>**erro de DNS \_ \_ sem \_ \_ âncoras de confiança válidas \_**
</dt> <dd> <dl> <dt>

9127 (0x23A7)
</dt> <dt>



Esta operação foi concluída, mas nenhuma âncora de confiança foi adicionada porque todas as âncoras de confiança recebidas eram inválidas, sem suporte, expiraram ou não se tornarão válidas em menos de 30 dias.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_ROLLOVER_NOT_POKEABLE"></span><span id="dns_error_rollover_not_pokeable"></span>**substituição de erro de DNS \_ \_ \_ não \_ puder ser acessada**
</dt> <dd> <dl> <dt>

9128 (0x23A8)
</dt> <dt>



A chave de assinatura especificada não está aguardando a atualização do DS pai.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_NSEC3_NAME_COLLISION"></span><span id="dns_error_nsec3_name_collision"></span>**Erro de DNS \_ \_ colisão de nome de NSEC3 \_ \_**
</dt> <dd> <dl> <dt>

9129 (0x23A9)
</dt> <dt>



Colisão de hash detectada durante assinatura de NSEC3. Especifique um Salt fornecido pelo usuário diferente ou use um Salt gerado aleatoriamente e tente assinar a zona novamente.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_NSEC_INCOMPATIBLE_WITH_NSEC3_RSA_SHA1"></span><span id="dns_error_nsec_incompatible_with_nsec3_rsa_sha1"></span>**\_Erro DNS \_ \_ de NSEC incompatível \_ com \_ NSEC3 \_ RSA \_ SHA1**
</dt> <dd> <dl> <dt>

9130 (0x23AA)
</dt> <dt>



NSEC não é compatível com o algoritmo NSEC3-RSA-SHA-1. Escolha um algoritmo diferente ou use NSEC3.


</dt> </dl> </dd> <dt>

<span id="DNS_INFO_NO_RECORDS"></span><span id="dns_info_no_records"></span>**informações de DNS \_ \_ sem \_ registros**
</dt> <dd> <dl> <dt>

9501 (0x251D)
</dt> <dt>



Não foram encontrados registros para uma determinada consulta ao DNS.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_BAD_PACKET"></span><span id="dns_error_bad_packet"></span>**erro DNS de \_ \_ pacote insatisfatório \_**
</dt> <dd> <dl> <dt>

9502 (0x251E)
</dt> <dt>



Pacote DNS inadequado.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_NO_PACKET"></span><span id="dns_error_no_packet"></span>**erro de DNS \_ \_ sem \_ pacote**
</dt> <dd> <dl> <dt>

9503 (0x251F)
</dt> <dt>



Nenhum pacote DNS.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_RCODE"></span><span id="dns_error_rcode"></span>**erro de DNS \_ \_ RCODE**
</dt> <dd> <dl> <dt>

9504 (0x2520)
</dt> <dt>



Erro de DNS, verifique RCODE.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_UNSECURE_PACKET"></span><span id="dns_error_unsecure_packet"></span>**pacote de erro de DNS \_ \_ não seguro \_**
</dt> <dd> <dl> <dt>

9505 (0x2521)
</dt> <dt>



Pacote DNS não seguro.


</dt> </dl> </dd> <dt>

<span id="DNS_REQUEST_PENDING"></span><span id="dns_request_pending"></span>**solicitação de DNS \_ \_ pendente**
</dt> <dd> <dl> <dt>

9506 (0x2522)
</dt> <dt>



A solicitação de consulta DNS está pendente.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_INVALID_TYPE"></span><span id="dns_error_invalid_type"></span>**\_ \_ tipo inválido de erro DNS \_**
</dt> <dd> <dl> <dt>

9551 (0x254F)
</dt> <dt>



Tipo DNS inválido.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_INVALID_IP_ADDRESS"></span><span id="dns_error_invalid_ip_address"></span>**\_ \_ \_ endereço IP inválido do erro DNS \_**
</dt> <dd> <dl> <dt>

9552 (0x2550)
</dt> <dt>



Endereço IP inválido.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_INVALID_PROPERTY"></span><span id="dns_error_invalid_property"></span>**\_ \_ Propriedade inválida de erro DNS \_**
</dt> <dd> <dl> <dt>

9553 (0x2551)
</dt> <dt>



Propriedade inválida.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_TRY_AGAIN_LATER"></span><span id="dns_error_try_again_later"></span>**erro de DNS \_ \_ tente \_ novamente \_ mais tarde**
</dt> <dd> <dl> <dt>

9554 (0x2552)
</dt> <dt>



Tente a operação DNS novamente mais tarde.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_NOT_UNIQUE"></span><span id="dns_error_not_unique"></span>**erro de DNS \_ \_ não \_ exclusivo**
</dt> <dd> <dl> <dt>

9555 (0x2553)
</dt> <dt>



O registro para o nome e tipo fornecidos não é exclusivo.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_NON_RFC_NAME"></span><span id="dns_error_non_rfc_name"></span>**\_erro DNS \_ não \_ RFC \_ nome**
</dt> <dd> <dl> <dt>

9556 (0x2554)
</dt> <dt>



O nome DNS não está em conformidade com as especificações RFC.


</dt> </dl> </dd> <dt>

<span id="DNS_STATUS_FQDN"></span><span id="dns_status_fqdn"></span>**\_FQDN de status DNS \_**
</dt> <dd> <dl> <dt>

9557 (0x2555)
</dt> <dt>



O nome DNS é um nome DNS totalmente qualificado.


</dt> </dl> </dd> <dt>

<span id="DNS_STATUS_DOTTED_NAME"></span><span id="dns_status_dotted_name"></span>**nome do DNS de \_ status \_ pontilhado \_**
</dt> <dd> <dl> <dt>

9558 (0x2556)
</dt> <dt>



O nome DNS é pontilhado (vários rótulos).


</dt> </dl> </dd> <dt>

<span id="DNS_STATUS_SINGLE_PART_NAME"></span><span id="dns_status_single_part_name"></span>**\_nome de \_ \_ parte única do status \_ DNS**
</dt> <dd> <dl> <dt>

9559 (0x2557)
</dt> <dt>



O nome DNS é um nome de parte única.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_INVALID_NAME_CHAR"></span><span id="dns_error_invalid_name_char"></span>**erro de DNS \_ \_ \_ nome inválido \_ Char**
</dt> <dd> <dl> <dt>

9560 (0x2558)
</dt> <dt>



O nome DNS contém um caractere inválido.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_NUMERIC_NAME"></span><span id="dns_error_numeric_name"></span>**\_ \_ nome numérico do erro DNS \_**
</dt> <dd> <dl> <dt>

9561 (0x2559)
</dt> <dt>



O nome DNS é totalmente numérico.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_NOT_ALLOWED_ON_ROOT_SERVER"></span><span id="dns_error_not_allowed_on_root_server"></span>**\_erro \_ de DNS não \_ permitido \_ no \_ \_ servidor raiz**
</dt> <dd> <dl> <dt>

9562 (0x255A)
</dt> <dt>



A operação solicitada não é permitida em um servidor raiz DNS.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_NOT_ALLOWED_UNDER_DELEGATION"></span><span id="dns_error_not_allowed_under_delegation"></span>**erro de DNS \_ \_ não \_ permitido \_ em \_ delegação**
</dt> <dd> <dl> <dt>

9563 (0x255B)
</dt> <dt>



Não foi possível criar o registro porque esta parte do namespace DNS foi delegada a outro servidor.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_CANNOT_FIND_ROOT_HINTS"></span><span id="dns_error_cannot_find_root_hints"></span>**erro de DNS \_ \_ não pode \_ localizar \_ dicas de raiz \_**
</dt> <dd> <dl> <dt>

9564 (0x255C)
</dt> <dt>



O servidor DNS não pôde encontrar um conjunto de dicas de raiz.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_INCONSISTENT_ROOT_HINTS"></span><span id="dns_error_inconsistent_root_hints"></span>**\_dicas de \_ raiz inconsistentes de erro DNS \_ \_**
</dt> <dd> <dl> <dt>

9565 (0x255D)
</dt> <dt>



O servidor DNS encontrou dicas de raiz, mas elas não eram consistentes em todos os adaptadores.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_DWORD_VALUE_TOO_SMALL"></span><span id="dns_error_dword_value_too_small"></span>**valor de DWORD de erro de DNS \_ \_ \_ \_ muito \_ pequeno**
</dt> <dd> <dl> <dt>

9566 (0x255E)
</dt> <dt>



O valor especificado é muito pequeno para esse parâmetro.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_DWORD_VALUE_TOO_LARGE"></span><span id="dns_error_dword_value_too_large"></span>**valor de DWORD de erro de DNS \_ \_ \_ \_ muito \_ grande**
</dt> <dd> <dl> <dt>

9567 (0x255F)
</dt> <dt>



O valor especificado é muito grande para esse parâmetro.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_BACKGROUND_LOADING"></span><span id="dns_error_background_loading"></span>**\_ \_ carregamento em segundo plano de erro DNS \_**
</dt> <dd> <dl> <dt>

9568 (0x2560)
</dt> <dt>



Esta operação não é permitida enquanto o servidor DNS está carregando zonas em segundo plano. Tente novamente mais tarde.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_NOT_ALLOWED_ON_RODC"></span><span id="dns_error_not_allowed_on_rodc"></span>**\_erro \_ de DNS não \_ permitido \_ no \_ RODC**
</dt> <dd> <dl> <dt>

9569 (0x2561)
</dt> <dt>



A operação solicitada não é permitida em um servidor DNS em execução em um controlador de domínio somente leitura.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_NOT_ALLOWED_UNDER_DNAME"></span><span id="dns_error_not_allowed_under_dname"></span>**erro de DNS \_ \_ não \_ permitido \_ sob \_ dname**
</dt> <dd> <dl> <dt>

9570 (0x2562)
</dt> <dt>



Nenhum dado pode existir sob um registro DNAME.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_DELEGATION_REQUIRED"></span><span id="dns_error_delegation_required"></span>**Delegação de erro de DNS \_ \_ \_ necessária**
</dt> <dd> <dl> <dt>

9571 (0x2563)
</dt> <dt>



Esta operação requer delegação de credenciais.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_INVALID_POLICY_TABLE"></span><span id="dns_error_invalid_policy_table"></span>**\_tabela de política de erro DNS \_ inválido \_ \_**
</dt> <dd> <dl> <dt>

9572 (0x2564)
</dt> <dt>



A tabela de políticas de resolução de nomes foi corrompida. A resolução de DNS falhará até que seja corrigida. Entre em contato com o administrador de rede.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_ZONE_DOES_NOT_EXIST"></span><span id="dns_error_zone_does_not_exist"></span>**a \_ zona de erro DNS não \_ \_ \_ \_ existe**
</dt> <dd> <dl> <dt>

9601 (0x2581)
</dt> <dt>



A zona DNS não existe.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_NO_ZONE_INFO"></span><span id="dns_error_no_zone_info"></span>**erro de DNS \_ \_ sem \_ informações de zona \_**
</dt> <dd> <dl> <dt>

9602 (0x2582)
</dt> <dt>



Informações de zona DNS não disponíveis.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_INVALID_ZONE_OPERATION"></span><span id="dns_error_invalid_zone_operation"></span>**\_operação de \_ zona inválida de erro \_ DNS \_**
</dt> <dd> <dl> <dt>

9603 (0x2583)
</dt> <dt>



Operação inválida para a zona DNS.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_ZONE_CONFIGURATION_ERROR"></span><span id="dns_error_zone_configuration_error"></span>**\_erro de \_ configuração de zona de erro DNS \_ \_**
</dt> <dd> <dl> <dt>

9604 (0x2584)
</dt> <dt>



Configuração de zona DNS inválida.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_ZONE_HAS_NO_SOA_RECORD"></span><span id="dns_error_zone_has_no_soa_record"></span>**a \_ zona de erro DNS \_ \_ \_ não tem \_ \_ registro soa**
</dt> <dd> <dl> <dt>

9605 (0x2585)
</dt> <dt>



A zona DNS não tem registro de início de autoridade (SOA).


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_ZONE_HAS_NO_NS_RECORDS"></span><span id="dns_error_zone_has_no_ns_records"></span>**a \_ zona de erro DNS \_ \_ \_ não tem \_ \_ registros NS**
</dt> <dd> <dl> <dt>

9606 (0x2586)
</dt> <dt>



A zona DNS não tem registro de servidor de nomes (NS).


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_ZONE_LOCKED"></span><span id="dns_error_zone_locked"></span>**\_zona de erro DNS \_ \_ bloqueada**
</dt> <dd> <dl> <dt>

9607 (0x2587)
</dt> <dt>



A zona DNS está bloqueada.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_ZONE_CREATION_FAILED"></span><span id="dns_error_zone_creation_failed"></span>**\_ \_ \_ falha na criação de zona de erro DNS \_**
</dt> <dd> <dl> <dt>

9608 (0x2588)
</dt> <dt>



Falha na criação da zona DNS.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_ZONE_ALREADY_EXISTS"></span><span id="dns_error_zone_already_exists"></span>**a \_ zona de erro DNS \_ \_ já \_ existe**
</dt> <dd> <dl> <dt>

9609 (0x2589)
</dt> <dt>



A zona DNS já existe.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_AUTOZONE_ALREADY_EXISTS"></span><span id="dns_error_autozone_already_exists"></span>**a \_ AUTOzona de erro DNS \_ \_ já \_ existe**
</dt> <dd> <dl> <dt>

9610 (0x258A)
</dt> <dt>



A zona automática de DNS já existe.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_INVALID_ZONE_TYPE"></span><span id="dns_error_invalid_zone_type"></span>**\_erro DNS \_ \_ tipo de zona inválido \_**
</dt> <dd> <dl> <dt>

9611 (0x258B)
</dt> <dt>



Tipo de zona DNS inválido.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_SECONDARY_REQUIRES_MASTER_IP"></span><span id="dns_error_secondary_requires_master_ip"></span>**o \_ erro de DNS \_ secundário \_ requer \_ \_ IP mestre**
</dt> <dd> <dl> <dt>

9612 (0x258C)
</dt> <dt>



A zona DNS secundária requer um endereço IP mestre.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_ZONE_NOT_SECONDARY"></span><span id="dns_error_zone_not_secondary"></span>**\_zona de erro DNS \_ \_ não \_ secundária**
</dt> <dd> <dl> <dt>

9613 (0x258D)
</dt> <dt>



Zona DNS não secundária.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_NEED_SECONDARY_ADDRESSES"></span><span id="dns_error_need_secondary_addresses"></span>**erro de DNS \_ \_ precisa de \_ endereços secundários \_**
</dt> <dd> <dl> <dt>

9614 (0x258E)
</dt> <dt>



É necessário um endereço IP secundário.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_WINS_INIT_FAILED"></span><span id="dns_error_wins_init_failed"></span>**\_erro DNS \_ \_ \_ falha na inicialização do WINS**
</dt> <dd> <dl> <dt>

9615 (0x258F)
</dt> <dt>



Falha na inicialização do WINS.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_NEED_WINS_SERVERS"></span><span id="dns_error_need_wins_servers"></span>**o \_ erro DNS \_ precisa de \_ \_ servidores WINS**
</dt> <dd> <dl> <dt>

9616 (0x2590)
</dt> <dt>



Servidores WINS necessários.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_NBSTAT_INIT_FAILED"></span><span id="dns_error_nbstat_init_failed"></span>**\_erro de \_ DNS \_ \_ falha na inicialização de NBSTAT**
</dt> <dd> <dl> <dt>

9617 (0x2591)
</dt> <dt>



Falha na chamada de inicialização de NBTSTAT.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_SOA_DELETE_INVALID"></span><span id="dns_error_soa_delete_invalid"></span>**\_exclusão de soa de erro DNS \_ \_ \_ inválida**
</dt> <dd> <dl> <dt>

9618 (0x2592)
</dt> <dt>



Exclusão de início de autoridade (SOA) inválida.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_FORWARDER_ALREADY_EXISTS"></span><span id="dns_error_forwarder_already_exists"></span>**o \_ encaminhador de erro DNS \_ \_ já \_ existe**
</dt> <dd> <dl> <dt>

9619 (0x2593)
</dt> <dt>



Já existe uma zona de encaminhamento condicional para esse nome.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_ZONE_REQUIRES_MASTER_IP"></span><span id="dns_error_zone_requires_master_ip"></span>**a \_ zona de erro DNS \_ requer o \_ \_ \_ IP mestre**
</dt> <dd> <dl> <dt>

9620 (0x2594)
</dt> <dt>



Essa zona deve ser configurada com um ou mais endereços IP do servidor DNS mestre.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_ZONE_IS_SHUTDOWN"></span><span id="dns_error_zone_is_shutdown"></span>**a \_ zona de erro DNS \_ \_ está \_ desligada**
</dt> <dd> <dl> <dt>

9621 (0x2595)
</dt> <dt>



A operação não pode ser executada porque esta zona está desligada.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_ZONE_LOCKED_FOR_SIGNING"></span><span id="dns_error_zone_locked_for_signing"></span>**\_ \_ zona de erro DNS \_ bloqueada \_ para \_ assinatura**
</dt> <dd> <dl> <dt>

9622 (0x2596)
</dt> <dt>



Esta operação não pode ser executada porque a zona está sendo assinada no momento. Tente novamente mais tarde.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_PRIMARY_REQUIRES_DATAFILE"></span><span id="dns_error_primary_requires_datafile"></span>**o \_ erro de DNS \_ primário \_ requer o \_ DataFile**
</dt> <dd> <dl> <dt>

9651 (0x25B3)
</dt> <dt>



A zona DNS primária requer o DataFile.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_INVALID_DATAFILE_NAME"></span><span id="dns_error_invalid_datafile_name"></span>**\_nome de \_ \_ DataFile inválido do erro \_ DNS**
</dt> <dd> <dl> <dt>

9652 (0x25B4)
</dt> <dt>



Nome de DataFile inválido para a zona DNS.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_DATAFILE_OPEN_FAILURE"></span><span id="dns_error_datafile_open_failure"></span>**\_falha de \_ abertura de DataFile de erro DNS \_ \_**
</dt> <dd> <dl> <dt>

9653 (0x25B5)
</dt> <dt>



Falha ao abrir o DataFile para a zona DNS.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_FILE_WRITEBACK_FAILED"></span><span id="dns_error_file_writeback_failed"></span>**\_ \_ \_ falha no write-back do arquivo de erro DNS \_**
</dt> <dd> <dl> <dt>

9654 (0x25B6)
</dt> <dt>



Falha ao gravar o arquivo de configuração para a zona DNS.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_DATAFILE_PARSING"></span><span id="dns_error_datafile_parsing"></span>**erro de DNS \_ \_ análise de DataFile \_**
</dt> <dd> <dl> <dt>

9655 (0x25B7)
</dt> <dt>



Falha ao ler o arquivo de leitura para a zona DNS.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_RECORD_DOES_NOT_EXIST"></span><span id="dns_error_record_does_not_exist"></span>**\_o registro de erro DNS não \_ \_ \_ \_ existe**
</dt> <dd> <dl> <dt>

9701 (0x25E5)
</dt> <dt>



O registro DNS não existe.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_RECORD_FORMAT"></span><span id="dns_error_record_format"></span>**\_formato de \_ registro de erro DNS \_**
</dt> <dd> <dl> <dt>

9702 (0x25E6)
</dt> <dt>



Erro de formato de registro DNS.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_NODE_CREATION_FAILED"></span><span id="dns_error_node_creation_failed"></span>**\_ \_ \_ falha na criação do nó de erro DNS \_**
</dt> <dd> <dl> <dt>

9703 (0x25E7)
</dt> <dt>



Falha na criação de nó no DNS.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_UNKNOWN_RECORD_TYPE"></span><span id="dns_error_unknown_record_type"></span>**\_tipo de registro de erro DNS \_ desconhecido \_ \_**
</dt> <dd> <dl> <dt>

9704 (0x25E8)
</dt> <dt>



Tipo de registro DNS desconhecido.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_RECORD_TIMED_OUT"></span><span id="dns_error_record_timed_out"></span>**o \_ registro de erro DNS \_ atingiu o \_ tempo \_ limite**
</dt> <dd> <dl> <dt>

9705 (0x25E9)
</dt> <dt>



O registro DNS atingiu o tempo limite.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_NAME_NOT_IN_ZONE"></span><span id="dns_error_name_not_in_zone"></span>**\_ \_ nome de erro DNS não está \_ \_ na \_ zona**
</dt> <dd> <dl> <dt>

9706 (0x25EA)
</dt> <dt>



Nome não está na zona DNS.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_CNAME_LOOP"></span><span id="dns_error_cname_loop"></span>**\_ \_ loop CNAME de erro DNS \_**
</dt> <dd> <dl> <dt>

9707 (0x25EB)
</dt> <dt>



Loop CNAME detectado.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_NODE_IS_CNAME"></span><span id="dns_error_node_is_cname"></span>**o \_ nó de erro DNS \_ \_ é \_ CNAME**
</dt> <dd> <dl> <dt>

9708 (0x25EC)
</dt> <dt>



O nó é um registro DNS CNAME.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_CNAME_COLLISION"></span><span id="dns_error_cname_collision"></span>**\_colisão de \_ CNAME de erro DNS \_**
</dt> <dd> <dl> <dt>

9709 (0x25ED)
</dt> <dt>



Já existe um registro CNAME para o nome fornecido.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_RECORD_ONLY_AT_ZONE_ROOT"></span><span id="dns_error_record_only_at_zone_root"></span>**\_ \_ registro de erro \_ DNS \_ somente \_ na \_ raiz da zona**
</dt> <dd> <dl> <dt>

9710 (0x25EE)
</dt> <dt>



Registrar somente na raiz da zona DNS.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_RECORD_ALREADY_EXISTS"></span><span id="dns_error_record_already_exists"></span>**o \_ registro de erro DNS \_ \_ já \_ existe**
</dt> <dd> <dl> <dt>

9711 (0x25EF)
</dt> <dt>



O registro DNS já existe.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_SECONDARY_DATA"></span><span id="dns_error_secondary_data"></span>**\_ \_ dados secundários de erro DNS \_**
</dt> <dd> <dl> <dt>

9712 (0x25F0)
</dt> <dt>



Erro de dados de zona DNS secundário.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_NO_CREATE_CACHE_DATA"></span><span id="dns_error_no_create_cache_data"></span>**erro de DNS \_ \_ sem \_ criar \_ dados de cache \_**
</dt> <dd> <dl> <dt>

9713 (0x25F1)
</dt> <dt>



Não foi possível criar dados de cache DNS.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_NAME_DOES_NOT_EXIST"></span><span id="dns_error_name_does_not_exist"></span>**\_o nome do erro DNS não \_ \_ \_ \_ existe**
</dt> <dd> <dl> <dt>

9714 (0x25F2)
</dt> <dt>



O nome do DNS não existe.


</dt> </dl> </dd> <dt>

<span id="DNS_WARNING_PTR_CREATE_FAILED"></span><span id="dns_warning_ptr_create_failed"></span>**\_ \_ \_ falha ao criar PTR de aviso DNS \_**
</dt> <dd> <dl> <dt>

9715 (0x25F3)
</dt> <dt>



Não foi possível criar o registro de ponteiro (PTR).


</dt> </dl> </dd> <dt>

<span id="DNS_WARNING_DOMAIN_UNDELETED"></span><span id="dns_warning_domain_undeleted"></span>**o domínio de aviso DNS não foi \_ \_ \_ excluído**
</dt> <dd> <dl> <dt>

9716 (0x25F4)
</dt> <dt>



O domínio DNS não foi excluído.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_DS_UNAVAILABLE"></span><span id="dns_error_ds_unavailable"></span>**\_erro DNS \_ DS \_ não disponível**
</dt> <dd> <dl> <dt>

9717 (0x25F5)
</dt> <dt>



O serviço de diretório não está disponível.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_DS_ZONE_ALREADY_EXISTS"></span><span id="dns_error_ds_zone_already_exists"></span>**a \_ zona DS de erro DNS \_ \_ \_ já \_ existe**
</dt> <dd> <dl> <dt>

9718 (0x25F6)
</dt> <dt>



A zona DNS já existe no serviço de diretório.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_NO_BOOTFILE_IF_DS_ZONE"></span><span id="dns_error_no_bootfile_if_ds_zone"></span>**erro de DNS \_ \_ sem \_ Bootfile \_ se a \_ \_ zona DS**
</dt> <dd> <dl> <dt>

9719 (0x25F7)
</dt> <dt>



O servidor DNS não está criando ou lendo o arquivo de inicialização para a zona DNS integrada ao serviço de diretório.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_NODE_IS_DNAME"></span><span id="dns_error_node_is_dname"></span>**o \_ nó de erro DNS \_ \_ é \_ dname**
</dt> <dd> <dl> <dt>

9720 (0x25F8)
</dt> <dt>



O nó é um registro DNS DNAME.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_DNAME_COLLISION"></span><span id="dns_error_dname_collision"></span>**colisão de erro de DNS \_ \_ dname \_**
</dt> <dd> <dl> <dt>

9721 (0x25F9)
</dt> <dt>



Um registro DNAME já existe para o nome fornecido.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_ALIAS_LOOP"></span><span id="dns_error_alias_loop"></span>**\_loop de \_ alias de erro DNS \_**
</dt> <dd> <dl> <dt>

9722 (0x25FA)
</dt> <dt>



Um loop de alias foi detectado com registros CNAME ou DNAME.


</dt> </dl> </dd> <dt>

<span id="DNS_INFO_AXFR_COMPLETE"></span><span id="dns_info_axfr_complete"></span>**\_ \_ AXFR completo de informações de DNS \_**
</dt> <dd> <dl> <dt>

9751 (0x2617)
</dt> <dt>



DNS AXFR (transferência de zona) concluído.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_AXFR"></span><span id="dns_error_axfr"></span>**erro de DNS \_ \_ AXFR**
</dt> <dd> <dl> <dt>

9752 (0x2618)
</dt> <dt>



Falha na transferência de zona DNS.


</dt> </dl> </dd> <dt>

<span id="DNS_INFO_ADDED_LOCAL_WINS"></span><span id="dns_info_added_local_wins"></span>**informações de DNS \_ \_ adicionadas \_ \_ WINS local**
</dt> <dd> <dl> <dt>

9753 (0x2619)
</dt> <dt>



Servidor WINS local adicionado.


</dt> </dl> </dd> <dt>

<span id="DNS_STATUS_CONTINUE_NEEDED"></span><span id="dns_status_continue_needed"></span>**o \_ status do DNS \_ continua \_ necessário**
</dt> <dd> <dl> <dt>

9801 (0x2649)
</dt> <dt>



A chamada de atualização segura precisa continuar a solicitação de atualização.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_NO_TCPIP"></span><span id="dns_error_no_tcpip"></span>**erro de DNS \_ \_ sem \_ tcpip**
</dt> <dd> <dl> <dt>

9851 (0x267B)
</dt> <dt>



Protocolo de rede TCP/IP não instalado.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_NO_DNS_SERVERS"></span><span id="dns_error_no_dns_servers"></span>**erro de DNS \_ \_ sem \_ \_ servidores DNS**
</dt> <dd> <dl> <dt>

9852 (0x267C)
</dt> <dt>



Nenhum servidor DNS configurado para o sistema local.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_DP_DOES_NOT_EXIST"></span><span id="dns_error_dp_does_not_exist"></span>**\_o erro DNS \_ DP não \_ \_ \_ existe**
</dt> <dd> <dl> <dt>

9901 (0x26AD)
</dt> <dt>



A partição de diretório especificada não existe.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_DP_ALREADY_EXISTS"></span><span id="dns_error_dp_already_exists"></span>**o \_ erro DNS \_ DP \_ já \_ existe**
</dt> <dd> <dl> <dt>

9902 (0x26AE)
</dt> <dt>



A partição de diretório especificada já existe.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_DP_NOT_ENLISTED"></span><span id="dns_error_dp_not_enlisted"></span>**\_erro DNS \_ DP \_ não \_ inscrito**
</dt> <dd> <dl> <dt>

9903 (0x26AF)
</dt> <dt>



Este servidor DNS não está inscrito na partição de diretório especificada.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_DP_ALREADY_ENLISTED"></span><span id="dns_error_dp_already_enlisted"></span>**\_erro DNS \_ DP \_ já \_ inscrito**
</dt> <dd> <dl> <dt>

9904 (0x26B0)
</dt> <dt>



Este servidor DNS já está inscrito na partição de diretório especificada.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_DP_NOT_AVAILABLE"></span><span id="dns_error_dp_not_available"></span>**\_erro DNS \_ DP \_ não \_ disponível**
</dt> <dd> <dl> <dt>

9905 (0x26B1)
</dt> <dt>



A partição de diretório não está disponível no momento. Aguarde alguns minutos e tente novamente.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_DP_FSMO_ERROR"></span><span id="dns_error_dp_fsmo_error"></span>**erro de DNS \_ \_ DP \_ FSMO \_**
</dt> <dd> <dl> <dt>

9906 (0x26B2)
</dt> <dt>



A operação falhou porque a função FSMO do mestre de nomeação de domínio não pôde ser acessada. O controlador de domínio que contém a função FSMO do mestre de nomeação de domínio está inoperante ou não pode atender à solicitação ou não está executando o Windows Server 2003 ou posterior.


</dt> </dl> </dd> <dt>

<span id="WSAEINTR"></span><span id="wsaeintr"></span>**WSAEINTR**
</dt> <dd> <dl> <dt>

10004 (0x2714)
</dt> <dt>



Uma operação de bloqueio foi interrompida por uma chamada para WSACancelBlockingCall.


</dt> </dl> </dd> <dt>

<span id="WSAEBADF"></span><span id="wsaebadf"></span>**WSAEBADF**
</dt> <dd> <dl> <dt>

10009 (0x2719)
</dt> <dt>



O identificador de arquivo fornecido não é válido.


</dt> </dl> </dd> <dt>

<span id="WSAEACCES"></span><span id="wsaeacces"></span>**WSAEACCES**
</dt> <dd> <dl> <dt>

10013 (0x271D)
</dt> <dt>



Foi feita uma tentativa de acessar um soquete de uma maneira proibida por suas permissões de acesso.


</dt> </dl> </dd> <dt>

<span id="WSAEFAULT"></span><span id="wsaefault"></span>**WSAEFAULT**
</dt> <dd> <dl> <dt>

10014 (0x271E)
</dt> <dt>



O sistema detectou um endereço de ponteiro inválido ao tentar usar um argumento de ponteiro em uma chamada.


</dt> </dl> </dd> <dt>

<span id="WSAEINVAL"></span><span id="wsaeinval"></span>**WSAEINVAL**
</dt> <dd> <dl> <dt>

10022 (0x2726)
</dt> <dt>



Foi fornecido um argumento inválido.


</dt> </dl> </dd> <dt>

<span id="WSAEMFILE"></span><span id="wsaemfile"></span>**WSAEMFILE**
</dt> <dd> <dl> <dt>

10024 (0x2728)
</dt> <dt>



Muitos soquetes abertos.


</dt> </dl> </dd> <dt>

<span id="WSAEWOULDBLOCK"></span><span id="wsaewouldblock"></span>**WSAEWOULDBLOCK**
</dt> <dd> <dl> <dt>

10035 (0x2733)
</dt> <dt>



Uma operação de soquete sem bloqueio não pôde ser concluída imediatamente.


</dt> </dl> </dd> <dt>

<span id="WSAEINPROGRESS"></span><span id="wsaeinprogress"></span>**WSAEINPROGRESS**
</dt> <dd> <dl> <dt>

10036 (0x2734)
</dt> <dt>



Uma operação de bloqueio está atualmente em execução.


</dt> </dl> </dd> <dt>

<span id="WSAEALREADY"></span><span id="wsaealready"></span>**WSAEALREADY**
</dt> <dd> <dl> <dt>

10037 (0x2735)
</dt> <dt>



Foi tentada uma operação em um soquete sem bloqueio que já tinha uma operação em andamento.


</dt> </dl> </dd> <dt>

<span id="WSAENOTSOCK"></span><span id="wsaenotsock"></span>**WSAENOTSOCK**
</dt> <dd> <dl> <dt>

10038 (0x2736)
</dt> <dt>



Uma operação foi tentada em algo que não é um soquete.


</dt> </dl> </dd> <dt>

<span id="WSAEDESTADDRREQ"></span><span id="wsaedestaddrreq"></span>**WSAEDESTADDRREQ**
</dt> <dd> <dl> <dt>

10039 (0x2737)
</dt> <dt>



Um endereço necessário foi omitido de uma operação em um soquete.


</dt> </dl> </dd> <dt>

<span id="WSAEMSGSIZE"></span><span id="wsaemsgsize"></span>**WSAEMSGSIZE**
</dt> <dd> <dl> <dt>

10040 (0x2738)
</dt> <dt>



Uma mensagem enviada em um soquete de datagrama era maior do que o buffer de mensagem interno ou que algum outro limite de rede, ou o buffer usado para receber um datagrama era menor que o próprio datagrama.


</dt> </dl> </dd> <dt>

<span id="WSAEPROTOTYPE"></span><span id="wsaeprototype"></span>**WSAEPROTOTYPE**
</dt> <dd> <dl> <dt>

10041 (0x2739)
</dt> <dt>



Um protocolo foi especificado na chamada de função de soquete que não oferece suporte à semântica do tipo de soquete solicitado.


</dt> </dl> </dd> <dt>

<span id="WSAENOPROTOOPT"></span><span id="wsaenoprotoopt"></span>**WSAENOPROTOOPT**
</dt> <dd> <dl> <dt>

10042 (0x273A)
</dt> <dt>



Uma opção ou um nível desconhecido, inválido ou sem suporte foi especificado em uma chamada de getsockopt ou setsockopt.


</dt> </dl> </dd> <dt>

<span id="WSAEPROTONOSUPPORT"></span><span id="wsaeprotonosupport"></span>**WSAEPROTONOSUPPORT**
</dt> <dd> <dl> <dt>

10043 (0x273B)
</dt> <dt>



O protocolo solicitado não foi configurado no sistema ou não existe nenhuma implementação para ele.


</dt> </dl> </dd> <dt>

<span id="WSAESOCKTNOSUPPORT"></span><span id="wsaesocktnosupport"></span>**WSAESOCKTNOSUPPORT**
</dt> <dd> <dl> <dt>

10044 (0x273C)
</dt> <dt>



O suporte para o tipo de soquete especificado não existe nessa família de endereços.


</dt> </dl> </dd> <dt>

<span id="WSAEOPNOTSUPP"></span><span id="wsaeopnotsupp"></span>**WSAEOPNOTSUPP**
</dt> <dd> <dl> <dt>

10045 (0x273D)
</dt> <dt>



Não há suporte para a operação tentada para o tipo de objeto referenciado.


</dt> </dl> </dd> <dt>

<span id="WSAEPFNOSUPPORT"></span><span id="wsaepfnosupport"></span>**WSAEPFNOSUPPORT**
</dt> <dd> <dl> <dt>

10046 (0x273E)
</dt> <dt>



A família de protocolos não foi configurada no sistema ou não existe nenhuma implementação para ela.


</dt> </dl> </dd> <dt>

<span id="WSAEAFNOSUPPORT"></span><span id="wsaeafnosupport"></span>**WSAEAFNOSUPPORT**
</dt> <dd> <dl> <dt>

10047 (0x273F)
</dt> <dt>



Foi usado um endereço incompatível com o protocolo solicitado.


</dt> </dl> </dd> <dt>

<span id="WSAEADDRINUSE"></span><span id="wsaeaddrinuse"></span>**WSAEADDRINUSE**
</dt> <dd> <dl> <dt>

10048 (0x2740)
</dt> <dt>



Normalmente, apenas um tipo de uso de cada endereço de soquete (endereço de rede/protocolo/porta) é permitido.


</dt> </dl> </dd> <dt>

<span id="WSAEADDRNOTAVAIL"></span><span id="wsaeaddrnotavail"></span>**WSAEADDRNOTAVAIL**
</dt> <dd> <dl> <dt>

10049 (0x2741)
</dt> <dt>



O endereço solicitado não é válido em seu contexto.


</dt> </dl> </dd> <dt>

<span id="WSAENETDOWN"></span><span id="wsaenetdown"></span>**WSAENETDOWN**
</dt> <dd> <dl> <dt>

10050 (0x2742)
</dt> <dt>



Uma operação de soquete encontrou uma rede inoperante.


</dt> </dl> </dd> <dt>

<span id="WSAENETUNREACH"></span><span id="wsaenetunreach"></span>**WSAENETUNREACH**
</dt> <dd> <dl> <dt>

10051 (0x2743)
</dt> <dt>



Uma operação de soquete foi tentada em uma rede inacessível.


</dt> </dl> </dd> <dt>

<span id="WSAENETRESET"></span><span id="wsaenetreset"></span>**WSAENETRESET**
</dt> <dd> <dl> <dt>

10052 (0x2744)
</dt> <dt>



A conexão foi interrompida devido à atividade Keep Alive que detecta uma falha enquanto a operação estava em andamento.


</dt> </dl> </dd> <dt>

<span id="WSAECONNABORTED"></span><span id="wsaeconnaborted"></span>**WSAECONNABORTED**
</dt> <dd> <dl> <dt>

10053 (0x2745)
</dt> <dt>



Uma conexão estabelecida foi interrompida pelo software na sua máquina host.


</dt> </dl> </dd> <dt>

<span id="WSAECONNRESET"></span><span id="wsaeconnreset"></span>**WSAECONNRESET**
</dt> <dd> <dl> <dt>

10054 (0x2746)
</dt> <dt>



uma conexão existente foi fechada forçadamente pelo host remoto.


</dt> </dl> </dd> <dt>

<span id="WSAENOBUFS"></span><span id="wsaenobufs"></span>**WSAENOBUFS**
</dt> <dd> <dl> <dt>

10055 (0x2747)
</dt> <dt>



Uma operação em um soquete não pôde ser executada porque o sistema não tem espaço suficiente no buffer ou porque uma fila estava cheia.


</dt> </dl> </dd> <dt>

<span id="WSAEISCONN"></span><span id="wsaeisconn"></span>**WSAEISCONN**
</dt> <dd> <dl> <dt>

10056 (0x2748)
</dt> <dt>



Uma solicitação de conexão foi feita em um soquete já conectado.


</dt> </dl> </dd> <dt>

<span id="WSAENOTCONN"></span><span id="wsaenotconn"></span>**WSAENOTCONN**
</dt> <dd> <dl> <dt>

10057 (0x2749)
</dt> <dt>



Uma solicitação de envio ou recebimento de dados foi impedida porque o soquete não está conectado e (durante o envio em um soquete de datagrama usando uma chamada sendto) nenhum endereço foi informado.


</dt> </dl> </dd> <dt>

<span id="WSAESHUTDOWN"></span><span id="wsaeshutdown"></span>**WSAESHUTDOWN**
</dt> <dd> <dl> <dt>

10058 (0x274A)
</dt> <dt>



Uma solicitação para enviar ou receber dados não foi permitida, pois o soquete já havia sido desligado nessa direção com uma chamada de desligamento anterior.


</dt> </dl> </dd> <dt>

<span id="WSAETOOMANYREFS"></span><span id="wsaetoomanyrefs"></span>**WSAETOOMANYREFS**
</dt> <dd> <dl> <dt>

10059 (0x274B)
</dt> <dt>



Muitas referências a algum objeto de kernel.


</dt> </dl> </dd> <dt>

<span id="WSAETIMEDOUT"></span><span id="wsaetimedout"></span>**WSAETIMEDOUT**
</dt> <dd> <dl> <dt>

10060 (0x274C)
</dt> <dt>



Uma tentativa de conexão falhou porque a parte conectada não respondeu corretamente após um período de tempo ou a conexão estabelecida falhou porque o host conectado falhou ao responder.


</dt> </dl> </dd> <dt>

<span id="WSAECONNREFUSED"></span><span id="wsaeconnrefused"></span>**WSAECONNREFUSED**
</dt> <dd> <dl> <dt>

10061 (0x274D)
</dt> <dt>



Não foi possível estabelecer uma conexão porque a máquina de destino a recusou ativamente.


</dt> </dl> </dd> <dt>

<span id="WSAELOOP"></span><span id="wsaeloop"></span>**WSAELOOP**
</dt> <dd> <dl> <dt>

10062 (0x274E)
</dt> <dt>



Não é possível converter o nome.


</dt> </dl> </dd> <dt>

<span id="WSAENAMETOOLONG"></span><span id="wsaenametoolong"></span>**WSAENAMETOOLONG**
</dt> <dd> <dl> <dt>

10063 (0x274F)
</dt> <dt>



O nome ou componente de nome era muito longo.


</dt> </dl> </dd> <dt>

<span id="WSAEHOSTDOWN"></span><span id="wsaehostdown"></span>**WSAEHOSTDOWN**
</dt> <dd> <dl> <dt>

10064 (0x2750)
</dt> <dt>



Uma operação de soquete falhou porque o host de destino estava inoperante.


</dt> </dl> </dd> <dt>

<span id="WSAEHOSTUNREACH"></span><span id="wsaehostunreach"></span>**WSAEHOSTUNREACH**
</dt> <dd> <dl> <dt>

10065 (0x2751)
</dt> <dt>



Uma operação de soquete foi tentada em um host inacessível.


</dt> </dl> </dd> <dt>

<span id="WSAENOTEMPTY"></span><span id="wsaenotempty"></span>**WSAENOTEMPTY**
</dt> <dd> <dl> <dt>

10066 (0x2752)
</dt> <dt>



Não é possível remover um diretório que não esteja vazio.


</dt> </dl> </dd> <dt>

<span id="WSAEPROCLIM"></span><span id="wsaeproclim"></span>**WSAEPROCLIM**
</dt> <dd> <dl> <dt>

10067 (0x2753)
</dt> <dt>



Uma implementação do Windows Sockets pode ter um limite no número de aplicativos que podem usá-lo simultaneamente.


</dt> </dl> </dd> <dt>

<span id="WSAEUSERS"></span><span id="wsaeusers"></span>**WSAEUSERS**
</dt> <dd> <dl> <dt>

10068 (0x2754)
</dt> <dt>



Ficou sem cota.


</dt> </dl> </dd> <dt>

<span id="WSAEDQUOT"></span><span id="wsaedquot"></span>**WSAEDQUOT**
</dt> <dd> <dl> <dt>

10069 (0x2755)
</dt> <dt>



Cota de disco esgotada.


</dt> </dl> </dd> <dt>

<span id="WSAESTALE"></span><span id="wsaestale"></span>**WSAESTALE**
</dt> <dd> <dl> <dt>

10070 (0x2756)
</dt> <dt>



A referência de identificador de arquivo não está mais disponível.


</dt> </dl> </dd> <dt>

<span id="WSAEREMOTE"></span><span id="wsaeremote"></span>**WSAEREMOTE**
</dt> <dd> <dl> <dt>

10071 (0x2757)
</dt> <dt>



O item não está disponível localmente.


</dt> </dl> </dd> <dt>

<span id="WSASYSNOTREADY"></span><span id="wsasysnotready"></span>**WSASYSNOTREADY**
</dt> <dd> <dl> <dt>

10091 (0x276B)
</dt> <dt>



O WSAStartup não pode funcionar neste momento porque o sistema subjacente usado para fornecer serviços de rede não está disponível no momento.


</dt> </dl> </dd> <dt>

<span id="WSAVERNOTSUPPORTED"></span><span id="wsavernotsupported"></span>**WSAVERNOTSUPPORTED**
</dt> <dd> <dl> <dt>

10092 (0x276C)
</dt> <dt>



Não há suporte para a versão solicitada do Windows Sockets.


</dt> </dl> </dd> <dt>

<span id="WSANOTINITIALISED"></span><span id="wsanotinitialised"></span>**WSANOTINITIALISED**
</dt> <dd> <dl> <dt>

10093 (0x276D)
</dt> <dt>



O aplicativo não chamou WSAStartup ou WSAStartup falhou.


</dt> </dl> </dd> <dt>

<span id="WSAEDISCON"></span><span id="wsaediscon"></span>**WSAEDISCON**
</dt> <dd> <dl> <dt>

10101 (0x2775)
</dt> <dt>



Retornado por WSARecv ou WSARecvFrom para indicar que a parte remota iniciou uma sequência de desligamento normal.


</dt> </dl> </dd> <dt>

<span id="WSAENOMORE"></span><span id="wsaenomore"></span>**WSAENOMORE**
</dt> <dd> <dl> <dt>

10102 (0x2776)
</dt> <dt>



Não é possível retornar mais resultados por WSALookupServiceNext.


</dt> </dl> </dd> <dt>

<span id="WSAECANCELLED"></span><span id="wsaecancelled"></span>**WSAECANCELLED**
</dt> <dd> <dl> <dt>

10103 (0x2777)
</dt> <dt>



Uma chamada para WSALookupServiceEnd foi feita enquanto essa chamada ainda estava sendo processada. A chamada foi cancelada.


</dt> </dl> </dd> <dt>

<span id="WSAEINVALIDPROCTABLE"></span><span id="wsaeinvalidproctable"></span>**WSAEINVALIDPROCTABLE**
</dt> <dd> <dl> <dt>

10104 (0x2778)
</dt> <dt>



A tabela de chamada de procedimento é inválida.


</dt> </dl> </dd> <dt>

<span id="WSAEINVALIDPROVIDER"></span><span id="wsaeinvalidprovider"></span>**WSAEINVALIDPROVIDER**
</dt> <dd> <dl> <dt>

10105 (0x2779)
</dt> <dt>



O provedor de serviços solicitado é inválido.


</dt> </dl> </dd> <dt>

<span id="WSAEPROVIDERFAILEDINIT"></span><span id="wsaeproviderfailedinit"></span>**WSAEPROVIDERFAILEDINIT**
</dt> <dd> <dl> <dt>

10106 (0x277A)
</dt> <dt>



O provedor de serviços solicitado não pôde ser carregado ou inicializado.


</dt> </dl> </dd> <dt>

<span id="WSASYSCALLFAILURE"></span><span id="wsasyscallfailure"></span>**WSASYSCALLFAILURE**
</dt> <dd> <dl> <dt>

10107 (0x277B)
</dt> <dt>



Falha em uma chamada do sistema.


</dt> </dl> </dd> <dt>

<span id="WSASERVICE_NOT_FOUND"></span><span id="wsaservice_not_found"></span>**WSASERVICE \_ não \_ encontrado**
</dt> <dd> <dl> <dt>

10108 (0x277C)
</dt> <dt>



Esse serviço não é conhecido. O serviço não pode ser encontrado no espaço de nome especificado.


</dt> </dl> </dd> <dt>

<span id="WSATYPE_NOT_FOUND"></span><span id="wsatype_not_found"></span>**WSATYPE \_ não \_ encontrado**
</dt> <dd> <dl> <dt>

10109 (0x277D)
</dt> <dt>



A classe especificada não foi encontrada.


</dt> </dl> </dd> <dt>

<span id="WSA_E_NO_MORE"></span><span id="wsa_e_no_more"></span>**CABEÇALHO \_ E \_ não \_ mais**
</dt> <dd> <dl> <dt>

10110 (0x277E)
</dt> <dt>



Não é possível retornar mais resultados por WSALookupServiceNext.


</dt> </dl> </dd> <dt>

<span id="WSA_E_CANCELLED"></span><span id="wsa_e_cancelled"></span>**WSA \_ E \_ cancelado**
</dt> <dd> <dl> <dt>

10111 (0x277F)
</dt> <dt>



Uma chamada para WSALookupServiceEnd foi feita enquanto essa chamada ainda estava sendo processada. A chamada foi cancelada.


</dt> </dl> </dd> <dt>

<span id="WSAEREFUSED"></span><span id="wsaerefused"></span>**WSAEREFUSED**
</dt> <dd> <dl> <dt>

10112 (0x2780)
</dt> <dt>



Uma consulta de banco de dados falhou porque foi ativamente recusada.


</dt> </dl> </dd> <dt>

<span id="WSAHOST_NOT_FOUND"></span><span id="wsahost_not_found"></span>**WSAHOST \_ não \_ encontrado**
</dt> <dd> <dl> <dt>

11001 (0x2AF9)
</dt> <dt>



Esse host não é conhecido.


</dt> </dl> </dd> <dt>

<span id="WSATRY_AGAIN"></span><span id="wsatry_again"></span>**WSATRY \_ novamente**
</dt> <dd> <dl> <dt>

11002 (0x2AFA)
</dt> <dt>



Esse é geralmente um erro temporário durante a resolução do nome do host e significa que o servidor local não recebeu uma resposta de um servidor autorizado.


</dt> </dl> </dd> <dt>

<span id="WSANO_RECOVERY"></span><span id="wsano_recovery"></span>**recuperação do WSANO \_**
</dt> <dd> <dl> <dt>

11003 (0x2AFB)
</dt> <dt>



Ocorreu um erro não recuperável durante uma pesquisa de banco de dados.


</dt> </dl> </dd> <dt>

<span id="WSANO_DATA"></span><span id="wsano_data"></span>**dados do WSANO \_**
</dt> <dd> <dl> <dt>

11004 (0x2AFC)
</dt> <dt>



O nome solicitado é válido, mas nenhum dado do tipo solicitado foi encontrado.


</dt> </dl> </dd> <dt>

<span id="WSA_QOS_RECEIVERS"></span><span id="wsa_qos_receivers"></span>**\_receptores de QoS de WSA \_**
</dt> <dd> <dl> <dt>

11005 (0x2AFD)
</dt> <dt>



Pelo menos uma reserva chegou.


</dt> </dl> </dd> <dt>

<span id="WSA_QOS_SENDERS"></span><span id="wsa_qos_senders"></span>**\_remetentes de QoS de WSA \_**
</dt> <dd> <dl> <dt>

11006 (0x2AFE)
</dt> <dt>



Pelo menos um caminho chegou.


</dt> </dl> </dd> <dt>

<span id="WSA_QOS_NO_SENDERS"></span><span id="wsa_qos_no_senders"></span>**QoS de WSA \_ \_ sem \_ remetentes**
</dt> <dd> <dl> <dt>

11007 (0x2AFF)
</dt> <dt>



Não há remetentes.


</dt> </dl> </dd> <dt>

<span id="WSA_QOS_NO_RECEIVERS"></span><span id="wsa_qos_no_receivers"></span>**QoS de WSA \_ \_ sem \_ receptores**
</dt> <dd> <dl> <dt>

11008 (0x2B00)
</dt> <dt>



Não há destinatários.


</dt> </dl> </dd> <dt>

<span id="WSA_QOS_REQUEST_CONFIRMED"></span><span id="wsa_qos_request_confirmed"></span>**solicitação de QoS de WSA \_ \_ \_ confirmada**
</dt> <dd> <dl> <dt>

11009 (0x2B01)
</dt> <dt>



A reserva foi confirmada.


</dt> </dl> </dd> <dt>

<span id="WSA_QOS_ADMISSION_FAILURE"></span><span id="wsa_qos_admission_failure"></span>**\_falha de \_ admissão de QoS de WSA \_**
</dt> <dd> <dl> <dt>

11010 (0x2B02)
</dt> <dt>



Erro devido à falta de recursos.


</dt> </dl> </dd> <dt>

<span id="WSA_QOS_POLICY_FAILURE"></span><span id="wsa_qos_policy_failure"></span>**\_ \_ falha na política de QoS de WSA \_**
</dt> <dd> <dl> <dt>

11011 (0x2B03)
</dt> <dt>



Rejeitado por motivos administrativos-credenciais inadequadas.


</dt> </dl> </dd> <dt>

<span id="WSA_QOS_BAD_STYLE"></span><span id="wsa_qos_bad_style"></span>**\_ \_ estilo insatisfatório de QoS de WSA \_**
</dt> <dd> <dl> <dt>

11012 (0x2B04)
</dt> <dt>



Estilo desconhecido ou conflitante.


</dt> </dl> </dd> <dt>

<span id="WSA_QOS_BAD_OBJECT"></span><span id="wsa_qos_bad_object"></span>**\_ \_ objeto insatisfatório de QoS de WSA \_**
</dt> <dd> <dl> <dt>

11013 (0x2B05)
</dt> <dt>



Problema com alguma parte do buffer filterspec ou ProviderSpecific em geral.


</dt> </dl> </dd> <dt>

<span id="WSA_QOS_TRAFFIC_CTRL_ERROR"></span><span id="wsa_qos_traffic_ctrl_error"></span>**\_erro de \_ Ctrl de tráfego de QoS de WSA \_ \_**
</dt> <dd> <dl> <dt>

11014 (0x2B06)
</dt> <dt>



Problema com alguma parte do FLOWSPEC.


</dt> </dl> </dd> <dt>

<span id="WSA_QOS_GENERIC_ERROR"></span><span id="wsa_qos_generic_error"></span>**\_ \_ erro genérico de QoS de WSA \_**
</dt> <dd> <dl> <dt>

11015 (0x2B07)
</dt> <dt>



Erro de QOS geral.


</dt> </dl> </dd> <dt>

<span id="WSA_QOS_ESERVICETYPE"></span><span id="wsa_qos_eservicetype"></span>**\_ESERVICETYPE de QoS de WSA \_**
</dt> <dd> <dl> <dt>

11016 (0x2B08)
</dt> <dt>



Um tipo de serviço inválido ou não reconhecido foi encontrado no FLOWSPEC.


</dt> </dl> </dd> <dt>

<span id="WSA_QOS_EFLOWSPEC"></span><span id="wsa_qos_eflowspec"></span>**\_EFLOWSPEC de QoS de WSA \_**
</dt> <dd> <dl> <dt>

11017 (0x2B09)
</dt> <dt>



Um FLOWSPEC inválido ou inconsistente foi encontrado na estrutura de QOS.


</dt> </dl> </dd> <dt>

<span id="WSA_QOS_EPROVSPECBUF"></span><span id="wsa_qos_eprovspecbuf"></span>**\_EPROVSPECBUF de QoS de WSA \_**
</dt> <dd> <dl> <dt>

11018 (0x2B0A)
</dt> <dt>



Buffer específico do provedor de QOS inválido.


</dt> </dl> </dd> <dt>

<span id="WSA_QOS_EFILTERSTYLE"></span><span id="wsa_qos_efilterstyle"></span>**\_EFILTERSTYLE de QoS de WSA \_**
</dt> <dd> <dl> <dt>

11019 (0x2B0B)
</dt> <dt>



Um estilo de filtro QOS inválido foi usado.


</dt> </dl> </dd> <dt>

<span id="WSA_QOS_EFILTERTYPE"></span><span id="wsa_qos_efiltertype"></span>**\_EFILTERTYPE de QoS de WSA \_**
</dt> <dd> <dl> <dt>

11020 (0x2B0C)
</dt> <dt>



Foi usado um tipo de filtro QOS inválido.


</dt> </dl> </dd> <dt>

<span id="WSA_QOS_EFILTERCOUNT"></span><span id="wsa_qos_efiltercount"></span>**\_EFILTERCOUNT de QoS de WSA \_**
</dt> <dd> <dl> <dt>

11021 (0x2B0D)
</dt> <dt>



Um número incorreto de FILTERSPECs de QOS foi especificado no FLOWDESCRIPTOR.


</dt> </dl> </dd> <dt>

<span id="WSA_QOS_EOBJLENGTH"></span><span id="wsa_qos_eobjlength"></span>**\_EOBJLENGTH de QoS de WSA \_**
</dt> <dd> <dl> <dt>

11022 (0x2B0E)
</dt> <dt>



Um objeto com um campo ObjectLength inválido foi especificado no buffer específico do provedor de QOS.


</dt> </dl> </dd> <dt>

<span id="WSA_QOS_EFLOWCOUNT"></span><span id="wsa_qos_eflowcount"></span>**\_EFLOWCOUNT de QoS de WSA \_**
</dt> <dd> <dl> <dt>

11023 (0x2B0F)
</dt> <dt>



Um número incorreto de descritores de fluxo foi especificado na estrutura de QOS.


</dt> </dl> </dd> <dt>

<span id="WSA_QOS_EUNKOWNPSOBJ"></span><span id="wsa_qos_eunkownpsobj"></span>**\_EUNKOWNPSOBJ de QoS de WSA \_**
</dt> <dd> <dl> <dt>

11024 (0x2B10)
</dt> <dt>



Um objeto não reconhecido foi encontrado no buffer específico do provedor de QOS.


</dt> </dl> </dd> <dt>

<span id="WSA_QOS_EPOLICYOBJ"></span><span id="wsa_qos_epolicyobj"></span>**\_EPOLICYOBJ de QoS de WSA \_**
</dt> <dd> <dl> <dt>

11025 (0x2B11)
</dt> <dt>



Um objeto de política inválido foi encontrado no buffer específico do provedor de QOS.


</dt> </dl> </dd> <dt>

<span id="WSA_QOS_EFLOWDESC"></span><span id="wsa_qos_eflowdesc"></span>**\_EFLOWDESC de QoS de WSA \_**
</dt> <dd> <dl> <dt>

11026 (0x2B12)
</dt> <dt>



Foi encontrado um descritor de fluxo QOS inválido na lista de descritores de fluxo.


</dt> </dl> </dd> <dt>

<span id="WSA_QOS_EPSFLOWSPEC"></span><span id="wsa_qos_epsflowspec"></span>**\_EPSFLOWSPEC de QoS de WSA \_**
</dt> <dd> <dl> <dt>

11027 (0x2B13)
</dt> <dt>



Um FLOWSPEC inválido ou inconsistente foi encontrado no buffer específico do provedor de QOS.


</dt> </dl> </dd> <dt>

<span id="WSA_QOS_EPSFILTERSPEC"></span><span id="wsa_qos_epsfilterspec"></span>**\_EPSFILTERSPEC de QoS de WSA \_**
</dt> <dd> <dl> <dt>

11028 (0x2B14)
</dt> <dt>



Um FILTERSPEC inválido foi encontrado no buffer específico do provedor de QOS.


</dt> </dl> </dd> <dt>

<span id="WSA_QOS_ESDMODEOBJ"></span><span id="wsa_qos_esdmodeobj"></span>**\_ESDMODEOBJ de QoS de WSA \_**
</dt> <dd> <dl> <dt>

11029 (0x2B15)
</dt> <dt>



Um objeto de modo de descarte de forma inválido foi encontrado no buffer específico do provedor de QOS.


</dt> </dl> </dd> <dt>

<span id="WSA_QOS_ESHAPERATEOBJ"></span><span id="wsa_qos_eshaperateobj"></span>**\_ESHAPERATEOBJ de QoS de WSA \_**
</dt> <dd> <dl> <dt>

11030 (0x2B16)
</dt> <dt>



Um objeto de taxa de formatação inválido foi encontrado no buffer específico do provedor de QOS.


</dt> </dl> </dd> <dt>

<span id="WSA_QOS_RESERVED_PETYPE"></span><span id="wsa_qos_reserved_petype"></span>**\_ \_ PETYPE reservado de QoS de WSA \_**
</dt> <dd> <dl> <dt>

11031 (0x2B17)
</dt> <dt>



Um elemento de política reservado foi encontrado no buffer específico do provedor de QOS.


</dt> </dl> </dd> <dt>

<span id="WSA_SECURE_HOST_NOT_FOUND"></span><span id="wsa_secure_host_not_found"></span>**\_host seguro do WSA \_ \_ não \_ encontrado**
</dt> <dd> <dl> <dt>

11032 (0x2B18)
</dt> <dt>



Esse host não é conhecido com segurança.


</dt> </dl> </dd> <dt>

<span id="WSA_IPSEC_NAME_POLICY_ERROR"></span><span id="wsa_ipsec_name_policy_error"></span>**\_erro de \_ política de nome de IPsec do WSA \_ \_**
</dt> <dd> <dl> <dt>

11033 (0x2B19)
</dt> <dt>



Não foi possível adicionar a política IPSEC baseada em nome.


</dt> </dl> </dd> </dl>


## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows XP\]<br/>                                           |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>WinError. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Códigos de erro do sistema](system-error-codes.md)
</dt> </dl>

 

 




