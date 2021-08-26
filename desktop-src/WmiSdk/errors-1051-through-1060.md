---
description: Descreve os erros de provedor WMI SNMP 1051 a 1060.
ms.assetid: 789cc5b6-e3ef-4f66-8dec-6970d6df1fe9
ms.tgt_platform: multiple
title: Erros de 1051 a 1060
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3405a799d71b33fa1dabd7c84964b8d1726d2e27
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122882588"
---
# <a name="errors-1051-through-1060"></a>Erros de 1051 a 1060

Descreve os erros de provedor WMI SNMP 1051 a 1060.

[Erro fatal 1051](#fatal-error-1051)

[Erro fatal 1054](#fatal-error-1054)

[Erro fatal 1055](#fatal-error-1055)

## <a name="fatal-error-1051"></a>Erro fatal 1051

<dl> <dt>

<span id="_1051__Fatal_____fileName___line____Ambiguous_reference_to_symbol__identifier__"></span><span id="_1051__fatal_____filename___line____ambiguous_reference_to_symbol__identifier__"></span><span id="_1051__FATAL_____FILENAME___LINE____AMBIGUOUS_REFERENCE_TO_SYMBOL__IDENTIFIER__"></span>**<1051, Fatal>: " &lt; fileName :<line>: Referência ambígua ao &gt; \# &lt; identificador de símbolo &gt; "**
</dt> <dd>

Erro semântico de módulo da seção IMPORTS, específico para SNMPv1 nem SNMPv2C. Cada descritor de objeto correspondente a um objeto em um Internet Standard MIB deve ser exclusivo. Como os MIBs empresariais podem ter descritores de objeto comuns, esses descritores importados de dois módulos devem ser usados de forma não ambígua no módulo MIB usando a notação "module.descriptor".

</dd> </dl>

## <a name="fatal-error-1054"></a>Erro fatal 1054

<dl> <dt>

<span id="_1054__Fatal_____fileName___line_____identifier__in_INDEX_clause_does_not_resolve_to_one_of_the_allowed_types_"></span><span id="_1054__fatal_____filename___line_____identifier__in_index_clause_does_not_resolve_to_one_of_the_allowed_types_"></span><span id="_1054__FATAL_____FILENAME___LINE_____IDENTIFIER__IN_INDEX_CLAUSE_DOES_NOT_RESOLVE_TO_ONE_OF_THE_ALLOWED_TYPES_"></span>**<1054, Fatal>: " &lt; fileName &gt; :<line \#>: identifier in INDEX clause não resolve para um dos tipos &lt; &gt; permitidos"**
</dt> <dd>

**Erro semântico de** módulo de invocação de macro OBJECT-TYPE. O tipo de um objeto na cláusula INDEX ou qualquer tipo especificado na cláusula INDEX deve ser resolvido para um tipo escalar, ou seja, um tipo não SEQUENCE ou não SEQUENCE OF. Qualquer tipo especificado na cláusula INDEX também deve ser resolvido para um deles.

Esse erro pode ocorrer em SNMPv1 ou SNMPv2C.

</dd> </dl>

## <a name="fatal-error-1055"></a>Erro fatal 1055

<dl> <dt>

<span id="_1055__Fatal____fileName___line____SYNTAX_of_INDEX_OBJECT-TYPE__identifier___does_not_resolve_to_one_of_the_allowed_types_"></span><span id="_1055__fatal____filename___line____syntax_of_index_object-type__identifier___does_not_resolve_to_one_of_the_allowed_types_"></span><span id="_1055__FATAL____FILENAME___LINE____SYNTAX_OF_INDEX_OBJECT-TYPE__IDENTIFIER___DOES_NOT_RESOLVE_TO_ONE_OF_THE_ALLOWED_TYPES_"></span>**<1055, Fatal>:" &lt; fileName &gt; :<line \#>: SINTAXE do identificador INDEX OBJECT-TYPE , não resolve para um dos tipos &lt; &gt; permitidos"**
</dt> <dd>

**Erro semântico de** módulo de invocação de macro OBJECT-TYPE. O tipo de um objeto na cláusula INDEX ou qualquer tipo especificado na cláusula INDEX deve ser resolvido para um tipo escalar, ou seja, um tipo não SEQUENCE ou não SEQUENCE OF.

Esse erro pode ocorrer em SNMPv1 ou SNMPv2C.

</dd> </dl>

 

 



