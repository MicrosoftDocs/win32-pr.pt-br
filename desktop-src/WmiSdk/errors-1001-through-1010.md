---
description: Descreve os erros do provedor SNMP WMI 1001 a 1010.
ms.assetid: dbc0e062-6b2f-41b1-8d6a-ab2c37d2dd1f
ms.tgt_platform: multiple
title: Erros 1001 a 1010
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa10b83c660d617bdbf37b6f119e824bbba60616
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105793951"
---
# <a name="errors-1001-through-1010"></a><span data-ttu-id="de980-103">Erros 1001 a 1010</span><span class="sxs-lookup"><span data-stu-id="de980-103">Errors 1001 through 1010</span></span>

<span data-ttu-id="de980-104">Descreve os erros do provedor SNMP WMI 1001 a 1010.</span><span class="sxs-lookup"><span data-stu-id="de980-104">Describes WMI SNMP provider errors 1001 through 1010.</span></span>

[<span data-ttu-id="de980-105">Erro fatal 1001</span><span class="sxs-lookup"><span data-stu-id="de980-105">Fatal Error 1001</span></span>](#fatal-error-1001)

[<span data-ttu-id="de980-106">Erro fatal 1002</span><span class="sxs-lookup"><span data-stu-id="de980-106">Fatal Error 1002</span></span>](#fatal-error-1002)

[<span data-ttu-id="de980-107">Erro fatal 1003</span><span class="sxs-lookup"><span data-stu-id="de980-107">Fatal Error 1003</span></span>](#fatal-error-1003)

[<span data-ttu-id="de980-108">Aviso 1004</span><span class="sxs-lookup"><span data-stu-id="de980-108">Warning 1004</span></span>](#warning-1004)

[<span data-ttu-id="de980-109">Aviso 1005</span><span class="sxs-lookup"><span data-stu-id="de980-109">Warning 1005</span></span>](#warning-1005)

[<span data-ttu-id="de980-110">Erro fatal 1006</span><span class="sxs-lookup"><span data-stu-id="de980-110">Fatal Error 1006</span></span>](#fatal-error-1006)

[<span data-ttu-id="de980-111">Erro fatal 1008</span><span class="sxs-lookup"><span data-stu-id="de980-111">Fatal Error 1008</span></span>](#fatal-error-1008)

## <a name="fatal-error-1001"></a><span data-ttu-id="de980-112">Erro fatal 1001</span><span class="sxs-lookup"><span data-stu-id="de980-112">Fatal Error 1001</span></span>

<dl> <dt>

<span data-ttu-id="de980-113"><span id="_1001__Fatal_____fileName___line____SYNTAX_clause_of_OBJECT-TYPE_does_not_resolve_to_allowed_types_"></span><span id="_1001__fatal_____filename___line____syntax_clause_of_object-type_does_not_resolve_to_allowed_types_"></span><span id="_1001__FATAL_____FILENAME___LINE____SYNTAX_CLAUSE_OF_OBJECT-TYPE_DOES_NOT_RESOLVE_TO_ALLOWED_TYPES_"></span><1001, fatal>: " <fileName> : <linha \#>: a cláusula Syntax do tipo Object não é resolvida para tipos permitidos"</span><span class="sxs-lookup"><span data-stu-id="de980-113"><span id="_1001__Fatal_____fileName___line____SYNTAX_clause_of_OBJECT-TYPE_does_not_resolve_to_allowed_types_"></span><span id="_1001__fatal_____filename___line____syntax_clause_of_object-type_does_not_resolve_to_allowed_types_"></span><span id="_1001__FATAL_____FILENAME___LINE____SYNTAX_CLAUSE_OF_OBJECT-TYPE_DOES_NOT_RESOLVE_TO_ALLOWED_TYPES_"></span><1001, Fatal>: "<fileName>:<line\#>: SYNTAX clause of OBJECT-TYPE does not resolve to allowed types"</span></span>
</dt> <dd>

<span data-ttu-id="de980-114">Erro semântico do módulo de invocação de macro do tipo de objeto.</span><span class="sxs-lookup"><span data-stu-id="de980-114">OBJECT-TYPE macro invocation module semantic error.</span></span> <span data-ttu-id="de980-115">A cláusula de sintaxe da macro do tipo de objeto deve ser resolvida para um tipo ou subtipo, formado usando a especificação de tamanho ou intervalo que o SMI ou de SNMPv2C permite.</span><span class="sxs-lookup"><span data-stu-id="de980-115">The SYNTAX clause of the OBJECT-TYPE macro must resolve to a type or subtype, formed by using the SIZE or range specification that the SNMPv1 or SNMPv2C SMI allows.</span></span> <span data-ttu-id="de980-116">Se esse não for o caso, o erro fatal 1001 será relatado.</span><span class="sxs-lookup"><span data-stu-id="de980-116">If this is not the case, fatal error 1001 is reported.</span></span>

<span data-ttu-id="de980-117">Esse erro pode ocorrer durante a compilação de uma MIB ou do SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="de980-117">This error can occur when compiling either an SNMPv1 or SNMPv2C MIB.</span></span>

<span data-ttu-id="de980-118">Os tipos permitidos pelo SMI do SNMPv1 são:</span><span class="sxs-lookup"><span data-stu-id="de980-118">Types allowed by the SNMPv1 SMI are:</span></span>

-   <span data-ttu-id="de980-119">INTEGER</span><span class="sxs-lookup"><span data-stu-id="de980-119">INTEGER</span></span>
-   <span data-ttu-id="de980-120">NULO</span><span class="sxs-lookup"><span data-stu-id="de980-120">NULL</span></span>
-   <span data-ttu-id="de980-121">CADEIA DE CARACTERES DE OCTETO</span><span class="sxs-lookup"><span data-stu-id="de980-121">OCTET STRING</span></span>
-   <span data-ttu-id="de980-122">IDENTIFICADOR DE OBJETO</span><span class="sxs-lookup"><span data-stu-id="de980-122">OBJECT IDENTIFIER</span></span>
-   <span data-ttu-id="de980-123">NetworkAddress</span><span class="sxs-lookup"><span data-stu-id="de980-123">NetworkAddress</span></span>
-   <span data-ttu-id="de980-124">IpAddress</span><span class="sxs-lookup"><span data-stu-id="de980-124">IpAddress</span></span>
-   <span data-ttu-id="de980-125">Contador</span><span class="sxs-lookup"><span data-stu-id="de980-125">Counter</span></span>
-   <span data-ttu-id="de980-126">Medidor</span><span class="sxs-lookup"><span data-stu-id="de980-126">Gauge</span></span>
-   <span data-ttu-id="de980-127">TimeTicks</span><span class="sxs-lookup"><span data-stu-id="de980-127">TimeTicks</span></span>
-   <span data-ttu-id="de980-128">Opaco</span><span class="sxs-lookup"><span data-stu-id="de980-128">Opaque</span></span>
-   <span data-ttu-id="de980-129">DisplayString</span><span class="sxs-lookup"><span data-stu-id="de980-129">DisplayString</span></span>
-   <span data-ttu-id="de980-130">PhysAddress</span><span class="sxs-lookup"><span data-stu-id="de980-130">PhysAddress</span></span>

<span data-ttu-id="de980-131">Os tipos permitidos pelo SMI do SNMPv2C são:</span><span class="sxs-lookup"><span data-stu-id="de980-131">Types allowed by the SNMPv2C SMI are:</span></span>

-   <span data-ttu-id="de980-132">INTEGER</span><span class="sxs-lookup"><span data-stu-id="de980-132">INTEGER</span></span>
-   <span data-ttu-id="de980-133">CADEIA DE CARACTERES DE OCTETO</span><span class="sxs-lookup"><span data-stu-id="de980-133">OCTET STRING</span></span>
-   <span data-ttu-id="de980-134">IDENTIFICADOR DE OBJETO</span><span class="sxs-lookup"><span data-stu-id="de980-134">OBJECT IDENTIFIER</span></span>
-   <span data-ttu-id="de980-135">BITS</span><span class="sxs-lookup"><span data-stu-id="de980-135">BITS</span></span>
-   <span data-ttu-id="de980-136">Integer32</span><span class="sxs-lookup"><span data-stu-id="de980-136">Integer32</span></span>
-   <span data-ttu-id="de980-137">IpAddress</span><span class="sxs-lookup"><span data-stu-id="de980-137">IpAddress</span></span>
-   <span data-ttu-id="de980-138">Counter32</span><span class="sxs-lookup"><span data-stu-id="de980-138">Counter32</span></span>
-   <span data-ttu-id="de980-139">TimeTicks</span><span class="sxs-lookup"><span data-stu-id="de980-139">TimeTicks</span></span>
-   <span data-ttu-id="de980-140">Opaco</span><span class="sxs-lookup"><span data-stu-id="de980-140">Opaque</span></span>
-   <span data-ttu-id="de980-141">Counter64</span><span class="sxs-lookup"><span data-stu-id="de980-141">Counter64</span></span>
-   <span data-ttu-id="de980-142">Unsigned32</span><span class="sxs-lookup"><span data-stu-id="de980-142">Unsigned32</span></span>
-   <span data-ttu-id="de980-143">DisplayString</span><span class="sxs-lookup"><span data-stu-id="de980-143">DisplayString</span></span>
-   <span data-ttu-id="de980-144">PhysAddress</span><span class="sxs-lookup"><span data-stu-id="de980-144">PhysAddress</span></span>
-   <span data-ttu-id="de980-145">MacAddress</span><span class="sxs-lookup"><span data-stu-id="de980-145">MacAddress</span></span>
-   <span data-ttu-id="de980-146">Verdadevalue</span><span class="sxs-lookup"><span data-stu-id="de980-146">TruthValue</span></span>
-   <span data-ttu-id="de980-147">TestAndIncr</span><span class="sxs-lookup"><span data-stu-id="de980-147">TestAndIncr</span></span>
-   <span data-ttu-id="de980-148">Autônomo</span><span class="sxs-lookup"><span data-stu-id="de980-148">AutonomousType</span></span>
-   <span data-ttu-id="de980-149">InstancePointer</span><span class="sxs-lookup"><span data-stu-id="de980-149">InstancePointer</span></span>
-   <span data-ttu-id="de980-150">VariablePointer</span><span class="sxs-lookup"><span data-stu-id="de980-150">VariablePointer</span></span>
-   <span data-ttu-id="de980-151">Ponto de extremidade</span><span class="sxs-lookup"><span data-stu-id="de980-151">RowPointer</span></span>
-   <span data-ttu-id="de980-152">UserStatus</span><span class="sxs-lookup"><span data-stu-id="de980-152">RowStatus</span></span>
-   <span data-ttu-id="de980-153">TimeStamp</span><span class="sxs-lookup"><span data-stu-id="de980-153">TimeStamp</span></span>
-   <span data-ttu-id="de980-154">TimeInterval</span><span class="sxs-lookup"><span data-stu-id="de980-154">TimeInterval</span></span>
-   <span data-ttu-id="de980-155">DateAndTime</span><span class="sxs-lookup"><span data-stu-id="de980-155">DateAndTime</span></span>
-   <span data-ttu-id="de980-156">StorageType</span><span class="sxs-lookup"><span data-stu-id="de980-156">StorageType</span></span>
-   <span data-ttu-id="de980-157">Tdomain</span><span class="sxs-lookup"><span data-stu-id="de980-157">Tdomain</span></span>
-   <span data-ttu-id="de980-158">Taddress</span><span class="sxs-lookup"><span data-stu-id="de980-158">Taddress</span></span>

</dd> </dl>

## <a name="fatal-error-1002"></a><span data-ttu-id="de980-159">Erro fatal 1002</span><span class="sxs-lookup"><span data-stu-id="de980-159">Fatal Error 1002</span></span>

<dl> <dt>

<span data-ttu-id="de980-160"><span id="_1002__Fatal_____fileName___line____Invalid_ACCESS_clause__clause__"></span><span id="_1002__fatal_____filename___line____invalid_access_clause__clause__"></span><span id="_1002__FATAL_____FILENAME___LINE____INVALID_ACCESS_CLAUSE__CLAUSE__"></span><1002,> fatal: " <fileName> : <linha \#>: cláusula de acesso inválida <clause> "</span><span class="sxs-lookup"><span data-stu-id="de980-160"><span id="_1002__Fatal_____fileName___line____Invalid_ACCESS_clause__clause__"></span><span id="_1002__fatal_____filename___line____invalid_access_clause__clause__"></span><span id="_1002__FATAL_____FILENAME___LINE____INVALID_ACCESS_CLAUSE__CLAUSE__"></span><1002, Fatal>: "<fileName>:<line\#>: Invalid ACCESS clause <clause>"</span></span>
</dt> <dd>

<span data-ttu-id="de980-161">Erro semântico do módulo de invocação de macro do tipo de objeto.</span><span class="sxs-lookup"><span data-stu-id="de980-161">OBJECT-TYPE macro invocation module semantic error.</span></span> <span data-ttu-id="de980-162">Para SNMPv1, a cláusula de acesso da macro do tipo de objeto deve ser "somente leitura", "somente gravação", "leitura/gravação" ou "não acessível".</span><span class="sxs-lookup"><span data-stu-id="de980-162">For SNMPv1, the ACCESS clause of the OBJECT-TYPE macro must be "read-only," "write-only," "read/write," or "not-accessible."</span></span>

<span data-ttu-id="de980-163">Para o SNMPv2C, a cláusula MAX-ACCESS deve ser "somente leitura", "leitura-criação", "leitura/gravação" ou "não acessível".</span><span class="sxs-lookup"><span data-stu-id="de980-163">For SNMPv2C, the MAX-ACCESS clause must be "read-only," "read-create," "read/write," or "not-accessible."</span></span>

</dd> </dl>

## <a name="fatal-error-1003"></a><span data-ttu-id="de980-164">Erro fatal 1003</span><span class="sxs-lookup"><span data-stu-id="de980-164">Fatal Error 1003</span></span>

<dl> <dt>

<span data-ttu-id="de980-165"><span id="_1003__Fatal_____fileName___line____Invalid_STATUS_clause__clause__"></span><span id="_1003__fatal_____filename___line____invalid_status_clause__clause__"></span><span id="_1003__FATAL_____FILENAME___LINE____INVALID_STATUS_CLAUSE__CLAUSE__"></span><1003,> fatal: " <fileName> : <linha \#>: cláusula status inválida <clause> "</span><span class="sxs-lookup"><span data-stu-id="de980-165"><span id="_1003__Fatal_____fileName___line____Invalid_STATUS_clause__clause__"></span><span id="_1003__fatal_____filename___line____invalid_status_clause__clause__"></span><span id="_1003__FATAL_____FILENAME___LINE____INVALID_STATUS_CLAUSE__CLAUSE__"></span><1003, Fatal>: "<fileName>:<line\#>: Invalid STATUS clause <clause>"</span></span>
</dt> <dd>

<span data-ttu-id="de980-166">Erro semântico do módulo de invocação de macro do tipo de objeto.</span><span class="sxs-lookup"><span data-stu-id="de980-166">OBJECT-TYPE macro invocation module semantic error.</span></span> <span data-ttu-id="de980-167">Para SNMPv1, a cláusula STATUS de uma chamada de macro de tipo de objeto deve ser "obrigatória", "opcional," "obsoleto" ou "preterido".</span><span class="sxs-lookup"><span data-stu-id="de980-167">For SNMPv1, the STATUS clause of an OBJECT-TYPE macro invocation must be "mandatory," "optional," "obsolete," or "deprecated."</span></span>

<span data-ttu-id="de980-168">Para o SNMPv2C, a cláusula STATUS de uma chamada de macro de tipo de objeto deve ser "Current", "preterido" ou "obsoleto".</span><span class="sxs-lookup"><span data-stu-id="de980-168">For SNMPv2C, the STATUS clause of an OBJECT-TYPE macro invocation must be "current," "deprecated," or "obsolete."</span></span>

</dd> </dl>

## <a name="warning-1004"></a><span data-ttu-id="de980-169">Aviso 1004</span><span class="sxs-lookup"><span data-stu-id="de980-169">Warning 1004</span></span>

<dl> <dt>

<span data-ttu-id="de980-170"><span id="_1004__Warning_____fileName___line____OBJECT-TYPE__identifier___whose_syntax_resolves_to_one_of_the_Counter_types_does_not_end_with_the_letter__s___"></span><span id="_1004__warning_____filename___line____object-type__identifier___whose_syntax_resolves_to_one_of_the_counter_types_does_not_end_with_the_letter__s___"></span><span id="_1004__WARNING_____FILENAME___LINE____OBJECT-TYPE__IDENTIFIER___WHOSE_SYNTAX_RESOLVES_TO_ONE_OF_THE_COUNTER_TYPES_DOES_NOT_END_WITH_THE_LETTER__S___"></span><1004, aviso>: " <fileName> : <linha \#>: tipo de objeto <identifier> , cuja sintaxe resolve para um dos tipos de contadores não termina com a letra '"</span><span class="sxs-lookup"><span data-stu-id="de980-170"><span id="_1004__Warning_____fileName___line____OBJECT-TYPE__identifier___whose_syntax_resolves_to_one_of_the_Counter_types_does_not_end_with_the_letter__s___"></span><span id="_1004__warning_____filename___line____object-type__identifier___whose_syntax_resolves_to_one_of_the_counter_types_does_not_end_with_the_letter__s___"></span><span id="_1004__WARNING_____FILENAME___LINE____OBJECT-TYPE__IDENTIFIER___WHOSE_SYNTAX_RESOLVES_TO_ONE_OF_THE_COUNTER_TYPES_DOES_NOT_END_WITH_THE_LETTER__S___"></span><1004, Warning>: "<fileName>:<line\#>: OBJECT-TYPE <identifier>, whose syntax resolves to one of the Counter types does not end with the letter 's' "</span></span>
</dt> <dd>

<span data-ttu-id="de980-171">Aviso semântico do módulo de invocação de macro do tipo de objeto.</span><span class="sxs-lookup"><span data-stu-id="de980-171">OBJECT-TYPE macro invocation module semantic warning.</span></span> <span data-ttu-id="de980-172">O identificador de um objeto do contador de sintaxe (SNMPv1) ou Counter32 e Counter64 (SNMPv2C) deve ser plural.</span><span class="sxs-lookup"><span data-stu-id="de980-172">The identifier for an object of SYNTAX Counter (SNMPv1) or Counter32 and Counter64 (SNMPv2C) must be plural.</span></span>

<span data-ttu-id="de980-173">Esse aviso pode ocorrer durante a compilação de uma MIB ou do SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="de980-173">This warning can occur when compiling either an SNMPv1 or SNMPv2C MIB.</span></span>

</dd> </dl>

## <a name="warning-1005"></a><span data-ttu-id="de980-174">Aviso 1005</span><span class="sxs-lookup"><span data-stu-id="de980-174">Warning 1005</span></span>

<dl> <dt>

<span data-ttu-id="de980-175"><span id="_1005__Warning_____fileName___line____OBJECT-TYPE_with_SYNTAX__SEQUENCE_OF___should_have_an_ACCESS_clause__not-accessible_"></span><span id="_1005__warning_____filename___line____object-type_with_syntax__sequence_of___should_have_an_access_clause__not-accessible_"></span><span id="_1005__WARNING_____FILENAME___LINE____OBJECT-TYPE_WITH_SYNTAX__SEQUENCE_OF___SHOULD_HAVE_AN_ACCESS_CLAUSE__NOT-ACCESSIBLE_"></span><1005, aviso>: " <fileName> : <linha \#>: tipo de objeto com sintaxe" Sequence of ", deve ter uma cláusula de acesso" não acessível "</span><span class="sxs-lookup"><span data-stu-id="de980-175"><span id="_1005__Warning_____fileName___line____OBJECT-TYPE_with_SYNTAX__SEQUENCE_OF___should_have_an_ACCESS_clause__not-accessible_"></span><span id="_1005__warning_____filename___line____object-type_with_syntax__sequence_of___should_have_an_access_clause__not-accessible_"></span><span id="_1005__WARNING_____FILENAME___LINE____OBJECT-TYPE_WITH_SYNTAX__SEQUENCE_OF___SHOULD_HAVE_AN_ACCESS_CLAUSE__NOT-ACCESSIBLE_"></span><1005, Warning>: "<fileName>:<line\#>: OBJECT-TYPE with SYNTAX "SEQUENCE OF", should have an ACCESS clause "not-accessible"</span></span>
</dt> <dd>

<span data-ttu-id="de980-176">Aviso semântico do módulo de invocação de macro do tipo de objeto.</span><span class="sxs-lookup"><span data-stu-id="de980-176">OBJECT-TYPE macro invocation module semantic warning.</span></span> <span data-ttu-id="de980-177">Uma tabela ou linha conceitual (sequência ou tipos de objetos de sequência, respectivamente) deve ser "não acessível".</span><span class="sxs-lookup"><span data-stu-id="de980-177">A table or conceptual row (SEQUENCE OF or SEQUENCE object types, respectively) must be "not-accessible."</span></span>

<span data-ttu-id="de980-178">Esse aviso pode ocorrer em SNMPv1 ou SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="de980-178">This warning can occur in either SNMPv1 or SNMPv2C.</span></span>

</dd> </dl>

## <a name="fatal-error-1006"></a><span data-ttu-id="de980-179">Erro fatal 1006</span><span class="sxs-lookup"><span data-stu-id="de980-179">Fatal Error 1006</span></span>

<dl> <dt>

<span data-ttu-id="de980-180"><span id="_1006__Fatal_____fileName___line___OBJECT-TYPE__identifier___which_is_of_SYNTAX_SEQUENCE__does_not_have_an_INDEX_or_AUGMENTS_clause_"></span><span id="_1006__fatal_____filename___line___object-type__identifier___which_is_of_syntax_sequence__does_not_have_an_index_or_augments_clause_"></span><span id="_1006__FATAL_____FILENAME___LINE___OBJECT-TYPE__IDENTIFIER___WHICH_IS_OF_SYNTAX_SEQUENCE__DOES_NOT_HAVE_AN_INDEX_OR_AUGMENTS_CLAUSE_"></span><1006, fatal>: " <fileName> : linha \# de <> tipo de objeto <identifier> , que é da sequência de sintaxe, não tem um índice ou uma cláusula de aumentos"</span><span class="sxs-lookup"><span data-stu-id="de980-180"><span id="_1006__Fatal_____fileName___line___OBJECT-TYPE__identifier___which_is_of_SYNTAX_SEQUENCE__does_not_have_an_INDEX_or_AUGMENTS_clause_"></span><span id="_1006__fatal_____filename___line___object-type__identifier___which_is_of_syntax_sequence__does_not_have_an_index_or_augments_clause_"></span><span id="_1006__FATAL_____FILENAME___LINE___OBJECT-TYPE__IDENTIFIER___WHICH_IS_OF_SYNTAX_SEQUENCE__DOES_NOT_HAVE_AN_INDEX_OR_AUGMENTS_CLAUSE_"></span><1006, Fatal>: "<fileName>:<line\#> OBJECT-TYPE <identifier>, which is of SYNTAX SEQUENCE, does not have an INDEX or AUGMENTS clause"</span></span>
</dt> <dd>

<span data-ttu-id="de980-181">Erro semântico do módulo de invocação de macro do tipo de objeto.</span><span class="sxs-lookup"><span data-stu-id="de980-181">OBJECT-TYPE macro invocation module semantic error.</span></span> <span data-ttu-id="de980-182">Para SNMPv1, a cláusula INDEX deve estar presente para uma definição de tipo de objeto cuja sintaxe seja resolvida para um tipo de sequência.</span><span class="sxs-lookup"><span data-stu-id="de980-182">For SNMPv1, the INDEX clause must be present for an OBJECT-TYPE definition whose SYNTAX resolves to a SEQUENCE type.</span></span>

<span data-ttu-id="de980-183">Para o SNMPv2C, a cláusula de índice ou de AUMENTOs deve estar presente para uma declaração de linha conceitual.</span><span class="sxs-lookup"><span data-stu-id="de980-183">For SNMPv2C, either the INDEX or the AUGMENTS clause must be present for a conceptual row declaration.</span></span>

</dd> </dl>

## <a name="fatal-error-1008"></a><span data-ttu-id="de980-184">Erro fatal 1008</span><span class="sxs-lookup"><span data-stu-id="de980-184">Fatal Error 1008</span></span>

<dl> <dt>

<span data-ttu-id="de980-185"><span id="_1008__Fatal_____fileName___line____OBJECT-TYPE__identifier___which_is_of_SYNTAX__SEQUENCE__has_not_been_referenced_"></span><span id="_1008__fatal_____filename___line____object-type__identifier___which_is_of_syntax__sequence__has_not_been_referenced_"></span><span id="_1008__FATAL_____FILENAME___LINE____OBJECT-TYPE__IDENTIFIER___WHICH_IS_OF_SYNTAX__SEQUENCE__HAS_NOT_BEEN_REFERENCED_"></span><1008, fatal>: " <fileName> : <linha \#>: tipo de objeto <identifier> , que é da sintaxe" Sequence "não foi referenciada"</span><span class="sxs-lookup"><span data-stu-id="de980-185"><span id="_1008__Fatal_____fileName___line____OBJECT-TYPE__identifier___which_is_of_SYNTAX__SEQUENCE__has_not_been_referenced_"></span><span id="_1008__fatal_____filename___line____object-type__identifier___which_is_of_syntax__sequence__has_not_been_referenced_"></span><span id="_1008__FATAL_____FILENAME___LINE____OBJECT-TYPE__IDENTIFIER___WHICH_IS_OF_SYNTAX__SEQUENCE__HAS_NOT_BEEN_REFERENCED_"></span><1008, Fatal>: "<fileName>:<line\#>: OBJECT-TYPE <identifier>, which is of SYNTAX "SEQUENCE" has not been referenced"</span></span>
</dt> <dd>

<span data-ttu-id="de980-186">Erro semântico do módulo de invocação de macro do tipo de objeto.</span><span class="sxs-lookup"><span data-stu-id="de980-186">OBJECT-TYPE macro invocation module semantic error.</span></span> <span data-ttu-id="de980-187">Um tipo de objeto com a cláusula SYNTAX como um tipo de sequência deve ser exibido na cláusula SYNTAX de exatamente uma invocação de tipo de objeto que significa uma declaração de tabela, ou seja, um objeto com a cláusula SYNTAX como uma sequência do tipo.</span><span class="sxs-lookup"><span data-stu-id="de980-187">An OBJECT-TYPE with the SYNTAX clause as a SEQUENCE type must figure in the SYNTAX clause of exactly one OBJECT-TYPE invocation that stands for a table declaration, that is, an object with the SYNTAX clause as a SEQUENCE OF type.</span></span> <span data-ttu-id="de980-188">O parâmetro de> de linha de <\# refere-se ao segundo ponto de referência.</span><span class="sxs-lookup"><span data-stu-id="de980-188">The <line\#> parameter refers to the second point of reference.</span></span>

<span data-ttu-id="de980-189">Esse erro pode ocorrer em SNMPv1 ou SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="de980-189">This error can occur in either SNMPv1 or SNMPv2C.</span></span>

</dd> </dl>

 

 



