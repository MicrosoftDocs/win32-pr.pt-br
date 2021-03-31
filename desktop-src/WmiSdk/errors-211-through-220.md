---
description: Descreve os erros do provedor SNMP WMI 211 a 220.
ms.assetid: beaa644d-51b3-4a57-8853-0b37f69f615a
ms.tgt_platform: multiple
title: Erros 211 a 220
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f25dbf8cb8f27d4c58a1505176eca218b8d947d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103663133"
---
# <a name="errors-211-through-220"></a><span data-ttu-id="eb287-103">Erros 211 a 220</span><span class="sxs-lookup"><span data-stu-id="eb287-103">Errors 211 through 220</span></span>

<span data-ttu-id="eb287-104">Descreve os erros do provedor SNMP WMI 211 a 220.</span><span class="sxs-lookup"><span data-stu-id="eb287-104">Describes WMI SNMP provider errors 211 through 220.</span></span>

[<span data-ttu-id="eb287-105">Mensagem de informação 211</span><span class="sxs-lookup"><span data-stu-id="eb287-105">Information Message 211</span></span>](#information-message-211)

[<span data-ttu-id="eb287-106">Erro fatal 212</span><span class="sxs-lookup"><span data-stu-id="eb287-106">Fatal Error 212</span></span>](#fatal-error-212)

[<span data-ttu-id="eb287-107">Erro fatal 213</span><span class="sxs-lookup"><span data-stu-id="eb287-107">Fatal Error 213</span></span>](#fatal-error-213)

[<span data-ttu-id="eb287-108">Erro fatal 214</span><span class="sxs-lookup"><span data-stu-id="eb287-108">Fatal Error 214</span></span>](#fatal-error-214)

[<span data-ttu-id="eb287-109">Erro fatal 215</span><span class="sxs-lookup"><span data-stu-id="eb287-109">Fatal Error 215</span></span>](#fatal-error-215)

[<span data-ttu-id="eb287-110">Erro fatal 216</span><span class="sxs-lookup"><span data-stu-id="eb287-110">Fatal Error 216</span></span>](#fatal-error-216)

[<span data-ttu-id="eb287-111">Erro fatal 217</span><span class="sxs-lookup"><span data-stu-id="eb287-111">Fatal Error 217</span></span>](#fatal-error-217)

[<span data-ttu-id="eb287-112">Erro fatal 218</span><span class="sxs-lookup"><span data-stu-id="eb287-112">Fatal Error 218</span></span>](#fatal-error-218)

[<span data-ttu-id="eb287-113">Erro fatal 219</span><span class="sxs-lookup"><span data-stu-id="eb287-113">Fatal Error 219</span></span>](#fatal-error-219)

[<span data-ttu-id="eb287-114">Erro fatal 220</span><span class="sxs-lookup"><span data-stu-id="eb287-114">Fatal Error 220</span></span>](#fatal-error-220)

## <a name="information-message-211"></a><span data-ttu-id="eb287-115">Mensagem de informação 211</span><span class="sxs-lookup"><span data-stu-id="eb287-115">Information Message 211</span></span>

<dl> <dt>

<span data-ttu-id="eb287-116"><span id="_211__Information____Skipping_TRAP-TYPE__identifier__"></span><span id="_211__information____skipping_trap-type__identifier__"></span><span id="_211__INFORMATION____SKIPPING_TRAP-TYPE__IDENTIFIER__"></span>**<211, informações>: "ignorando tipo de INTERCEPTAção <identifier> "**</span><span class="sxs-lookup"><span data-stu-id="eb287-116"><span id="_211__Information____Skipping_TRAP-TYPE__identifier__"></span><span id="_211__information____skipping_trap-type__identifier__"></span><span id="_211__INFORMATION____SKIPPING_TRAP-TYPE__IDENTIFIER__"></span>**<211, Information>: "Skipping TRAP-TYPE <identifier>"**</span></span>
</dt> <dd>

<span data-ttu-id="eb287-117">Quaisquer erros na definição de tipo de INTERCEPTAção geram essa mensagem.</span><span class="sxs-lookup"><span data-stu-id="eb287-117">Any errors in the TRAP-TYPE definition generate this message.</span></span>

</dd> </dl>

## <a name="fatal-error-212"></a><span data-ttu-id="eb287-118">Erro fatal 212</span><span class="sxs-lookup"><span data-stu-id="eb287-118">Fatal Error 212</span></span>

<dl> <dt>

<span data-ttu-id="eb287-119"><span id="_212__Fatal_____fileName___line____Syntax_Error_in_SEQUENCE_definition._Last_token_read_is__token__"></span><span id="_212__fatal_____filename___line____syntax_error_in_sequence_definition._last_token_read_is__token__"></span><span id="_212__FATAL_____FILENAME___LINE____SYNTAX_ERROR_IN_SEQUENCE_DEFINITION._LAST_TOKEN_READ_IS__TOKEN__"></span>**<212,> fatal: " <fileName> : <linha \#>: erro de sintaxe na definição de sequência. O último token lido é <token> "**</span><span class="sxs-lookup"><span data-stu-id="eb287-119"><span id="_212__Fatal_____fileName___line____Syntax_Error_in_SEQUENCE_definition._Last_token_read_is__token__"></span><span id="_212__fatal_____filename___line____syntax_error_in_sequence_definition._last_token_read_is__token__"></span><span id="_212__FATAL_____FILENAME___LINE____SYNTAX_ERROR_IN_SEQUENCE_DEFINITION._LAST_TOKEN_READ_IS__TOKEN__"></span>**<212, Fatal>: "<fileName>:<line\#>: Syntax Error in SEQUENCE definition. Last token read is <token>"**</span></span>
</dt> <dd>

<span data-ttu-id="eb287-120">Erro de sintaxe do módulo na atribuição de tipo.</span><span class="sxs-lookup"><span data-stu-id="eb287-120">Module syntax error in type assignment.</span></span> <span data-ttu-id="eb287-121">Há um erro entre as chaves esquerda e direita de uma construção de sequência, que resulta em um erro de sintaxe em uma atribuição de tipo MIB.</span><span class="sxs-lookup"><span data-stu-id="eb287-121">There is an error between the left and right braces of a SEQUENCE construct, which amounts to a syntax error in a MIB type assignment.</span></span>

</dd> </dl>

## <a name="fatal-error-213"></a><span data-ttu-id="eb287-122">Erro fatal 213</span><span class="sxs-lookup"><span data-stu-id="eb287-122">Fatal Error 213</span></span>

<dl> <dt>

<span data-ttu-id="eb287-123"><span id="_213__Fatal_____fileName___line____Syntax_Error_in_Object_Identifier_value._Last_token_read_is__token__"></span><span id="_213__fatal_____filename___line____syntax_error_in_object_identifier_value._last_token_read_is__token__"></span><span id="_213__FATAL_____FILENAME___LINE____SYNTAX_ERROR_IN_OBJECT_IDENTIFIER_VALUE._LAST_TOKEN_READ_IS__TOKEN__"></span>**<213,> fatal: " <fileName> : <linha \#>: erro de sintaxe no valor do identificador de objeto. O último token lido é <token> "**</span><span class="sxs-lookup"><span data-stu-id="eb287-123"><span id="_213__Fatal_____fileName___line____Syntax_Error_in_Object_Identifier_value._Last_token_read_is__token__"></span><span id="_213__fatal_____filename___line____syntax_error_in_object_identifier_value._last_token_read_is__token__"></span><span id="_213__FATAL_____FILENAME___LINE____SYNTAX_ERROR_IN_OBJECT_IDENTIFIER_VALUE._LAST_TOKEN_READ_IS__TOKEN__"></span>**<213, Fatal>: "<fileName>:<line\#>: Syntax Error in Object Identifier value. Last token read is <token>"**</span></span>
</dt> <dd>

<span data-ttu-id="eb287-124">Erro de sintaxe do módulo na atribuição de valor.</span><span class="sxs-lookup"><span data-stu-id="eb287-124">Module syntax error in value assignment.</span></span> <span data-ttu-id="eb287-125">Há um erro entre as chaves esquerda e direita de um valor de identificador de objeto.</span><span class="sxs-lookup"><span data-stu-id="eb287-125">There is an error between the left and right braces of an object identifier value.</span></span>

</dd> </dl>

## <a name="fatal-error-214"></a><span data-ttu-id="eb287-126">Erro fatal 214</span><span class="sxs-lookup"><span data-stu-id="eb287-126">Fatal Error 214</span></span>

<dl> <dt>

<span data-ttu-id="eb287-127"><span id="_214__Fatal_____fileName___line____Syntax_Error_in_the_list_of_symbols_in_IMPORTS._Last_token_read_is__token__"></span><span id="_214__fatal_____filename___line____syntax_error_in_the_list_of_symbols_in_imports._last_token_read_is__token__"></span><span id="_214__FATAL_____FILENAME___LINE____SYNTAX_ERROR_IN_THE_LIST_OF_SYMBOLS_IN_IMPORTS._LAST_TOKEN_READ_IS__TOKEN__"></span>**<214,> fatal: " <fileName> : <linha \#>: erro de sintaxe na lista de símbolos em importações. O último token lido é <token> "**</span><span class="sxs-lookup"><span data-stu-id="eb287-127"><span id="_214__Fatal_____fileName___line____Syntax_Error_in_the_list_of_symbols_in_IMPORTS._Last_token_read_is__token__"></span><span id="_214__fatal_____filename___line____syntax_error_in_the_list_of_symbols_in_imports._last_token_read_is__token__"></span><span id="_214__FATAL_____FILENAME___LINE____SYNTAX_ERROR_IN_THE_LIST_OF_SYMBOLS_IN_IMPORTS._LAST_TOKEN_READ_IS__TOKEN__"></span>**<214, Fatal>: "<fileName>:<line\#>: Syntax Error in the list of symbols in IMPORTS. Last token read is <token>"**</span></span>
</dt> <dd>

<span data-ttu-id="eb287-128">Erro de sintaxe do módulo na seção Imports.</span><span class="sxs-lookup"><span data-stu-id="eb287-128">Module syntax error in the IMPORTS section.</span></span>

</dd> </dl>

## <a name="fatal-error-215"></a><span data-ttu-id="eb287-129">Erro fatal 215</span><span class="sxs-lookup"><span data-stu-id="eb287-129">Fatal Error 215</span></span>

<dl> <dt>

<span data-ttu-id="eb287-130"><span id="_215__Fatal_____fileName___line____Syntax_Error_in_IMPORTS__missing_module_name__._Last_token_read_is__token__"></span><span id="_215__fatal_____filename___line____syntax_error_in_imports__missing_module_name__._last_token_read_is__token__"></span><span id="_215__FATAL_____FILENAME___LINE____SYNTAX_ERROR_IN_IMPORTS__MISSING_MODULE_NAME__._LAST_TOKEN_READ_IS__TOKEN__"></span>**<215, fatal>: " <fileName> : <linha \#>: erro de sintaxe em Imports (nome de módulo ausente?). O último token lido é <token> "**</span><span class="sxs-lookup"><span data-stu-id="eb287-130"><span id="_215__Fatal_____fileName___line____Syntax_Error_in_IMPORTS__missing_module_name__._Last_token_read_is__token__"></span><span id="_215__fatal_____filename___line____syntax_error_in_imports__missing_module_name__._last_token_read_is__token__"></span><span id="_215__FATAL_____FILENAME___LINE____SYNTAX_ERROR_IN_IMPORTS__MISSING_MODULE_NAME__._LAST_TOKEN_READ_IS__TOKEN__"></span>**<215, Fatal>: "<fileName>:<line\#>: Syntax Error in IMPORTS (missing module name?). Last token read is <token>"**</span></span>
</dt> <dd>

<span data-ttu-id="eb287-131">Erro de sintaxe do módulo na seção Imports.</span><span class="sxs-lookup"><span data-stu-id="eb287-131">Module syntax error in the IMPORTS section.</span></span>

</dd> </dl>

## <a name="fatal-error-216"></a><span data-ttu-id="eb287-132">Erro fatal 216</span><span class="sxs-lookup"><span data-stu-id="eb287-132">Fatal Error 216</span></span>

<dl> <dt>

<span data-ttu-id="eb287-133"><span id="_216__Fatal_____fileName___line____Syntax_Error_in_the_IMPORTS_section._Last_token_read_is__token__"></span><span id="_216__fatal_____filename___line____syntax_error_in_the_imports_section._last_token_read_is__token__"></span><span id="_216__FATAL_____FILENAME___LINE____SYNTAX_ERROR_IN_THE_IMPORTS_SECTION._LAST_TOKEN_READ_IS__TOKEN__"></span>**<216,> fatal: " <fileName> : <linha \#>: erro de sintaxe na seção Imports. O último token lido é <token> "**</span><span class="sxs-lookup"><span data-stu-id="eb287-133"><span id="_216__Fatal_____fileName___line____Syntax_Error_in_the_IMPORTS_section._Last_token_read_is__token__"></span><span id="_216__fatal_____filename___line____syntax_error_in_the_imports_section._last_token_read_is__token__"></span><span id="_216__FATAL_____FILENAME___LINE____SYNTAX_ERROR_IN_THE_IMPORTS_SECTION._LAST_TOKEN_READ_IS__TOKEN__"></span>**<216, Fatal>: "<fileName>:<line\#>: Syntax Error in the IMPORTS section. Last token read is <token>"**</span></span>
</dt> <dd>

<span data-ttu-id="eb287-134">Erro de sintaxe do módulo na seção Imports.</span><span class="sxs-lookup"><span data-stu-id="eb287-134">Module syntax error in the IMPORTS section.</span></span>

</dd> </dl>

## <a name="fatal-error-217"></a><span data-ttu-id="eb287-135">Erro fatal 217</span><span class="sxs-lookup"><span data-stu-id="eb287-135">Fatal Error 217</span></span>

<dl> <dt>

<span data-ttu-id="eb287-136"><span id="_217__Fatal_____fileName___line____Syntax_error_in_INTEGER_Enumeration._Last_token_read_is__token__"></span><span id="_217__fatal_____filename___line____syntax_error_in_integer_enumeration._last_token_read_is__token__"></span><span id="_217__FATAL_____FILENAME___LINE____SYNTAX_ERROR_IN_INTEGER_ENUMERATION._LAST_TOKEN_READ_IS__TOKEN__"></span>**<217,> fatal: " <fileName> : <linha \#>: erro de sintaxe em enumeração de inteiros. O último token lido é <token> "**</span><span class="sxs-lookup"><span data-stu-id="eb287-136"><span id="_217__Fatal_____fileName___line____Syntax_error_in_INTEGER_Enumeration._Last_token_read_is__token__"></span><span id="_217__fatal_____filename___line____syntax_error_in_integer_enumeration._last_token_read_is__token__"></span><span id="_217__FATAL_____FILENAME___LINE____SYNTAX_ERROR_IN_INTEGER_ENUMERATION._LAST_TOKEN_READ_IS__TOKEN__"></span>**<217, Fatal>: "<fileName>:<line\#>: Syntax error in INTEGER Enumeration. Last token read is <token>"**</span></span>
</dt> <dd>

<span data-ttu-id="eb287-137">Qualquer erro de sintaxe de módulo entre as chaves esquerda e direita de uma definição de enumeração MIB gera essa mensagem.</span><span class="sxs-lookup"><span data-stu-id="eb287-137">Any module syntax error between the left and right braces of a MIB enumeration definition generates this message.</span></span>

</dd> </dl>

## <a name="fatal-error-218"></a><span data-ttu-id="eb287-138">Erro fatal 218</span><span class="sxs-lookup"><span data-stu-id="eb287-138">Fatal Error 218</span></span>

<dl> <dt>

<span data-ttu-id="eb287-139"><span id="_218__Fatal_____fileName___line____Syntax_Error_in_sub-type_specification._Last_token_read_is__token__"></span><span id="_218__fatal_____filename___line____syntax_error_in_sub-type_specification._last_token_read_is__token__"></span><span id="_218__FATAL_____FILENAME___LINE____SYNTAX_ERROR_IN_SUB-TYPE_SPECIFICATION._LAST_TOKEN_READ_IS__TOKEN__"></span>**<218, fatal>: " <fileName> : <linha \#>: erro de sintaxe em especificação de subtipo. O último token lido é <token> "**</span><span class="sxs-lookup"><span data-stu-id="eb287-139"><span id="_218__Fatal_____fileName___line____Syntax_Error_in_sub-type_specification._Last_token_read_is__token__"></span><span id="_218__fatal_____filename___line____syntax_error_in_sub-type_specification._last_token_read_is__token__"></span><span id="_218__FATAL_____FILENAME___LINE____SYNTAX_ERROR_IN_SUB-TYPE_SPECIFICATION._LAST_TOKEN_READ_IS__TOKEN__"></span>**<218, Fatal>: "<fileName>:<line\#>: Syntax Error in sub-type specification. Last token read is <token>"**</span></span>
</dt> <dd>

<span data-ttu-id="eb287-140">Qualquer erro de sintaxe de módulo entre os parênteses em uma especificação de subtipo gera essa mensagem.</span><span class="sxs-lookup"><span data-stu-id="eb287-140">Any module syntax error between the parentheses in a sub-type specification generates this message.</span></span>

</dd> </dl>

## <a name="fatal-error-219"></a><span data-ttu-id="eb287-141">Erro fatal 219</span><span class="sxs-lookup"><span data-stu-id="eb287-141">Fatal Error 219</span></span>

<dl> <dt>

<span data-ttu-id="eb287-142"><span id="_219__Fatal____fileName___line____Syntax_Error_in_the_SIZE_specification._Last_token_read_is__token__"></span><span id="_219__fatal____filename___line____syntax_error_in_the_size_specification._last_token_read_is__token__"></span><span id="_219__FATAL____FILENAME___LINE____SYNTAX_ERROR_IN_THE_SIZE_SPECIFICATION._LAST_TOKEN_READ_IS__TOKEN__"></span>**<219,> fatal: " <fileName> : <linha \#>: erro de sintaxe na especificação de tamanho. O último token lido é <token> "**</span><span class="sxs-lookup"><span data-stu-id="eb287-142"><span id="_219__Fatal____fileName___line____Syntax_Error_in_the_SIZE_specification._Last_token_read_is__token__"></span><span id="_219__fatal____filename___line____syntax_error_in_the_size_specification._last_token_read_is__token__"></span><span id="_219__FATAL____FILENAME___LINE____SYNTAX_ERROR_IN_THE_SIZE_SPECIFICATION._LAST_TOKEN_READ_IS__TOKEN__"></span>**<219, Fatal>:"<fileName>:<line\#>: Syntax Error in the SIZE specification. Last token read is <token>"**</span></span>
</dt> <dd>

<span data-ttu-id="eb287-143">Qualquer erro de sintaxe de módulo na cláusula SIZE entre os parênteses esquerdo e direito gera essa mensagem.</span><span class="sxs-lookup"><span data-stu-id="eb287-143">Any module syntax error in the SIZE clause between the left and right parentheses generates this message.</span></span>

</dd> </dl>

## <a name="fatal-error-220"></a><span data-ttu-id="eb287-144">Erro fatal 220</span><span class="sxs-lookup"><span data-stu-id="eb287-144">Fatal Error 220</span></span>

<dl> <dt>

<span data-ttu-id="eb287-145"><span id="_220__Fatal____fileName___line____OBJECT-TYPE_invocation_of_SNMPv2SMI_not_allowed_"></span><span id="_220__fatal____filename___line____object-type_invocation_of_snmpv2smi_not_allowed_"></span><span id="_220__FATAL____FILENAME___LINE____OBJECT-TYPE_INVOCATION_OF_SNMPV2SMI_NOT_ALLOWED_"></span>**<220, fatal>: " <fileName> : <linha \#>: a invocação de tipo de objeto de SNMPv2SMI não é permitida"**</span><span class="sxs-lookup"><span data-stu-id="eb287-145"><span id="_220__Fatal____fileName___line____OBJECT-TYPE_invocation_of_SNMPv2SMI_not_allowed_"></span><span id="_220__fatal____filename___line____object-type_invocation_of_snmpv2smi_not_allowed_"></span><span id="_220__FATAL____FILENAME___LINE____OBJECT-TYPE_INVOCATION_OF_SNMPV2SMI_NOT_ALLOWED_"></span>**<220, Fatal>:"<fileName>:<line\#>: OBJECT-TYPE invocation of SNMPv2SMI not allowed"**</span></span>
</dt> <dd>

<span data-ttu-id="eb287-146">Erro de sintaxe do módulo.</span><span class="sxs-lookup"><span data-stu-id="eb287-146">Module syntax error.</span></span> <span data-ttu-id="eb287-147">Você usou a invocação do **tipo de objeto** específico do SNMPV2C na MIB, mas especificou a opção **/v1** , que requer conformidade estrita com a sintaxe SNMPv1.</span><span class="sxs-lookup"><span data-stu-id="eb287-147">You have used the SNMPv2C-specific **OBJECT-TYPE** invocation in the MIB, but have specified the **/v1** switch, which requires strict conformance to SNMPv1 syntax.</span></span>

</dd> </dl>

 

 



