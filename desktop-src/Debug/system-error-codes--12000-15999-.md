---
description: Descreve os códigos de erro 12000-1599 definidos no arquivo de cabeçalho WinError. h e destina-se a desenvolvedores.
ms.assetid: bb3c658d-96db-495a-a0dc-e93949c3835d
title: Códigos de erro do sistema (12000-15999) (WinError. h)
ms.topic: reference
ms.date: 07/18/2019
ms.openlocfilehash: 8cac8adf6d8a4cf8f60fe978eb6f99f5efc1b9fe
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104457025"
---
# <a name="system-error-codes-12000-15999"></a>Códigos de erro do sistema (12000-15999)

> [!NOTE]
> Essas informações destinam-se a desenvolvedores Depurando erros do sistema. Para outros erros, como problemas com Windows Update, há uma lista de recursos na página códigos de [erro](system-error-codes.md) .

A lista a seguir descreve os [códigos de erro do sistema](system-error-codes.md) (erros 12000 a 15999). Elas são retornadas pela função [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) quando muitas funções falham. Para recuperar o texto de descrição do erro em seu aplicativo, use a função [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) com a **mensagem de formato \_ \_ do sinalizador do \_ sistema** .

<dl> <dt>

<span id="ERROR_INTERNET__"></span><span id="error_internet__"></span>**Erro \_ do \_Internet \** _
</dt> <dd> <dl> <dt>

12000-12175 (0x2EE0)
</dt> <dt>



Consulte [códigos de erro da Internet](../wininet/wininet-errors.md) e Wininet. h.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_QM_POLICY_EXISTS"></span><span id="error_ipsec_qm_policy_exists"></span>_ *erro \_ a \_ política IPSec qm \_ \_ existe**
</dt> <dd> <dl> <dt>

13000 (0x32C8)
</dt> <dt>



A política de modo rápido especificada já existe.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_QM_POLICY_NOT_FOUND"></span><span id="error_ipsec_qm_policy_not_found"></span>**ERRO \_ de \_ política IPSec qm \_ \_ não \_ encontrada**
</dt> <dd> <dl> <dt>

13001 (0x32C9)
</dt> <dt>



A política de modo rápido especificada não foi encontrada.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_QM_POLICY_IN_USE"></span><span id="error_ipsec_qm_policy_in_use"></span>**ERRO \_ \_ \_ de política IPSec qm \_ em \_ uso**
</dt> <dd> <dl> <dt>

13002 (0x32CA)
</dt> <dt>



A política de modo rápido especificada está sendo usada.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_MM_POLICY_EXISTS"></span><span id="error_ipsec_mm_policy_exists"></span>**ERRO \_ a \_ política IPSec mm \_ \_ existe**
</dt> <dd> <dl> <dt>

13003 (0x32CB)
</dt> <dt>



A política de modo principal especificada já existe.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_MM_POLICY_NOT_FOUND"></span><span id="error_ipsec_mm_policy_not_found"></span>**ERRO \_ de \_ política IPSec mm \_ \_ não \_ encontrada**
</dt> <dd> <dl> <dt>

13004 (0x32CC)
</dt> <dt>



A política de modo principal especificada não foi encontrada.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_MM_POLICY_IN_USE"></span><span id="error_ipsec_mm_policy_in_use"></span>**ERRO \_ \_ \_ de política IPSec mm \_ em \_ uso**
</dt> <dd> <dl> <dt>

13005 (0x32CD)
</dt> <dt>



A política de modo principal especificada está sendo usada.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_MM_FILTER_EXISTS"></span><span id="error_ipsec_mm_filter_exists"></span>**ERRO \_ o \_ filtro IPSec mm \_ \_ existe**
</dt> <dd> <dl> <dt>

13006 (0x32CE)
</dt> <dt>



O filtro de modo principal especificado já existe.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_MM_FILTER_NOT_FOUND"></span><span id="error_ipsec_mm_filter_not_found"></span>**ERRO \_ de \_ filtro IPSec mm \_ \_ não \_ encontrado**
</dt> <dd> <dl> <dt>

13007 (0x32CF)
</dt> <dt>



O filtro de modo principal especificado não foi encontrado.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_TRANSPORT_FILTER_EXISTS"></span><span id="error_ipsec_transport_filter_exists"></span>**ERRO \_ o \_ filtro de transporte IPSec \_ \_ existe**
</dt> <dd> <dl> <dt>

13008 (0x32D0)
</dt> <dt>



O filtro de modo de transporte especificado já existe.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_TRANSPORT_FILTER_NOT_FOUND"></span><span id="error_ipsec_transport_filter_not_found"></span>**ERRO \_ de \_ filtro de transporte IPSec \_ \_ não \_ encontrado**
</dt> <dd> <dl> <dt>

13009 (0x32D1)
</dt> <dt>



O filtro de modo de transporte especificado não existe.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_MM_AUTH_EXISTS"></span><span id="error_ipsec_mm_auth_exists"></span>**ERRO \_ a \_ autenticação IPsec mm \_ \_ existe**
</dt> <dd> <dl> <dt>

13010 (0x32D2)
</dt> <dt>



A lista de autenticação de modo principal especificada existe.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_MM_AUTH_NOT_FOUND"></span><span id="error_ipsec_mm_auth_not_found"></span>**ERRO \_ de \_ autenticação IPsec mm \_ \_ não \_ encontrado**
</dt> <dd> <dl> <dt>

13011 (0x32D3)
</dt> <dt>



A lista de autenticação de modo principal especificada não foi encontrada.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_MM_AUTH_IN_USE"></span><span id="error_ipsec_mm_auth_in_use"></span>**ERRO \_ \_ \_ de autenticação IPsec mm \_ em \_ uso**
</dt> <dd> <dl> <dt>

13012 (0x32D4)
</dt> <dt>



A lista de autenticação de modo principal especificada está sendo usada.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_DEFAULT_MM_POLICY_NOT_FOUND"></span><span id="error_ipsec_default_mm_policy_not_found"></span>**ERRO \_ de \_ política de IPSec padrão \_ mm \_ \_ não \_ encontrada**
</dt> <dd> <dl> <dt>

13013 (0x32D5)
</dt> <dt>



A política de modo principal padrão especificada não foi encontrada.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_DEFAULT_MM_AUTH_NOT_FOUND"></span><span id="error_ipsec_default_mm_auth_not_found"></span>**ERRO \_ IPSec \_ padrão \_ mm de \_ autenticação \_ não \_ encontrado**
</dt> <dd> <dl> <dt>

13014 (0x32D6)
</dt> <dt>



A lista de autenticação de modo principal padrão especificada não foi encontrada.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_DEFAULT_QM_POLICY_NOT_FOUND"></span><span id="error_ipsec_default_qm_policy_not_found"></span>**ERRO \_ de \_ política IPSec de \_ QM padrão \_ \_ não \_ encontrada**
</dt> <dd> <dl> <dt>

13015 (0x32D7)
</dt> <dt>



A política de modo rápido padrão especificada não foi encontrada.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_TUNNEL_FILTER_EXISTS"></span><span id="error_ipsec_tunnel_filter_exists"></span>**ERRO \_ o \_ filtro de túnel IPSec \_ \_ existe**
</dt> <dd> <dl> <dt>

13016 (0x32D8)
</dt> <dt>



O filtro de modo de túnel especificado existe.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_TUNNEL_FILTER_NOT_FOUND"></span><span id="error_ipsec_tunnel_filter_not_found"></span>**ERRO \_ de \_ filtro de túnel IPSec \_ \_ não \_ encontrado**
</dt> <dd> <dl> <dt>

13017 (0x32D9)
</dt> <dt>



O filtro de modo de túnel especificado não foi encontrado.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_MM_FILTER_PENDING_DELETION"></span><span id="error_ipsec_mm_filter_pending_deletion"></span>**ERRO \_ de \_ \_ \_ exclusão pendente do filtro IPSec mm \_**
</dt> <dd> <dl> <dt>

13018 (0x32DA)
</dt> <dt>



O filtro de modo principal está com a exclusão pendente.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_TRANSPORT_FILTER_PENDING_DELETION"></span><span id="error_ipsec_transport_filter_pending_deletion"></span>**ERRO \_ de \_ \_ \_ exclusão pendente do filtro de transporte IPSec \_**
</dt> <dd> <dl> <dt>

13019 (0x32DB)
</dt> <dt>



O filtro de transporte está com a exclusão pendente.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_TUNNEL_FILTER_PENDING_DELETION"></span><span id="error_ipsec_tunnel_filter_pending_deletion"></span>**ERRO \_ de \_ \_ \_ exclusão pendente do filtro de túnel IPSec \_**
</dt> <dd> <dl> <dt>

13020 (0x32DC)
</dt> <dt>



O filtro de túnel está com a exclusão pendente.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_MM_POLICY_PENDING_DELETION"></span><span id="error_ipsec_mm_policy_pending_deletion"></span>**ERRO \_ de \_ \_ \_ exclusão pendente da política IPSec mm \_**
</dt> <dd> <dl> <dt>

13021 (0x32DD)
</dt> <dt>



A política de modo principal tem exclusão pendente.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_MM_AUTH_PENDING_DELETION"></span><span id="error_ipsec_mm_auth_pending_deletion"></span>**ERRO de \_ exclusão de autenticação do IPSec \_ mm \_ \_ pendente \_**
</dt> <dd> <dl> <dt>

13022 (0x32DE)
</dt> <dt>



O grupo de autenticação de modo principal tem exclusão pendente.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_QM_POLICY_PENDING_DELETION"></span><span id="error_ipsec_qm_policy_pending_deletion"></span>**ERRO \_ de \_ \_ \_ exclusão pendente da política IPSec qm \_**
</dt> <dd> <dl> <dt>

13023 (0x32DF)
</dt> <dt>



A política de modo rápido tem exclusão pendente.


</dt> </dl> </dd> <dt>

<span id="WARNING_IPSEC_MM_POLICY_PRUNED"></span><span id="warning_ipsec_mm_policy_pruned"></span>**AVISO \_ de \_ política IPSec mm \_ \_ removida**
</dt> <dd> <dl> <dt>

13024 (0x32E0)
</dt> <dt>



A política de modo principal foi adicionada com êxito, mas não há suporte para algumas das ofertas solicitadas.


</dt> </dl> </dd> <dt>

<span id="WARNING_IPSEC_QM_POLICY_PRUNED"></span><span id="warning_ipsec_qm_policy_pruned"></span>**\_política de IPSec qm de aviso \_ \_ \_ removida**
</dt> <dd> <dl> <dt>

13025 (0x32E1)
</dt> <dt>



A política de modo rápido foi adicionada com êxito, mas não há suporte para algumas das ofertas solicitadas.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_NEG_STATUS_BEGIN"></span><span id="error_ipsec_ike_neg_status_begin"></span>**ERRO \_ de \_ \_ início de status de neg IPSec IKE \_ \_**
</dt> <dd> <dl> <dt>

13800 (0x35E8)
</dt> <dt>



ERRO \_ de \_ \_ início de status de neg IPSec IKE \_ \_


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_AUTH_FAIL"></span><span id="error_ipsec_ike_auth_fail"></span>**ERRO \_ de \_ autenticação IKE IPsec com \_ \_ falha**
</dt> <dd> <dl> <dt>

13801 (0x35E9)
</dt> <dt>



As credenciais de autenticação IKE são inaceitáveis.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_ATTRIB_FAIL"></span><span id="error_ipsec_ike_attrib_fail"></span>**ERRO \_ de \_ Atrib IPSec IKE com \_ \_ falha**
</dt> <dd> <dl> <dt>

13802 (0x35EA)
</dt> <dt>



Os atributos de segurança IKE são inaceitáveis.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_NEGOTIATION_PENDING"></span><span id="error_ipsec_ike_negotiation_pending"></span>**ERRO \_ de \_ negociação IKE IPSec \_ \_ pendente**
</dt> <dd> <dl> <dt>

13803 (0x35EB)
</dt> <dt>



Negociação IKE em andamento.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_GENERAL_PROCESSING_ERROR"></span><span id="error_ipsec_ike_general_processing_error"></span>**erro \_ de \_ \_ processamento geral de Ike de \_ IPSec \_**
</dt> <dd> <dl> <dt>

13804 (0x35EC)
</dt> <dt>



Erro geral de processamento.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_TIMED_OUT"></span><span id="error_ipsec_ike_timed_out"></span>**ERRO \_ \_ IKE IPSec \_ atingiu o tempo \_ limite**
</dt> <dd> <dl> <dt>

13805 (0x35ED)
</dt> <dt>



A negociação atingiu o tempo limite.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_NO_CERT"></span><span id="error_ipsec_ike_no_cert"></span>**ERRO \_ IPSec \_ Ike \_ sem \_ certificado**
</dt> <dd> <dl> <dt>

13806 (0x35EE)
</dt> <dt>



Falha de IKE ao localizar certificado de máquina válido. Entre em contato com o administrador de segurança de rede para instalar um certificado válido no repositório de certificados apropriado.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_SA_DELETED"></span><span id="error_ipsec_ike_sa_deleted"></span>**ERRO \_ \_ Ike \_ SA IPsec \_ excluído**
</dt> <dd> <dl> <dt>

13807 (0x35EF)
</dt> <dt>



SA IKE excluído pelo par antes da conclusão do estabelecimento.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_SA_REAPED"></span><span id="error_ipsec_ike_sa_reaped"></span>**ERRO \_ de \_ SA IKE IPSec \_ \_ colher**
</dt> <dd> <dl> <dt>

13808 (0x35F0)
</dt> <dt>



SA de IKE excluído antes do estabelecimento ser concluído.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_MM_ACQUIRE_DROP"></span><span id="error_ipsec_ike_mm_acquire_drop"></span>**ERRO \_ IPSec \_ Ike \_ mm \_ adquirir \_ drop**
</dt> <dd> <dl> <dt>

13809 (0x35F1)
</dt> <dt>



Solicitação de negociação colocada em fila muito longa.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_QM_ACQUIRE_DROP"></span><span id="error_ipsec_ike_qm_acquire_drop"></span>**ERRO \_ IPSec \_ Ike \_ qm de \_ aquisição \_ drop**
</dt> <dd> <dl> <dt>

13810 (0x35F2)
</dt> <dt>



Solicitação de negociação colocada em fila muito longa.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_QUEUE_DROP_MM"></span><span id="error_ipsec_ike_queue_drop_mm"></span>**ERRO \_ ao \_ \_ \_ remover mm da fila Ike de IPSec \_**
</dt> <dd> <dl> <dt>

13811 (0x35F3)
</dt> <dt>



Solicitação de negociação colocada em fila muito longa.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_QUEUE_DROP_NO_MM"></span><span id="error_ipsec_ike_queue_drop_no_mm"></span>**ERRO \_ de \_ fila Ike de IPSec não é possível \_ \_ Remover \_ \_ mm**
</dt> <dd> <dl> <dt>

13812 (0x35F4)
</dt> <dt>



Solicitação de negociação colocada em fila muito longa.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_DROP_NO_RESPONSE"></span><span id="error_ipsec_ike_drop_no_response"></span>**ERRO \_ de \_ \_ descartar IPSec IKE \_ sem \_ resposta**
</dt> <dd> <dl> <dt>

13813 (0x35F5)
</dt> <dt>



Sem resposta do par.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_MM_DELAY_DROP"></span><span id="error_ipsec_ike_mm_delay_drop"></span>**ERRO \_ ao \_ \_ \_ remover atraso de IPSec IKE mm \_**
</dt> <dd> <dl> <dt>

13814 (0x35F6)
</dt> <dt>



A negociação demorou muito tempo.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_QM_DELAY_DROP"></span><span id="error_ipsec_ike_qm_delay_drop"></span>**ERRO \_ ao \_ \_ \_ remover atraso de IPSec IKE qm \_**
</dt> <dd> <dl> <dt>

13815 (0x35F7)
</dt> <dt>



A negociação demorou muito tempo.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_ERROR"></span><span id="error_ipsec_ike_error"></span>**erro de erro de \_ \_ IKE IPSec \_**
</dt> <dd> <dl> <dt>

13816 (0x35F8)
</dt> <dt>



Ocorreu um erro desconhecido.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_CRL_FAILED"></span><span id="error_ipsec_ike_crl_failed"></span>**ERRO \_ \_ CRL Ike \_ IPSec \_ com falha**
</dt> <dd> <dl> <dt>

13817 (0x35F9)
</dt> <dt>



Falha na verificação de revogação de certificado.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_INVALID_KEY_USAGE"></span><span id="error_ipsec_ike_invalid_key_usage"></span>**ERRO \_ de \_ \_ uso de \_ chave \_ inválido de IKE IPSec**
</dt> <dd> <dl> <dt>

13818 (0x35FA)
</dt> <dt>



Uso inválido de chave de certificado.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_INVALID_CERT_TYPE"></span><span id="error_ipsec_ike_invalid_cert_type"></span>**ERRO \_ \_ tipo de certificado IPSec IKE \_ inválido \_ \_**
</dt> <dd> <dl> <dt>

13819 (0x35FB)
</dt> <dt>



Tipo de certificado inválido.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_NO_PRIVATE_KEY"></span><span id="error_ipsec_ike_no_private_key"></span>**ERRO \_ IPSec \_ Ike \_ sem \_ \_ chave privada**
</dt> <dd> <dl> <dt>

13820 (0x35FC)
</dt> <dt>



A negociação IKE falhou porque o certificado da máquina usado não tem uma chave privada. Os certificados IPsec exigem uma chave privada. Entre em contato com o administrador de segurança de rede para substituir por um certificado que tenha uma chave privada.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_SIMULTANEOUS_REKEY"></span><span id="error_ipsec_ike_simultaneous_rekey"></span>**ERRO \_ de \_ \_ rechaveamento simultâneo de Ike de IPSec \_**
</dt> <dd> <dl> <dt>

13821 (0x35FD)
</dt> <dt>



Foram detectadas rechaves simultâneas.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_DH_FAIL"></span><span id="error_ipsec_ike_dh_fail"></span>**ERRO de \_ falha de IPSec \_ Ike \_ DH \_**
</dt> <dd> <dl> <dt>

13822 (0x35FE)
</dt> <dt>



Falha na computação Diffie-Hellman.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_CRITICAL_PAYLOAD_NOT_RECOGNIZED"></span><span id="error_ipsec_ike_critical_payload_not_recognized"></span>**ERRO \_ de \_ \_ carga crítica IPSec IKE \_ \_ não \_ reconhecida**
</dt> <dd> <dl> <dt>

13823 (0x35FF)
</dt> <dt>



Não sabe como processar a carga crítica.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_INVALID_HEADER"></span><span id="error_ipsec_ike_invalid_header"></span>**ERRO \_ de \_ \_ cabeçalho inválido de IPSec IKE \_**
</dt> <dd> <dl> <dt>

13824 (0x3600)
</dt> <dt>



Cabeçalho inválido.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_NO_POLICY"></span><span id="error_ipsec_ike_no_policy"></span>**ERRO \_ IPSec \_ Ike \_ sem \_ política**
</dt> <dd> <dl> <dt>

13825 (0x3601)
</dt> <dt>



Nenhuma política configurada.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_INVALID_SIGNATURE"></span><span id="error_ipsec_ike_invalid_signature"></span>**ERRO \_ de \_ assinatura de IKE IPSec \_ inválida \_**
</dt> <dd> <dl> <dt>

13826 (0x3602)
</dt> <dt>



Falha ao verificar assinatura.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_KERBEROS_ERROR"></span><span id="error_ipsec_ike_kerberos_error"></span>**erro \_ de \_ Kerberos Ike de IPSec \_ \_**
</dt> <dd> <dl> <dt>

13827 (0x3603)
</dt> <dt>



Falha ao autenticar usando Kerberos.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_NO_PUBLIC_KEY"></span><span id="error_ipsec_ike_no_public_key"></span>**ERRO \_ IPSec \_ Ike \_ sem \_ \_ chave pública**
</dt> <dd> <dl> <dt>

13828 (0x3604)
</dt> <dt>



O certificado do par não tinha uma chave pública.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_PROCESS_ERR"></span><span id="error_ipsec_ike_process_err"></span>**ERRO \_ de \_ processo Ike de IPSec \_ \_**
</dt> <dd> <dl> <dt>

13829 (0x3605)
</dt> <dt>



Erro ao processar carga de erro.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_PROCESS_ERR_SA"></span><span id="error_ipsec_ike_process_err_sa"></span>**ERRO \_ de \_ processo Ike de IPSec Error \_ \_ \_ SA**
</dt> <dd> <dl> <dt>

13830 (0x3606)
</dt> <dt>



Erro ao processar carga SA.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_PROCESS_ERR_PROP"></span><span id="error_ipsec_ike_process_err_prop"></span>**ERRO \_ \_ Ike do \_ processo \_ de \_ IPSec**
</dt> <dd> <dl> <dt>

13831 (0x3607)
</dt> <dt>



Erro ao processar a carga da proposta.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_PROCESS_ERR_TRANS"></span><span id="error_ipsec_ike_process_err_trans"></span>**ERRO \_ de \_ \_ transação do processo Ike \_ IPSec \_**
</dt> <dd> <dl> <dt>

13832 (0x3608)
</dt> <dt>



Erro ao processar carga de transformação.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_PROCESS_ERR_KE"></span><span id="error_ipsec_ike_process_err_ke"></span>**ERRO \_ de \_ processo IKE IPSec \_ \_ Err \_ ke**
</dt> <dd> <dl> <dt>

13833 (0x3609)
</dt> <dt>



Erro ao processar carga de KE.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_PROCESS_ERR_ID"></span><span id="error_ipsec_ike_process_err_id"></span>**ERRO \_ de \_ \_ ID do processo Ike \_ IPSec \_**
</dt> <dd> <dl> <dt>

13834 (0x360A)
</dt> <dt>



Erro ao processar carga de ID.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_PROCESS_ERR_CERT"></span><span id="error_ipsec_ike_process_err_cert"></span>**ERRO \_ de \_ certificado IKE do \_ processo IPSec \_ \_**
</dt> <dd> <dl> <dt>

13835 (0x360B)
</dt> <dt>



Erro ao processar carga de certificado.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_PROCESS_ERR_CERT_REQ"></span><span id="error_ipsec_ike_process_err_cert_req"></span>**ERRO \_ de \_ certificado IKE do processo de IPSec \_ \_ \_ \_**
</dt> <dd> <dl> <dt>

13836 (0x360C)
</dt> <dt>



Erro ao processar carga de solicitação de certificado.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_PROCESS_ERR_HASH"></span><span id="error_ipsec_ike_process_err_hash"></span>**ERRO \_ de \_ \_ hash do processo Ike \_ IPSec \_**
</dt> <dd> <dl> <dt>

13837 (0x360D)
</dt> <dt>



Erro ao processar carga de hash.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_PROCESS_ERR_SIG"></span><span id="error_ipsec_ike_process_err_sig"></span>**ERRO \_ \_ IKE IPSec \_ processo \_ Err \_ SIG**
</dt> <dd> <dl> <dt>

13838 (0x360E)
</dt> <dt>



Erro ao processar carga de assinatura.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_PROCESS_ERR_NONCE"></span><span id="error_ipsec_ike_process_err_nonce"></span>**ERRO de \_ processo de Ike de IPSec \_ \_ \_ \_ innonce**
</dt> <dd> <dl> <dt>

13839 (0x360F)
</dt> <dt>



Erro ao processar carga nonce.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_PROCESS_ERR_NOTIFY"></span><span id="error_ipsec_ike_process_err_notify"></span>**ERRO de notificação de erros de \_ \_ processo IKE IPSec \_ \_ \_**
</dt> <dd> <dl> <dt>

13840 (0x3610)
</dt> <dt>



Erro ao processar a carga de notificação.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_PROCESS_ERR_DELETE"></span><span id="error_ipsec_ike_process_err_delete"></span>**ERRO \_ de \_ \_ exclusão do processo Ike \_ IPSec \_**
</dt> <dd> <dl> <dt>

13841 (0x3611)
</dt> <dt>



Erro ao processar a carga de exclusão.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_PROCESS_ERR_VENDOR"></span><span id="error_ipsec_ike_process_err_vendor"></span>**ERRO de fornecedor de erros de \_ \_ processo IKE IPSec \_ \_ \_**
</dt> <dd> <dl> <dt>

13842 (0x3612)
</dt> <dt>



Erro ao processar a carga de VendorID.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_INVALID_PAYLOAD"></span><span id="error_ipsec_ike_invalid_payload"></span>**ERRO \_ de \_ \_ carga inválida de IKE IPSec \_**
</dt> <dd> <dl> <dt>

13843 (0x3613)
</dt> <dt>



Carga inválida recebida.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_LOAD_SOFT_SA"></span><span id="error_ipsec_ike_load_soft_sa"></span>**ERRO de \_ IP \_ Ike de \_ carga \_ \_ de IPSec**
</dt> <dd> <dl> <dt>

13844 (0x3614)
</dt> <dt>



SA suave carregado.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_SOFT_SA_TORN_DOWN"></span><span id="error_ipsec_ike_soft_sa_torn_down"></span>**ERRO \_ IPSec \_ Ike \_ Soft \_ SA \_ rasgado \_**
</dt> <dd> <dl> <dt>

13845 (0x3615)
</dt> <dt>



SA suave interrompida.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_INVALID_COOKIE"></span><span id="error_ipsec_ike_invalid_cookie"></span>**ERRO de \_ cookie de IPSec \_ Ike \_ inválido \_**
</dt> <dd> <dl> <dt>

13846 (0x3616)
</dt> <dt>



Cookie inválido recebido.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_NO_PEER_CERT"></span><span id="error_ipsec_ike_no_peer_cert"></span>**ERRO \_ IPSec \_ Ike \_ no \_ par de \_ certificados**
</dt> <dd> <dl> <dt>

13847 (0x3617)
</dt> <dt>



O par não pôde enviar um certificado de máquina válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_PEER_CRL_FAILED"></span><span id="error_ipsec_ike_peer_crl_failed"></span>**ERRO \_ \_ falha de \_ CRL de par Ike \_ IPSec \_**
</dt> <dd> <dl> <dt>

13848 (0x3618)
</dt> <dt>



Falha na verificação de revogação da certificação do certificado do par.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_POLICY_CHANGE"></span><span id="error_ipsec_ike_policy_change"></span>**ERRO \_ na \_ \_ alteração da política IKE IPSec \_**
</dt> <dd> <dl> <dt>

13849 (0x3619)
</dt> <dt>



Nova SAs invalidada de política formada com política antiga.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_NO_MM_POLICY"></span><span id="error_ipsec_ike_no_mm_policy"></span>**ERRO \_ de \_ política IPSec IKE \_ não \_ mm \_**
</dt> <dd> <dl> <dt>

13850 (0x361A)
</dt> <dt>



Não há nenhuma política IKE de modo principal disponível.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_NOTCBPRIV"></span><span id="error_ipsec_ike_notcbpriv"></span>**ERRO de \_ IPSec \_ Ike \_ NOTCBPRIV**
</dt> <dd> <dl> <dt>

13851 (0x361B)
</dt> <dt>



Falha ao habilitar o privilégio TCB.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_SECLOADFAIL"></span><span id="error_ipsec_ike_secloadfail"></span>**ERRO de \_ IPSec \_ Ike \_ SECLOADFAIL**
</dt> <dd> <dl> <dt>

13852 (0x361C)
</dt> <dt>



Falha ao carregar SECURITY.DLL.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_FAILSSPINIT"></span><span id="error_ipsec_ike_failsspinit"></span>**ERRO de \_ IPSec \_ Ike \_ FAILSSPINIT**
</dt> <dd> <dl> <dt>

13853 (0x361D)
</dt> <dt>



Falha ao obter o endereço de expedição da tabela da função de segurança do SSPI.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_FAILQUERYSSP"></span><span id="error_ipsec_ike_failqueryssp"></span>**ERRO de \_ IPSec \_ Ike \_ FAILQUERYSSP**
</dt> <dd> <dl> <dt>

13854 (0x361E)
</dt> <dt>



Falha ao consultar o pacote Kerberos para obter o tamanho máximo do token.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_SRVACQFAIL"></span><span id="error_ipsec_ike_srvacqfail"></span>**ERRO de \_ IPSec \_ Ike \_ SRVACQFAIL**
</dt> <dd> <dl> <dt>

13855 (0x361F)
</dt> <dt>



Falha ao obter as credenciais do servidor Kerberos para ISAKMP/erro \_ IPSec \_ Ike Service. A autenticação Kerberos não funcionará. O motivo mais provável para isso é a falta de associação de domínio. Isso é normal se o computador for membro de um grupo de trabalho.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_SRVQUERYCRED"></span><span id="error_ipsec_ike_srvquerycred"></span>**ERRO de \_ IPSec \_ Ike \_ SRVQUERYCRED**
</dt> <dd> <dl> <dt>

13856 (0x3620)
</dt> <dt>



Falha ao determinar o nome da entidade de segurança SSPI para ISAKMP/erro \_ IPSec \_ Ike Service ([**QueryCredentialsAttributes**](/windows/win32/api/sspi/nf-sspi-querycredentialsattributesa)).


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_GETSPIFAIL"></span><span id="error_ipsec_ike_getspifail"></span>**ERRO de \_ IPSec \_ Ike \_ GETSPIFAIL**
</dt> <dd> <dl> <dt>

13857 (0x3621)
</dt> <dt>



Falha ao obter o novo SPI para o SA de entrada do Driver IPsec. A causa mais comum para isso é que o driver não tem o filtro correto. Verifique sua política para verificar os filtros.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_INVALID_FILTER"></span><span id="error_ipsec_ike_invalid_filter"></span>**ERRO \_ de \_ \_ filtro inválido de IPSec IKE \_**
</dt> <dd> <dl> <dt>

13858 (0x3622)
</dt> <dt>



O filtro fornecido é inválido.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_OUT_OF_MEMORY"></span><span id="error_ipsec_ike_out_of_memory"></span>**ERRO \_ \_ IKE IPSec \_ sem \_ \_ memória**
</dt> <dd> <dl> <dt>

13859 (0x3623)
</dt> <dt>



Falha na alocação de memória.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_ADD_UPDATE_KEY_FAILED"></span><span id="error_ipsec_ike_add_update_key_failed"></span>**ERRO \_ IPSec \_ Ike \_ \_ \_ falha ao adicionar chave de atualização \_**
</dt> <dd> <dl> <dt>

13860 (0x3624)
</dt> <dt>



Falha ao adicionar Associação de segurança ao Driver IPsec. A causa mais comum para isso é se a negociação IKE demorou muito tempo para ser concluída. Se o problema persistir, reduza a carga no computador com falha.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_INVALID_POLICY"></span><span id="error_ipsec_ike_invalid_policy"></span>**ERRO \_ de \_ política de Ike \_ inválida IPSec \_**
</dt> <dd> <dl> <dt>

13861 (0x3625)
</dt> <dt>



Política inválida.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_UNKNOWN_DOI"></span><span id="error_ipsec_ike_unknown_doi"></span>**ERRO \_ de \_ doi de Ike \_ desconhecido IPSec \_**
</dt> <dd> <dl> <dt>

13862 (0x3626)
</dt> <dt>



DOI inválido.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_INVALID_SITUATION"></span><span id="error_ipsec_ike_invalid_situation"></span>**ERRO \_ de \_ situação de Ike \_ inválida de IPSec \_**
</dt> <dd> <dl> <dt>

13863 (0x3627)
</dt> <dt>



Situação inválida.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_DH_FAILURE"></span><span id="error_ipsec_ike_dh_failure"></span>**ERRO \_ de \_ \_ falha DH IPSec IKE \_**
</dt> <dd> <dl> <dt>

13864 (0x3628)
</dt> <dt>



Falha de Diffie-Hellman.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_INVALID_GROUP"></span><span id="error_ipsec_ike_invalid_group"></span>**ERRO \_ de \_ \_ grupo inválido de IPSec IKE \_**
</dt> <dd> <dl> <dt>

13865 (0x3629)
</dt> <dt>



Grupo de Diffie-Hellman inválido.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_ENCRYPT"></span><span id="error_ipsec_ike_encrypt"></span>**ERRO \_ de \_ criptografia IKE IPSec \_**
</dt> <dd> <dl> <dt>

13866 (0x362A)
</dt> <dt>



Erro ao criptografar a carga.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_DECRYPT"></span><span id="error_ipsec_ike_decrypt"></span>**ERRO \_ de \_ descriptografia de IPSec IKE \_**
</dt> <dd> <dl> <dt>

13867 (0x362B)
</dt> <dt>



Erro ao descriptografar a carga.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_POLICY_MATCH"></span><span id="error_ipsec_ike_policy_match"></span>**ERRO \_ de \_ \_ correspondência de política IKE IPSec \_**
</dt> <dd> <dl> <dt>

13868 (0x362C)
</dt> <dt>



Erro de correspondência de política.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_UNSUPPORTED_ID"></span><span id="error_ipsec_ike_unsupported_id"></span>**ERRO \_ de \_ \_ ID incompatível de IKE IPSec \_**
</dt> <dd> <dl> <dt>

13869 (0x362D)
</dt> <dt>



ID sem suporte.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_INVALID_HASH"></span><span id="error_ipsec_ike_invalid_hash"></span>**ERRO de \_ hash de IPSec \_ Ike \_ inválido \_**
</dt> <dd> <dl> <dt>

13870 (0x362E)
</dt> <dt>



Falha na verificação de hash.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_INVALID_HASH_ALG"></span><span id="error_ipsec_ike_invalid_hash_alg"></span>**ERRO \_ de \_ hash de IP Ike \_ inválido \_ \_ alg**
</dt> <dd> <dl> <dt>

13871 (0x362F)
</dt> <dt>



Algoritmo de hash inválido.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_INVALID_HASH_SIZE"></span><span id="error_ipsec_ike_invalid_hash_size"></span>**ERRO \_ de \_ \_ tamanho de \_ hash \_ inválido de IKE IPSec**
</dt> <dd> <dl> <dt>

13872 (0x3630)
</dt> <dt>



Tamanho de hash inválido.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_INVALID_ENCRYPT_ALG"></span><span id="error_ipsec_ike_invalid_encrypt_alg"></span>**ERRO \_ \_ IKE IPSec \_ inválido \_ criptografar \_ alg**
</dt> <dd> <dl> <dt>

13873 (0x3631)
</dt> <dt>



Algoritmo de criptografia inválido.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_INVALID_AUTH_ALG"></span><span id="error_ipsec_ike_invalid_auth_alg"></span>**ERRO \_ de \_ autenticação de IP Ike \_ inválido \_ \_ alg**
</dt> <dd> <dl> <dt>

13874 (0x3632)
</dt> <dt>



Algoritmo de autenticação inválido.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_INVALID_SIG"></span><span id="error_ipsec_ike_invalid_sig"></span>**ERRO \_ de \_ SIG IPSec IKE \_ inválido \_**
</dt> <dd> <dl> <dt>

13875 (0x3633)
</dt> <dt>



Assinatura de certificado inválida.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_LOAD_FAILED"></span><span id="error_ipsec_ike_load_failed"></span>**ERRO \_ \_ \_ ao carregar Ike de IPSec \_**
</dt> <dd> <dl> <dt>

13876 (0x3634)
</dt> <dt>



Falha no carregamento.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_RPC_DELETE"></span><span id="error_ipsec_ike_rpc_delete"></span>**ERRO \_ de \_ \_ exclusão de RPC IKE IPSec \_**
</dt> <dd> <dl> <dt>

13877 (0x3635)
</dt> <dt>



Excluído via chamada RPC.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_BENIGN_REINIT"></span><span id="error_ipsec_ike_benign_reinit"></span>**ERRO \_ de \_ \_ reinicialização de Ike de IPSec benigno \_**
</dt> <dd> <dl> <dt>

13878 (0x3636)
</dt> <dt>



Estado temporário criado para executar a reinicialização. Isso não é uma falha real.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_INVALID_RESPONDER_LIFETIME_NOTIFY"></span><span id="error_ipsec_ike_invalid_responder_lifetime_notify"></span>**ERRO \_ ao \_ \_ \_ \_ notificador de tempo de resposta de Ike inválido de IPSec \_**
</dt> <dd> <dl> <dt>

13879 (0x3637)
</dt> <dt>



O valor de tempo de vida recebido na notificação de tempo de vida do respondente está abaixo do valor mínimo configurado para o Windows 2000. Corrija a política na máquina par.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_INVALID_MAJOR_VERSION"></span><span id="error_ipsec_ike_invalid_major_version"></span>**ERRO \_ de \_ \_ \_ versão principal inválida de IKE IPSec \_**
</dt> <dd> <dl> <dt>

13880 (0x3638)
</dt> <dt>



O destinatário não pode manipular a versão do IKE especificada no cabeçalho.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_INVALID_CERT_KEYLEN"></span><span id="error_ipsec_ike_invalid_cert_keylen"></span>**ERRO \_ de \_ certificado IPSec IKE \_ inválido \_ \_ KEYLEN**
</dt> <dd> <dl> <dt>

13881 (0x3639)
</dt> <dt>



O comprimento da chave no certificado é muito pequeno para os requisitos de segurança configurados.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_MM_LIMIT"></span><span id="error_ipsec_ike_mm_limit"></span>**ERRO \_ de \_ limite de Ike mm de IPSec \_ \_**
</dt> <dd> <dl> <dt>

13882 (0x363A)
</dt> <dt>



Número máximo de SAs MM estabelecido para par excedido.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_NEGOTIATION_DISABLED"></span><span id="error_ipsec_ike_negotiation_disabled"></span>**ERRO \_ de \_ negociação IKE IPSec \_ \_ desabilitada**
</dt> <dd> <dl> <dt>

13883 (0x363B)
</dt> <dt>



O IKE recebeu uma política que desabilita a negociação.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_QM_LIMIT"></span><span id="error_ipsec_ike_qm_limit"></span>**ERRO de \_ limite de IPSec \_ Ike \_ qm \_**
</dt> <dd> <dl> <dt>

13884 (0x363C)
</dt> <dt>



Limite máximo de modo rápido atingido para o modo principal. O novo modo principal será iniciado.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_MM_EXPIRED"></span><span id="error_ipsec_ike_mm_expired"></span>**ERRO \_ \_ Ike mm de IPSec \_ \_ expirado**
</dt> <dd> <dl> <dt>

13885 (0x363D)
</dt> <dt>



O tempo de vida da SA de modo principal expirou ou o par enviou uma exclusão de modo principal.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_PEER_MM_ASSUMED_INVALID"></span><span id="error_ipsec_ike_peer_mm_assumed_invalid"></span>**ERRO \_ IPSec \_ Ike \_ peer \_ mm \_ considerado \_ inválido**
</dt> <dd> <dl> <dt>

13886 (0x363E)
</dt> <dt>



SA de modo principal assumido como inválido porque o par parou de responder.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_CERT_CHAIN_POLICY_MISMATCH"></span><span id="error_ipsec_ike_cert_chain_policy_mismatch"></span>**ERRO \_ de \_ \_ \_ \_ incompatibilidade de política de cadeia de certificado IKE IPSec \_**
</dt> <dd> <dl> <dt>

13887 (0x363F)
</dt> <dt>



O certificado não se encadea a uma raiz confiável na política IPsec.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_UNEXPECTED_MESSAGE_ID"></span><span id="error_ipsec_ike_unexpected_message_id"></span>**ERRO \_ de \_ \_ ID de \_ mensagem \_ inesperada IPSec IKE**
</dt> <dd> <dl> <dt>

13888 (0x3640)
</dt> <dt>



ID de mensagem inesperada recebida.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_INVALID_AUTH_PAYLOAD"></span><span id="error_ipsec_ike_invalid_auth_payload"></span>**ERRO \_ de \_ \_ carga de \_ autenticação inválida de IKE IPSec \_**
</dt> <dd> <dl> <dt>

13889 (0x3641)
</dt> <dt>



Ofertas de autenticação inválidas recebidas.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_DOS_COOKIE_SENT"></span><span id="error_ipsec_ike_dos_cookie_sent"></span>**ERRO \_ de \_ cookie de dos IPSec IKE \_ \_ \_ enviado**
</dt> <dd> <dl> <dt>

13890 (0x3642)
</dt> <dt>



Enviada notificação de cookie DoS para o iniciador.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_SHUTTING_DOWN"></span><span id="error_ipsec_ike_shutting_down"></span>**ERRO \_ de \_ \_ desligamento de IKE IPSec \_**
</dt> <dd> <dl> <dt>

13891 (0x3643)
</dt> <dt>



O serviço IKE está sendo desligado.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_CGA_AUTH_FAILED"></span><span id="error_ipsec_ike_cga_auth_failed"></span>**ERRO \_ de \_ \_ autenticação CGA IPSec IKE \_ \_ falhou**
</dt> <dd> <dl> <dt>

13892 (0x3644)
</dt> <dt>



Não foi possível verificar a associação entre o endereço CGA e o certificado.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_PROCESS_ERR_NATOA"></span><span id="error_ipsec_ike_process_err_natoa"></span>**ERRO \_ de \_ processo Ike de IPSec \_ \_ \_ NATOA**
</dt> <dd> <dl> <dt>

13893 (0x3645)
</dt> <dt>



Erro ao processar carga NatOA.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_INVALID_MM_FOR_QM"></span><span id="error_ipsec_ike_invalid_mm_for_qm"></span>**ERRO \_ \_ de IPSec IKE \_ inválido \_ mm \_ para \_ QM**
</dt> <dd> <dl> <dt>

13894 (0x3646)
</dt> <dt>



Os parâmetros do modo principal são inválidos para este modo rápido.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_QM_EXPIRED"></span><span id="error_ipsec_ike_qm_expired"></span>**ERRO \_ \_ IKE IPSec \_ qm \_ expirado**
</dt> <dd> <dl> <dt>

13895 (0x3647)
</dt> <dt>



O SA de modo rápido expirou pelo driver IPsec.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_TOO_MANY_FILTERS"></span><span id="error_ipsec_ike_too_many_filters"></span>**ERRO \_ Ike de IPSec em muitos \_ \_ \_ \_ filtros**
</dt> <dd> <dl> <dt>

13896 (0x3648)
</dt> <dt>



Muitos filtros IKEEXT adicionados dinamicamente foram detectados.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_NEG_STATUS_END"></span><span id="error_ipsec_ike_neg_status_end"></span>**ERRO \_ de \_ \_ neg de \_ status de IKE IPSec \_**
</dt> <dd> <dl> <dt>

13897 (0x3649)
</dt> <dt>



ERRO \_ de \_ \_ neg de \_ status de IKE IPSec \_


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_KILL_DUMMY_NAP_TUNNEL"></span><span id="error_ipsec_ike_kill_dummy_nap_tunnel"></span>**ERRO \_ IPSec \_ Ike \_ Kill \_ fictícia \_ NAP \_ Tunnel**
</dt> <dd> <dl> <dt>

13898 (0x364A)
</dt> <dt>



A reautenticação de NAP foi bem-sucedida e deve excluir o túnel IKEv2 NAP fictício.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_INNER_IP_ASSIGNMENT_FAILURE"></span><span id="error_ipsec_ike_inner_ip_assignment_failure"></span>**ERRO \_ \_ \_ \_ na atribuição de IP \_ interno \_ Ike do IPSec**
</dt> <dd> <dl> <dt>

13899 (0x364B)
</dt> <dt>



Erro ao atribuir o endereço IP interno ao iniciador no modo de túnel.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_REQUIRE_CP_PAYLOAD_MISSING"></span><span id="error_ipsec_ike_require_cp_payload_missing"></span>**ERRO \_ \_ IKE IPSec \_ requer \_ conteúdo de CP \_ \_ ausente**
</dt> <dd> <dl> <dt>

13900 (0x364C)
</dt> <dt>



Requer carga de configuração ausente.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_KEY_MODULE_IMPERSONATION_NEGOTIATION_PENDING"></span><span id="error_ipsec_key_module_impersonation_negotiation_pending"></span>**ERRO \_ de \_ negociação de representação de módulo de chave IPSec \_ \_ \_ \_ pendente**
</dt> <dd> <dl> <dt>

13901 (0x364D)
</dt> <dt>



Uma negociação em execução como o princípio de segurança que emitiu a conexão está em andamento.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_COEXISTENCE_SUPPRESS"></span><span id="error_ipsec_ike_coexistence_suppress"></span>**ERRO \_ de \_ \_ supressão de coexistência de IPSec IKE \_**
</dt> <dd> <dl> <dt>

13902 (0x364E)
</dt> <dt>



SA foi excluído devido à verificação de supressão de coexistência de IKEv1/AuthIP.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_RATELIMIT_DROP"></span><span id="error_ipsec_ike_ratelimit_drop"></span>**ERRO \_ IPSec \_ Ike \_ RATELIMIT \_ drop**
</dt> <dd> <dl> <dt>

13903 (0x364F)
</dt> <dt>



A solicitação SA de entrada foi descartada devido à limitação da taxa de endereço IP do par.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_PEER_DOESNT_SUPPORT_MOBIKE"></span><span id="error_ipsec_ike_peer_doesnt_support_mobike"></span>**ERRO \_ IPSec \_ Ike \_ peer \_ \_ não dá suporte a \_ MOBIKE**
</dt> <dd> <dl> <dt>

13904 (0x3650)
</dt> <dt>



O par não dá suporte a MOBIKE.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_AUTHORIZATION_FAILURE"></span><span id="error_ipsec_ike_authorization_failure"></span>**ERRO \_ de \_ \_ falha de autorização \_ de IPSec IKE**
</dt> <dd> <dl> <dt>

13905 (0x3651)
</dt> <dt>



Estabelecimento de SA não autorizado.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_STRONG_CRED_AUTHORIZATION_FAILURE"></span><span id="error_ipsec_ike_strong_cred_authorization_failure"></span>**ERRO \_ de \_ \_ falha de \_ autorização de credenciais fortes \_ IPSec IKE \_**
</dt> <dd> <dl> <dt>

13906 (0x3652)
</dt> <dt>



O estabelecimento de SA não é autorizado porque não há uma credencial baseada em PKINIT suficientemente forte.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_AUTHORIZATION_FAILURE_WITH_OPTIONAL_RETRY"></span><span id="error_ipsec_ike_authorization_failure_with_optional_retry"></span>**ERRO \_ \_ \_ \_ de falha de autorização IKE IPSec \_ com \_ \_ repetição opcional**
</dt> <dd> <dl> <dt>

13907 (0x3653)
</dt> <dt>



Estabelecimento de SA não autorizado. Talvez seja necessário inserir credenciais atualizadas ou diferentes, como um cartão inteligente.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_STRONG_CRED_AUTHORIZATION_AND_CERTMAP_FAILURE"></span><span id="error_ipsec_ike_strong_cred_authorization_and_certmap_failure"></span>**ERRO \_ \_ \_ \_ \_ de autorização de credenciais fortes \_ de Ike de IPSec e \_ falha de CERTMAP \_**
</dt> <dd> <dl> <dt>

13908 (0x3654)
</dt> <dt>



O estabelecimento de SA não é autorizado porque não há uma credencial baseada em PKINIT suficientemente forte. Isso pode estar relacionado à falha de mapeamento de certificado para conta para o SA.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_NEG_STATUS_EXTENDED_END"></span><span id="error_ipsec_ike_neg_status_extended_end"></span>**ERRO \_ IPSec \_ Ike \_ neg de \_ status \_ estendido \_ final**
</dt> <dd> <dl> <dt>

13909 (0x3655)
</dt> <dt>



ERRO \_ IPSec \_ Ike \_ neg de \_ status \_ estendido \_ final


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_BAD_SPI"></span><span id="error_ipsec_bad_spi"></span>**ERRO \_ SPI de IPSec \_ insatisfatório \_**
</dt> <dd> <dl> <dt>

13910 (0x3656)
</dt> <dt>



O SPI no pacote não corresponde a um SA IPsec válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_SA_LIFETIME_EXPIRED"></span><span id="error_ipsec_sa_lifetime_expired"></span>**ERRO \_ de \_ tempo de vida da SA IPsec \_ \_ expirado**
</dt> <dd> <dl> <dt>

13911 (0x3657)
</dt> <dt>



O pacote foi recebido em um SA IPsec cujo tempo de vida expirou.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_WRONG_SA"></span><span id="error_ipsec_wrong_sa"></span>**ERRO de \_ IPSec \_ errado \_ SA**
</dt> <dd> <dl> <dt>

13912 (0x3658)
</dt> <dt>



O pacote foi recebido em um SA IPsec que não corresponde às características do pacote.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_REPLAY_CHECK_FAILED"></span><span id="error_ipsec_replay_check_failed"></span>**ERRO \_ de \_ verificação de reprodução de IPSec \_ \_ falhou**
</dt> <dd> <dl> <dt>

13913 (0x3659)
</dt> <dt>



Falha na verificação de repetição do número de sequência de pacote.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_INVALID_PACKET"></span><span id="error_ipsec_invalid_packet"></span>**ERRO de \_ pacote de IPSec \_ inválido \_**
</dt> <dd> <dl> <dt>

13914 (0x365A)
</dt> <dt>



O cabeçalho IPsec e/ou o trailer no pacote é inválido.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_INTEGRITY_CHECK_FAILED"></span><span id="error_ipsec_integrity_check_failed"></span>**ERRO \_ \_ na verificação de integridade do IPSec \_ \_**
</dt> <dd> <dl> <dt>

13915 (0x365B)
</dt> <dt>



Falha na verificação de integridade do IPsec.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_CLEAR_TEXT_DROP"></span><span id="error_ipsec_clear_text_drop"></span>**ERRO \_ ao \_ \_ remover texto não criptografado IPSec \_**
</dt> <dd> <dl> <dt>

13916 (0x365C)
</dt> <dt>



O IPsec removeu um pacote de texto não criptografado.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_AUTH_FIREWALL_DROP"></span><span id="error_ipsec_auth_firewall_drop"></span>**ERRO \_ ao \_ \_ remover firewall de autenticação IPsec \_**
</dt> <dd> <dl> <dt>

13917 (0x365D)
</dt> <dt>



O IPsec removeu um pacote ESP de entrada no modo de firewall autenticado. Essa queda é benigna.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_THROTTLE_DROP"></span><span id="error_ipsec_throttle_drop"></span>**ERRO \_ ao \_ remover limitação IPSec \_**
</dt> <dd> <dl> <dt>

13918 (0x365E)
</dt> <dt>



O IPsec removeu um pacote devido à limitação do DoS.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_DOSP_BLOCK"></span><span id="error_ipsec_dosp_block"></span>**ERRO \_ de \_ bloqueio de DOSP IPSec \_**
</dt> <dd> <dl> <dt>

13925 (0x3665)
</dt> <dt>



A proteção de DoS IPsec correspondeu a uma regra de bloqueio explícita.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_DOSP_RECEIVED_MULTICAST"></span><span id="error_ipsec_dosp_received_multicast"></span>**ERRO \_ IPSec \_ DOSP \_ recebido \_ multicast**
</dt> <dd> <dl> <dt>

13926 (0x3666)
</dt> <dt>



A proteção de DoS IPsec recebeu um pacote multicast específico de IPsec que não é permitido.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_DOSP_INVALID_PACKET"></span><span id="error_ipsec_dosp_invalid_packet"></span>**ERRO de \_ pacote de IPSec \_ DOSP \_ inválido \_**
</dt> <dd> <dl> <dt>

13927 (0x3667)
</dt> <dt>



A proteção de DoS IPsec recebeu um pacote formatado incorretamente.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_DOSP_STATE_LOOKUP_FAILED"></span><span id="error_ipsec_dosp_state_lookup_failed"></span>**ERRO \_ de \_ pesquisa de estado de DOSP IPSec \_ \_ \_ falhou**
</dt> <dd> <dl> <dt>

13928 (0x3668)
</dt> <dt>



A proteção do DoS IPsec falhou ao pesquisar o estado.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_DOSP_MAX_ENTRIES"></span><span id="error_ipsec_dosp_max_entries"></span>**ERRO \_ ao \_ DOSP \_ máximo de \_ entradas IPSec**
</dt> <dd> <dl> <dt>

13929 (0x3669)
</dt> <dt>



Falha na proteção do DoS IPsec ao criar o estado porque o número máximo de entradas permitidas pela política foi atingido.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_DOSP_KEYMOD_NOT_ALLOWED"></span><span id="error_ipsec_dosp_keymod_not_allowed"></span>**ERRO \_ IPSec \_ DOSP \_ KEYMOD \_ não \_ permitido**
</dt> <dd> <dl> <dt>

13930 (0x366A)
</dt> <dt>



A proteção de DoS IPsec recebeu um pacote de negociação IPsec para um módulo de chaveamento que não é permitido pela política.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_DOSP_NOT_INSTALLED"></span><span id="error_ipsec_dosp_not_installed"></span>**ERRO \_ \_ DOSP IPSec \_ não \_ instalado**
</dt> <dd> <dl> <dt>

13931 (0x366B)
</dt> <dt>



A proteção de DoS IPsec não foi habilitada.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_DOSP_MAX_PER_IP_RATELIMIT_QUEUES"></span><span id="error_ipsec_dosp_max_per_ip_ratelimit_queues"></span>**ERRO \_ de \_ DOSP \_ máximo de IPSec \_ por \_ filas de RATELIMIT de IP \_ \_**
</dt> <dd> <dl> <dt>

13932 (0x366C)
</dt> <dt>



Falha na proteção do DoS IPsec ao criar uma fila por limite de taxa IP interna porque o número máximo de filas permitidas pela política foi atingido.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_SECTION_NOT_FOUND"></span><span id="error_sxs_section_not_found"></span>**ERRO \_ na \_ seção SxS \_ não \_ encontrada**
</dt> <dd> <dl> <dt>

14000 (0x36B0)
</dt> <dt>



A seção solicitada não estava presente no contexto de ativação.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_CANT_GEN_ACTCTX"></span><span id="error_sxs_cant_gen_actctx"></span>**ERRO \_ SxS não é \_ \_ Gen \_ ACTCTX**
</dt> <dd> <dl> <dt>

14001 (0x36B1)
</dt> <dt>



Falha ao iniciar o aplicativo porque sua configuração lado a lado está incorreta. Consulte o log de eventos do aplicativo ou use a ferramenta de sxstrace.exe de linha de comando para obter mais detalhes.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_INVALID_ACTCTXDATA_FORMAT"></span><span id="error_sxs_invalid_actctxdata_format"></span>**ERRO \_ do \_ \_ formato ACTCTXDATA \_ inválido de SXS**
</dt> <dd> <dl> <dt>

14002 (0x36B2)
</dt> <dt>



O formato de dados de associação de aplicativo é inválido.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_ASSEMBLY_NOT_FOUND"></span><span id="error_sxs_assembly_not_found"></span>**ERRO \_ de \_ assembly SxS \_ não \_ encontrado**
</dt> <dd> <dl> <dt>

14003 (0x36B3)
</dt> <dt>



O assembly referenciado não está instalado no seu sistema.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_MANIFEST_FORMAT_ERROR"></span><span id="error_sxs_manifest_format_error"></span>**erro \_ de \_ formato de manifesto SxS \_ \_**
</dt> <dd> <dl> <dt>

14004 (0x36B4)
</dt> <dt>



O arquivo de manifesto não começa com as informações de marca e formato necessárias.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_MANIFEST_PARSE_ERROR"></span><span id="error_sxs_manifest_parse_error"></span>**erro \_ de \_ análise do manifesto SxS \_ \_**
</dt> <dd> <dl> <dt>

14005 (0x36B5)
</dt> <dt>



O arquivo de manifesto contém um ou mais erros de sintaxe.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_ACTIVATION_CONTEXT_DISABLED"></span><span id="error_sxs_activation_context_disabled"></span>**ERRO \_ de \_ contexto de ativação SxS \_ \_ desabilitado**
</dt> <dd> <dl> <dt>

14006 (0x36B6)
</dt> <dt>



O aplicativo tentou ativar um contexto de ativação desabilitado.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_KEY_NOT_FOUND"></span><span id="error_sxs_key_not_found"></span>**ERRO \_ de \_ chave SxS \_ não \_ encontrada**
</dt> <dd> <dl> <dt>

14007 (0x36B7)
</dt> <dt>



A chave de pesquisa solicitada não foi encontrada em nenhum contexto de ativação ativo.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_VERSION_CONFLICT"></span><span id="error_sxs_version_conflict"></span>**ERRO \_ de \_ conflito de versão de SxS \_**
</dt> <dd> <dl> <dt>

14008 (0x36B8)
</dt> <dt>



Uma versão de componente exigida pelo aplicativo está em conflito com outra versão de componente já ativa.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_WRONG_SECTION_TYPE"></span><span id="error_sxs_wrong_section_type"></span>**ERRO \_ de \_ \_ tipo de seção errado de SxS \_**
</dt> <dd> <dl> <dt>

14009 (0x36B9)
</dt> <dt>



O tipo de seção de contexto de ativação solicitado não corresponde à API de consulta usada.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_THREAD_QUERIES_DISABLED"></span><span id="error_sxs_thread_queries_disabled"></span>**ERRO \_ de \_ consultas de thread SxS \_ \_ desabilitadas**
</dt> <dd> <dl> <dt>

14010 (0x36BA)
</dt> <dt>



A falta de recursos do sistema exigiu que a ativação isolada fosse desabilitada para o thread atual de execução.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_PROCESS_DEFAULT_ALREADY_SET"></span><span id="error_sxs_process_default_already_set"></span>**ERRO \_ de \_ processo SxS o \_ padrão \_ já está \_ definido**
</dt> <dd> <dl> <dt>

14011 (0x36BB)
</dt> <dt>



Falha ao tentar definir o contexto de ativação padrão do processo porque o contexto de ativação padrão do processo já foi definido.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_UNKNOWN_ENCODING_GROUP"></span><span id="error_sxs_unknown_encoding_group"></span>**ERRO \_ grupo de codificação de SxS \_ desconhecido \_ \_**
</dt> <dd> <dl> <dt>

14012 (0x36BC)
</dt> <dt>



O identificador do grupo de codificação especificado não é reconhecido.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_UNKNOWN_ENCODING"></span><span id="error_sxs_unknown_encoding"></span>**ERRO de \_ codificação de SxS \_ desconhecido \_**
</dt> <dd> <dl> <dt>

14013 (0x36BD)
</dt> <dt>



A codificação solicitada não é reconhecida.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_INVALID_XML_NAMESPACE_URI"></span><span id="error_sxs_invalid_xml_namespace_uri"></span>**ERRO \_ \_ URI de \_ namespace XML inválido \_ SxS \_**
</dt> <dd> <dl> <dt>

14014 (0x36BE)
</dt> <dt>



O manifesto contém uma referência a um URI inválido.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_ROOT_MANIFEST_DEPENDENCY_NOT_INSTALLED"></span><span id="error_sxs_root_manifest_dependency_not_installed"></span>**ERRO \_ de \_ dependência de manifesto raiz SxS \_ \_ \_ não \_ instalado**
</dt> <dd> <dl> <dt>

14015 (0x36BF)
</dt> <dt>



O manifesto do aplicativo contém uma referência a um assembly dependente que não está instalado.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_LEAF_MANIFEST_DEPENDENCY_NOT_INSTALLED"></span><span id="error_sxs_leaf_manifest_dependency_not_installed"></span>**ERRO \_ de \_ dependência de manifesto folha SxS \_ \_ \_ não \_ instalado**
</dt> <dd> <dl> <dt>

14016 (0x36C0)
</dt> <dt>



O manifesto para um assembly usado pelo aplicativo tem uma referência a um assembly dependente que não está instalado.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_INVALID_ASSEMBLY_IDENTITY_ATTRIBUTE"></span><span id="error_sxs_invalid_assembly_identity_attribute"></span>**ERRO \_ do \_ \_ atributo de identidade de assembly inválido \_ SxS \_**
</dt> <dd> <dl> <dt>

14017 (0x36C1)
</dt> <dt>



O manifesto contém um atributo para a identidade do assembly que não é válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_MANIFEST_MISSING_REQUIRED_DEFAULT_NAMESPACE"></span><span id="error_sxs_manifest_missing_required_default_namespace"></span>**ERRO \_ de \_ manifesto SxS \_ ausente no \_ \_ namespace padrão necessário \_**
</dt> <dd> <dl> <dt>

14018 (0x36C2)
</dt> <dt>



O manifesto não tem a especificação de namespace padrão necessária no elemento assembly.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_MANIFEST_INVALID_REQUIRED_DEFAULT_NAMESPACE"></span><span id="error_sxs_manifest_invalid_required_default_namespace"></span>**ERRO \_ de \_ manifesto \_ SxS \_ inválido \_ namespace padrão necessário \_**
</dt> <dd> <dl> <dt>

14019 (0x36C3)
</dt> <dt>



O manifesto tem um namespace padrão especificado no elemento assembly, mas seu valor não é "urn: schemas-microsoft-com: asm. v1".


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_PRIVATE_MANIFEST_CROSS_PATH_WITH_REPARSE_POINT"></span><span id="error_sxs_private_manifest_cross_path_with_reparse_point"></span>**ERRO \_ \_ de caminho privado do manifesto particular do SxS \_ \_ \_ \_ com \_ ponto de nova análise \_**
</dt> <dd> <dl> <dt>

14020 (0x36C4)
</dt> <dt>



A investigação do manifesto particular cruzou um caminho com um ponto de nova análise sem suporte.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_DUPLICATE_DLL_NAME"></span><span id="error_sxs_duplicate_dll_name"></span>**ERRO \_ \_ nome de \_ dll duplicado SxS \_**
</dt> <dd> <dl> <dt>

14021 (0x36C5)
</dt> <dt>



Dois ou mais componentes referenciados direta ou indiretamente pelo manifesto do aplicativo têm arquivos com o mesmo nome.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_DUPLICATE_WINDOWCLASS_NAME"></span><span id="error_sxs_duplicate_windowclass_name"></span>**ERRO \_ \_ nome de \_ WINDOWCLASS duplicado SxS \_**
</dt> <dd> <dl> <dt>

14022 (0x36C6)
</dt> <dt>



Dois ou mais componentes referenciados direta ou indiretamente pelo manifesto do aplicativo têm classes de janela com o mesmo nome.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_DUPLICATE_CLSID"></span><span id="error_sxs_duplicate_clsid"></span>**ERRO \_ de \_ CLSID duplicado de SxS \_**
</dt> <dd> <dl> <dt>

14023 (0x36C7)
</dt> <dt>



Dois ou mais componentes referenciados direta ou indiretamente pelo manifesto do aplicativo têm os mesmos CLSIDs de servidor COM.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_DUPLICATE_IID"></span><span id="error_sxs_duplicate_iid"></span>**ERRO \_ de \_ IID duplicado de SxS \_**
</dt> <dd> <dl> <dt>

14024 (0x36C8)
</dt> <dt>



Dois ou mais componentes referenciados direta ou indiretamente pelo manifesto do aplicativo têm proxies para a mesma interface COM IIDs.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_DUPLICATE_TLBID"></span><span id="error_sxs_duplicate_tlbid"></span>**ERRO \_ \_ TLBID duplicado SxS \_**
</dt> <dd> <dl> <dt>

14025 (0x36C9)
</dt> <dt>



Dois ou mais componentes referenciados direta ou indiretamente pelo manifesto do aplicativo têm a mesma biblioteca de tipos COM TLBIDs.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_DUPLICATE_PROGID"></span><span id="error_sxs_duplicate_progid"></span>**ERRO \_ \_ ProgID duplicado SxS \_**
</dt> <dd> <dl> <dt>

14026 (0x36CA)
</dt> <dt>



Dois ou mais componentes referenciados direta ou indiretamente pelo manifesto do aplicativo têm as mesmas ProgIDs COM.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_DUPLICATE_ASSEMBLY_NAME"></span><span id="error_sxs_duplicate_assembly_name"></span>**ERRO \_ de \_ \_ nome de assembly duplicado SxS \_**
</dt> <dd> <dl> <dt>

14027 (0x36CB)
</dt> <dt>



Dois ou mais componentes referenciados direta ou indiretamente pelo manifesto do aplicativo são versões diferentes do mesmo componente que não é permitido.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_FILE_HASH_MISMATCH"></span><span id="error_sxs_file_hash_mismatch"></span>**ERRO \_ de \_ \_ incompatibilidade de hash de arquivo SxS \_**
</dt> <dd> <dl> <dt>

14028 (0x36CC)
</dt> <dt>



O arquivo de um componente não corresponde às informações de verificação presentes no manifesto do componente.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_POLICY_PARSE_ERROR"></span><span id="error_sxs_policy_parse_error"></span>**erro \_ de \_ análise de política SxS \_ \_**
</dt> <dd> <dl> <dt>

14029 (0x36CD)
</dt> <dt>



O manifesto da política contém um ou mais erros de sintaxe.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_MISSINGQUOTE"></span><span id="error_sxs_xml_e_missingquote"></span>**ERRO de \_ SxS \_ XML \_ E \_ MISSINGQUOTE**
</dt> <dd> <dl> <dt>

14030 (0x36CE)
</dt> <dt>



Erro de análise do manifesto: um literal de cadeia de caracteres era esperado, mas nenhum caractere de aspas de abertura foi encontrado.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_COMMENTSYNTAX"></span><span id="error_sxs_xml_e_commentsyntax"></span>**ERRO de \_ SxS \_ XML \_ E \_ COMMENTSYNTAX**
</dt> <dd> <dl> <dt>

14031 (0x36CF)
</dt> <dt>



Erro de análise do manifesto: sintaxe incorreta usada em um comentário.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_BADSTARTNAMECHAR"></span><span id="error_sxs_xml_e_badstartnamechar"></span>**ERRO de \_ SxS \_ XML \_ E \_ BADSTARTNAMECHAR**
</dt> <dd> <dl> <dt>

14032 (0x36D0)
</dt> <dt>



Erro de análise do manifesto: um nome foi iniciado com um caractere inválido.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_BADNAMECHAR"></span><span id="error_sxs_xml_e_badnamechar"></span>**ERRO de \_ SxS \_ XML \_ E \_ BADNAMECHAR**
</dt> <dd> <dl> <dt>

14033 (0x36D1)
</dt> <dt>



Erro de análise do manifesto: um nome continha um caractere inválido.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_BADCHARINSTRING"></span><span id="error_sxs_xml_e_badcharinstring"></span>**ERRO de \_ SxS \_ XML \_ E \_ BADCHARINSTRING**
</dt> <dd> <dl> <dt>

14034 (0x36D2)
</dt> <dt>



Erro de análise do manifesto: um literal de cadeia de caracteres continha um caractere inválido.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_XMLDECLSYNTAX"></span><span id="error_sxs_xml_e_xmldeclsyntax"></span>**ERRO de \_ SxS \_ XML \_ E \_ XMLDECLSYNTAX**
</dt> <dd> <dl> <dt>

14035 (0x36D3)
</dt> <dt>



Erro de análise do manifesto: sintaxe inválida para uma declaração XML.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_BADCHARDATA"></span><span id="error_sxs_xml_e_badchardata"></span>**ERRO de \_ SxS \_ XML \_ E \_ BADCHARDATA**
</dt> <dd> <dl> <dt>

14036 (0x36D4)
</dt> <dt>



Erro de análise do manifesto: um caractere inválido foi encontrado no conteúdo do texto.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_MISSINGWHITESPACE"></span><span id="error_sxs_xml_e_missingwhitespace"></span>**ERRO de \_ SxS \_ XML \_ E \_ MISSINGWHITESPACE**
</dt> <dd> <dl> <dt>

14037 (0x36D5)
</dt> <dt>



Erro de análise do manifesto: espaço em branco necessário ausente.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_EXPECTINGTAGEND"></span><span id="error_sxs_xml_e_expectingtagend"></span>**ERRO de \_ SxS \_ XML \_ E \_ EXPECTINGTAGEND**
</dt> <dd> <dl> <dt>

14038 (0x36D6)
</dt> <dt>



Erro de análise do manifesto: o caractere ' > ' era esperado.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_MISSINGSEMICOLON"></span><span id="error_sxs_xml_e_missingsemicolon"></span>**ERRO de \_ SxS \_ XML \_ E \_ MISSINGSEMICOLON**
</dt> <dd> <dl> <dt>

14039 (0x36D7)
</dt> <dt>



Erro de análise do manifesto: um caractere de ponto e vírgula era esperado.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_UNBALANCEDPAREN"></span><span id="error_sxs_xml_e_unbalancedparen"></span>**ERRO de \_ SxS \_ XML \_ E \_ UNBALANCEDPAREN**
</dt> <dd> <dl> <dt>

14040 (0x36D8)
</dt> <dt>



Erro de análise do manifesto: parênteses desbalanceado.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_INTERNALERROR"></span><span id="error_sxs_xml_e_internalerror"></span>**ERRO de \_ SxS \_ XML \_ E \_ INTERNALERROR**
</dt> <dd> <dl> <dt>

14041 (0x36D9)
</dt> <dt>



Erro de análise do manifesto: erro interno.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_UNEXPECTED_WHITESPACE"></span><span id="error_sxs_xml_e_unexpected_whitespace"></span>**ERRO de \_ SxS \_ XML \_ E espaço em \_ branco inesperado \_**
</dt> <dd> <dl> <dt>

14042 (0x36DA)
</dt> <dt>



Erro de análise do manifesto: espaço em branco não é permitido neste local.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_INCOMPLETE_ENCODING"></span><span id="error_sxs_xml_e_incomplete_encoding"></span>**ERRO \_ de \_ codificação de XML E de SxS \_ \_ incompleto \_**
</dt> <dd> <dl> <dt>

14043 (0x36DB)
</dt> <dt>



Erro de análise do manifesto: fim do arquivo alcançado em estado inválido para a codificação atual.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_MISSING_PAREN"></span><span id="error_sxs_xml_e_missing_paren"></span>**ERRO \_ de \_ SxS \_ XML \_ E \_ parênteses ausentes**
</dt> <dd> <dl> <dt>

14044 (0x36DC)
</dt> <dt>



Erro de análise do manifesto: parêntese ausente.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_EXPECTINGCLOSEQUOTE"></span><span id="error_sxs_xml_e_expectingclosequote"></span>**ERRO de \_ SxS \_ XML \_ E \_ EXPECTINGCLOSEQUOTE**
</dt> <dd> <dl> <dt>

14045 (0x36DD)
</dt> <dt>



Erro de análise do manifesto: um caractere de aspas simples ou duplas ( \\ ' ou \\ ") está ausente.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_MULTIPLE_COLONS"></span><span id="error_sxs_xml_e_multiple_colons"></span>**ERRO de \_ SxS \_ XML \_ E \_ vários \_ dois-pontos**
</dt> <dd> <dl> <dt>

14046 (0x36DE)
</dt> <dt>



Erro de análise do manifesto: não são permitidos vários dois-pontos em um nome.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_INVALID_DECIMAL"></span><span id="error_sxs_xml_e_invalid_decimal"></span>**ERRO \_ de \_ SxS \_ XML \_ E \_ decimal inválido**
</dt> <dd> <dl> <dt>

14047 (0x36DF)
</dt> <dt>



Erro de análise do manifesto: caractere inválido para dígito decimal.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_INVALID_HEXIDECIMAL"></span><span id="error_sxs_xml_e_invalid_hexidecimal"></span>**ERRO \_ de \_ SxS \_ XML \_ E \_ hexadecimal inválido**
</dt> <dd> <dl> <dt>

14048 (0x36E0)
</dt> <dt>



Erro de análise do manifesto: caractere inválido para dígito hexadecimal.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_INVALID_UNICODE"></span><span id="error_sxs_xml_e_invalid_unicode"></span>**ERRO \_ de \_ SxS \_ XML \_ E \_ Unicode inválido**
</dt> <dd> <dl> <dt>

14049 (0x36E1)
</dt> <dt>



Erro de análise do manifesto: valor de caractere Unicode inválido para esta plataforma.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_WHITESPACEORQUESTIONMARK"></span><span id="error_sxs_xml_e_whitespaceorquestionmark"></span>**ERRO de \_ SxS \_ XML \_ E \_ WHITESPACEORQUESTIONMARK**
</dt> <dd> <dl> <dt>

14050 (0x36E2)
</dt> <dt>



Erro de análise do manifesto: esperando espaço em branco ou '? '.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_UNEXPECTEDENDTAG"></span><span id="error_sxs_xml_e_unexpectedendtag"></span>**ERRO de \_ SxS \_ XML \_ E \_ UNEXPECTEDENDTAG**
</dt> <dd> <dl> <dt>

14051 (0x36E3)
</dt> <dt>



Erro de análise do manifesto: a marca de fim não era esperada neste local.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_UNCLOSEDTAG"></span><span id="error_sxs_xml_e_unclosedtag"></span>**ERRO de \_ SxS \_ XML \_ E \_ UNCLOSEDTAG**
</dt> <dd> <dl> <dt>

14052 (0x36E4)
</dt> <dt>



Erro de análise do manifesto: as seguintes marcas não foram fechadas: %1.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_DUPLICATEATTRIBUTE"></span><span id="error_sxs_xml_e_duplicateattribute"></span>**ERRO de \_ SxS \_ XML \_ E \_ duplicataattribute**
</dt> <dd> <dl> <dt>

14053 (0x36E5)
</dt> <dt>



Erro de análise do manifesto: atributo duplicado.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_MULTIPLEROOTS"></span><span id="error_sxs_xml_e_multipleroots"></span>**ERRO de \_ SxS \_ XML \_ E \_ MULTIPLEROOTS**
</dt> <dd> <dl> <dt>

14054 (0x36E6)
</dt> <dt>



Erro de análise do manifesto: apenas um elemento de nível superior é permitido em um documento XML.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_INVALIDATROOTLEVEL"></span><span id="error_sxs_xml_e_invalidatrootlevel"></span>**ERRO de \_ SxS \_ XML \_ E \_ INVALIDATROOTLEVEL**
</dt> <dd> <dl> <dt>

14055 (0x36E7)
</dt> <dt>



Erro de análise do manifesto: inválido no nível superior do documento.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_BADXMLDECL"></span><span id="error_sxs_xml_e_badxmldecl"></span>**ERRO de \_ SxS \_ XML \_ E \_ BADXMLDECL**
</dt> <dd> <dl> <dt>

14056 (0x36E8)
</dt> <dt>



Erro de análise do manifesto: declaração XML inválida.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_MISSINGROOT"></span><span id="error_sxs_xml_e_missingroot"></span>**ERRO de \_ SxS \_ XML \_ E \_ MISSINGROOT**
</dt> <dd> <dl> <dt>

14057 (0x36E9)
</dt> <dt>



Erro de análise do manifesto: o documento XML deve ter um elemento de nível superior.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_UNEXPECTEDEOF"></span><span id="error_sxs_xml_e_unexpectedeof"></span>**ERRO de \_ SxS \_ XML \_ E \_ UNEXPECTEDEOF**
</dt> <dd> <dl> <dt>

14058 (0x36EA)
</dt> <dt>



Erro de análise do manifesto: fim de arquivo inesperado.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_BADPEREFINSUBSET"></span><span id="error_sxs_xml_e_badperefinsubset"></span>**ERRO de \_ SxS \_ XML \_ E \_ BADPEREFINSUBSET**
</dt> <dd> <dl> <dt>

14059 (0x36EB)
</dt> <dt>



Erro de análise do manifesto: entidades de parâmetro não podem ser usadas dentro de declarações de marcação em um subconjunto interno.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_UNCLOSEDSTARTTAG"></span><span id="error_sxs_xml_e_unclosedstarttag"></span>**ERRO de \_ SxS \_ XML \_ E \_ UNCLOSEDSTARTTAG**
</dt> <dd> <dl> <dt>

14060 (0x36EC)
</dt> <dt>



Erro de análise do manifesto: o elemento não foi fechado.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_UNCLOSEDENDTAG"></span><span id="error_sxs_xml_e_unclosedendtag"></span>**ERRO de \_ SxS \_ XML \_ E \_ UNCLOSEDENDTAG**
</dt> <dd> <dl> <dt>

14061 (0x36ED)
</dt> <dt>



Erro de análise do manifesto: o elemento final estava faltando o caractere ' > '.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_UNCLOSEDSTRING"></span><span id="error_sxs_xml_e_unclosedstring"></span>**ERRO \_ de \_ XML SxS \_ E não \_ closedstring**
</dt> <dd> <dl> <dt>

14062 (0x36EE)
</dt> <dt>



Erro de análise do manifesto: um literal de cadeia de caracteres não foi fechado.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_UNCLOSEDCOMMENT"></span><span id="error_sxs_xml_e_unclosedcomment"></span>**ERRO de \_ SxS \_ XML \_ E \_ UNCLOSEDCOMMENT**
</dt> <dd> <dl> <dt>

14063 (0x36EF)
</dt> <dt>



Erro de análise do manifesto: um comentário não foi fechado.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_UNCLOSEDDECL"></span><span id="error_sxs_xml_e_uncloseddecl"></span>**ERRO de \_ SxS \_ XML \_ E \_ UNCLOSEDDECL**
</dt> <dd> <dl> <dt>

14064 (0x36F0)
</dt> <dt>



Erro de análise do manifesto: uma declaração não foi fechada.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_UNCLOSEDCDATA"></span><span id="error_sxs_xml_e_unclosedcdata"></span>**ERRO de \_ SxS \_ XML \_ E \_ UNCLOSEDCDATA**
</dt> <dd> <dl> <dt>

14065 (0x36F1)
</dt> <dt>



Erro de análise do manifesto: uma seção CDATA não foi fechada.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_RESERVEDNAMESPACE"></span><span id="error_sxs_xml_e_reservednamespace"></span>**ERRO de \_ SxS \_ XML \_ E \_ RESERVEDNAMESPACE**
</dt> <dd> <dl> <dt>

14066 (0x36F2)
</dt> <dt>



Erro de análise do manifesto: o prefixo do namespace não tem permissão para iniciar com a cadeia de caracteres reservada "XML".


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_INVALIDENCODING"></span><span id="error_sxs_xml_e_invalidencoding"></span>**ERRO de \_ SxS \_ XML \_ E \_ INVALIDENCODING**
</dt> <dd> <dl> <dt>

14067 (0x36F3)
</dt> <dt>



Erro de análise do manifesto: o sistema não oferece suporte à codificação especificada.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_INVALIDSWITCH"></span><span id="error_sxs_xml_e_invalidswitch"></span>**ERRO de \_ SxS \_ XML \_ E \_ INVALIDSWITCH**
</dt> <dd> <dl> <dt>

14068 (0x36F4)
</dt> <dt>



Erro de análise do manifesto: não há suporte para alternar da codificação atual para a codificação especificada.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_BADXMLCASE"></span><span id="error_sxs_xml_e_badxmlcase"></span>**ERRO de \_ SxS \_ XML \_ E \_ BADXMLCASE**
</dt> <dd> <dl> <dt>

14069 (0x36F5)
</dt> <dt>



Erro de análise do manifesto: o nome ' XML ' está reservado e deve estar em letras minúsculas.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_INVALID_STANDALONE"></span><span id="error_sxs_xml_e_invalid_standalone"></span>**ERRO \_ de \_ SxS \_ XML \_ E \_ autônomos inválidos**
</dt> <dd> <dl> <dt>

14070 (0x36F6)
</dt> <dt>



Erro de análise do manifesto: o atributo autônomo deve ter o valor ' Yes ' ou ' no '.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_UNEXPECTED_STANDALONE"></span><span id="error_sxs_xml_e_unexpected_standalone"></span>**ERRO \_ de \_ SxS \_ XML \_ E \_ autônomo inesperado**
</dt> <dd> <dl> <dt>

14071 (0x36F7)
</dt> <dt>



Erro de análise do manifesto: o atributo autônomo não pode ser usado em entidades externas.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_INVALID_VERSION"></span><span id="error_sxs_xml_e_invalid_version"></span>**ERRO \_ de \_ SxS \_ XML \_ E \_ versão inválida**
</dt> <dd> <dl> <dt>

14072 (0x36F8)
</dt> <dt>



Erro de análise do manifesto: número de versão inválido.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_MISSINGEQUALS"></span><span id="error_sxs_xml_e_missingequals"></span>**ERRO de \_ SxS \_ XML \_ E \_ MISSINGEQUALS**
</dt> <dd> <dl> <dt>

14073 (0x36F9)
</dt> <dt>



Erro de análise do manifesto: sinal de igual ausente entre atributo e valor de atributo.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_PROTECTION_RECOVERY_FAILED"></span><span id="error_sxs_protection_recovery_failed"></span>**ERRO \_ \_ ao recuperar proteção de SxS \_ \_ falhou**
</dt> <dd> <dl> <dt>

14074 (0x36FA)
</dt> <dt>



Erro de proteção de assembly: não é possível recuperar o assembly especificado.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_PROTECTION_PUBLIC_KEY_TOO_SHORT"></span><span id="error_sxs_protection_public_key_too_short"></span>**ERRO \_ \_ chave pública de proteção SxS \_ \_ \_ muito \_ curta**
</dt> <dd> <dl> <dt>

14075 (0x36FB)
</dt> <dt>



Erro de proteção de assembly: a chave pública de um assembly era muito curta para ser permitida.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_PROTECTION_CATALOG_NOT_VALID"></span><span id="error_sxs_protection_catalog_not_valid"></span>**ERRO \_ o \_ Catálogo de proteção SxS \_ não é \_ \_ válido**
</dt> <dd> <dl> <dt>

14076 (0x36FC)
</dt> <dt>



Erro de proteção de assembly: o catálogo de um assembly não é válido ou não corresponde ao manifesto do assembly.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_UNTRANSLATABLE_HRESULT"></span><span id="error_sxs_untranslatable_hresult"></span>**ERRO \_ SxS não \_ traduzível \_ HRESULT**
</dt> <dd> <dl> <dt>

14077 (0x36FD)
</dt> <dt>



Não foi possível converter um HRESULT em um código de erro Win32 correspondente.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_PROTECTION_CATALOG_FILE_MISSING"></span><span id="error_sxs_protection_catalog_file_missing"></span>**ERRO \_ de \_ arquivo de catálogo de proteção SxS \_ \_ \_ ausente**
</dt> <dd> <dl> <dt>

14078 (0x36FE)
</dt> <dt>



Erro de proteção de assembly: o catálogo de um assembly está ausente.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_MISSING_ASSEMBLY_IDENTITY_ATTRIBUTE"></span><span id="error_sxs_missing_assembly_identity_attribute"></span>**ERRO \_ SxS \_ faltando \_ \_ atributo de identidade de assembly \_**
</dt> <dd> <dl> <dt>

14079 (0x36FF)
</dt> <dt>



A identidade do assembly fornecida não tem um ou mais atributos que devem estar presentes neste contexto.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_INVALID_ASSEMBLY_IDENTITY_ATTRIBUTE_NAME"></span><span id="error_sxs_invalid_assembly_identity_attribute_name"></span>**ERRO \_ SxS \_ \_ nome do \_ atributo de identidade de assembly inválido \_ \_**
</dt> <dd> <dl> <dt>

14080 (0x3700)
</dt> <dt>



A identidade do assembly fornecida tem um ou mais nomes de atributo que contêm caracteres não permitidos em nomes XML.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_ASSEMBLY_MISSING"></span><span id="error_sxs_assembly_missing"></span>**ERRO \_ de \_ assembly SxS \_ ausente**
</dt> <dd> <dl> <dt>

14081 (0x3701)
</dt> <dt>



Não foi possível encontrar o assembly referenciado.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_CORRUPT_ACTIVATION_STACK"></span><span id="error_sxs_corrupt_activation_stack"></span>**ERRO \_ de \_ \_ pilha de ativação corrompida SxS \_**
</dt> <dd> <dl> <dt>

14082 (0x3702)
</dt> <dt>



A pilha de ativação do contexto de ativação para o thread em execução de execução está corrompida.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_CORRUPTION"></span><span id="error_sxs_corruption"></span>**ERRO \_ de \_ corrupção de SXS**
</dt> <dd> <dl> <dt>

14083 (0x3703)
</dt> <dt>



Os metadados de isolamento de aplicativo para este processo ou thread foram corrompidos.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_EARLY_DEACTIVATION"></span><span id="error_sxs_early_deactivation"></span>**ERRO \_ de \_ desativação do SxS no início \_**
</dt> <dd> <dl> <dt>

14084 (0x3704)
</dt> <dt>



O contexto de ativação que está sendo desativado não é o que foi ativado mais recentemente.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_INVALID_DEACTIVATION"></span><span id="error_sxs_invalid_deactivation"></span>**ERRO \_ de \_ \_ desativação de SxS inválido**
</dt> <dd> <dl> <dt>

14085 (0x3705)
</dt> <dt>



O contexto de ativação que está sendo desativado não está ativo para o thread atual de execução.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_MULTIPLE_DEACTIVATION"></span><span id="error_sxs_multiple_deactivation"></span>**ERRO \_ de \_ várias \_ desativação SxS**
</dt> <dd> <dl> <dt>

14086 (0x3706)
</dt> <dt>



O contexto de ativação que está sendo desativado já foi desativado.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_PROCESS_TERMINATION_REQUESTED"></span><span id="error_sxs_process_termination_requested"></span>**ERRO \_ de \_ término do processo SxS \_ \_ solicitado**
</dt> <dd> <dl> <dt>

14087 (0x3707)
</dt> <dt>



Um componente usado pelo recurso de isolamento solicitou o encerramento do processo.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_RELEASE_ACTIVATION_CONTEXT"></span><span id="error_sxs_release_activation_context"></span>**ERRO \_ \_ contexto de \_ ativação da versão SxS \_**
</dt> <dd> <dl> <dt>

14088 (0x3708)
</dt> <dt>



Um componente de modo kernel está liberando uma referência em um contexto de ativação.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_SYSTEM_DEFAULT_ACTIVATION_CONTEXT_EMPTY"></span><span id="error_sxs_system_default_activation_context_empty"></span>**ERRO \_ de \_ \_ contexto de ativação padrão do sistema SxS \_ \_ \_ vazio**
</dt> <dd> <dl> <dt>

14089 (0x3709)
</dt> <dt>



Não foi possível gerar o contexto de ativação do assembly padrão do sistema.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_INVALID_IDENTITY_ATTRIBUTE_VALUE"></span><span id="error_sxs_invalid_identity_attribute_value"></span>**ERRO \_ o \_ \_ valor do atributo de identidade inválido \_ SxS \_**
</dt> <dd> <dl> <dt>

14090 (0x370A)
</dt> <dt>



O valor de um atributo em uma identidade não está dentro do intervalo válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_INVALID_IDENTITY_ATTRIBUTE_NAME"></span><span id="error_sxs_invalid_identity_attribute_name"></span>**ERRO \_ \_ nome do \_ atributo de identidade inválido \_ SxS \_**
</dt> <dd> <dl> <dt>

14091 (0x370B)
</dt> <dt>



O nome de um atributo em uma identidade não está dentro do intervalo válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_IDENTITY_DUPLICATE_ATTRIBUTE"></span><span id="error_sxs_identity_duplicate_attribute"></span>**ERRO \_ de \_ \_ atributo duplicado de identidade SxS \_**
</dt> <dd> <dl> <dt>

14092 (0x370C)
</dt> <dt>



Uma identidade contém duas definições para o mesmo atributo.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_IDENTITY_PARSE_ERROR"></span><span id="error_sxs_identity_parse_error"></span>**ERRO \_ de \_ análise de identidade SxS do \_ \_ erro**
</dt> <dd> <dl> <dt>

14093 (0x370D)
</dt> <dt>



A cadeia de caracteres de identidade está malformada. Isso pode ser devido a uma vírgula à direita, mais de dois atributos não nomeados, nome de atributo ausente ou valor de atributo ausente.


</dt> </dl> </dd> <dt>

<span id="ERROR_MALFORMED_SUBSTITUTION_STRING"></span><span id="error_malformed_substitution_string"></span>**ERRO \_ de \_ cadeia de substituição malformado \_**
</dt> <dd> <dl> <dt>

14094 (0x370E)
</dt> <dt>



Uma cadeia de caracteres que contém conteúdo substituível localizado foi malformada. Um cifrão ($) foi seguido por algo diferente de um parêntese esquerdo ou outro sinal de dólar ou o parêntese direito de substituição não foi encontrado.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_INCORRECT_PUBLIC_KEY_TOKEN"></span><span id="error_sxs_incorrect_public_key_token"></span>**ERRO \_ de \_ \_ token de \_ chave \_ pública incorreto de SXS**
</dt> <dd> <dl> <dt>

14095 (0x370F)
</dt> <dt>



O token de chave pública não corresponde à chave pública especificada.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNMAPPED_SUBSTITUTION_STRING"></span><span id="error_unmapped_substitution_string"></span>**ERRO ao \_ Mapear \_ cadeia de caracteres de substituição \_**
</dt> <dd> <dl> <dt>

14096 (0x3710)
</dt> <dt>



Uma cadeia de caracteres de substituição não tinha mapeamento.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_ASSEMBLY_NOT_LOCKED"></span><span id="error_sxs_assembly_not_locked"></span>**ERRO \_ \_ assembly SxS \_ não \_ bloqueado**
</dt> <dd> <dl> <dt>

14097 (0x3711)
</dt> <dt>



O componente deve ser bloqueado antes de fazer a solicitação.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_COMPONENT_STORE_CORRUPT"></span><span id="error_sxs_component_store_corrupt"></span>**ERRO \_ de \_ repositório de componentes SxS \_ \_ corrompido**
</dt> <dd> <dl> <dt>

14098 (0x3712)
</dt> <dt>



O repositório de componentes foi corrompido.


</dt> </dl> </dd> <dt>

<span id="ERROR_ADVANCED_INSTALLER_FAILED"></span><span id="error_advanced_installer_failed"></span>**ERRO \_ \_ no instalador \_ avançado**
</dt> <dd> <dl> <dt>

14099 (0x3713)
</dt> <dt>



Um instalador avançado falhou durante a instalação ou manutenção.


</dt> </dl> </dd> <dt>

<span id="ERROR_XML_ENCODING_MISMATCH"></span><span id="error_xml_encoding_mismatch"></span>**incompatibilidade de \_ codificação XML de erro \_ \_**
</dt> <dd> <dl> <dt>

14100 (0x3714)
</dt> <dt>



A codificação de caracteres na declaração XML não correspondeu à codificação usada no documento.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_MANIFEST_IDENTITY_SAME_BUT_CONTENTS_DIFFERENT"></span><span id="error_sxs_manifest_identity_same_but_contents_different"></span>**ERRO \_ de \_ identidade de manifesto SxS \_ \_ igual \_ , mas \_ conteúdo \_ diferente**
</dt> <dd> <dl> <dt>

14101 (0x3715)
</dt> <dt>



As identidades dos manifestos são idênticas, mas seu conteúdo é diferente.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_IDENTITIES_DIFFERENT"></span><span id="error_sxs_identities_different"></span>**ERRO \_ de \_ identidades SxS \_ diferentes**
</dt> <dd> <dl> <dt>

14102 (0x3716)
</dt> <dt>



As identidades dos componentes são diferentes.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_ASSEMBLY_IS_NOT_A_DEPLOYMENT"></span><span id="error_sxs_assembly_is_not_a_deployment"></span>**ERRO \_ \_ o assembly \_ SxS \_ não é \_ uma \_ implantação**
</dt> <dd> <dl> <dt>

14103 (0x3717)
</dt> <dt>



O assembly não é uma implantação.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_FILE_NOT_PART_OF_ASSEMBLY"></span><span id="error_sxs_file_not_part_of_assembly"></span>**ERRO \_ o \_ arquivo SxS \_ não \_ faz parte \_ do \_ assembly**
</dt> <dd> <dl> <dt>

14104 (0x3718)
</dt> <dt>



O arquivo não faz parte do assembly.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_MANIFEST_TOO_BIG"></span><span id="error_sxs_manifest_too_big"></span>**ERRO \_ de \_ manifesto SxS \_ muito \_ grande**
</dt> <dd> <dl> <dt>

14105 (0x3719)
</dt> <dt>



O tamanho do manifesto excede o máximo permitido.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_SETTING_NOT_REGISTERED"></span><span id="error_sxs_setting_not_registered"></span>**ERRO \_ de \_ configuração de SxS \_ não \_ registrado**
</dt> <dd> <dl> <dt>

14106 (0x371A)
</dt> <dt>



A configuração não está registrada.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_TRANSACTION_CLOSURE_INCOMPLETE"></span><span id="error_sxs_transaction_closure_incomplete"></span>**ERRO \_ de \_ fechamento de transação SxS \_ \_ incompleto**
</dt> <dd> <dl> <dt>

14107 (0x371B)
</dt> <dt>



Um ou mais membros necessários da transação não estão presentes.


</dt> </dl> </dd> <dt>

<span id="ERROR_SMI_PRIMITIVE_INSTALLER_FAILED"></span><span id="error_smi_primitive_installer_failed"></span>**ERRO \_ \_ \_ falha no instalador primitivo SMI \_**
</dt> <dd> <dl> <dt>

14108 (0x371C)
</dt> <dt>



O instalador do SMI Primitive falhou durante a instalação ou manutenção.


</dt> </dl> </dd> <dt>

<span id="ERROR_GENERIC_COMMAND_FAILED"></span><span id="error_generic_command_failed"></span>**ERRO \_ \_ \_ falha no comando genérico**
</dt> <dd> <dl> <dt>

14109 (0x371D)
</dt> <dt>



Um executável de comando genérico retornou um resultado que indica falha.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_FILE_HASH_MISSING"></span><span id="error_sxs_file_hash_missing"></span>**ERRO \_ de \_ hash de arquivo SxS \_ \_ ausente**
</dt> <dd> <dl> <dt>

14110 (0x371E)
</dt> <dt>



Um componente não tem informações de verificação de arquivo em seu manifesto.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_INVALID_CHANNEL_PATH"></span><span id="error_evt_invalid_channel_path"></span>**ERRO \_ EVT \_ \_ caminho de canal inválido \_**
</dt> <dd> <dl> <dt>

15000 (0x3A98)
</dt> <dt>



O caminho de canal especificado é inválido.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_INVALID_QUERY"></span><span id="error_evt_invalid_query"></span>**ERRO \_ EVT \_ de \_ consulta inválida**
</dt> <dd> <dl> <dt>

15001 (0x3A99)
</dt> <dt>



A consulta especificada é inválida.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_PUBLISHER_METADATA_NOT_FOUND"></span><span id="error_evt_publisher_metadata_not_found"></span>**ERRO \_ EVT \_ metadados do Publicador \_ \_ não \_ encontrados**
</dt> <dd> <dl> <dt>

15002 (0x3A9A)
</dt> <dt>



Os metadados do Publicador não podem ser encontrados no recurso.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_EVENT_TEMPLATE_NOT_FOUND"></span><span id="error_evt_event_template_not_found"></span>**ERRO \_ de \_ modelo de evento EVT \_ \_ não \_ encontrado**
</dt> <dd> <dl> <dt>

15003 (0x3A9B)
</dt> <dt>



O modelo para uma definição de evento não pode ser encontrado no recurso (erro = %1).


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_INVALID_PUBLISHER_NAME"></span><span id="error_evt_invalid_publisher_name"></span>**ERRO \_ EVT \_ \_ nome de editor inválido \_**
</dt> <dd> <dl> <dt>

15004 (0x3A9C)
</dt> <dt>



O nome de editor especificado é inválido.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_INVALID_EVENT_DATA"></span><span id="error_evt_invalid_event_data"></span>**ERRO \_ EVT \_ \_ dados de eventos inválidos \_**
</dt> <dd> <dl> <dt>

15005 (0x3A9D)
</dt> <dt>



Os dados de evento gerados pelo Publicador não são compatíveis com a definição do modelo de evento no manifesto do editor.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_CHANNEL_NOT_FOUND"></span><span id="error_evt_channel_not_found"></span>**ERRO \_ EVT \_ canal \_ não \_ encontrado**
</dt> <dd> <dl> <dt>

15007 (0x3A9F)
</dt> <dt>



O canal especificado não pôde ser encontrado. Verifique a configuração do canal.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_MALFORMED_XML_TEXT"></span><span id="error_evt_malformed_xml_text"></span>**ERRO \_ EVT \_ de \_ texto XML malformado \_**
</dt> <dd> <dl> <dt>

15008 (0x3AA0)
</dt> <dt>



O texto XML especificado não estava bem formado. Consulte erro estendido para obter mais detalhes.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_SUBSCRIPTION_TO_DIRECT_CHANNEL"></span><span id="error_evt_subscription_to_direct_channel"></span>**\_ \_ assinatura de erro \_ EVT \_ para \_ canal direto**
</dt> <dd> <dl> <dt>

15009 (0x3AA1)
</dt> <dt>



O chamador está tentando assinar um canal direto que não é permitido. Os eventos de um canal direto vão diretamente para um arquivo de log e não podem ser assinados.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_CONFIGURATION_ERROR"></span><span id="error_evt_configuration_error"></span>**erro \_ de \_ configuração de EVT \_**
</dt> <dd> <dl> <dt>

15010 (0x3AA2)
</dt> <dt>



Erro de configuração.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_QUERY_RESULT_STALE"></span><span id="error_evt_query_result_stale"></span>**ERRO \_ EVT \_ do \_ resultado da consulta \_ obsoleto**
</dt> <dd> <dl> <dt>

15011 (0x3AA3)
</dt> <dt>



O resultado da consulta é obsoleto/inválido. Isso pode ser devido ao log ser limpo ou revertida depois que o resultado da consulta foi criado. Os usuários devem lidar com esse código liberando o objeto de resultado da consulta e reemitindo a consulta.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_QUERY_RESULT_INVALID_POSITION"></span><span id="error_evt_query_result_invalid_position"></span>**ERRO \_ EVT do \_ resultado da consulta \_ \_ posição inválida \_**
</dt> <dd> <dl> <dt>

15012 (0x3AA4)
</dt> <dt>



O resultado da consulta está atualmente em uma posição inválida.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_NON_VALIDATING_MSXML"></span><span id="error_evt_non_validating_msxml"></span>**ERRO \_ EVT \_ não \_ Validando o \_ MSXML**
</dt> <dd> <dl> <dt>

15013 (0x3AA5)
</dt> <dt>



O MSXML registrado não dá suporte à validação.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_FILTER_ALREADYSCOPED"></span><span id="error_evt_filter_alreadyscoped"></span>**ERRO \_ EVT \_ filtro \_ ALREADYSCOPED**
</dt> <dd> <dl> <dt>

15014 (0x3AA6)
</dt> <dt>



Uma expressão só pode ser seguida por uma alteração de operação de escopo se ela for avaliada como um conjunto de nós e ainda não fizer parte de alguma outra alteração de operação de escopo.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_FILTER_NOTELTSET"></span><span id="error_evt_filter_noteltset"></span>**ERRO \_ EVT \_ filtro \_ NOTELTSET**
</dt> <dd> <dl> <dt>

15015 (0x3AA7)
</dt> <dt>



Não é possível executar uma operação de etapa a partir de um termo que não representa um conjunto de elementos.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_FILTER_INVARG"></span><span id="error_evt_filter_invarg"></span>**ERRO \_ EVT \_ filtro \_ INVARG**
</dt> <dd> <dl> <dt>

15016 (0x3AA8)
</dt> <dt>



Os argumentos do lado esquerdo para operadores binários devem ser atributos, nós ou variáveis e os argumentos do lado direito devem ser constantes.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_FILTER_INVTEST"></span><span id="error_evt_filter_invtest"></span>**ERRO \_ EVT \_ filtro \_ INVTEST**
</dt> <dd> <dl> <dt>

15017 (0x3AA9)
</dt> <dt>



Uma operação de etapa deve envolver um teste de nó ou, no caso de um predicado, uma expressão algébricas para testar cada nó no conjunto de nós identificado pelo conjunto de nós anterior pode ser avaliada.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_FILTER_INVTYPE"></span><span id="error_evt_filter_invtype"></span>**ERRO \_ EVT \_ filtro \_ INVTYPE**
</dt> <dd> <dl> <dt>

15018 (0x3AAA)
</dt> <dt>



Não há suporte para este tipo de dados no momento.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_FILTER_PARSEERR"></span><span id="error_evt_filter_parseerr"></span>**ERRO \_ EVT \_ filtro \_ PARSEERR**
</dt> <dd> <dl> <dt>

15019 (0x3AAB)
</dt> <dt>



Ocorreu um erro de sintaxe na posição %1! d!.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_FILTER_UNSUPPORTEDOP"></span><span id="error_evt_filter_unsupportedop"></span>**ERRO \_ EVT \_ filtro \_ UNSUPPORTEDOP**
</dt> <dd> <dl> <dt>

15020 (0x3AAC)
</dt> <dt>



Este operador não tem suporte nesta implementação do filtro.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_FILTER_UNEXPECTEDTOKEN"></span><span id="error_evt_filter_unexpectedtoken"></span>**ERRO \_ EVT \_ filtro \_ UNEXPECTEDTOKEN**
</dt> <dd> <dl> <dt>

15021 (0x3AAD)
</dt> <dt>



O token encontrado era inesperado.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_INVALID_OPERATION_OVER_ENABLED_DIRECT_CHANNEL"></span><span id="error_evt_invalid_operation_over_enabled_direct_channel"></span>**ERRO \_ EVT \_ de \_ operação inválida sobre o \_ \_ \_ canal direto habilitado \_**
</dt> <dd> <dl> <dt>

15022 (0x3AAE)
</dt> <dt>



A operação solicitada não pode ser executada em um canal direto habilitado. O canal deve primeiro ser desabilitado antes da execução da operação solicitada.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_INVALID_CHANNEL_PROPERTY_VALUE"></span><span id="error_evt_invalid_channel_property_value"></span>**ERRO \_ EVT \_ \_ valor de propriedade de canal inválido \_ \_**
</dt> <dd> <dl> <dt>

15023 (0x3AAF)
</dt> <dt>



Propriedade do canal %1! s! contém valor inválido. O valor tem tipo inválido, está fora do intervalo válido, não pode ser atualizado ou não é suportado por este tipo de canal.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_INVALID_PUBLISHER_PROPERTY_VALUE"></span><span id="error_evt_invalid_publisher_property_value"></span>**ERRO \_ EVT \_ \_ valor de \_ propriedade de Publicador inválido \_**
</dt> <dd> <dl> <dt>

15024 (0x3AB0)
</dt> <dt>



Propriedade do Publicador %1! s! contém valor inválido. O valor tem tipo inválido, está fora do intervalo válido, não pode ser atualizado ou não é suportado por este tipo de editor.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_CHANNEL_CANNOT_ACTIVATE"></span><span id="error_evt_channel_cannot_activate"></span>**ERRO \_ EVT de \_ canal \_ não pode \_ Ativar**
</dt> <dd> <dl> <dt>

15025 (0x3AB1)
</dt> <dt>



Falha na ativação do canal.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_FILTER_TOO_COMPLEX"></span><span id="error_evt_filter_too_complex"></span>**filtro de erro \_ EVT \_ \_ muito \_ complexo**
</dt> <dd> <dl> <dt>

15026 (0x3AB2)
</dt> <dt>



A expressão XPath excedeu a complexidade com suporte. Symplify-o ou divida-o em duas ou mais expressões simples.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_MESSAGE_NOT_FOUND"></span><span id="error_evt_message_not_found"></span>**mensagem de erro \_ EVT \_ \_ não \_ encontrada**
</dt> <dd> <dl> <dt>

15027 (0x3AB3)
</dt> <dt>



o recurso de mensagem está presente, mas a mensagem não foi encontrada na tabela de cadeia de caracteres/mensagem.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_MESSAGE_ID_NOT_FOUND"></span><span id="error_evt_message_id_not_found"></span>**ID de mensagem de erro \_ EVT \_ \_ \_ não \_ encontrada**
</dt> <dd> <dl> <dt>

15028 (0x3AB4)
</dt> <dt>



Não foi possível encontrar a ID da mensagem desejada.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_UNRESOLVED_VALUE_INSERT"></span><span id="error_evt_unresolved_value_insert"></span>**ERRO \_ EVT de \_ inserção de \_ valor não resolvido \_**
</dt> <dd> <dl> <dt>

15029 (0x3AB5)
</dt> <dt>



Não foi possível encontrar a cadeia de caracteres de substituição para o índice de inserção (%1).


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_UNRESOLVED_PARAMETER_INSERT"></span><span id="error_evt_unresolved_parameter_insert"></span>**ERRO \_ EVT de \_ inserção de \_ parâmetro não resolvido \_**
</dt> <dd> <dl> <dt>

15030 (0x3AB6)
</dt> <dt>



Não foi possível encontrar a cadeia de caracteres de descrição para a referência de parâmetro (%1).


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_MAX_INSERTS_REACHED"></span><span id="error_evt_max_inserts_reached"></span>**ERRO \_ EVT \_ máximo de \_ inserções \_ atingido**
</dt> <dd> <dl> <dt>

15031 (0x3AB7)
</dt> <dt>



O número máximo de substituições foi atingido.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_EVENT_DEFINITION_NOT_FOUND"></span><span id="error_evt_event_definition_not_found"></span>**\_definição de evento EVT de erro \_ \_ \_ não \_ encontrada**
</dt> <dd> <dl> <dt>

15032 (0x3AB8)
</dt> <dt>



Não foi possível encontrar a definição de evento para a ID de evento (%1).


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_MESSAGE_LOCALE_NOT_FOUND"></span><span id="error_evt_message_locale_not_found"></span>**ERRO \_ EVT \_ localidade de mensagem \_ \_ não \_ encontrada**
</dt> <dd> <dl> <dt>

15033 (0x3AB9)
</dt> <dt>



O recurso específico da localidade para a mensagem desejada não está presente.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_VERSION_TOO_OLD"></span><span id="error_evt_version_too_old"></span>**versão de erro \_ EVT \_ \_ muito \_ antiga**
</dt> <dd> <dl> <dt>

15034 (0x3ABA)
</dt> <dt>



O recurso é muito antigo para ser compatível.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_VERSION_TOO_NEW"></span><span id="error_evt_version_too_new"></span>**versão de erro \_ EVT \_ \_ muito \_ nova**
</dt> <dd> <dl> <dt>

15035 (0x3ABB)
</dt> <dt>



O recurso é muito novo para ser compatível.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_CANNOT_OPEN_CHANNEL_OF_QUERY"></span><span id="error_evt_cannot_open_channel_of_query"></span>**o erro \_ EVT \_ não pode \_ abrir o \_ canal \_ de \_ consulta**
</dt> <dd> <dl> <dt>

15036 (0x3ABC)
</dt> <dt>



O canal no índice %1! d! Não é possível abrir a consulta.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_PUBLISHER_DISABLED"></span><span id="error_evt_publisher_disabled"></span>**ERRO \_ EVT \_ Editor \_ desabilitado**
</dt> <dd> <dl> <dt>

15037 (0x3ABD)
</dt> <dt>



O Publicador foi desabilitado e seu recurso não está disponível. Isso geralmente ocorre quando o Publicador está no processo de ser desinstalado ou atualizado.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_FILTER_OUT_OF_RANGE"></span><span id="error_evt_filter_out_of_range"></span>**\_ \_ filtro de erro EVT \_ fora \_ do \_ intervalo**
</dt> <dd> <dl> <dt>

15038 (0x3ABE)
</dt> <dt>



Tentativa de criar um tipo numérico que está fora de seu intervalo válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_EC_SUBSCRIPTION_CANNOT_ACTIVATE"></span><span id="error_ec_subscription_cannot_activate"></span>**ERRO \_ a \_ assinatura do EC \_ não pode \_ Ativar**
</dt> <dd> <dl> <dt>

15080 (0x3AE8)
</dt> <dt>



Falha na ativação da assinatura.


</dt> </dl> </dd> <dt>

<span id="ERROR_EC_LOG_DISABLED"></span><span id="error_ec_log_disabled"></span>**ERRO \_ de \_ log do EC \_ desabilitado**
</dt> <dd> <dl> <dt>

15081 (0x3AE9)
</dt> <dt>



O log da assinatura está em estado desabilitado e não pode ser usado para encaminhar eventos para o. O log deve ser habilitado primeiro para que a assinatura possa ser ativada.


</dt> </dl> </dd> <dt>

<span id="ERROR_EC_CIRCULAR_FORWARDING"></span><span id="error_ec_circular_forwarding"></span>**ERRO \_ de \_ encaminhamento circular do EC \_**
</dt> <dd> <dl> <dt>

15082 (0x3AEA)
</dt> <dt>



Ao encaminhar eventos do computador local para ele mesmo, a consulta da assinatura não pode conter o log de destino da assinatura.


</dt> </dl> </dd> <dt>

<span id="ERROR_EC_CREDSTORE_FULL"></span><span id="error_ec_credstore_full"></span>**ERRO \_ EC \_ CREDSTORE \_ completo**
</dt> <dd> <dl> <dt>

15083 (0x3AEB)
</dt> <dt>



O repositório de credenciais usado para salvar as credenciais está cheio.


</dt> </dl> </dd> <dt>

<span id="ERROR_EC_CRED_NOT_FOUND"></span><span id="error_ec_cred_not_found"></span>**ERRO \_ de \_ credenciais do EC \_ não \_ encontrado**
</dt> <dd> <dl> <dt>

15084 (0x3AEC)
</dt> <dt>



A credencial usada por essa assinatura não pode ser encontrada no repositório de credenciais.


</dt> </dl> </dd> <dt>

<span id="ERROR_EC_NO_ACTIVE_CHANNEL"></span><span id="error_ec_no_active_channel"></span>**ERRO \_ EC \_ nenhum \_ \_ canal ativo**
</dt> <dd> <dl> <dt>

15085 (0x3AED)
</dt> <dt>



Nenhum canal ativo foi encontrado para a consulta.


</dt> </dl> </dd> <dt>

<span id="ERROR_MUI_FILE_NOT_FOUND"></span><span id="error_mui_file_not_found"></span>**ERRO \_ de \_ arquivo MUI \_ não \_ encontrado**
</dt> <dd> <dl> <dt>

15100 (0x3AFC)
</dt> <dt>



Falha do carregador de recursos ao localizar o arquivo MUI.


</dt> </dl> </dd> <dt>

<span id="ERROR_MUI_INVALID_FILE"></span><span id="error_mui_invalid_file"></span>**ERRO \_ de \_ arquivo inválido MUI \_**
</dt> <dd> <dl> <dt>

15101 (0x3AFD)
</dt> <dt>



Falha do carregador de recursos ao carregar o arquivo MUI porque o arquivo não pôde passar na validação.


</dt> </dl> </dd> <dt>

<span id="ERROR_MUI_INVALID_RC_CONFIG"></span><span id="error_mui_invalid_rc_config"></span>**ERRO \_ de \_ \_ configuração RC inválida do MUI \_**
</dt> <dd> <dl> <dt>

15102 (0x3AFE)
</dt> <dt>



O manifesto RC está corrompido com dados de lixo ou de versão sem suporte ou com um item necessário ausente.


</dt> </dl> </dd> <dt>

<span id="ERROR_MUI_INVALID_LOCALE_NAME"></span><span id="error_mui_invalid_locale_name"></span>**ERRO \_ \_ nome de \_ localidade \_ inválido do MUI**
</dt> <dd> <dl> <dt>

15103 (0x3AFF)
</dt> <dt>



O manifesto RC tem um nome de cultura inválido.


</dt> </dl> </dd> <dt>

<span id="ERROR_MUI_INVALID_ULTIMATEFALLBACK_NAME"></span><span id="error_mui_invalid_ultimatefallback_name"></span>**ERRO \_ \_ nome de \_ ULTIMATEFALLBACK \_ inválido do MUI**
</dt> <dd> <dl> <dt>

15104 (0x3B00)
</dt> <dt>



O manifesto RC tem um nome de ultimatefallback inválido.


</dt> </dl> </dd> <dt>

<span id="ERROR_MUI_FILE_NOT_LOADED"></span><span id="error_mui_file_not_loaded"></span>**ERRO \_ \_ arquivo MUI \_ não \_ carregado**
</dt> <dd> <dl> <dt>

15105 (0x3B01)
</dt> <dt>



O cache do carregador de recursos não tem a entrada MUI carregada.


</dt> </dl> </dd> <dt>

<span id="ERROR_RESOURCE_ENUM_USER_STOP"></span><span id="error_resource_enum_user_stop"></span>**\_parada de \_ usuário de enumeração de recurso de erro \_ \_**
</dt> <dd> <dl> <dt>

15106 (0x3B02)
</dt> <dt>



Enumeração de recursos interrompida pelo usuário.


</dt> </dl> </dd> <dt>

<span id="ERROR_MUI_INTLSETTINGS_UILANG_NOT_INSTALLED"></span><span id="error_mui_intlsettings_uilang_not_installed"></span>**ERRO \_ MUI \_ INTLSETTINGS \_ UILANG \_ não \_ instalado**
</dt> <dd> <dl> <dt>

15107 (0x3B03)
</dt> <dt>



Falha na instalação do idioma da interface do usuário.


</dt> </dl> </dd> <dt>

<span id="ERROR_MUI_INTLSETTINGS_INVALID_LOCALE_NAME"></span><span id="error_mui_intlsettings_invalid_locale_name"></span>**ERRO \_ MUI \_ INTLSETTINGS \_ \_ nome de localidade inválido \_**
</dt> <dd> <dl> <dt>

15108 (0x3B04)
</dt> <dt>



Falha na instalação da localidade.


</dt> </dl> </dd> <dt>

<span id="ERROR_MRM_RUNTIME_NO_DEFAULT_OR_NEUTRAL_RESOURCE"></span><span id="error_mrm_runtime_no_default_or_neutral_resource"></span>**ERRO \_ MRM \_ tempo \_ de execução sem \_ \_ recurso padrão ou \_ neutro \_**
</dt> <dd> <dl> <dt>

15110 (0x3B06)
</dt> <dt>



Um recurso não tem valor padrão ou neutro.


</dt> </dl> </dd> <dt>

<span id="ERROR_MRM_INVALID_PRICONFIG"></span><span id="error_mrm_invalid_priconfig"></span>**ERRO \_ MRM \_ \_ PRICONFIG inválido**
</dt> <dd> <dl> <dt>

15111 (0x3B07)
</dt> <dt>



Arquivo de configuração PRI inválido.


</dt> </dl> </dd> <dt>

<span id="ERROR_MRM_INVALID_FILE_TYPE"></span><span id="error_mrm_invalid_file_type"></span>**ERRO \_ MRM \_ \_ tipo de arquivo inválido \_**
</dt> <dd> <dl> <dt>

15112 (0x3B08)
</dt> <dt>



Tipo de arquivo inválido.


</dt> </dl> </dd> <dt>

<span id="ERROR_MRM_UNKNOWN_QUALIFIER"></span><span id="error_mrm_unknown_qualifier"></span>**ERRO \_ MRM \_ \_ qualificador desconhecido**
</dt> <dd> <dl> <dt>

15113 (0x3B09)
</dt> <dt>



Qualificador desconhecido.


</dt> </dl> </dd> <dt>

<span id="ERROR_MRM_INVALID_QUALIFIER_VALUE"></span><span id="error_mrm_invalid_qualifier_value"></span>**ERRO \_ MRM \_ \_ valor de qualificador inválido \_**
</dt> <dd> <dl> <dt>

15114 (0x3B0A)
</dt> <dt>



Valor de qualificador inválido.


</dt> </dl> </dd> <dt>

<span id="ERROR_MRM_NO_CANDIDATE"></span><span id="error_mrm_no_candidate"></span>**ERRO \_ MRM \_ nenhum \_ candidato**
</dt> <dd> <dl> <dt>

15115 (0x3B0B)
</dt> <dt>



Nenhum candidato encontrado.


</dt> </dl> </dd> <dt>

<span id="ERROR_MRM_NO_MATCH_OR_DEFAULT_CANDIDATE"></span><span id="error_mrm_no_match_or_default_candidate"></span>**ERRO \_ MRM \_ sem \_ correspondência \_ ou \_ \_ candidato padrão**
</dt> <dd> <dl> <dt>

15116 (0x3B0C)
</dt> <dt>



ResourceMap ou NamedResource tem um item que não tem recurso padrão ou neutro..


</dt> </dl> </dd> <dt>

<span id="ERROR_MRM_RESOURCE_TYPE_MISMATCH"></span><span id="error_mrm_resource_type_mismatch"></span>**ERRO \_ de \_ \_ incompatibilidade de tipo de recurso MRM \_**
</dt> <dd> <dl> <dt>

15117 (0x3B0D)
</dt> <dt>



Tipo de ResourceCandidate inválido.


</dt> </dl> </dd> <dt>

<span id="ERROR_MRM_DUPLICATE_MAP_NAME"></span><span id="error_mrm_duplicate_map_name"></span>**ERRO \_ MRM \_ \_ nome do mapa duplicado \_**
</dt> <dd> <dl> <dt>

15118 (0x3B0E)
</dt> <dt>



Mapa de recursos duplicado.


</dt> </dl> </dd> <dt>

<span id="ERROR_MRM_DUPLICATE_ENTRY"></span><span id="error_mrm_duplicate_entry"></span>**ERRO \_ MRM \_ entrada duplicada \_**
</dt> <dd> <dl> <dt>

15119 (0x3B0F)
</dt> <dt>



Entrada duplicada.


</dt> </dl> </dd> <dt>

<span id="ERROR_MRM_INVALID_RESOURCE_IDENTIFIER"></span><span id="error_mrm_invalid_resource_identifier"></span>**ERRO \_ MRM \_ \_ identificador de recurso inválido \_**
</dt> <dd> <dl> <dt>

15120 (0x3B10)
</dt> <dt>



Identificador de recurso inválido.


</dt> </dl> </dd> <dt>

<span id="ERROR_MRM_FILEPATH_TOO_LONG"></span><span id="error_mrm_filepath_too_long"></span>**ERRO \_ MRM \_ FilePath \_ muito \_ longo**
</dt> <dd> <dl> <dt>

15121 (0x3B11)
</dt> <dt>



FilePath muito longo.


</dt> </dl> </dd> <dt>

<span id="ERROR_MRM_UNSUPPORTED_DIRECTORY_TYPE"></span><span id="error_mrm_unsupported_directory_type"></span>**ERRO \_ MRM \_ tipo de diretório sem suporte \_ \_**
</dt> <dd> <dl> <dt>

15122 (0x3B12)
</dt> <dt>



Tipo de diretório sem suporte.


</dt> </dl> </dd> <dt>

<span id="ERROR_MRM_INVALID_PRI_FILE"></span><span id="error_mrm_invalid_pri_file"></span>**ERRO \_ MRM \_ \_ arquivo pri \_ inválido**
</dt> <dd> <dl> <dt>

15126 (0x3B16)
</dt> <dt>



Arquivo PRI inválido.


</dt> </dl> </dd> <dt>

<span id="ERROR_MRM_NAMED_RESOURCE_NOT_FOUND"></span><span id="error_mrm_named_resource_not_found"></span>**ERRO \_ MRM com o \_ \_ recurso nomeado \_ não \_ encontrado**
</dt> <dd> <dl> <dt>

15127 (0x3B17)
</dt> <dt>



NamedResource não encontrado.


</dt> </dl> </dd> <dt>

<span id="ERROR_MRM_MAP_NOT_FOUND"></span><span id="error_mrm_map_not_found"></span>**mapa de MRM de erro \_ \_ \_ não \_ encontrado**
</dt> <dd> <dl> <dt>

15135 (0x3B1F)
</dt> <dt>



ResourceMap não encontrado.


</dt> </dl> </dd> <dt>

<span id="ERROR_MRM_UNSUPPORTED_PROFILE_TYPE"></span><span id="error_mrm_unsupported_profile_type"></span>**ERRO \_ MRM \_ tipo de perfil sem suporte \_ \_**
</dt> <dd> <dl> <dt>

15136 (0x3B20)
</dt> <dt>



Tipo de perfil MRT sem suporte.


</dt> </dl> </dd> <dt>

<span id="ERROR_MRM_INVALID_QUALIFIER_OPERATOR"></span><span id="error_mrm_invalid_qualifier_operator"></span>**ERRO \_ MRM \_ \_ operador qualificador inválido \_**
</dt> <dd> <dl> <dt>

15137 (0x3B21)
</dt> <dt>



Operador qualificador inválido.


</dt> </dl> </dd> <dt>

<span id="ERROR_MRM_INDETERMINATE_QUALIFIER_VALUE"></span><span id="error_mrm_indeterminate_qualifier_value"></span>**ERRO \_ MRM \_ \_ valor de qualificador indeterminado \_**
</dt> <dd> <dl> <dt>

15138 (0x3B22)
</dt> <dt>



Não é possível determinar se o valor do qualificador ou o valor do qualificador não foi definido.


</dt> </dl> </dd> <dt>

<span id="ERROR_MRM_AUTOMERGE_ENABLED"></span><span id="error_mrm_automerge_enabled"></span>**ERRO \_ MRM \_ mesclagem automática \_ habilitada**
</dt> <dd> <dl> <dt>

15139 (0x3B23)
</dt> <dt>



A mesclagem automática está habilitada no arquivo PRI.


</dt> </dl> </dd> <dt>

<span id="ERROR_MRM_TOO_MANY_RESOURCES"></span><span id="error_mrm_too_many_resources"></span>**ERRO \_ MRM \_ \_ muitos \_ recursos**
</dt> <dd> <dl> <dt>

15140 (0x3B24)
</dt> <dt>



Muitos recursos definidos para o pacote.


</dt> </dl> </dd> <dt>

<span id="ERROR_MCA_INVALID_CAPABILITIES_STRING"></span><span id="error_mca_invalid_capabilities_string"></span>**ERRO \_ de \_ cadeia de \_ caracteres de funcionalidades inválidas MCA \_**
</dt> <dd> <dl> <dt>

15200 (0x3B60)
</dt> <dt>



O monitor retornou uma cadeia de recursos DDC/CI que não estava em conformidade com a especificação ACCESS. Bus 3,0, DDC/CI 1,1 ou MCCS 2 revisão 1.


</dt> </dl> </dd> <dt>

<span id="ERROR_MCA_INVALID_VCP_VERSION"></span><span id="error_mca_invalid_vcp_version"></span>**ERRO \_ MCA \_ \_ versão de VCP inválida \_**
</dt> <dd> <dl> <dt>

15201 (0x3B61)
</dt> <dt>



O código VCP da versão VCP do monitor (0xDF) retornou um valor de versão inválido.


</dt> </dl> </dd> <dt>

<span id="ERROR_MCA_MONITOR_VIOLATES_MCCS_SPECIFICATION"></span><span id="error_mca_monitor_violates_mccs_specification"></span>**ERRO \_ o \_ Monitor MCA \_ viola \_ a \_ especificação MCCS**
</dt> <dd> <dl> <dt>

15202 (0x3B62)
</dt> <dt>



O monitor não está em conformidade com a especificação MCCS para a qual ele alega dar suporte.


</dt> </dl> </dd> <dt>

<span id="ERROR_MCA_MCCS_VERSION_MISMATCH"></span><span id="error_mca_mccs_version_mismatch"></span>**ERRO \_ de \_ \_ incompatibilidade de versão MCA MCCs \_**
</dt> <dd> <dl> <dt>

15203 (0x3B63)
</dt> <dt>



A versão MCCS no recurso MCCs ver de um monitor \_ não corresponde à versão MCCS que o monitor relata quando o código VCP de versão VCP (0xDF) é usado.


</dt> </dl> </dd> <dt>

<span id="ERROR_MCA_UNSUPPORTED_MCCS_VERSION"></span><span id="error_mca_unsupported_mccs_version"></span>**ERRO \_ de \_ versão do MCCs sem suporte para MCA \_ \_**
</dt> <dd> <dl> <dt>

15204 (0x3B64)
</dt> <dt>



A API de configuração do monitor só funciona com monitores que dão suporte à especificação MCCS 1,0, MCCS 2,0 ou a especificação MCCS 2,0 revisão 1.


</dt> </dl> </dd> <dt>

<span id="ERROR_MCA_INTERNAL_ERROR"></span><span id="error_mca_internal_error"></span>**erro \_ interno de MCA \_ \_**
</dt> <dd> <dl> <dt>

15205 (0x3B65)
</dt> <dt>



Ocorreu um erro interno de API de configuração de monitor.


</dt> </dl> </dd> <dt>

<span id="ERROR_MCA_INVALID_TECHNOLOGY_TYPE_RETURNED"></span><span id="error_mca_invalid_technology_type_returned"></span>**ERRO \_ \_ tipo de \_ tecnologia inválido MCA \_ \_ retornado**
</dt> <dd> <dl> <dt>

15206 (0x3B66)
</dt> <dt>



O monitor retornou um tipo de tecnologia de monitor inválido. CRT, plasma e LCD (TFT) são exemplos de tipos de tecnologia de monitor. Esse erro indica que o monitor violou a especificação MCCS 2,0 ou MCCS 2,0 revisão 1.


</dt> </dl> </dd> <dt>

<span id="ERROR_MCA_UNSUPPORTED_COLOR_TEMPERATURE"></span><span id="error_mca_unsupported_color_temperature"></span>**ERRO \_ de \_ temperatura de cor sem suporte para MCA \_ \_**
</dt> <dd> <dl> <dt>

15207 (0x3B67)
</dt> <dt>



O chamador de [**SetMonitorColorTemperature**](/windows/win32/api/highlevelmonitorconfigurationapi/nf-highlevelmonitorconfigurationapi-setmonitorcolortemperature) especificou uma temperatura de cor para a qual o monitor atual não tinha suporte. Esse erro indica que o monitor violou a especificação MCCS 2,0 ou MCCS 2,0 revisão 1.


</dt> </dl> </dd> <dt>

<span id="ERROR_AMBIGUOUS_SYSTEM_DEVICE"></span><span id="error_ambiguous_system_device"></span>**ERRO \_ de \_ dispositivo de sistema ambíguo \_**
</dt> <dd> <dl> <dt>

15250 (0x3B92)
</dt> <dt>



O dispositivo de sistema solicitado não pode ser identificado porque vários dispositivos indistinguíveis potencialmente correspondem aos critérios de identificação.


</dt> </dl> </dd> <dt>

<span id="ERROR_SYSTEM_DEVICE_NOT_FOUND"></span><span id="error_system_device_not_found"></span>**dispositivo de sistema de erro \_ \_ \_ não \_ encontrado**
</dt> <dd> <dl> <dt>

15299 (0x3BC3)
</dt> <dt>



Não é possível encontrar o dispositivo de sistema solicitado.


</dt> </dl> </dd> <dt>

<span id="ERROR_HASH_NOT_SUPPORTED"></span><span id="error_hash_not_supported"></span>**HASH de erro \_ \_ sem \_ suporte**
</dt> <dd> <dl> <dt>

15300 (0x3BC4)
</dt> <dt>



A geração de hash para a versão de hash especificada e o tipo de hash não está habilitada no servidor.


</dt> </dl> </dd> <dt>

<span id="ERROR_HASH_NOT_PRESENT"></span><span id="error_hash_not_present"></span>**o \_ hash de erro \_ não \_ está presente**
</dt> <dd> <dl> <dt>

15301 (0x3BC5)
</dt> <dt>



O hash solicitado do servidor não está disponível ou não é mais válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_SECONDARY_IC_PROVIDER_NOT_REGISTERED"></span><span id="error_secondary_ic_provider_not_registered"></span>**ERRO \_ de \_ provedor IC secundário \_ \_ não \_ registrado**
</dt> <dd> <dl> <dt>

15321 (0x3BD9)
</dt> <dt>



A instância do controlador de interrupção secundário que gerencia a interrupção especificada não está registrada.


</dt> </dl> </dd> <dt>

<span id="ERROR_GPIO_CLIENT_INFORMATION_INVALID"></span><span id="error_gpio_client_information_invalid"></span>**ERRO \_ de \_ informações do cliente GPIO \_ \_ inválido**
</dt> <dd> <dl> <dt>

15322 (0x3BDA)
</dt> <dt>



As informações fornecidas pelo driver do cliente GPIO são inválidas.


</dt> </dl> </dd> <dt>

<span id="ERROR_GPIO_VERSION_NOT_SUPPORTED"></span><span id="error_gpio_version_not_supported"></span>**versão do GPIO de erro \_ \_ \_ sem \_ suporte**
</dt> <dd> <dl> <dt>

15323 (0x3BDB)
</dt> <dt>



Não há suporte para a versão especificada pelo driver do cliente GPIO.


</dt> </dl> </dd> <dt>

<span id="ERROR_GPIO_INVALID_REGISTRATION_PACKET"></span><span id="error_gpio_invalid_registration_packet"></span>**ERRO \_ GPIO \_ \_ pacote de registro inválido \_**
</dt> <dd> <dl> <dt>

15324 (0x3BDC)
</dt> <dt>



O pacote de registro fornecido pelo driver do cliente GPIO não é válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_GPIO_OPERATION_DENIED"></span><span id="error_gpio_operation_denied"></span>**operação de GPIO de erro \_ \_ \_ negada**
</dt> <dd> <dl> <dt>

15325 (0x3BDD)
</dt> <dt>



A operação solicitada não tem suporte para o identificador especificado.


</dt> </dl> </dd> <dt>

<span id="ERROR_GPIO_INCOMPATIBLE_CONNECT_MODE"></span><span id="error_gpio_incompatible_connect_mode"></span>**ERRO \_ GPIO \_ modo de \_ conexão incompatível \_**
</dt> <dd> <dl> <dt>

15326 (0x3BDE)
</dt> <dt>



O modo de conexão solicitado está em conflito com um modo existente em um ou mais dos Pins especificados.


</dt> </dl> </dd> <dt>

<span id="ERROR_GPIO_INTERRUPT_ALREADY_UNMASKED"></span><span id="error_gpio_interrupt_already_unmasked"></span>**ERRO \_ de \_ interrupção de GPIO já não \_ \_ mascarado**
</dt> <dd> <dl> <dt>

15327 (0x3BDF)
</dt> <dt>



A interrupção solicitada para não mascarada não é mascarada.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANNOT_SWITCH_RUNLEVEL"></span><span id="error_cannot_switch_runlevel"></span>**ERRO \_ não é possível \_ alternar \_ runlevel**
</dt> <dd> <dl> <dt>

15400 (0x3C28)
</dt> <dt>



A opção de nível de execução solicitada não pode ser concluída com êxito.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_RUNLEVEL_SETTING"></span><span id="error_invalid_runlevel_setting"></span>**ERRO \_ de \_ configuração de runlevel inválida \_**
</dt> <dd> <dl> <dt>

15401 (0x3C29)
</dt> <dt>



O serviço tem uma configuração de nível de execução inválida. O nível de execução para um serviço não deve ser maior que o nível de execução de seus serviços dependentes.


</dt> </dl> </dd> <dt>

<span id="ERROR_RUNLEVEL_SWITCH_TIMEOUT"></span><span id="error_runlevel_switch_timeout"></span>**ERRO \_ runlevel \_ alternar \_ tempo limite**
</dt> <dd> <dl> <dt>

15402 (0x3C2A)
</dt> <dt>



A opção de nível de execução solicitada não pode ser concluída com êxito, pois um ou mais serviços não serão interrompidos ou reiniciados dentro do tempo limite especificado.


</dt> </dl> </dd> <dt>

<span id="ERROR_RUNLEVEL_SWITCH_AGENT_TIMEOUT"></span><span id="error_runlevel_switch_agent_timeout"></span>**ERRO \_ runlevel \_ \_ tempo limite do agente de comutador \_**
</dt> <dd> <dl> <dt>

15403 (0x3C2B)
</dt> <dt>



Um agente de opção de nível de execução não respondeu dentro do tempo limite especificado.


</dt> </dl> </dd> <dt>

<span id="ERROR_RUNLEVEL_SWITCH_IN_PROGRESS"></span><span id="error_runlevel_switch_in_progress"></span>**ERRO \_ runlevel \_ opção \_ em \_ andamento**
</dt> <dd> <dl> <dt>

15404 (0x3C2C)
</dt> <dt>



Uma opção de nível de execução está em andamento no momento.


</dt> </dl> </dd> <dt>

<span id="ERROR_SERVICES_FAILED_AUTOSTART"></span><span id="error_services_failed_autostart"></span>**\_ \_ falha na \_ inicialização automática dos serviços de erro**
</dt> <dd> <dl> <dt>

15405 (0x3C2D)
</dt> <dt>



Um ou mais serviços não foram iniciados durante a fase de inicialização do serviço de uma opção de nível de execução.


</dt> </dl> </dd> <dt>

<span id="ERROR_COM_TASK_STOP_PENDING"></span><span id="error_com_task_stop_pending"></span>**ERRO \_ de \_ parada de tarefa com \_ \_ pendente**
</dt> <dd> <dl> <dt>

15501 (0x3C8D)
</dt> <dt>



A solicitação de parada de tarefa não pode ser concluída imediatamente, pois a tarefa precisa de mais tempo para ser desligada.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_OPEN_PACKAGE_FAILED"></span><span id="error_install_open_package_failed"></span>**ERRO \_ \_ ao instalar \_ pacote aberto \_ com falha**
</dt> <dd> <dl> <dt>

15600 (0x3CF0)
</dt> <dt>



Não foi possível abrir o pacote.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_PACKAGE_NOT_FOUND"></span><span id="error_install_package_not_found"></span>**ERRO ao \_ instalar o \_ pacote \_ não \_ encontrado**
</dt> <dd> <dl> <dt>

15601 (0x3CF1)
</dt> <dt>



O pacote não foi encontrado.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_INVALID_PACKAGE"></span><span id="error_install_invalid_package"></span>**ERRO \_ ao \_ instalar \_ pacote inválido**
</dt> <dd> <dl> <dt>

15602 (0x3CF2)
</dt> <dt>



Os dados do pacote são inválidos.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_RESOLVE_DEPENDENCY_FAILED"></span><span id="error_install_resolve_dependency_failed"></span>**ERRO \_ ao instalar a \_ dependência de resolução \_ \_**
</dt> <dd> <dl> <dt>

15603 (0x3CF3)
</dt> <dt>



Atualizações com falha de pacote, dependência ou validação de conflito.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_OUT_OF_DISK_SPACE"></span><span id="error_install_out_of_disk_space"></span>**ERRO \_ \_ de instalação \_ sem \_ \_ espaço em disco**
</dt> <dd> <dl> <dt>

15604 (0x3CF4)
</dt> <dt>



Não há espaço em disco suficiente no computador. Libere espaço e tente novamente.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_NETWORK_FAILURE"></span><span id="error_install_network_failure"></span>**ERRO \_ ao \_ instalar \_ falha de rede**
</dt> <dd> <dl> <dt>

15605 (0x3CF5)
</dt> <dt>



Houve um problema ao baixar seu produto.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_REGISTRATION_FAILURE"></span><span id="error_install_registration_failure"></span>**ERRO \_ ao \_ instalar \_ falha de registro**
</dt> <dd> <dl> <dt>

15606 (0x3CF6)
</dt> <dt>



Não foi possível registrar o pacote.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_DEREGISTRATION_FAILURE"></span><span id="error_install_deregistration_failure"></span>**ERRO ao \_ instalar falha de \_ cancelamento de registro \_**
</dt> <dd> <dl> <dt>

15607 (0x3CF7)
</dt> <dt>



Não foi possível cancelar o registro do pacote.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_CANCEL"></span><span id="error_install_cancel"></span>**ERRO ao \_ instalar \_ cancelar**
</dt> <dd> <dl> <dt>

15608 (0x3CF8)
</dt> <dt>



O usuário cancelou a solicitação de instalação.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_FAILED"></span><span id="error_install_failed"></span>**\_falha na instalação do erro \_**
</dt> <dd> <dl> <dt>

15609 (0x3CF9)
</dt> <dt>



Falha na instalação. Entre em contato com seu fornecedor de software.


</dt> </dl> </dd> <dt>

<span id="ERROR_REMOVE_FAILED"></span><span id="error_remove_failed"></span>**\_ \_ falha ao remover erro**
</dt> <dd> <dl> <dt>

15610 (0x3CFA)
</dt> <dt>



Falha na remoção. Entre em contato com seu fornecedor de software.


</dt> </dl> </dd> <dt>

<span id="ERROR_PACKAGE_ALREADY_EXISTS"></span><span id="error_package_already_exists"></span>**o \_ pacote de erros \_ já \_ existe**
</dt> <dd> <dl> <dt>

15611 (0x3CFB)
</dt> <dt>



O pacote fornecido já está instalado e a reinstalação do pacote foi bloqueada. Verifique o log de eventos AppXDeployment-Server para obter detalhes.


</dt> </dl> </dd> <dt>

<span id="ERROR_NEEDS_REMEDIATION"></span><span id="error_needs_remediation"></span>**ERRO \_ precisa de \_ correção**
</dt> <dd> <dl> <dt>

15612 (0x3CFC)
</dt> <dt>



O aplicativo não pode ser iniciado. Tente reinstalar o aplicativo para corrigir o problema.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_PREREQUISITE_FAILED"></span><span id="error_install_prerequisite_failed"></span>**ERRO \_ ao instalar o \_ pré-requisito \_**
</dt> <dd> <dl> <dt>

15613 (0x3CFD)
</dt> <dt>



Um pré-requisito para uma instalação não pôde ser atendido.


</dt> </dl> </dd> <dt>

<span id="ERROR_PACKAGE_REPOSITORY_CORRUPTED"></span><span id="error_package_repository_corrupted"></span>**repositório de pacotes de erros \_ \_ \_ corrompido**
</dt> <dd> <dl> <dt>

15614 (0x3CFE)
</dt> <dt>



O repositório do pacote está corrompido.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_POLICY_FAILURE"></span><span id="error_install_policy_failure"></span>**ERRO \_ de \_ falha na política de instalação \_**
</dt> <dd> <dl> <dt>

15615 (0x3CFF)
</dt> <dt>



Para instalar este aplicativo, você precisa de uma licença de desenvolvedor do Windows ou de um sistema habilitado para Sideload.


</dt> </dl> </dd> <dt>

<span id="ERROR_PACKAGE_UPDATING"></span><span id="error_package_updating"></span>**\_atualização do pacote de erros \_**
</dt> <dd> <dl> <dt>

15616 (0x3D00)
</dt> <dt>



O aplicativo não pode ser iniciado porque está sendo atualizado no momento.


</dt> </dl> </dd> <dt>

<span id="ERROR_DEPLOYMENT_BLOCKED_BY_POLICY"></span><span id="error_deployment_blocked_by_policy"></span>**\_implantação \_ de erro bloqueada \_ pela \_ política**
</dt> <dd> <dl> <dt>

15617 (0x3D01)
</dt> <dt>



A operação de implantação de pacote está bloqueada pela política. Entre em contato com o administrador do sistema.


</dt> </dl> </dd> <dt>

<span id="ERROR_PACKAGES_IN_USE"></span><span id="error_packages_in_use"></span>**\_pacotes \_ de erro em \_ uso**
</dt> <dd> <dl> <dt>

15618 (0x3D02)
</dt> <dt>



O pacote não pôde ser instalado porque os recursos que ele modifica estão em uso no momento.


</dt> </dl> </dd> <dt>

<span id="ERROR_RECOVERY_FILE_CORRUPT"></span><span id="error_recovery_file_corrupt"></span>**ERRO \_ de \_ arquivo de recuperação \_ corrompido**
</dt> <dd> <dl> <dt>

15619 (0x3D03)
</dt> <dt>



O pacote não pôde ser recuperado porque os dados necessários para recuperação foram corrompidos.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_STAGED_SIGNATURE"></span><span id="error_invalid_staged_signature"></span>**ERRO \_ de \_ assinatura preparada inválida \_**
</dt> <dd> <dl> <dt>

15620 (0x3D04)
</dt> <dt>



A assinatura é inválida. Para se registrar no modo de desenvolvedor, AppxSignature. P7X e AppxBlockMap.xml devem ser válidos ou não devem estar presentes.


</dt> </dl> </dd> <dt>

<span id="ERROR_DELETING_EXISTING_APPLICATIONDATA_STORE_FAILED"></span><span id="error_deleting_existing_applicationdata_store_failed"></span>**ERRO ao \_ excluir o \_ \_ repositório de APPLICATIONDATA existente \_ \_**
</dt> <dd> <dl> <dt>

15621 (0x3D05)
</dt> <dt>



Ocorreu um erro ao excluir os dados de aplicativo anteriormente existentes do pacote.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_PACKAGE_DOWNGRADE"></span><span id="error_install_package_downgrade"></span>**ERRO ao \_ instalar o \_ downgrade do pacote \_**
</dt> <dd> <dl> <dt>

15622 (0x3D06)
</dt> <dt>



Não foi possível instalar o pacote porque uma versão mais recente deste pacote já está instalada.


</dt> </dl> </dd> <dt>

<span id="ERROR_SYSTEM_NEEDS_REMEDIATION"></span><span id="error_system_needs_remediation"></span>**o \_ sistema de erros \_ precisa de \_ correção**
</dt> <dd> <dl> <dt>

15623 (0x3D07)
</dt> <dt>



Foi detectado um erro em um binário do sistema. Tente atualizar o PC para corrigir o problema.


</dt> </dl> </dd> <dt>

<span id="ERROR_APPX_INTEGRITY_FAILURE_CLR_NGEN"></span><span id="error_appx_integrity_failure_clr_ngen"></span>**ERRO \_ de \_ integridade Appx \_ falha no \_ CLR \_ NGen**
</dt> <dd> <dl> <dt>

15624 (0x3D08)
</dt> <dt>



Foi detectado um binário do CLR NGEN corrompido no sistema.


</dt> </dl> </dd> <dt>

<span id="ERROR_RESILIENCY_FILE_CORRUPT"></span><span id="error_resiliency_file_corrupt"></span>**arquivo de resiliência de erro \_ \_ \_ corrompido**
</dt> <dd> <dl> <dt>

15625 (0x3D09)
</dt> <dt>



A operação não pôde ser retomada porque os dados necessários para recuperação foram corrompidos.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_FIREWALL_SERVICE_NOT_RUNNING"></span><span id="error_install_firewall_service_not_running"></span>**ERRO ao \_ instalar o \_ serviço de firewall \_ \_ não \_ está em execução**
</dt> <dd> <dl> <dt>

15626 (0x3D0A)
</dt> <dt>



Não foi possível instalar o pacote porque o serviço de firewall do Windows não está em execução. Habilite o serviço de firewall do Windows e tente novamente.


</dt> </dl> </dd> <dt>

<span id="APPMODEL_ERROR_NO_PACKAGE"></span><span id="appmodel_error_no_package"></span>**erro de APPMODEL \_ \_ sem \_ pacote**
</dt> <dd> <dl> <dt>

15700 (0x3D54)
</dt> <dt>



O processo não tem nenhuma identidade de pacote.


</dt> </dl> </dd> <dt>

<span id="APPMODEL_ERROR_PACKAGE_RUNTIME_CORRUPT"></span><span id="appmodel_error_package_runtime_corrupt"></span>**tempo de execução do pacote de erros do APPMODEL \_ \_ \_ \_ corrompido**
</dt> <dd> <dl> <dt>

15701 (0x3D55)
</dt> <dt>



As informações de tempo de execução do pacote estão corrompidas.


</dt> </dl> </dd> <dt>

<span id="APPMODEL_ERROR_PACKAGE_IDENTITY_CORRUPT"></span><span id="appmodel_error_package_identity_corrupt"></span>**\_ \_ \_ identidade \_ corrompida do pacote de erros do APPMODEL**
</dt> <dd> <dl> <dt>

15702 (0x3D56)
</dt> <dt>



A identidade do pacote está corrompida.


</dt> </dl> </dd> <dt>

<span id="APPMODEL_ERROR_NO_APPLICATION"></span><span id="appmodel_error_no_application"></span>**erro de APPMODEL \_ \_ sem \_ aplicativo**
</dt> <dd> <dl> <dt>

15703 (0x3D57)
</dt> <dt>



O processo não tem nenhuma identidade de aplicativo.


</dt> </dl> </dd> <dt>

<span id="ERROR_STATE_LOAD_STORE_FAILED"></span><span id="error_state_load_store_failed"></span>**\_ \_ \_ falha no repositório de carregamento do estado de erro \_**
</dt> <dd> <dl> <dt>

15800 (0x3DB8)
</dt> <dt>



Falha ao carregar o armazenamento de estado.


</dt> </dl> </dd> <dt>

<span id="ERROR_STATE_GET_VERSION_FAILED"></span><span id="error_state_get_version_failed"></span>**\_ \_ \_ falha ao obter versão do estado \_ de erro**
</dt> <dd> <dl> <dt>

15801 (0x3DB9)
</dt> <dt>



Falha ao recuperar a versão de estado do aplicativo.


</dt> </dl> </dd> <dt>

<span id="ERROR_STATE_SET_VERSION_FAILED"></span><span id="error_state_set_version_failed"></span>**\_ \_ \_ falha na versão do conjunto de estado de erro \_**
</dt> <dd> <dl> <dt>

15802 (0x3DBA)
</dt> <dt>



Falha ao definir a versão de estado para o aplicativo.


</dt> </dl> </dd> <dt>

<span id="ERROR_STATE_STRUCTURED_RESET_FAILED"></span><span id="error_state_structured_reset_failed"></span>**\_ \_ \_ falha na redefinição estruturada do estado de erro \_**
</dt> <dd> <dl> <dt>

15803 (0x3DBB)
</dt> <dt>



Falha na redefinição do estado estruturado do aplicativo.


</dt> </dl> </dd> <dt>

<span id="ERROR_STATE_OPEN_CONTAINER_FAILED"></span><span id="error_state_open_container_failed"></span>**\_falha no estado do erro \_ abrir \_ contêiner \_**
</dt> <dd> <dl> <dt>

15804 (0x3DBC)
</dt> <dt>



Falha do Gerenciador de estado ao abrir o contêiner.


</dt> </dl> </dd> <dt>

<span id="ERROR_STATE_CREATE_CONTAINER_FAILED"></span><span id="error_state_create_container_failed"></span>**\_ \_ \_ falha ao criar contêiner de estado \_ de erro**
</dt> <dd> <dl> <dt>

15805 (0x3DBD)
</dt> <dt>



Falha do Gerenciador de estado ao criar o contêiner.


</dt> </dl> </dd> <dt>

<span id="ERROR_STATE_DELETE_CONTAINER_FAILED"></span><span id="error_state_delete_container_failed"></span>**\_ \_ \_ falha ao excluir contêiner de estado \_**
</dt> <dd> <dl> <dt>

15806 (0x3DBE)
</dt> <dt>



Falha do Gerenciador de estado ao excluir o contêiner.


</dt> </dl> </dd> <dt>

<span id="ERROR_STATE_READ_SETTING_FAILED"></span><span id="error_state_read_setting_failed"></span>**\_ \_ \_ falha na configuração de leitura do estado de erro \_**
</dt> <dd> <dl> <dt>

15807 (0x3DBF)
</dt> <dt>



Falha do Gerenciador de estado ao ler a configuração.


</dt> </dl> </dd> <dt>

<span id="ERROR_STATE_WRITE_SETTING_FAILED"></span><span id="error_state_write_setting_failed"></span>**\_ \_ \_ falha na configuração de gravação do estado do erro \_**
</dt> <dd> <dl> <dt>

15808 (0x3DC0)
</dt> <dt>



Falha do Gerenciador de estado ao gravar a configuração.


</dt> </dl> </dd> <dt>

<span id="ERROR_STATE_DELETE_SETTING_FAILED"></span><span id="error_state_delete_setting_failed"></span>**\_ \_ \_ falha na configuração de exclusão do estado do erro \_**
</dt> <dd> <dl> <dt>

15809 (0x3DC1)
</dt> <dt>



Falha do Gerenciador de estado ao excluir a configuração.


</dt> </dl> </dd> <dt>

<span id="ERROR_STATE_QUERY_SETTING_FAILED"></span><span id="error_state_query_setting_failed"></span>**\_ \_ \_ falha na configuração de consulta de estado de erro \_**
</dt> <dd> <dl> <dt>

15810 (0x3DC2)
</dt> <dt>



Falha do Gerenciador de estado ao consultar a configuração.


</dt> </dl> </dd> <dt>

<span id="ERROR_STATE_READ_COMPOSITE_SETTING_FAILED"></span><span id="error_state_read_composite_setting_failed"></span>**\_ \_ \_ \_ falha na configuração de composição de leitura de estado \_ de erro**
</dt> <dd> <dl> <dt>

15811 (0x3DC3)
</dt> <dt>



Falha do Gerenciador de estado ao ler a configuração composta.


</dt> </dl> </dd> <dt>

<span id="ERROR_STATE_WRITE_COMPOSITE_SETTING_FAILED"></span><span id="error_state_write_composite_setting_failed"></span>**\_ \_ \_ \_ falha na configuração de composição de gravação de estado \_ de erro**
</dt> <dd> <dl> <dt>

15812 (0x3DC4)
</dt> <dt>



Falha do Gerenciador de estado ao gravar a configuração composta.


</dt> </dl> </dd> <dt>

<span id="ERROR_STATE_ENUMERATE_CONTAINER_FAILED"></span><span id="error_state_enumerate_container_failed"></span>**\_ \_ \_ falha no contêiner enumerar o estado do erro \_**
</dt> <dd> <dl> <dt>

15813 (0x3DC5)
</dt> <dt>



Falha do Gerenciador de estado ao enumerar os contêineres.


</dt> </dl> </dd> <dt>

<span id="ERROR_STATE_ENUMERATE_SETTINGS_FAILED"></span><span id="error_state_enumerate_settings_failed"></span>**\_ \_ \_ falha nas configurações de enumeração de estado de erro \_**
</dt> <dd> <dl> <dt>

15814 (0x3DC6)
</dt> <dt>



Falha do Gerenciador de estado ao enumerar as configurações.


</dt> </dl> </dd> <dt>

<span id="ERROR_STATE_COMPOSITE_SETTING_VALUE_SIZE_LIMIT_EXCEEDED"></span><span id="error_state_composite_setting_value_size_limit_exceeded"></span>**Estado de erro \_ \_ \_ configuração composta limite de tamanho de \_ valor \_ \_ \_ excedido**
</dt> <dd> <dl> <dt>

15815 (0x3DC7)
</dt> <dt>



O tamanho do valor da configuração composta do Gerenciador de estado excedeu o limite.


</dt> </dl> </dd> <dt>

<span id="ERROR_STATE_SETTING_VALUE_SIZE_LIMIT_EXCEEDED"></span><span id="error_state_setting_value_size_limit_exceeded"></span>**limite de tamanho de valor de configuração de estado de erro \_ \_ \_ \_ \_ \_ excedido**
</dt> <dd> <dl> <dt>

15816 (0x3DC8)
</dt> <dt>



O tamanho do valor da configuração do Gerenciador de estado excedeu o limite.


</dt> </dl> </dd> <dt>

<span id="ERROR_STATE_SETTING_NAME_SIZE_LIMIT_EXCEEDED"></span><span id="error_state_setting_name_size_limit_exceeded"></span>**limite de tamanho de nome de configuração de estado de erro \_ \_ \_ \_ \_ \_ excedido**
</dt> <dd> <dl> <dt>

15817 (0x3DC9)
</dt> <dt>



O comprimento do nome da configuração do Gerenciador de estado excedeu o limite.


</dt> </dl> </dd> <dt>

<span id="ERROR_STATE_CONTAINER_NAME_SIZE_LIMIT_EXCEEDED"></span><span id="error_state_container_name_size_limit_exceeded"></span>**limite de tamanho do nome do contêiner de estado de erro \_ \_ \_ \_ \_ \_ excedido**
</dt> <dd> <dl> <dt>

15818 (0x3DCA)
</dt> <dt>



O comprimento do nome do contêiner do Gerenciador de estado excedeu o limite.


</dt> </dl> </dd> <dt>

<span id="ERROR_API_UNAVAILABLE"></span><span id="error_api_unavailable"></span>**API de erro \_ \_ indisponível**
</dt> <dd> <dl> <dt>

15841 (0x3DE1)
</dt> <dt>



Essa API não pode ser usada no contexto do tipo de aplicativo do chamador.


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

 

 
