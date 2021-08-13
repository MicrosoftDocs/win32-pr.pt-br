---
description: Descreve os erros de provedor WMI SNMP de 211 a 220.
ms.assetid: beaa644d-51b3-4a57-8853-0b37f69f615a
ms.tgt_platform: multiple
title: Erros de 211 a 220
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3394f6ca4317d14e83ca17b3a8ef9b516d218c072659041f7c6f5b035e6cdcc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118556698"
---
# <a name="errors-211-through-220"></a>Erros de 211 a 220

Descreve os erros de provedor WMI SNMP de 211 a 220.

[Mensagem de informações 211](#information-message-211)

[Erro fatal 212](#fatal-error-212)

[Erro fatal 213](#fatal-error-213)

[Erro fatal 214](#fatal-error-214)

[Erro fatal 215](#fatal-error-215)

[Erro fatal 216](#fatal-error-216)

[Erro fatal 217](#fatal-error-217)

[Erro fatal 218](#fatal-error-218)

[Erro fatal 219](#fatal-error-219)

[Erro fatal 220](#fatal-error-220)

## <a name="information-message-211"></a>Mensagem de informações 211

<dl> <dt>

<span id="_211__Information____Skipping_TRAP-TYPE__identifier__"></span><span id="_211__information____skipping_trap-type__identifier__"></span><span id="_211__INFORMATION____SKIPPING_TRAP-TYPE__IDENTIFIER__"></span>**<211, Informações>: "Ignorando TRAP-TYPE" <identifier>**
</dt> <dd>

Todos os erros na definição TRAP-TYPE geram essa mensagem.

</dd> </dl>

## <a name="fatal-error-212"></a>Erro fatal 212

<dl> <dt>

<span id="_212__Fatal_____fileName___line____Syntax_Error_in_SEQUENCE_definition._Last_token_read_is__token__"></span><span id="_212__fatal_____filename___line____syntax_error_in_sequence_definition._last_token_read_is__token__"></span><span id="_212__FATAL_____FILENAME___LINE____SYNTAX_ERROR_IN_SEQUENCE_DEFINITION._LAST_TOKEN_READ_IS__TOKEN__"></span>**<212, Fatal>: " <fileName> :<line>: Erro de sintaxe \# na definição SEQUENCE. A última leitura do token <token> é "**
</dt> <dd>

Erro de sintaxe do módulo na atribuição de tipo. Há um erro entre as chaves esquerda e direita de um constructo SEQUENCE, que equivale a um erro de sintaxe em uma atribuição de tipo MIB.

</dd> </dl>

## <a name="fatal-error-213"></a>Erro fatal 213

<dl> <dt>

<span id="_213__Fatal_____fileName___line____Syntax_Error_in_Object_Identifier_value._Last_token_read_is__token__"></span><span id="_213__fatal_____filename___line____syntax_error_in_object_identifier_value._last_token_read_is__token__"></span><span id="_213__FATAL_____FILENAME___LINE____SYNTAX_ERROR_IN_OBJECT_IDENTIFIER_VALUE._LAST_TOKEN_READ_IS__TOKEN__"></span>**<213, Fatal>: " :<line>: Erro de sintaxe no valor <fileName> \# do Identificador de Objeto. A última leitura do token <token> é "**
</dt> <dd>

Erro de sintaxe do módulo na atribuição de valor. Há um erro entre as chaves esquerda e direita de um valor de identificador de objeto.

</dd> </dl>

## <a name="fatal-error-214"></a>Erro fatal 214

<dl> <dt>

<span id="_214__Fatal_____fileName___line____Syntax_Error_in_the_list_of_symbols_in_IMPORTS._Last_token_read_is__token__"></span><span id="_214__fatal_____filename___line____syntax_error_in_the_list_of_symbols_in_imports._last_token_read_is__token__"></span><span id="_214__FATAL_____FILENAME___LINE____SYNTAX_ERROR_IN_THE_LIST_OF_SYMBOLS_IN_IMPORTS._LAST_TOKEN_READ_IS__TOKEN__"></span>**<214, Fatal>: " :<line>: Erro de sintaxe na lista de símbolos em <fileName> \# IMPORTS. A última leitura do token <token> é "**
</dt> <dd>

Erro de sintaxe do módulo na seção IMPORTS.

</dd> </dl>

## <a name="fatal-error-215"></a>Erro fatal 215

<dl> <dt>

<span id="_215__Fatal_____fileName___line____Syntax_Error_in_IMPORTS__missing_module_name__._Last_token_read_is__token__"></span><span id="_215__fatal_____filename___line____syntax_error_in_imports__missing_module_name__._last_token_read_is__token__"></span><span id="_215__FATAL_____FILENAME___LINE____SYNTAX_ERROR_IN_IMPORTS__MISSING_MODULE_NAME__._LAST_TOKEN_READ_IS__TOKEN__"></span>**<215, fatal>: " :<line>: Erro de sintaxe em <fileName> \# IMPORTS (nome do módulo ausente?). A última leitura do token <token> é "**
</dt> <dd>

Erro de sintaxe do módulo na seção IMPORTS.

</dd> </dl>

## <a name="fatal-error-216"></a>Erro fatal 216

<dl> <dt>

<span id="_216__Fatal_____fileName___line____Syntax_Error_in_the_IMPORTS_section._Last_token_read_is__token__"></span><span id="_216__fatal_____filename___line____syntax_error_in_the_imports_section._last_token_read_is__token__"></span><span id="_216__FATAL_____FILENAME___LINE____SYNTAX_ERROR_IN_THE_IMPORTS_SECTION._LAST_TOKEN_READ_IS__TOKEN__"></span>**<216, fatal>: " :<line>: Erro de sintaxe na <fileName> \# seção IMPORTS. A última leitura do token <token> é "**
</dt> <dd>

Erro de sintaxe do módulo na seção IMPORTS.

</dd> </dl>

## <a name="fatal-error-217"></a>Erro fatal 217

<dl> <dt>

<span id="_217__Fatal_____fileName___line____Syntax_error_in_INTEGER_Enumeration._Last_token_read_is__token__"></span><span id="_217__fatal_____filename___line____syntax_error_in_integer_enumeration._last_token_read_is__token__"></span><span id="_217__FATAL_____FILENAME___LINE____SYNTAX_ERROR_IN_INTEGER_ENUMERATION._LAST_TOKEN_READ_IS__TOKEN__"></span>**<217, Fatal>: " :<line>: Erro de sintaxe <fileName> \# na enumeração INTEGER. A última leitura do token <token> é "**
</dt> <dd>

Qualquer erro de sintaxe de módulo entre as chaves esquerda e direita de uma definição de enumeração MIB gera essa mensagem.

</dd> </dl>

## <a name="fatal-error-218"></a>Erro fatal 218

<dl> <dt>

<span id="_218__Fatal_____fileName___line____Syntax_Error_in_sub-type_specification._Last_token_read_is__token__"></span><span id="_218__fatal_____filename___line____syntax_error_in_sub-type_specification._last_token_read_is__token__"></span><span id="_218__FATAL_____FILENAME___LINE____SYNTAX_ERROR_IN_SUB-TYPE_SPECIFICATION._LAST_TOKEN_READ_IS__TOKEN__"></span>**<218, Fatal>: " :<line>: Erro de sintaxe na <fileName> \# especificação de subtipo. A última leitura do token <token> é "**
</dt> <dd>

Qualquer erro de sintaxe de módulo entre os parênteses em uma especificação de subtipo gera essa mensagem.

</dd> </dl>

## <a name="fatal-error-219"></a>Erro fatal 219

<dl> <dt>

<span id="_219__Fatal____fileName___line____Syntax_Error_in_the_SIZE_specification._Last_token_read_is__token__"></span><span id="_219__fatal____filename___line____syntax_error_in_the_size_specification._last_token_read_is__token__"></span><span id="_219__FATAL____FILENAME___LINE____SYNTAX_ERROR_IN_THE_SIZE_SPECIFICATION._LAST_TOKEN_READ_IS__TOKEN__"></span>**<219, fatal>:" :<linha>: Erro de sintaxe <fileName> \# na especificação SIZE. A última leitura do token <token> é "**
</dt> <dd>

Qualquer erro de sintaxe de módulo na cláusula SIZE entre os parênteses esquerdo e direito gera essa mensagem.

</dd> </dl>

## <a name="fatal-error-220"></a>Erro fatal 220

<dl> <dt>

<span id="_220__Fatal____fileName___line____OBJECT-TYPE_invocation_of_SNMPv2SMI_not_allowed_"></span><span id="_220__fatal____filename___line____object-type_invocation_of_snmpv2smi_not_allowed_"></span><span id="_220__FATAL____FILENAME___LINE____OBJECT-TYPE_INVOCATION_OF_SNMPV2SMI_NOT_ALLOWED_"></span>**<220, fatal>:" :<linha>: invocação <fileName> \# OBJECT-TYPE de SNMPv2SMI não permitida"**
</dt> <dd>

Erro de sintaxe do módulo. Você usou a invocação **OBJECT-TYPE** específica de SNMPv2C no MIB, mas especificou a opção **/v1,** que requer conformidade estrita com a sintaxe SNMPv1.

</dd> </dl>

 

 



