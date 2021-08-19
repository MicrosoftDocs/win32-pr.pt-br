---
description: Recupera o status de validade da cadeia ou um certificado específico na cadeia.
title: Propriedade IChain2::Status
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
ms.openlocfilehash: 5307d03d340a0a960a5d78226d26e7b5553d27af72f255131651690e5b723355
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117769546"
---
# <a name="ichain2status-property"></a>Propriedade IChain2::Status

\[CAPICOM é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista e Windows XP. Em vez disso, [**use a Classe X509Chain**](/dotnet/api/system.security.cryptography.x509certificates.x509chain?view=netcore-3.1) no namespace [**System.Security.Cryptography.X509Certificates.**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)\]

A **propriedade Status** recupera o status de validade da cadeia ou um certificado específico na cadeia.

## <a name="syntax"></a>Syntax


```VB
Chain.Status( _
  ByVal Index _
) As Long
```



## <a name="property-value"></a>Valor da propriedade

Um **valor LONG** que representa o indicador de status de validade da cadeia ou do certificado especificado. A tabela a seguir mostra os valores possíveis. Essa propriedade conterá zero se a cadeia ou o certificado especificado for válido. Caso contrário, essa propriedade conterá uma combinação de um ou mais dos valores a seguir.

<dt>

<span id="CAPICOM_TRUST_IS_NOT_TIME_VALID"></span><span id="capicom_trust_is_not_time_valid"></span>

<span id="CAPICOM_TRUST_IS_NOT_TIME_VALID"></span><span id="capicom_trust_is_not_time_valid"></span>**CAPICOM \_ A \_ CONFIANÇA NÃO É \_ \_ \_ VÁLIDA** (&H00000001)


</dt> <dd>

Esse certificado ou um dos certificados na cadeia de certificados não é válido.

</dd> <dt>

<span id="CAPICOM_TRUST_IS_NOT_TIME_NESTED"></span><span id="capicom_trust_is_not_time_nested"></span>

<span id="CAPICOM_TRUST_IS_NOT_TIME_NESTED"></span><span id="capicom_trust_is_not_time_nested"></span>**CAPICOM \_ A \_ CONFIANÇA NÃO É \_ \_ \_ ANINHADA** POR TEMPO (&H00000002)


</dt> <dd>

Os certificados na cadeia não são aninhados corretamente.

</dd> <dt>

<span id="CAPICOM_TRUST_IS_REVOKED"></span><span id="capicom_trust_is_revoked"></span>

<span id="CAPICOM_TRUST_IS_REVOKED"></span><span id="capicom_trust_is_revoked"></span>**CAPICOM \_ TRUST \_ É \_ REVOGADO** (&H00000004)


</dt> <dd>

A confiança para esse certificado ou um dos certificados na cadeia de certificados foi revogada.

</dd> <dt>

<span id="CAPICOM_TRUST_IS_NOT_SIGNATURE_VALID"></span><span id="capicom_trust_is_not_signature_valid"></span>

<span id="CAPICOM_TRUST_IS_NOT_SIGNATURE_VALID"></span><span id="capicom_trust_is_not_signature_valid"></span>**CAPICOM \_ TRUST \_ NÃO É UMA ASSINATURA \_ \_ \_ VÁLIDA** (&H000000008)


</dt> <dd>

O certificado ou um dos certificados na cadeia de certificados não tem uma assinatura válida.

</dd> <dt>

<span id="CAPICOM_TRUST_IS_NOT_VALID_FOR_USAGE"></span><span id="capicom_trust_is_not_valid_for_usage"></span>

<span id="CAPICOM_TRUST_IS_NOT_VALID_FOR_USAGE"></span><span id="capicom_trust_is_not_valid_for_usage"></span>**CAPICOM \_ A \_ CONFIANÇA NÃO É VÁLIDA PARA \_ \_ \_ \_ USO** (&H000000010)


</dt> <dd>

A cadeia de certificados ou certificados não é válida para seu uso proposto.

</dd> <dt>

<span id="CAPICOM_TRUST_IS_UNTRUSTED_ROOT"></span><span id="capicom_trust_is_untrusted_root"></span>

<span id="CAPICOM_TRUST_IS_UNTRUSTED_ROOT"></span><span id="capicom_trust_is_untrusted_root"></span>**CAPICOM \_ TRUST \_ É UMA RAIZ NÃO \_ \_ CONFIÁVEL** (&H00000020)


</dt> <dd>

A cadeia de certificados ou certificados baseia-se em uma raiz não falsa.

</dd> <dt>

<span id="CAPICOM_TRUST_REVOCATION_STATUS_UNKNOWN"></span><span id="capicom_trust_revocation_status_unknown"></span>

<span id="CAPICOM_TRUST_REVOCATION_STATUS_UNKNOWN"></span><span id="capicom_trust_revocation_status_unknown"></span>**CAPICOM \_ TRUST \_ REVOCATION \_ STATUS \_ UNKNOWN** (&H00000040)


</dt> <dd>

O status de revogação do certificado ou um dos certificados na cadeia de certificados é desconhecido.

</dd> <dt>

<span id="CAPICOM_TRUST_IS_CYCLIC"></span><span id="capicom_trust_is_cyclic"></span>

<span id="CAPICOM_TRUST_IS_CYCLIC"></span><span id="capicom_trust_is_cyclic"></span>**CAPICOM \_ TRUST \_ IS \_ CÍCLICO** (&H00000080)


</dt> <dd>

Um dos certificados na cadeia foi emitido por uma autoridade de [*certificação*](../secgloss/c-gly.md) que o certificado original certificou.

</dd> <dt>

<span id="CAPICOM_TRUST_INVALID_EXTENSION"></span><span id="capicom_trust_invalid_extension"></span>

<span id="CAPICOM_TRUST_INVALID_EXTENSION"></span><span id="capicom_trust_invalid_extension"></span>**CAPICOM \_ TRUST \_ INVALID \_ EXTENSION** (&H00000100)


</dt> <dd>

Um dos certificados tem uma extensão que não é válida.

</dd> <dt>

<span id="CAPICOM_TRUST_INVALID_POLICY_CONSTRAINTS"></span><span id="capicom_trust_invalid_policy_constraints"></span>

<span id="CAPICOM_TRUST_INVALID_POLICY_CONSTRAINTS"></span><span id="capicom_trust_invalid_policy_constraints"></span>**CAPICOM \_ RESTRIÇÕES \_ \_ DE POLÍTICA \_ INVÁLIDAS DE** CONFIANÇA (&H000000200)


</dt> <dd>

O certificado ou um dos certificados na cadeia de certificados tem uma extensão de restrições de política e um dos certificados emitidos tem uma extensão de mapeamento de política não permitido ou não tem uma extensão de políticas de emissão necessária.

</dd> <dt>

<span id="CAPICOM_TRUST_INVALID_BASIC_CONSTRAINTS"></span><span id="capicom_trust_invalid_basic_constraints"></span>

<span id="CAPICOM_TRUST_INVALID_BASIC_CONSTRAINTS"></span><span id="capicom_trust_invalid_basic_constraints"></span>**CAPICOM \_ \_RESTRIÇÕES \_ \_ BÁSICAS INVÁLIDAS** DE CONFIANÇA (&H00000400)


</dt> <dd>

O certificado ou um dos certificados na cadeia de certificados tem uma extensão de restrições básica e o certificado não pode ser usado para emitir outros certificados ou o comprimento do caminho da cadeia foi excedido.

</dd> <dt>

<span id="CAPICOM_TRUST_INVALID_NAME_CONSTRAINTS"></span><span id="capicom_trust_invalid_name_constraints"></span>

<span id="CAPICOM_TRUST_INVALID_NAME_CONSTRAINTS"></span><span id="capicom_trust_invalid_name_constraints"></span>**CAPICOM \_ RESTRIÇÕES \_ \_ DE NOME INVÁLIDO \_ DE** CONFIANÇA (&H00000800)


</dt> <dd>

O certificado ou um dos certificados na cadeia de certificados tem uma extensão de restrições de nome que não é válida.

</dd> <dt>

<span id="CAPICOM_TRUST_HAS_NOT_SUPPORTED_NAME_CONSTRAINT"></span><span id="capicom_trust_has_not_supported_name_constraint"></span>

<span id="CAPICOM_TRUST_HAS_NOT_SUPPORTED_NAME_CONSTRAINT"></span><span id="capicom_trust_has_not_supported_name_constraint"></span>**CAPICOM \_ A \_ \_ \_ RESTRIÇÃO DE NOME \_ CONFIÁVEL \_ NÃO** TEM SUPORTE (&H00001000)


</dt> <dd>

O certificado ou um dos certificados na cadeia de certificados tem uma extensão de restrições de nome que contém campos sem suporte. Não há suporte para os campos mínimo e máximo. Portanto, o mínimo sempre deve ser zero e o máximo sempre deve estar ausente. Somente UPN tem suporte para um Outro Nome. Não há suporte para as seguintes opções de nome alternativo:

-   Endereço X400
-   Nome da Parte EDI
-   ID registrada

</dd> <dt>

<span id="CAPICOM_TRUST_HAS_NOT_DEFINED_NAME_CONSTRAINT"></span><span id="capicom_trust_has_not_defined_name_constraint"></span>

<span id="CAPICOM_TRUST_HAS_NOT_DEFINED_NAME_CONSTRAINT"></span><span id="capicom_trust_has_not_defined_name_constraint"></span>**CAPICOM \_ TRUST \_ NÃO \_ \_ DEFINIU A \_ \_ RESTRIÇÃO DE** NOME (&H00002000)


</dt> <dd>

O certificado ou um dos certificados na cadeia de certificados tem uma extensão de restrições de nome e uma restrição de nome está ausente para uma das opções de nome no certificado final.

</dd> <dt>

<span id="CAPICOM_TRUST_HAS_NOT_PERMITTED_NAME_CONSTRAINT"></span><span id="capicom_trust_has_not_permitted_name_constraint"></span>

<span id="CAPICOM_TRUST_HAS_NOT_PERMITTED_NAME_CONSTRAINT"></span><span id="capicom_trust_has_not_permitted_name_constraint"></span>**CAPICOM \_ TRUST \_ NÃO \_ PERMITIU \_ \_ RESTRIÇÃO DE \_ NOME** (&H00004000)


</dt> <dd>

O certificado ou um dos certificados na cadeia de certificados tem uma extensão de restrições de nome e não há uma restrição de nome permitida para uma das opções de nome no certificado final.

</dd> <dt>

<span id="CAPICOM_TRUST_HAS_EXCLUDED_NAME_CONSTRAINT"></span><span id="capicom_trust_has_excluded_name_constraint"></span>

<span id="CAPICOM_TRUST_HAS_EXCLUDED_NAME_CONSTRAINT"></span><span id="capicom_trust_has_excluded_name_constraint"></span>**CAPICOM \_ TRUST \_ \_ EXCLUIU \_ A \_ RESTRIÇÃO DE** NOME (&H00008000)


</dt> <dd>

O certificado ou um dos certificados na cadeia de certificados tem uma extensão de restrições de nome e uma das opções de nome no certificado final é excluída explicitamente.

</dd> <dt>

<span id="CAPICOM_TRUST_IS_OFFLINE_REVOCATION"></span><span id="capicom_trust_is_offline_revocation"></span>

<span id="CAPICOM_TRUST_IS_OFFLINE_REVOCATION"></span><span id="capicom_trust_is_offline_revocation"></span>**CAPICOM \_ TRUST \_ IS \_ OFFLINE \_ REVOCATION** (&H010000000)


</dt> <dd>

O status de revogação do certificado ou um dos certificados na cadeia de certificados está offline ou desalocado.

</dd> <dt>

<span id="CAPICOM_TRUST_NO_ISSUANCE_CHAIN_POLICY"></span><span id="capicom_trust_no_issuance_chain_policy"></span>

<span id="CAPICOM_TRUST_NO_ISSUANCE_CHAIN_POLICY"></span><span id="capicom_trust_no_issuance_chain_policy"></span>**CAPICOM \_ TRUST \_ NO \_ ISSUANCE \_ CHAIN \_ POLICY** (&H02000000)


</dt> <dd>

O certificado final não tem nenhuma política de emissão resultante e um dos certificados de AC em emissão tem uma extensão de restrições de política que a exige.

</dd> <dt>

<span id="CAPICOM_TRUST_IS_PARTIAL_CHAIN"></span><span id="capicom_trust_is_partial_chain"></span>

<span id="CAPICOM_TRUST_IS_PARTIAL_CHAIN"></span><span id="capicom_trust_is_partial_chain"></span>**CAPICOM \_ CONFIANÇA \_ É \_ CADEIA \_ PARCIAL** (&H00010000)


</dt> <dd>

A cadeia de certificados não é compete.

</dd> <dt>

<span id="CAPICOM_TRUST_CTL_IS_NOT_TIME_VALID"></span><span id="capicom_trust_ctl_is_not_time_valid"></span>

<span id="CAPICOM_TRUST_CTL_IS_NOT_TIME_VALID"></span><span id="capicom_trust_ctl_is_not_time_valid"></span>**CAPICOM \_ A \_ CTL DE \_ CONFIANÇA NÃO \_ É \_ VÁLIDA \_** (&H00020000)


</dt> <dd>

Uma CTL usada para criar essa cadeia não era válida.

</dd> <dt>

<span id="CAPICOM_TRUST_CTL_IS_NOT_SIGNATURE_VALID"></span><span id="capicom_trust_ctl_is_not_signature_valid"></span>

<span id="CAPICOM_TRUST_CTL_IS_NOT_SIGNATURE_VALID"></span><span id="capicom_trust_ctl_is_not_signature_valid"></span>**CAPICOM \_ TRUST \_ CTL \_ NÃO É UMA ASSINATURA \_ \_ \_ VÁLIDA** (&H00040000)


</dt> <dd>

Uma CTL usada para criar essa cadeia não tinha uma assinatura válida.

</dd> <dt>

<span id="CAPICOM_TRUST_CTL_IS_NOT_VALID_FOR_USAGE"></span><span id="capicom_trust_ctl_is_not_valid_for_usage"></span>

<span id="CAPICOM_TRUST_CTL_IS_NOT_VALID_FOR_USAGE"></span><span id="capicom_trust_ctl_is_not_valid_for_usage"></span>**CAPICOM \_ A \_ CTL DE \_ CONFIANÇA NÃO É VÁLIDA PARA \_ \_ \_ \_ USO** (&H00080000)


</dt> <dd>

Uma CTL usada para criar essa cadeia não é válida para esse uso.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fim do suporte ao cliente<br/> | Windows Vista<br/>                                                               |
| Fim do suporte ao servidor<br/> | Windows Server 2008<br/>                                                         |
| Redistribuível<br/>       | CAPICOM 2.0 ou posterior no Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
