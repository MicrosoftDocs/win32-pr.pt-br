---
description: Recupera o status de validade da cadeia ou um certificado específico na cadeia.
title: 'Propriedade IChain2:: status'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IChain2.Status
- IChain.Status
- Chain.Status
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 23673289e2ff39d4180a4be8dc0be61f4a5cffc4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105758165"
---
# <a name="ichain2status-property"></a>Propriedade IChain2:: status

\[O CAPICOM é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista e Windows XP. Em vez disso, use a [**classe X509Chain**](/dotnet/api/system.security.cryptography.x509certificates.x509chain?view=netcore-3.1) no namespace [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

A propriedade **status** recupera o status de validade da cadeia ou um certificado específico na cadeia.

## <a name="syntax"></a>Syntax


```VB
Chain.Status( _
  ByVal Index _
) As Long
```



## <a name="property-value"></a>Valor da propriedade

Um valor **longo** que representa o indicador de status de validade da cadeia ou o certificado especificado. A tabela a seguir mostra os valores possíveis. Essa propriedade conterá zero se a cadeia ou o certificado especificado for válido. Caso contrário, essa propriedade conterá uma combinação de um ou mais dos valores a seguir.

<dt>

<span id="CAPICOM_TRUST_IS_NOT_TIME_VALID"></span><span id="capicom_trust_is_not_time_valid"></span>

<span id="CAPICOM_TRUST_IS_NOT_TIME_VALID"></span><span id="capicom_trust_is_not_time_valid"></span>**CAPICOM \_ A relação de confiança \_ não é um \_ \_ tempo \_ válido** (&H00000001)


</dt> <dd>

Este certificado ou um dos certificados na cadeia de certificados não é válido.

</dd> <dt>

<span id="CAPICOM_TRUST_IS_NOT_TIME_NESTED"></span><span id="capicom_trust_is_not_time_nested"></span>

<span id="CAPICOM_TRUST_IS_NOT_TIME_NESTED"></span><span id="capicom_trust_is_not_time_nested"></span>**CAPICOM \_ A relação de confiança \_ não é um \_ \_ tempo \_ aninhado** (&H00000002)


</dt> <dd>

Os certificados na cadeia não têm o tempo corretamente aninhado.

</dd> <dt>

<span id="CAPICOM_TRUST_IS_REVOKED"></span><span id="capicom_trust_is_revoked"></span>

<span id="CAPICOM_TRUST_IS_REVOKED"></span><span id="capicom_trust_is_revoked"></span>**CAPICOM \_ A confiança \_ é \_ revogada** (&H00000004)


</dt> <dd>

A confiança para este certificado ou um dos certificados na cadeia de certificados foi revogada.

</dd> <dt>

<span id="CAPICOM_TRUST_IS_NOT_SIGNATURE_VALID"></span><span id="capicom_trust_is_not_signature_valid"></span>

<span id="CAPICOM_TRUST_IS_NOT_SIGNATURE_VALID"></span><span id="capicom_trust_is_not_signature_valid"></span>**CAPICOM \_ A \_ confiança \_ não é uma \_ assinatura \_ válida** (&H00000008)


</dt> <dd>

O certificado ou um dos certificados na cadeia de certificados não tem uma assinatura válida.

</dd> <dt>

<span id="CAPICOM_TRUST_IS_NOT_VALID_FOR_USAGE"></span><span id="capicom_trust_is_not_valid_for_usage"></span>

<span id="CAPICOM_TRUST_IS_NOT_VALID_FOR_USAGE"></span><span id="capicom_trust_is_not_valid_for_usage"></span>**CAPICOM \_ \_A relação \_ de confiança não é \_ válida \_ para \_ uso** (&H00000010)


</dt> <dd>

O certificado ou a cadeia de certificados não é válido para seu uso proposto.

</dd> <dt>

<span id="CAPICOM_TRUST_IS_UNTRUSTED_ROOT"></span><span id="capicom_trust_is_untrusted_root"></span>

<span id="CAPICOM_TRUST_IS_UNTRUSTED_ROOT"></span><span id="capicom_trust_is_untrusted_root"></span>**CAPICOM \_ CONFIAR \_ é \_ \_ raiz não confiável** (&H00000020)


</dt> <dd>

O certificado ou a cadeia de certificados baseia-se em uma raiz não confiável.

</dd> <dt>

<span id="CAPICOM_TRUST_REVOCATION_STATUS_UNKNOWN"></span><span id="capicom_trust_revocation_status_unknown"></span>

<span id="CAPICOM_TRUST_REVOCATION_STATUS_UNKNOWN"></span><span id="capicom_trust_revocation_status_unknown"></span>**CAPICOM \_ \_Status de revogação de confiança \_ \_ desconhecido** (&H00000040)


</dt> <dd>

O status de revogação do certificado ou um dos certificados na cadeia de certificados é desconhecido.

</dd> <dt>

<span id="CAPICOM_TRUST_IS_CYCLIC"></span><span id="capicom_trust_is_cyclic"></span>

<span id="CAPICOM_TRUST_IS_CYCLIC"></span><span id="capicom_trust_is_cyclic"></span>**CAPICOM \_ A relação de confiança \_ é \_ cíclica** (&H00000080)


</dt> <dd>

Um dos certificados na cadeia foi emitido por uma autoridade de [*certificação*](../secgloss/c-gly.md) que o certificado original certificou.

</dd> <dt>

<span id="CAPICOM_TRUST_INVALID_EXTENSION"></span><span id="capicom_trust_invalid_extension"></span>

<span id="CAPICOM_TRUST_INVALID_EXTENSION"></span><span id="capicom_trust_invalid_extension"></span>**CAPICOM \_ \_ \_ Extensão de confiança inválida** (&H00000100)


</dt> <dd>

Um dos certificados tem uma extensão que não é válida.

</dd> <dt>

<span id="CAPICOM_TRUST_INVALID_POLICY_CONSTRAINTS"></span><span id="capicom_trust_invalid_policy_constraints"></span>

<span id="CAPICOM_TRUST_INVALID_POLICY_CONSTRAINTS"></span><span id="capicom_trust_invalid_policy_constraints"></span>**CAPICOM \_ CONFIAR \_ em \_ \_ restrições de política inválidas** (&H00000200)


</dt> <dd>

O certificado ou um dos certificados na cadeia de certificados tem uma extensão de restrições de política e um dos certificados emitidos tem uma extensão de mapeamento de política não permitida ou não tem uma extensão de políticas de emissão necessária.

</dd> <dt>

<span id="CAPICOM_TRUST_INVALID_BASIC_CONSTRAINTS"></span><span id="capicom_trust_invalid_basic_constraints"></span>

<span id="CAPICOM_TRUST_INVALID_BASIC_CONSTRAINTS"></span><span id="capicom_trust_invalid_basic_constraints"></span>**CAPICOM \_ CONFIAR \_ em \_ \_ restrições básicas inválidas** (&H00000400)


</dt> <dd>

O certificado ou um dos certificados na cadeia de certificados tem uma extensão de restrições básicas e o certificado não pode ser usado para emitir outros certificados ou o comprimento do caminho da cadeia foi excedido.

</dd> <dt>

<span id="CAPICOM_TRUST_INVALID_NAME_CONSTRAINTS"></span><span id="capicom_trust_invalid_name_constraints"></span>

<span id="CAPICOM_TRUST_INVALID_NAME_CONSTRAINTS"></span><span id="capicom_trust_invalid_name_constraints"></span>**CAPICOM \_ CONFIAR \_ em \_ \_ restrições de nome inválido** (&H00000800)


</dt> <dd>

O certificado ou um dos certificados na cadeia de certificados tem uma extensão de restrições de nome que não é válida.

</dd> <dt>

<span id="CAPICOM_TRUST_HAS_NOT_SUPPORTED_NAME_CONSTRAINT"></span><span id="capicom_trust_has_not_supported_name_constraint"></span>

<span id="CAPICOM_TRUST_HAS_NOT_SUPPORTED_NAME_CONSTRAINT"></span><span id="capicom_trust_has_not_supported_name_constraint"></span>**CAPICOM \_ TRUST \_ \_ não tem \_ suporte para a \_ \_ restrição de nome** (&H00001000)


</dt> <dd>

O certificado ou um dos certificados na cadeia de certificados tem uma extensão de restrições de nome que contém campos sem suporte. Não há suporte para os campos mínimo e máximo. Portanto, o mínimo sempre deve ser zero e o máximo deve estar sempre ausente. Somente o UPN tem suporte para um outro nome. Não há suporte para as seguintes opções de nome alternativo:

-   Endereço X400
-   Nome da parte EDI
-   ID registrada

</dd> <dt>

<span id="CAPICOM_TRUST_HAS_NOT_DEFINED_NAME_CONSTRAINT"></span><span id="capicom_trust_has_not_defined_name_constraint"></span>

<span id="CAPICOM_TRUST_HAS_NOT_DEFINED_NAME_CONSTRAINT"></span><span id="capicom_trust_has_not_defined_name_constraint"></span>**CAPICOM \_ A relação de confiança \_ \_ não \_ definiu a \_ \_ restrição de nome** (&H00002000)


</dt> <dd>

O certificado ou um dos certificados na cadeia de certificados tem uma extensão de restrições de nome e uma restrição de nome está ausente para uma das opções de nome no certificado final.

</dd> <dt>

<span id="CAPICOM_TRUST_HAS_NOT_PERMITTED_NAME_CONSTRAINT"></span><span id="capicom_trust_has_not_permitted_name_constraint"></span>

<span id="CAPICOM_TRUST_HAS_NOT_PERMITTED_NAME_CONSTRAINT"></span><span id="capicom_trust_has_not_permitted_name_constraint"></span>**CAPICOM \_ TRUST \_ \_ não \_ permitiu a \_ \_ restrição de nome** (&H00004000)


</dt> <dd>

O certificado ou um dos certificados na cadeia de certificados tem uma extensão de restrições de nome e não há uma restrição de nome permitida para uma das opções de nome no certificado final.

</dd> <dt>

<span id="CAPICOM_TRUST_HAS_EXCLUDED_NAME_CONSTRAINT"></span><span id="capicom_trust_has_excluded_name_constraint"></span>

<span id="CAPICOM_TRUST_HAS_EXCLUDED_NAME_CONSTRAINT"></span><span id="capicom_trust_has_excluded_name_constraint"></span>**CAPICOM \_ A confiança \_ tem uma \_ \_ \_ restrição de nome excluída** (&H00008000)


</dt> <dd>

O certificado ou um dos certificados na cadeia de certificados tem uma extensão de restrições de nome e uma das opções de nome no certificado final é explicitamente excluída.

</dd> <dt>

<span id="CAPICOM_TRUST_IS_OFFLINE_REVOCATION"></span><span id="capicom_trust_is_offline_revocation"></span>

<span id="CAPICOM_TRUST_IS_OFFLINE_REVOCATION"></span><span id="capicom_trust_is_offline_revocation"></span>**CAPICOM \_ A relação de confiança \_ é de \_ \_ revogação offline** (&H01000000)


</dt> <dd>

O status de revogação do certificado ou um dos certificados na cadeia de certificados está offline ou obsoleto.

</dd> <dt>

<span id="CAPICOM_TRUST_NO_ISSUANCE_CHAIN_POLICY"></span><span id="capicom_trust_no_issuance_chain_policy"></span>

<span id="CAPICOM_TRUST_NO_ISSUANCE_CHAIN_POLICY"></span><span id="capicom_trust_no_issuance_chain_policy"></span>**CAPICOM \_ CONFIAR \_ em \_ nenhuma \_ \_ política de cadeia de emissão** (&H02000000)


</dt> <dd>

O certificado final não tem nenhuma política de emissão resultante e um dos certificados de AC emissora tem uma extensão de restrições de política que o exige.

</dd> <dt>

<span id="CAPICOM_TRUST_IS_PARTIAL_CHAIN"></span><span id="capicom_trust_is_partial_chain"></span>

<span id="CAPICOM_TRUST_IS_PARTIAL_CHAIN"></span><span id="capicom_trust_is_partial_chain"></span>**CAPICOM \_ CONFIAR \_ é \_ uma \_ cadeia parcial** (&H00010000)


</dt> <dd>

A cadeia de certificados não é concorrente.

</dd> <dt>

<span id="CAPICOM_TRUST_CTL_IS_NOT_TIME_VALID"></span><span id="capicom_trust_ctl_is_not_time_valid"></span>

<span id="CAPICOM_TRUST_CTL_IS_NOT_TIME_VALID"></span><span id="capicom_trust_ctl_is_not_time_valid"></span>**CAPICOM \_ A \_ CTL de confiança \_ não é um \_ \_ tempo \_ válido** (&H00020000)


</dt> <dd>

Uma CTL usada para criar essa cadeia não estava em tempo válido.

</dd> <dt>

<span id="CAPICOM_TRUST_CTL_IS_NOT_SIGNATURE_VALID"></span><span id="capicom_trust_ctl_is_not_signature_valid"></span>

<span id="CAPICOM_TRUST_CTL_IS_NOT_SIGNATURE_VALID"></span><span id="capicom_trust_ctl_is_not_signature_valid"></span>**CAPICOM \_ A \_ CTL \_ confiável \_ não é uma \_ assinatura \_ válida** (&H00040000)


</dt> <dd>

Uma CTL usada para criar essa cadeia não tinha uma assinatura válida.

</dd> <dt>

<span id="CAPICOM_TRUST_CTL_IS_NOT_VALID_FOR_USAGE"></span><span id="capicom_trust_ctl_is_not_valid_for_usage"></span>

<span id="CAPICOM_TRUST_CTL_IS_NOT_VALID_FOR_USAGE"></span><span id="capicom_trust_ctl_is_not_valid_for_usage"></span>**CAPICOM \_ \_A CTL \_ \_ de confiança não é \_ válida \_ para \_ uso** (&H00080000)


</dt> <dd>

Uma CTL usada para criar esta cadeia não é válida para esse uso.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fim do suporte do cliente<br/> | Windows Vista<br/>                                                               |
| Fim do suporte do servidor<br/> | Windows Server 2008<br/>                                                         |
| Redistribuível<br/>       | CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
