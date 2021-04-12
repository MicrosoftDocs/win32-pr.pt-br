---
description: Descreve os erros do provedor SNMP WMI 231 a 240.
ms.assetid: edb3dabb-6a65-4285-97d3-f7025d3bb5da
ms.tgt_platform: multiple
title: Erros 231 a 240
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76d053cac57eec9d0055dec56bbfab8304ad3f97
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171449"
---
# <a name="errors-231-through-240"></a>Erros 231 a 240

Descreve os erros do provedor SNMP WMI 231 a 240.

[Erro fatal 232](#fatal-error-232)

[Erro fatal 233](#fatal-error-233)

[Erro fatal 234](#fatal-error-234)

[Erro fatal 236](#fatal-error-236)

## <a name="fatal-error-232"></a>Erro fatal 232

<dl> <dt>

<span id="_232__Fatal____fileName___line___Invocation_of_SNMPv1_SMI_OBJECT-TYPE_disallowed_"></span><span id="_232__fatal____filename___line___invocation_of_snmpv1_smi_object-type_disallowed_"></span><span id="_232__FATAL____FILENAME___LINE___INVOCATION_OF_SNMPV1_SMI_OBJECT-TYPE_DISALLOWED_"></span>**<232, fatal>: " <fileName> : <linha \#>: invocação de tipo de objeto de SMI de SNMPv1 não permitido"**
</dt> <dd>

Erro de sintaxe do módulo. Você usou a invocação de **tipo de objeto** específica de SNMPV1 na MIB, mas especificou a opção **/v2c** , que requer conformidade estrita com a sintaxe de SNMPv2c.

</dd> </dl>

## <a name="fatal-error-233"></a>Erro fatal 233

<dl> <dt>

<span id="_233__Fatal_____fileName___line____Invocation_of_SNMPv1_SMI_TRAP-TYPE_disallowed_"></span><span id="_233__fatal_____filename___line____invocation_of_snmpv1_smi_trap-type_disallowed_"></span><span id="_233__FATAL_____FILENAME___LINE____INVOCATION_OF_SNMPV1_SMI_TRAP-TYPE_DISALLOWED_"></span>**<233, fatal>: " <fileName> : <linha \#>: invocação de tipo de interceptação de SMI de SNMPv1 não permitido"**
</dt> <dd>

Erro de sintaxe do módulo. Você usou a invocação de **tipo de interceptação** específica de SNMPV1 na MIB, mas especificou a opção **/v2c** , que requer conformidade estrita com a sintaxe de SNMPv2c.

</dd> </dl>

## <a name="fatal-error-234"></a>Erro fatal 234

<dl> <dt>

<span id="_234__Fatal____fileName___line____MODULE-IDENTITY_invocation_is_allowed_only_immediately_after_the_IMPORTS_section_"></span><span id="_234__fatal____filename___line____module-identity_invocation_is_allowed_only_immediately_after_the_imports_section_"></span><span id="_234__FATAL____FILENAME___LINE____MODULE-IDENTITY_INVOCATION_IS_ALLOWED_ONLY_IMMEDIATELY_AFTER_THE_IMPORTS_SECTION_"></span>**<234, fatal>: " <fileName> : <linha \#>: módulo-a invocação de identidade é permitida apenas imediatamente após a seção Imports"**
</dt> <dd>

Erro de sintaxe do módulo. A invocação de **identidade de módulo** é incorreta.

</dd> </dl>

## <a name="fatal-error-236"></a>Erro fatal 236

<dl> <dt>

<span id="_236__Fatal_____fileName___line____Number_does_not_fit_into_the_32_bit_representation_used_by_the_compiler_"></span><span id="_236__fatal_____filename___line____number_does_not_fit_into_the_32_bit_representation_used_by_the_compiler_"></span><span id="_236__FATAL_____FILENAME___LINE____NUMBER_DOES_NOT_FIT_INTO_THE_32_BIT_REPRESENTATION_USED_BY_THE_COMPILER_"></span>**<236,> fatal: " <fileName> : <da linha \#>: Number não cabe na representação de bit 32 usada pelo compilador"**
</dt> <dd>

Erro de sintaxe do módulo na atribuição de valor. Há um erro de atribuição de valor de MIB no qual um valor inteiro é tão grande que requer mais de 32 bits para representá-lo.

</dd> </dl>

 

 



