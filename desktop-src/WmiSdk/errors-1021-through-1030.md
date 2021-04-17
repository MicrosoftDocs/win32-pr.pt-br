---
description: Descreve os erros do provedor SNMP WMI 1021 a 1033.
ms.assetid: fc638d0f-20f4-46d0-a36a-c3898415f35c
ms.tgt_platform: multiple
title: Erros 1021 a 1030
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8bce9c7c4d70250fa63ad0100cf93c8d5b26984
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105754089"
---
# <a name="errors-1021-through-1030"></a>Erros 1021 a 1030

Descreve os erros do provedor SNMP WMI 1021 a 1033.

[Erro fatal 1021](#fatal-error-1021)

[Erro fatal 1022](#fatal-error-1022)

[Erro fatal 1023](#fatal-error-1023)

[Erro fatal 1024](#fatal-error-1024)

[Erro fatal 1025](#fatal-error-1025)

[Erro fatal 1026](#fatal-error-1026)

[Aviso 1027](#warning-1027)

[Erro fatal 1028](#fatal-error-1028)

[Erro fatal 1029](#fatal-error-1029)

[Erro fatal 1030](#fatal-error-1030)

## <a name="fatal-error-1021"></a>Erro fatal 1021

<dl> <dt>

<span id="_1021__Fatal_____fileName__line____Identifier__identifier__in_the_VARIABLES_clause_of_TRAP-TYPE_does_not_resolve_to_a_scalar_OBJECT-TYPE_"></span><span id="_1021__fatal_____filename__line____identifier__identifier__in_the_variables_clause_of_trap-type_does_not_resolve_to_a_scalar_object-type_"></span><span id="_1021__FATAL_____FILENAME__LINE____IDENTIFIER__IDENTIFIER__IN_THE_VARIABLES_CLAUSE_OF_TRAP-TYPE_DOES_NOT_RESOLVE_TO_A_SCALAR_OBJECT-TYPE_"></span>**<1021,> fatal: " <fileName><da linha \#>: <identifier> o identificador na cláusula Variables do tipo de interceptação não é resolvido para um tipo de objeto escalar"**
</dt> <dd>

Invocação de macro do **tipo Trap** , erro semântico de módulo específico de SNMPv1. Cada item na lista de variáveis usado na cláusula VARIABLEs de uma chamada de macro de **tipo de interceptação** deve ser resolvido para o nome de uma instância de tipo de objeto escalar.

</dd> </dl>

## <a name="fatal-error-1022"></a>Erro fatal 1022

<dl> <dt>

<span id="_1022__Fatal_____fileName__line____Value_does_not_resolve_to_type__type__"></span><span id="_1022__fatal_____filename__line____value_does_not_resolve_to_type__type__"></span><span id="_1022__FATAL_____FILENAME__LINE____VALUE_DOES_NOT_RESOLVE_TO_TYPE__TYPE__"></span>**<1022,> fatal: " <fileName><da linha \#>: o valor não é resolvido para o tipo <type> "**
</dt> <dd>

Erro semântico de módulo de atribuição de valor, específico para nenhum SNMPv1 nem SNMPv2C. O valor no RHS de um número inteiro, **nulo**, Cadeia de caracteres de octeto ou de valor do identificador de objeto é do tipo errado.

</dd> </dl>

## <a name="fatal-error-1023"></a>Erro fatal 1023

<dl> <dt>

<span id="_1023__Fatal_____fileName__line____Identifier__identifier__does_not_resolve_to_the_type__identifier__"></span><span id="_1023__fatal_____filename__line____identifier__identifier__does_not_resolve_to_the_type__identifier__"></span><span id="_1023__FATAL_____FILENAME__LINE____IDENTIFIER__IDENTIFIER__DOES_NOT_RESOLVE_TO_THE_TYPE__IDENTIFIER__"></span>**<1023,> fatal: " <fileName><da linha \#>: <identifier> o identificador não é resolvido para o tipo <identifier> "**
</dt> <dd>

Erro semântico de módulo de atribuição de valor, específico para nenhum SNMPv1 nem SNMPv2C. Um símbolo (referência de valor) no RHS de um inteiro, **nulo**, Cadeia de caracteres de octeto ou atribuição de valor de identificador de objeto não é resolvido para o tipo correto.

</dd> </dl>

## <a name="fatal-error-1024"></a>Erro fatal 1024

<dl> <dt>

<span id="_1024__Fatal_____fileName__line____Negative_integer_in_OID_value_definition_"></span><span id="_1024__fatal_____filename__line____negative_integer_in_oid_value_definition_"></span><span id="_1024__FATAL_____FILENAME__LINE____NEGATIVE_INTEGER_IN_OID_VALUE_DEFINITION_"></span>**<1024,> fatal: " <fileName><da linha \#>: inteiro negativo na definição do valor de OID"**
</dt> <dd>

Erro semântico de módulo de atribuição de valor, específico para nenhum SNMPv1 nem SNMPv2C. Todos os valores em uma lista de componentes de OID devem ser inteiros não negativos (preferivelmente positivos).

</dd> </dl>

## <a name="fatal-error-1025"></a>Erro fatal 1025

<dl> <dt>

<span id="_1025__Fatal____Identifier__identifier__in_OID_value_does_not_resolve_to_a_positive_integer_"></span><span id="_1025__fatal____identifier__identifier__in_oid_value_does_not_resolve_to_a_positive_integer_"></span><span id="_1025__FATAL____IDENTIFIER__IDENTIFIER__IN_OID_VALUE_DOES_NOT_RESOLVE_TO_A_POSITIVE_INTEGER_"></span>**<1025,> fatal: " <identifier> o identificador no valor de OID não é resolvido para um inteiro positivo"**
</dt> <dd>

Erro semântico de módulo de atribuição de valor, específico para nenhum SNMPv1 nem SNMPv2C. Todos os valores em uma lista de componentes de OID devem ser inteiros não negativos (preferivelmente positivos).

</dd> </dl>

## <a name="fatal-error-1026"></a>Erro fatal 1026

<dl> <dt>

<span id="_1026__Fatal_____fileName__line____Identifier__identifier__in_OID_value_neither_resolves_to_an_OID_value_nor_a_positive_integer_"></span><span id="_1026__fatal_____filename__line____identifier__identifier__in_oid_value_neither_resolves_to_an_oid_value_nor_a_positive_integer_"></span><span id="_1026__FATAL_____FILENAME__LINE____IDENTIFIER__IDENTIFIER__IN_OID_VALUE_NEITHER_RESOLVES_TO_AN_OID_VALUE_NOR_A_POSITIVE_INTEGER_"></span>**<1026,> fatal: " <fileName><da linha \#>: o identificador <identifier> no valor de OID não é resolvido para um valor de OID nem um inteiro positivo"**
</dt> <dd>

Erro semântico de módulo de atribuição de valor, específico para nenhum SNMPv1 nem SNMPv2C. O primeiro componente usado em um valor de OID deve ser resolvido para um valor OID ou um inteiro.

</dd> </dl>

## <a name="warning-1027"></a>Aviso 1027

<dl> <dt>

<span id="_1027__Warning_____fileName__line____Imported_symbol__identifier__unused_"></span><span id="_1027__warning_____filename__line____imported_symbol__identifier__unused_"></span><span id="_1027__WARNING_____FILENAME__LINE____IMPORTED_SYMBOL__IDENTIFIER__UNUSED_"></span>**<1027, aviso>: " <fileName> linha de<\#>: símbolo importado <identifier> não utilizado"**
</dt> <dd>

Seção de importações aviso semântico do módulo, específico para não SNMPv1 nem SNMPv2C. Um aviso é emitido para cada símbolo importado não utilizado.

</dd> </dl>

## <a name="fatal-error-1028"></a>Erro fatal 1028

<dl> <dt>

<span id="_1028__Fatal____Module__identifier__not_imported_in_the_IMPORTS_section_"></span><span id="_1028__fatal____module__identifier__not_imported_in_the_imports_section_"></span><span id="_1028__FATAL____MODULE__IDENTIFIER__NOT_IMPORTED_IN_THE_IMPORTS_SECTION_"></span>**<1028,> fatal: "módulo <identifier> não importado na seção de importações"**
</dt> <dd>

Erro semântico de módulo de seção Imports, específico para nem SNMPv1 nem SNMPv2C. Um nome de módulo usado para fazer referência a um símbolo deve estar presente na cláusula Imports ou ser o nome do módulo atual.

</dd> </dl>

## <a name="fatal-error-1029"></a>Erro fatal 1029

<dl> <dt>

<span id="_1029__Fatal_____fileName__line____Current_module__identifier__cannot_be_imported_"></span><span id="_1029__fatal_____filename__line____current_module__identifier__cannot_be_imported_"></span><span id="_1029__FATAL_____FILENAME__LINE____CURRENT_MODULE__IDENTIFIER__CANNOT_BE_IMPORTED_"></span>**<1029,> fatal: " <fileName> linha de<\#>: o módulo atual <identifier> não pode ser importado"**
</dt> <dd>

Erro semântico de módulo de seção Imports, específico para nem SNMPv1 nem SNMPv2C. O nome do módulo atual também é ilustrado na lista de importações.

</dd> </dl>

## <a name="fatal-error-1030"></a>Erro fatal 1030

<dl> <dt>

<span id="_1030__Fatal____fileName__line____Symbol__identifier__not_imported_from_Module__identifier__"></span><span id="_1030__fatal____filename__line____symbol__identifier__not_imported_from_module__identifier__"></span><span id="_1030__FATAL____FILENAME__LINE____SYMBOL__IDENTIFIER__NOT_IMPORTED_FROM_MODULE__IDENTIFIER__"></span>**<1030,> fatal: " <fileName> linha de<\#>: símbolo <identifier> não importado do módulo <identifier> "**
</dt> <dd>

Erro semântico de módulo de seção Imports, específico para nem SNMPv1 nem SNMPv2C. Você usou a notação "Module. Symbol", mas o símbolo não foi importado do módulo especificado na seção Imports.

</dd> </dl>

 

 



