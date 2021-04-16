---
description: Descreve os erros do provedor SNMP WMI 1031 a 1040.
ms.assetid: 5fc519ac-ae05-4daf-a681-7935190f1d46
ms.tgt_platform: multiple
title: Erros 1031 a 1040
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d34079c2cbdb8e50aef04e8c364ba99abee760fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105753691"
---
# <a name="errors-1031-through-1040"></a><span data-ttu-id="2c454-103">Erros 1031 a 1040</span><span class="sxs-lookup"><span data-stu-id="2c454-103">Errors 1031 through 1040</span></span>

<span data-ttu-id="2c454-104">Descreve os erros do provedor SNMP WMI 1031 a 1040.</span><span class="sxs-lookup"><span data-stu-id="2c454-104">Describes WMI SNMP provider errors 1031 through 1040.</span></span>

[<span data-ttu-id="2c454-105">Aviso 1031</span><span class="sxs-lookup"><span data-stu-id="2c454-105">Warning 1031</span></span>](#warning-1031)

[<span data-ttu-id="2c454-106">Erro fatal 1032</span><span class="sxs-lookup"><span data-stu-id="2c454-106">Fatal Error 1032</span></span>](#fatal-error-1032)

[<span data-ttu-id="2c454-107">Erro fatal 1033</span><span class="sxs-lookup"><span data-stu-id="2c454-107">Fatal Error 1033</span></span>](#fatal-error-1033)

[<span data-ttu-id="2c454-108">Aviso 1034</span><span class="sxs-lookup"><span data-stu-id="2c454-108">Warning 1034</span></span>](#warning-1034)

[<span data-ttu-id="2c454-109">Aviso 1036</span><span class="sxs-lookup"><span data-stu-id="2c454-109">Warning 1036</span></span>](#warning-1036)

[<span data-ttu-id="2c454-110">Erro fatal 1037</span><span class="sxs-lookup"><span data-stu-id="2c454-110">Fatal Error 1037</span></span>](#fatal-error-1037)

[<span data-ttu-id="2c454-111">Erro fatal 1038</span><span class="sxs-lookup"><span data-stu-id="2c454-111">Fatal Error 1038</span></span>](#fatal-error-1038)

[<span data-ttu-id="2c454-112">Erro fatal 1039</span><span class="sxs-lookup"><span data-stu-id="2c454-112">Fatal Error 1039</span></span>](#fatal-error-1039)

[<span data-ttu-id="2c454-113">Erro fatal 1040</span><span class="sxs-lookup"><span data-stu-id="2c454-113">Fatal Error 1040</span></span>](#fatal-error-1040)

## <a name="warning-1031"></a><span data-ttu-id="2c454-114">Aviso 1031</span><span class="sxs-lookup"><span data-stu-id="2c454-114">Warning 1031</span></span>

<dl> <dt>

<span data-ttu-id="2c454-115"><span id="_1031__Warning_____fileName___line____Standard_symbol__identifier__should_be_imported_from_module__identifier_._Assuming_the_standard_definition._"></span><span id="_1031__warning_____filename___line____standard_symbol__identifier__should_be_imported_from_module__identifier_._assuming_the_standard_definition._"></span><span id="_1031__WARNING_____FILENAME___LINE____STANDARD_SYMBOL__IDENTIFIER__SHOULD_BE_IMPORTED_FROM_MODULE__IDENTIFIER_._ASSUMING_THE_STANDARD_DEFINITION._"></span>**<1031, aviso>: " <fileName> : <linha \#>: o símbolo padrão <identifier> deve ser importado do módulo <identifier> . Assumindo a definição padrão. "**</span><span class="sxs-lookup"><span data-stu-id="2c454-115"><span id="_1031__Warning_____fileName___line____Standard_symbol__identifier__should_be_imported_from_module__identifier_._Assuming_the_standard_definition._"></span><span id="_1031__warning_____filename___line____standard_symbol__identifier__should_be_imported_from_module__identifier_._assuming_the_standard_definition._"></span><span id="_1031__WARNING_____FILENAME___LINE____STANDARD_SYMBOL__IDENTIFIER__SHOULD_BE_IMPORTED_FROM_MODULE__IDENTIFIER_._ASSUMING_THE_STANDARD_DEFINITION._"></span>**<1031, Warning>: "<fileName>:<line\#>: Standard symbol <identifier> should be imported from module <identifier>. Assuming the standard definition."**</span></span>
</dt> <dd>

<span data-ttu-id="2c454-116">Seção de importações aviso semântico do módulo, específico para não SNMPv1 nem SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="2c454-116">IMPORTS section module semantic warning, specific to neither SNMPv1 nor SNMPv2C.</span></span> <span data-ttu-id="2c454-117">Se um identificador SNMP conhecido pelo compilador estiver na seção importações, o módulo do qual ele é importado deverá ser um dos módulos padrão.</span><span class="sxs-lookup"><span data-stu-id="2c454-117">If an SNMP identifier known to the compiler is in the IMPORTS section, then the module from which it is imported must be one of the standard modules.</span></span>

<span data-ttu-id="2c454-118">Determinadas importações comumente usadas são "conhecimento assumido" na parte do compilador.</span><span class="sxs-lookup"><span data-stu-id="2c454-118">Certain commonly used IMPORTS are "assumed knowledge" on the part of the compiler.</span></span> <span data-ttu-id="2c454-119">É desnecessário que o compilador exija acesso a outros módulos de informações para resolvê-los.</span><span class="sxs-lookup"><span data-stu-id="2c454-119">It is unnecessary for the compiler to require access to other information modules to resolve these.</span></span>

<span data-ttu-id="2c454-120">As importações de SNMPv1 e SNMPv2C internas são descritas nas tabelas a seguir.</span><span class="sxs-lookup"><span data-stu-id="2c454-120">The built-in SNMPv1 and SNMPv2C IMPORTS are described in the following tables.</span></span>

</dd> </dl>

<span data-ttu-id="2c454-121">**IMPORTAÇÕES de SNMPv1 internas**</span><span class="sxs-lookup"><span data-stu-id="2c454-121">**Built-in SNMPv1 IMPORTS**</span></span>



| <span data-ttu-id="2c454-122">Classe de importação</span><span class="sxs-lookup"><span data-stu-id="2c454-122">Import Class</span></span> | <span data-ttu-id="2c454-123">Módulo</span><span class="sxs-lookup"><span data-stu-id="2c454-123">Module</span></span>      | <span data-ttu-id="2c454-124">Instâncias</span><span class="sxs-lookup"><span data-stu-id="2c454-124">Instances</span></span>                                                           |
|--------------|-------------|---------------------------------------------------------------------|
| <span data-ttu-id="2c454-125">Valor ASN. 1</span><span class="sxs-lookup"><span data-stu-id="2c454-125">ASN.1 Value</span></span>  | <span data-ttu-id="2c454-126">RFC1155-SMI</span><span class="sxs-lookup"><span data-stu-id="2c454-126">RFC1155-SMI</span></span> | <span data-ttu-id="2c454-127">Internet, diretório, gerenciamento, experimental, privado, empresas</span><span class="sxs-lookup"><span data-stu-id="2c454-127">Internet, directory, management, experimental, private, enterprises</span></span> |
|              | <span data-ttu-id="2c454-128">RFC1213-MIB</span><span class="sxs-lookup"><span data-stu-id="2c454-128">RFC1213-MIB</span></span> | <span data-ttu-id="2c454-129">MIB-II e IP, interfaces, transmissão</span><span class="sxs-lookup"><span data-stu-id="2c454-129">MIB-II and IP, interfaces, transmission</span></span>                             |
| <span data-ttu-id="2c454-130">Tipo ASN. 1</span><span class="sxs-lookup"><span data-stu-id="2c454-130">ASN.1 Type</span></span>   | <span data-ttu-id="2c454-131">RFC1155-SMI</span><span class="sxs-lookup"><span data-stu-id="2c454-131">RFC1155-SMI</span></span> | <span data-ttu-id="2c454-132">NetworkAddress, IpAddress, contador, medidor, timetiques, opaco</span><span class="sxs-lookup"><span data-stu-id="2c454-132">NetworkAddress, IpAddress, Counter, Gauge, TimeTicks, Opaque</span></span>        |
|              | <span data-ttu-id="2c454-133">RFC1213-MIB</span><span class="sxs-lookup"><span data-stu-id="2c454-133">RFC1213-MIB</span></span> | <span data-ttu-id="2c454-134">DisplayString, PhysAddress</span><span class="sxs-lookup"><span data-stu-id="2c454-134">DisplayString, PhysAddress</span></span>                                          |
| <span data-ttu-id="2c454-135">Macro ASN. 1</span><span class="sxs-lookup"><span data-stu-id="2c454-135">ASN.1 Macro</span></span>  | <span data-ttu-id="2c454-136">RFC-1212</span><span class="sxs-lookup"><span data-stu-id="2c454-136">RFC-1212</span></span>    | <span data-ttu-id="2c454-137">TIPO DE OBJETO</span><span class="sxs-lookup"><span data-stu-id="2c454-137">OBJECT-TYPE</span></span>                                                         |
|              | <span data-ttu-id="2c454-138">RFC-1215</span><span class="sxs-lookup"><span data-stu-id="2c454-138">RFC-1215</span></span>    | <span data-ttu-id="2c454-139">TIPO DE INTERCEPTAÇÃO</span><span class="sxs-lookup"><span data-stu-id="2c454-139">TRAP-TYPE</span></span>                                                           |



 

<span data-ttu-id="2c454-140">**IMPORTAÇÕES de SNMPv2C internas**</span><span class="sxs-lookup"><span data-stu-id="2c454-140">**Built-in SNMPv2C IMPORTS**</span></span>



| <span data-ttu-id="2c454-141">Classe de importação</span><span class="sxs-lookup"><span data-stu-id="2c454-141">Import Class</span></span>       | <span data-ttu-id="2c454-142">Módulo</span><span class="sxs-lookup"><span data-stu-id="2c454-142">Module</span></span>      | <span data-ttu-id="2c454-143">Instâncias</span><span class="sxs-lookup"><span data-stu-id="2c454-143">Instances</span></span>                                                                                                                                                                                                      |
|--------------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2c454-144">Valor ASN. 1</span><span class="sxs-lookup"><span data-stu-id="2c454-144">ASN.1 Value</span></span>        | <span data-ttu-id="2c454-145">SNMPv2-SMI</span><span class="sxs-lookup"><span data-stu-id="2c454-145">SNMPv2-SMI</span></span>  | <span data-ttu-id="2c454-146">org, DOD, Internet, diretório, gerenciamento, MiB-2, transmissão, experimental, privado, empresas, segurança, SNMPv2, snmpDomains, snmpProxys, snmpModules</span><span class="sxs-lookup"><span data-stu-id="2c454-146">org, dod, Internet, directory, mgmt, mib-2, transmission, experimental, private, enterprises, security, snmpv2, snmpDomains, snmpProxys, snmpModules</span></span>                                                           |
|                    | <span data-ttu-id="2c454-147">SNMPv2-TM</span><span class="sxs-lookup"><span data-stu-id="2c454-147">SNMPv2-TM</span></span>   | <span data-ttu-id="2c454-148">rfc1157Proxy</span><span class="sxs-lookup"><span data-stu-id="2c454-148">rfc1157Proxy</span></span>                                                                                                                                                                                                   |
| <span data-ttu-id="2c454-149">Identidade do objeto</span><span class="sxs-lookup"><span data-stu-id="2c454-149">Object Identity</span></span>    | <span data-ttu-id="2c454-150">SNMPv2-SMI</span><span class="sxs-lookup"><span data-stu-id="2c454-150">SNMPv2-SMI</span></span>  | <span data-ttu-id="2c454-151">zeroDotZero</span><span class="sxs-lookup"><span data-stu-id="2c454-151">zeroDotZero</span></span>                                                                                                                                                                                                    |
|                    | <span data-ttu-id="2c454-152">SNMPv2-TM</span><span class="sxs-lookup"><span data-stu-id="2c454-152">SNMPv2-TM</span></span>   | <span data-ttu-id="2c454-153">snmpUDPDomain, snmpCLNSDomain, smnpCONSDomain, snmpDDPDomain, snmpIPXDomain, rfc1157Domain</span><span class="sxs-lookup"><span data-stu-id="2c454-153">snmpUDPDomain, snmpCLNSDomain, smnpCONSDomain, snmpDDPDomain, snmpIPXDomain, rfc1157Domain</span></span>                                                                                                                     |
| <span data-ttu-id="2c454-154">Tipo ASN. 1</span><span class="sxs-lookup"><span data-stu-id="2c454-154">ASN.1 Type</span></span>         | <span data-ttu-id="2c454-155">SNMPv2-SMI</span><span class="sxs-lookup"><span data-stu-id="2c454-155">SNMPv2-SMI</span></span>  | <span data-ttu-id="2c454-156">Integer32, IpAddress, Counter32, timetiques, opaco, Counter64, Unsigned32, Gauge32</span><span class="sxs-lookup"><span data-stu-id="2c454-156">Integer32, IpAddress, Counter32, TimeTicks, Opaque, Counter64, Unsigned32, Gauge32</span></span>                                                                                                                             |
| <span data-ttu-id="2c454-157">Macro ASN. 1</span><span class="sxs-lookup"><span data-stu-id="2c454-157">ASN.1 Macro</span></span>        | <span data-ttu-id="2c454-158">SNMPv2-SMI</span><span class="sxs-lookup"><span data-stu-id="2c454-158">SNMPv2-SMI</span></span>  | <span data-ttu-id="2c454-159">MÓDULO-IDENTIDADE, OBJETO-IDENTIDADE, TIPO DE OBJETO, TIPO DE NOTIFICAÇÃO</span><span class="sxs-lookup"><span data-stu-id="2c454-159">MODULE-IDENTITY, OBJECT-IDENTITY, OBJECT-TYPE, NOTIFICATION-TYPE</span></span>                                                                                                                                               |
|                    | <span data-ttu-id="2c454-160">SNMPv2-CONF</span><span class="sxs-lookup"><span data-stu-id="2c454-160">SNMPv2-CONF</span></span> | <span data-ttu-id="2c454-161">GRUPO DE OBJETOS, NOTIFICAÇÃO-GRUPO, MÓDULO-CONFORMIDADE, RECURSOS DO AGENTE</span><span class="sxs-lookup"><span data-stu-id="2c454-161">OBJECT-GROUP, NOTIFICATION-GROUP, MODULE-COMPLIANCE, AGENT-CAPABILITIES</span></span>                                                                                                                                        |
|                    | <span data-ttu-id="2c454-162">SNMPv2-TC</span><span class="sxs-lookup"><span data-stu-id="2c454-162">SNMPv2-TC</span></span>   | <span data-ttu-id="2c454-163">CONVENÇÃO TEXTUAL</span><span class="sxs-lookup"><span data-stu-id="2c454-163">TEXTUAL-CONVENTION</span></span>                                                                                                                                                                                             |
| <span data-ttu-id="2c454-164">Convenção textual</span><span class="sxs-lookup"><span data-stu-id="2c454-164">Textual Convention</span></span> | <span data-ttu-id="2c454-165">SNMPv2-TC</span><span class="sxs-lookup"><span data-stu-id="2c454-165">SNMPv2-TC</span></span>   | <span data-ttu-id="2c454-166">DisplayString, PhysAddress, MacAddress, Verdadevalue, TestAndIncr, undeler, InstancePointer, VariablePointer, multipointr,, carimbo de data/hora, o-intervalo, DateAndTime, storagetype, Tdomain, Taddress</span><span class="sxs-lookup"><span data-stu-id="2c454-166">DisplayString, PhysAddress, MacAddress, TruthValue, TestAndIncr, AutonomousType, InstancePointer, VariablePointer, RowPointer, RowStatus, TimeStamp, TimeInterval, DateAndTime, StorageType, Tdomain, Taddress</span></span> |
|                    | <span data-ttu-id="2c454-167">SNMPv2-TM</span><span class="sxs-lookup"><span data-stu-id="2c454-167">SNMPv2-TM</span></span>   | <span data-ttu-id="2c454-168">SnmpUDPAddress, SnmpOSIAddress, SnmpNBPAddress, SnmpIPXAddress</span><span class="sxs-lookup"><span data-stu-id="2c454-168">SnmpUDPAddress, SnmpOSIAddress, SnmpNBPAddress, SnmpIPXAddress</span></span>                                                                                                                                                 |



 

## <a name="fatal-error-1032"></a><span data-ttu-id="2c454-169">Erro fatal 1032</span><span class="sxs-lookup"><span data-stu-id="2c454-169">Fatal Error 1032</span></span>

<dl> <dt>

<span data-ttu-id="2c454-170"><span id="_1032__Fatal_____fileName__line____Duplicate_value__value__in_enumeration_"></span><span id="_1032__fatal_____filename__line____duplicate_value__value__in_enumeration_"></span><span id="_1032__FATAL_____FILENAME__LINE____DUPLICATE_VALUE__VALUE__IN_ENUMERATION_"></span>**<1032,> fatal: " <fileName> linha de<\#>: valor duplicado <value> na enumeração"**</span><span class="sxs-lookup"><span data-stu-id="2c454-170"><span id="_1032__Fatal_____fileName__line____Duplicate_value__value__in_enumeration_"></span><span id="_1032__fatal_____filename__line____duplicate_value__value__in_enumeration_"></span><span id="_1032__FATAL_____FILENAME__LINE____DUPLICATE_VALUE__VALUE__IN_ENUMERATION_"></span>**<1032, Fatal>: "<fileName><line\#>: Duplicate value <value> in enumeration"**</span></span>
</dt> <dd>

<span data-ttu-id="2c454-171">Erro semântico de módulo em uma enumeração, específico para nenhum SNMPv1 nem o SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="2c454-171">Module semantic error in an enumeration, specific to neither SNMPv1 nor SNMPv2C.</span></span> <span data-ttu-id="2c454-172">Não deve haver nenhum valor duplicado.</span><span class="sxs-lookup"><span data-stu-id="2c454-172">There must not be any duplicate values.</span></span> <span data-ttu-id="2c454-173">O parâmetro de> de linha de <\# é a posição da recorrência do nome/valor.</span><span class="sxs-lookup"><span data-stu-id="2c454-173">The <line\#> parameter is the position of the recurrence of the name/value.</span></span>

</dd> </dl>

## <a name="fatal-error-1033"></a><span data-ttu-id="2c454-174">Erro fatal 1033</span><span class="sxs-lookup"><span data-stu-id="2c454-174">Fatal Error 1033</span></span>

<dl> <dt>

<span data-ttu-id="2c454-175"><span id="_1033__Fatal_____fileName__line____Duplicate_name__identifier__in_enumeration_"></span><span id="_1033__fatal_____filename__line____duplicate_name__identifier__in_enumeration_"></span><span id="_1033__FATAL_____FILENAME__LINE____DUPLICATE_NAME__IDENTIFIER__IN_ENUMERATION_"></span>**<1033,> fatal: " <fileName> linha de<\#>: nome duplicado <identifier> na enumeração"**</span><span class="sxs-lookup"><span data-stu-id="2c454-175"><span id="_1033__Fatal_____fileName__line____Duplicate_name__identifier__in_enumeration_"></span><span id="_1033__fatal_____filename__line____duplicate_name__identifier__in_enumeration_"></span><span id="_1033__FATAL_____FILENAME__LINE____DUPLICATE_NAME__IDENTIFIER__IN_ENUMERATION_"></span>**<1033, Fatal>: "<fileName><line\#>: Duplicate name <identifier> in enumeration"**</span></span>
</dt> <dd>

<span data-ttu-id="2c454-176">Erro semântico de módulo em uma enumeração, específico para nenhum SNMPv1 nem o SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="2c454-176">Module semantic error in an enumeration, specific to neither SNMPv1 nor SNMPv2C.</span></span> <span data-ttu-id="2c454-177">Não deve haver nenhum nome duplicado.</span><span class="sxs-lookup"><span data-stu-id="2c454-177">There must not be any duplicate names.</span></span> <span data-ttu-id="2c454-178">O parâmetro de> de linha de <\# é a posição da recorrência do nome/valor.</span><span class="sxs-lookup"><span data-stu-id="2c454-178">The <line\#> parameter is the position of the recurrence of the name/value.</span></span>

</dd> </dl>

## <a name="warning-1034"></a><span data-ttu-id="2c454-179">Aviso 1034</span><span class="sxs-lookup"><span data-stu-id="2c454-179">Warning 1034</span></span>

<dl> <dt>

<span data-ttu-id="2c454-180"><span id="_1034__Warning_____fileName__line____A_value_of_0_disallowed_in_an_enumeration_"></span><span id="_1034__warning_____filename__line____a_value_of_0_disallowed_in_an_enumeration_"></span><span id="_1034__WARNING_____FILENAME__LINE____A_VALUE_OF_0_DISALLOWED_IN_AN_ENUMERATION_"></span>**<1034, aviso>: " <fileName> linha \# de<>: um valor de 0 não permitido em uma enumeração"**</span><span class="sxs-lookup"><span data-stu-id="2c454-180"><span id="_1034__Warning_____fileName__line____A_value_of_0_disallowed_in_an_enumeration_"></span><span id="_1034__warning_____filename__line____a_value_of_0_disallowed_in_an_enumeration_"></span><span id="_1034__WARNING_____FILENAME__LINE____A_VALUE_OF_0_DISALLOWED_IN_AN_ENUMERATION_"></span>**<1034, Warning>: "<fileName><line\#>: A value of 0 disallowed in an enumeration"**</span></span>
</dt> <dd>

<span data-ttu-id="2c454-181">Aviso semântico de módulo em uma enumeração, específico para nem SNMPv1 nem SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="2c454-181">Module semantic warning in an enumeration, specific to neither SNMPv1 nor SNMPv2C.</span></span> <span data-ttu-id="2c454-182">É recomendável que um valor nomeado de zero não seja usado em uma enumeração.</span><span class="sxs-lookup"><span data-stu-id="2c454-182">It is recommended that a named value of zero not be used in an enumeration.</span></span>

</dd> </dl>

## <a name="warning-1036"></a><span data-ttu-id="2c454-183">Aviso 1036</span><span class="sxs-lookup"><span data-stu-id="2c454-183">Warning 1036</span></span>

<dl> <dt>

<span data-ttu-id="2c454-184"><span id="_1036__Warning____fileName__line____Value_in_enumeration_does_not_resolve_to_a_positive_integer_"></span><span id="_1036__warning____filename__line____value_in_enumeration_does_not_resolve_to_a_positive_integer_"></span><span id="_1036__WARNING____FILENAME__LINE____VALUE_IN_ENUMERATION_DOES_NOT_RESOLVE_TO_A_POSITIVE_INTEGER_"></span>**<1036, Warning> " <fileName><line \#>: o valor na enumeração não é resolvido para um inteiro positivo"**</span><span class="sxs-lookup"><span data-stu-id="2c454-184"><span id="_1036__Warning____fileName__line____Value_in_enumeration_does_not_resolve_to_a_positive_integer_"></span><span id="_1036__warning____filename__line____value_in_enumeration_does_not_resolve_to_a_positive_integer_"></span><span id="_1036__WARNING____FILENAME__LINE____VALUE_IN_ENUMERATION_DOES_NOT_RESOLVE_TO_A_POSITIVE_INTEGER_"></span>**<1036, Warning> "<fileName><line\#>: Value in enumeration does not resolve to a positive integer"**</span></span>
</dt> <dd>

<span data-ttu-id="2c454-185">Aviso semântico de módulo em uma enumeração, específico para nem SNMPv1 nem SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="2c454-185">Module semantic warning in an enumeration, specific to neither SNMPv1 nor SNMPv2C.</span></span> <span data-ttu-id="2c454-186">Um valor negativo não é permitido em uma enumeração.</span><span class="sxs-lookup"><span data-stu-id="2c454-186">A negative value is not allowed in an enumeration.</span></span>

</dd> </dl>

## <a name="fatal-error-1037"></a><span data-ttu-id="2c454-187">Erro fatal 1037</span><span class="sxs-lookup"><span data-stu-id="2c454-187">Fatal Error 1037</span></span>

<dl> <dt>

<span data-ttu-id="2c454-188"><span id="_1037__Fatal_____fileName__line____Identifier__identifier__does_not_resolve_to_OCTET_STRING_or_Opaque_types_"></span><span id="_1037__fatal_____filename__line____identifier__identifier__does_not_resolve_to_octet_string_or_opaque_types_"></span><span id="_1037__FATAL_____FILENAME__LINE____IDENTIFIER__IDENTIFIER__DOES_NOT_RESOLVE_TO_OCTET_STRING_OR_OPAQUE_TYPES_"></span>**<1037,> fatal: " <fileName><da linha \#>: <identifier> o identificador não é resolvido para a cadeia de caracteres de octeto ou tipos opacos"**</span><span class="sxs-lookup"><span data-stu-id="2c454-188"><span id="_1037__Fatal_____fileName__line____Identifier__identifier__does_not_resolve_to_OCTET_STRING_or_Opaque_types_"></span><span id="_1037__fatal_____filename__line____identifier__identifier__does_not_resolve_to_octet_string_or_opaque_types_"></span><span id="_1037__FATAL_____FILENAME__LINE____IDENTIFIER__IDENTIFIER__DOES_NOT_RESOLVE_TO_OCTET_STRING_OR_OPAQUE_TYPES_"></span>**<1037, Fatal>: "<fileName><line\#>: Identifier <identifier> does not resolve to OCTET STRING or Opaque types"**</span></span>
</dt> <dd>

<span data-ttu-id="2c454-189">Erro semântico de módulo em especificação de tamanho, específico para nem SNMPv1 nem SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="2c454-189">Module semantic error in SIZE specification, specific to neither SNMPv1 nor SNMPv2C.</span></span> <span data-ttu-id="2c454-190">O símbolo usado em uma especificação de tamanho deve ser resolvido para a cadeia de caracteres de OCTETO ou opaco.</span><span class="sxs-lookup"><span data-stu-id="2c454-190">The symbol used in a SIZE specification must resolve to OCTET STRING or Opaque.</span></span>

</dd> </dl>

## <a name="fatal-error-1038"></a><span data-ttu-id="2c454-191">Erro fatal 1038</span><span class="sxs-lookup"><span data-stu-id="2c454-191">Fatal Error 1038</span></span>

<dl> <dt>

<span data-ttu-id="2c454-192"><span id="_1038__Fatal_____fileName__line____Identifier__identifier__does_not_resolve_an_INTEGER_or_Gauge_type_"></span><span id="_1038__fatal_____filename__line____identifier__identifier__does_not_resolve_an_integer_or_gauge_type_"></span><span id="_1038__FATAL_____FILENAME__LINE____IDENTIFIER__IDENTIFIER__DOES_NOT_RESOLVE_AN_INTEGER_OR_GAUGE_TYPE_"></span>**<1038,> fatal: " <fileName> linha de<\#>: <identifier> o identificador não resolve um tipo de número inteiro ou de medidor"**</span><span class="sxs-lookup"><span data-stu-id="2c454-192"><span id="_1038__Fatal_____fileName__line____Identifier__identifier__does_not_resolve_an_INTEGER_or_Gauge_type_"></span><span id="_1038__fatal_____filename__line____identifier__identifier__does_not_resolve_an_integer_or_gauge_type_"></span><span id="_1038__FATAL_____FILENAME__LINE____IDENTIFIER__IDENTIFIER__DOES_NOT_RESOLVE_AN_INTEGER_OR_GAUGE_TYPE_"></span>**<1038, Fatal>: "<fileName><line\#>: Identifier <identifier> does not resolve an INTEGER or Gauge type"**</span></span>
</dt> <dd>

<span data-ttu-id="2c454-193">Erro semântico de módulo na especificação de intervalo.</span><span class="sxs-lookup"><span data-stu-id="2c454-193">Module semantic error in range specification.</span></span> <span data-ttu-id="2c454-194">Esse erro pode ocorrer em SNMPv1 ou SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="2c454-194">This error can occur in either SNMPv1 or SNMPv2C.</span></span>

<span data-ttu-id="2c454-195">No SNMPv1, o símbolo usado em uma especificação de intervalo deve ser resolvido para inteiro ou medidor.</span><span class="sxs-lookup"><span data-stu-id="2c454-195">In SNMPv1, the symbol used in a Range specification must resolve to INTEGER or Gauge.</span></span>

<span data-ttu-id="2c454-196">No SNMPv2C, o símbolo usado em uma especificação de intervalo deve ser resolvido para INTEGER, Gauge32, Integer32 ou Unsigned32.</span><span class="sxs-lookup"><span data-stu-id="2c454-196">In SNMPv2C, the symbol used in a Range specification must resolve to INTEGER, Gauge32, Integer32, or Unsigned32.</span></span>

</dd> </dl>

## <a name="fatal-error-1039"></a><span data-ttu-id="2c454-197">Erro fatal 1039</span><span class="sxs-lookup"><span data-stu-id="2c454-197">Fatal Error 1039</span></span>

<dl> <dt>

<span data-ttu-id="2c454-198"><span id="_1039__Fatal___fileName__line____Negative_value_used_in_SIZE_specification_"></span><span id="_1039__fatal___filename__line____negative_value_used_in_size_specification_"></span><span id="_1039__FATAL___FILENAME__LINE____NEGATIVE_VALUE_USED_IN_SIZE_SPECIFICATION_"></span>**<1039,> fatal: <fileName><linha \#>: valor negativo usado na especificação de tamanho "**</span><span class="sxs-lookup"><span data-stu-id="2c454-198"><span id="_1039__Fatal___fileName__line____Negative_value_used_in_SIZE_specification_"></span><span id="_1039__fatal___filename__line____negative_value_used_in_size_specification_"></span><span id="_1039__FATAL___FILENAME__LINE____NEGATIVE_VALUE_USED_IN_SIZE_SPECIFICATION_"></span>**<1039, Fatal>:<fileName><line\#>: Negative value used in SIZE specification"**</span></span>
</dt> <dd>

<span data-ttu-id="2c454-199">Erro semântico de módulo em especificação de tamanho, específico para nem SNMPv1 nem SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="2c454-199">Module semantic error in SIZE specification, specific to neither SNMPv1 nor SNMPv2C.</span></span> <span data-ttu-id="2c454-200">Qualquer valor usado na especificação do tamanho deve ser não negativo.</span><span class="sxs-lookup"><span data-stu-id="2c454-200">Any value used in specifying the SIZE must be non-negative.</span></span>

</dd> </dl>

## <a name="fatal-error-1040"></a><span data-ttu-id="2c454-201">Erro fatal 1040</span><span class="sxs-lookup"><span data-stu-id="2c454-201">Fatal Error 1040</span></span>

<dl> <dt>

<span data-ttu-id="2c454-202"><span id="_1040__Fatal_____fileName__line____Identifier__identifier__in_SIZE_specification_does_not_resolve_to_a_non-negative_integral_value_"></span><span id="_1040__fatal_____filename__line____identifier__identifier__in_size_specification_does_not_resolve_to_a_non-negative_integral_value_"></span><span id="_1040__FATAL_____FILENAME__LINE____IDENTIFIER__IDENTIFIER__IN_SIZE_SPECIFICATION_DOES_NOT_RESOLVE_TO_A_NON-NEGATIVE_INTEGRAL_VALUE_"></span>**<1040,> fatal: " <fileName><da linha \#>: <identifier> o identificador em especificação de tamanho não é resolvido para um valor integral não negativo"**</span><span class="sxs-lookup"><span data-stu-id="2c454-202"><span id="_1040__Fatal_____fileName__line____Identifier__identifier__in_SIZE_specification_does_not_resolve_to_a_non-negative_integral_value_"></span><span id="_1040__fatal_____filename__line____identifier__identifier__in_size_specification_does_not_resolve_to_a_non-negative_integral_value_"></span><span id="_1040__FATAL_____FILENAME__LINE____IDENTIFIER__IDENTIFIER__IN_SIZE_SPECIFICATION_DOES_NOT_RESOLVE_TO_A_NON-NEGATIVE_INTEGRAL_VALUE_"></span>**<1040, Fatal>: "<fileName><line\#>: Identifier <identifier> in SIZE specification does not resolve to a non-negative integral value"**</span></span>
</dt> <dd>

<span data-ttu-id="2c454-203">Erro semântico de módulo em especificação de intervalo ou de tamanho, específico para nem SNMPv1 nem SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="2c454-203">Module semantic error in range or size specification, specific to neither SNMPv1 nor SNMPv2C.</span></span> <span data-ttu-id="2c454-204">Qualquer símbolo usado para especificar um valor em uma especificação de tamanho é resolvido para um valor não negativo.</span><span class="sxs-lookup"><span data-stu-id="2c454-204">Any symbol used in specifying a value in a SIZE specification resolves to a non-negative value.</span></span>

</dd> </dl>

 

 



