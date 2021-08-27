---
description: Descreve os erros de provedor WMI SNMP 1031 a 1040.
ms.assetid: 5fc519ac-ae05-4daf-a681-7935190f1d46
ms.tgt_platform: multiple
title: Erros de 1031 a 1040
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5986ba80a55d2d8f3d4a87b0587331765aa38d67
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122886873"
---
# <a name="errors-1031-through-1040"></a>Erros de 1031 a 1040

Descreve os erros de provedor WMI SNMP 1031 a 1040.

[Aviso 1031](#warning-1031)

[Erro fatal 1032](#fatal-error-1032)

[Erro fatal 1033](#fatal-error-1033)

[Aviso 1034](#warning-1034)

[Aviso 1036](#warning-1036)

[Erro fatal 1037](#fatal-error-1037)

[Erro fatal 1038](#fatal-error-1038)

[Erro fatal 1039](#fatal-error-1039)

[Erro fatal 1040](#fatal-error-1040)

## <a name="warning-1031"></a>Aviso 1031

<dl> <dt>

<span id="_1031__Warning_____fileName___line____Standard_symbol__identifier__should_be_imported_from_module__identifier_._Assuming_the_standard_definition._"></span><span id="_1031__warning_____filename___line____standard_symbol__identifier__should_be_imported_from_module__identifier_._assuming_the_standard_definition._"></span><span id="_1031__WARNING_____FILENAME___LINE____STANDARD_SYMBOL__IDENTIFIER__SHOULD_BE_IMPORTED_FROM_MODULE__IDENTIFIER_._ASSUMING_THE_STANDARD_DEFINITION._"></span>**<1031, Aviso>: " &lt; fileName &gt; :<line \#>: O identificador de símbolo padrão deve ser importado do &lt; &gt; &lt; identificador do módulo &gt; . Supondo a definição padrão."**
</dt> <dd>

Aviso semântico de módulo da seção IMPORTS, específico para SNMPv1 nem SNMPv2C. Se um identificador SNMP conhecido pelo compilador estiver na seção IMPORTS, o módulo do qual ele é importado deverá ser um dos módulos padrão.

Alguns IMPORTS comumente usados são "conhecimento presumido" por parte do compilador. É desnecessário para o compilador exigir acesso a outros módulos de informações para resolvê-los.

O SNMPv1 e o SNMPv2C IMPORTS integrados são descritos nas tabelas a seguir.

</dd> </dl>

**IMPORTAÇÕES SNMPv1 integrados**



| Classe Import | Módulo      | Instâncias                                                           |
|--------------|-------------|---------------------------------------------------------------------|
| Valor ASN.1  | RFC1155-SMI | Internet, diretório, gerenciamento, experimental, privado, empresas |
|              | RFC1213-MIB | MIB-II e IP, interfaces, transmissão                             |
| Tipo ASN.1   | RFC1155-SMI | NetworkAddress, IpAddress, Counter, Gauge, TimeTicks, Opaque        |
|              | RFC1213-MIB | DisplayString, PhysAddress                                          |
| ASN.1 Macro  | RFC-1212    | TIPO DE OBJETO                                                         |
|              | RFC-1215    | TIPO TRAP                                                           |



 

**IMPORTAÇÕES SNMPv2C integrados**



| Classe Import       | Módulo      | Instâncias                                                                                                                                                                                                      |
|--------------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Valor ASN.1        | SNMPv2-SMI  | org, dod, Internet, directory, mgmt, mib-2, transmissão, experimental, privada, enterprises, security, snmpv2, snmpDomains, snmpProxys, snmpModules                                                           |
|                    | SNMPv2-TM   | rfc1157Proxy                                                                                                                                                                                                   |
| Identidade do objeto    | SNMPv2-SMI  | zeroDotZero                                                                                                                                                                                                    |
|                    | SNMPv2-TM   | snmpUDPDomain, snmpCLNSDomain, smnpCONSDomain, snmpDDPDomain, snmpIPXDomain, rfc1157Domain                                                                                                                     |
| Tipo ASN.1         | SNMPv2-SMI  | Integer32, IpAddress, Counter32, TimeTicks, Opaque, Counter64, Unsigned32, Gauge32                                                                                                                             |
| ASN.1 Macro        | SNMPv2-SMI  | MODULE-IDENTITY, OBJECT-IDENTITY, OBJECT-TYPE, NOTIFICATION-TYPE                                                                                                                                               |
|                    | SNMPv2-CONF | OBJECT-GROUP, NOTIFICATION-GROUP, MODULE-COMPLIANCE, AGENT-CAPABILITIES                                                                                                                                        |
|                    | SNMPv2-TC   | TEXTUAL-CONVENTION                                                                                                                                                                                             |
| Convenção textual | SNMPv2-TC   | DisplayString, PhysAddress, MacAddress, TruthValue, TestAndIncr, AutonomousType, InstancePointer, VariablePointer, RowPointer, RowStatus, TimeStamp, TimeInterval, DateAndTime, StorageType, Tdomain,Dress |
|                    | SNMPv2-TM   | SnmpUDPAddress, SnmpOSIAddress, SnmpNBPAddress, SnmpIPXAddress                                                                                                                                                 |



 

## <a name="fatal-error-1032"></a>Erro fatal 1032

<dl> <dt>

<span id="_1032__Fatal_____fileName__line____Duplicate_value__value__in_enumeration_"></span><span id="_1032__fatal_____filename__line____duplicate_value__value__in_enumeration_"></span><span id="_1032__FATAL_____FILENAME__LINE____DUPLICATE_VALUE__VALUE__IN_ENUMERATION_"></span>**<1032, Fatal>: " &lt; fileName &gt;<line \#>: Valor &lt; duplicado na &gt; enumeração"**
</dt> <dd>

Erro semântico de módulo em uma enumeração, específico para SNMPv1 nem SNMPv2C. Não deve haver nenhum valor duplicado. O <linha> parâmetro é a \# posição da recorrência do nome/valor.

</dd> </dl>

## <a name="fatal-error-1033"></a>Erro fatal 1033

<dl> <dt>

<span id="_1033__Fatal_____fileName__line____Duplicate_name__identifier__in_enumeration_"></span><span id="_1033__fatal_____filename__line____duplicate_name__identifier__in_enumeration_"></span><span id="_1033__FATAL_____FILENAME__LINE____DUPLICATE_NAME__IDENTIFIER__IN_ENUMERATION_"></span>**<1033, Fatal>: " fileName<line>: Identificador de nome duplicado na &lt; &gt; \# &lt; &gt; enumeração"**
</dt> <dd>

Erro semântico de módulo em uma enumeração, específico para SNMPv1 nem SNMPv2C. Não deve haver nenhum nome duplicado. O <linha> parâmetro é a \# posição da recorrência do nome/valor.

</dd> </dl>

## <a name="warning-1034"></a>Aviso 1034

<dl> <dt>

<span id="_1034__Warning_____fileName__line____A_value_of_0_disallowed_in_an_enumeration_"></span><span id="_1034__warning_____filename__line____a_value_of_0_disallowed_in_an_enumeration_"></span><span id="_1034__WARNING_____FILENAME__LINE____A_VALUE_OF_0_DISALLOWED_IN_AN_ENUMERATION_"></span>**<1034, Aviso>: " fileName<linha>: um valor de 0 não permitido em uma &lt; &gt; \# enumeração"**
</dt> <dd>

Aviso semântico de módulo em uma enumeração, específico para SNMPv1 nem SNMPv2C. É recomendável que um valor nomeado de zero não seja usado em uma enumeração.

</dd> </dl>

## <a name="warning-1036"></a>Aviso 1036

<dl> <dt>

<span id="_1036__Warning____fileName__line____Value_in_enumeration_does_not_resolve_to_a_positive_integer_"></span><span id="_1036__warning____filename__line____value_in_enumeration_does_not_resolve_to_a_positive_integer_"></span><span id="_1036__WARNING____FILENAME__LINE____VALUE_IN_ENUMERATION_DOES_NOT_RESOLVE_TO_A_POSITIVE_INTEGER_"></span>**<1036, Aviso> " fileName<linha>: o valor na enumeração não resolve para um inteiro &lt; &gt; \# positivo"**
</dt> <dd>

Aviso semântico de módulo em uma enumeração, específico para SNMPv1 nem SNMPv2C. Um valor negativo não é permitido em uma enumeração.

</dd> </dl>

## <a name="fatal-error-1037"></a>Erro fatal 1037

<dl> <dt>

<span id="_1037__Fatal_____fileName__line____Identifier__identifier__does_not_resolve_to_OCTET_STRING_or_Opaque_types_"></span><span id="_1037__fatal_____filename__line____identifier__identifier__does_not_resolve_to_octet_string_or_opaque_types_"></span><span id="_1037__FATAL_____FILENAME__LINE____IDENTIFIER__IDENTIFIER__DOES_NOT_RESOLVE_TO_OCTET_STRING_OR_OPAQUE_TYPES_"></span>**<1037, Fatal>: " fileName<line>: Identificador identifier não resolve para &lt; &gt; tipos \# OCTET STRING ou &lt; &gt; Opaque"**
</dt> <dd>

Erro semântico do módulo na especificação SIZE, específico para SNMPv1 nem SNMPv2C. O símbolo usado em uma especificação SIZE deve ser resolvido para OCTET STRING ou Opaque.

</dd> </dl>

## <a name="fatal-error-1038"></a>Erro fatal 1038

<dl> <dt>

<span id="_1038__Fatal_____fileName__line____Identifier__identifier__does_not_resolve_an_INTEGER_or_Gauge_type_"></span><span id="_1038__fatal_____filename__line____identifier__identifier__does_not_resolve_an_integer_or_gauge_type_"></span><span id="_1038__FATAL_____FILENAME__LINE____IDENTIFIER__IDENTIFIER__DOES_NOT_RESOLVE_AN_INTEGER_OR_GAUGE_TYPE_"></span>**<1038, Fatal>: " &lt; fileName &gt;<line \#>: &lt; Identificador identifier não resolve um tipo INTEGER ou &gt; Gauge"**
</dt> <dd>

Erro semântico do módulo na especificação de intervalo. Esse erro pode ocorrer em SNMPv1 ou SNMPv2C.

Em SNMPv1, o símbolo usado em uma especificação range deve ser resolvido como INTEGER ou Gauge.

No SNMPv2C, o símbolo usado em uma especificação range deve ser resolvido como INTEGER, Gauge32, Integer32 ou Unsigned32.

</dd> </dl>

## <a name="fatal-error-1039"></a>Erro fatal 1039

<dl> <dt>

<span id="_1039__Fatal___fileName__line____Negative_value_used_in_SIZE_specification_"></span><span id="_1039__fatal___filename__line____negative_value_used_in_size_specification_"></span><span id="_1039__FATAL___FILENAME__LINE____NEGATIVE_VALUE_USED_IN_SIZE_SPECIFICATION_"></span>**<1039, Fatal>: fileName<linha>: valor negativo usado na &lt; &gt; \# especificação SIZE"**
</dt> <dd>

Erro semântico do módulo na especificação SIZE, específico para SNMPv1 nem SNMPv2C. Qualquer valor usado na especificação do SIZE deve ser não negativo.

</dd> </dl>

## <a name="fatal-error-1040"></a>Erro fatal 1040

<dl> <dt>

<span id="_1040__Fatal_____fileName__line____Identifier__identifier__in_SIZE_specification_does_not_resolve_to_a_non-negative_integral_value_"></span><span id="_1040__fatal_____filename__line____identifier__identifier__in_size_specification_does_not_resolve_to_a_non-negative_integral_value_"></span><span id="_1040__FATAL_____FILENAME__LINE____IDENTIFIER__IDENTIFIER__IN_SIZE_SPECIFICATION_DOES_NOT_RESOLVE_TO_A_NON-NEGATIVE_INTEGRAL_VALUE_"></span>**<1040, Fatal>: " &lt; fileName &gt;<line \#>: &lt; Identifier identifier in SIZE specification não resolve para um valor integral não &gt; negativo"**
</dt> <dd>

Erro semântico de módulo na especificação de intervalo ou tamanho, específico para SNMPv1 nem SNMPv2C. Qualquer símbolo usado na especificação de um valor em uma especificação SIZE é resolvido para um valor não negativo.

</dd> </dl>

 

 



