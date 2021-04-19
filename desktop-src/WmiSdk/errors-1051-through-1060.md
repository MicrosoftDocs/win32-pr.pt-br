---
description: Descreve os erros do provedor SNMP WMI 1051 a 1060.
ms.assetid: 789cc5b6-e3ef-4f66-8dec-6970d6df1fe9
ms.tgt_platform: multiple
title: Erros 1051 a 1060
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 170eddf3126a40f929aa36899259b731fa244941
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105813274"
---
# <a name="errors-1051-through-1060"></a>Erros 1051 a 1060

Descreve os erros do provedor SNMP WMI 1051 a 1060.

[Erro fatal 1051](#fatal-error-1051)

[Erro fatal 1054](#fatal-error-1054)

[Erro fatal 1055](#fatal-error-1055)

## <a name="fatal-error-1051"></a>Erro fatal 1051

<dl> <dt>

<span id="_1051__Fatal_____fileName___line____Ambiguous_reference_to_symbol__identifier__"></span><span id="_1051__fatal_____filename___line____ambiguous_reference_to_symbol__identifier__"></span><span id="_1051__FATAL_____FILENAME___LINE____AMBIGUOUS_REFERENCE_TO_SYMBOL__IDENTIFIER__"></span>**<1051,> fatal: " <fileName> : <linha \#>: referência ambígua ao símbolo <identifier> "**
</dt> <dd>

Erro semântico de módulo de seção Imports, específico para nem SNMPv1 nem SNMPv2C. Cada descritor de objeto correspondente a um objeto em uma MIB padrão da Internet deve ser exclusivo. Como os MIBs corporativos podem ter descritores de objeto comuns, tais descritores importados de dois módulos devem ser usados de forma não ambígua no módulo MIB usando a notação "Module. Descriptor".

</dd> </dl>

## <a name="fatal-error-1054"></a>Erro fatal 1054

<dl> <dt>

<span id="_1054__Fatal_____fileName___line_____identifier__in_INDEX_clause_does_not_resolve_to_one_of_the_allowed_types_"></span><span id="_1054__fatal_____filename___line_____identifier__in_index_clause_does_not_resolve_to_one_of_the_allowed_types_"></span><span id="_1054__FATAL_____FILENAME___LINE_____IDENTIFIER__IN_INDEX_CLAUSE_DOES_NOT_RESOLVE_TO_ONE_OF_THE_ALLOWED_TYPES_"></span>**<1054,> fatal: " <fileName> : <linha \#>: <identifier> na cláusula index não é resolvida para um dos tipos permitidos"**
</dt> <dd>

Erro semântico do módulo de invocação de macro do **tipo de objeto** . O tipo de um objeto na cláusula INDEX ou qualquer tipo especificado na cláusula INDEX, deve ser resolvido para um tipo escalar, ou seja, uma não sequência ou não sequência de tipo. Qualquer tipo especificado na cláusula INDEX também deve ser resolvido para um deles.

Esse erro pode ocorrer em SNMPv1 ou SNMPv2C.

</dd> </dl>

## <a name="fatal-error-1055"></a>Erro fatal 1055

<dl> <dt>

<span id="_1055__Fatal____fileName___line____SYNTAX_of_INDEX_OBJECT-TYPE__identifier___does_not_resolve_to_one_of_the_allowed_types_"></span><span id="_1055__fatal____filename___line____syntax_of_index_object-type__identifier___does_not_resolve_to_one_of_the_allowed_types_"></span><span id="_1055__FATAL____FILENAME___LINE____SYNTAX_OF_INDEX_OBJECT-TYPE__IDENTIFIER___DOES_NOT_RESOLVE_TO_ONE_OF_THE_ALLOWED_TYPES_"></span>**<1055, fatal>: " <fileName> : <linha \#>: a sintaxe do tipo de objeto de índice <identifier> , não é resolvida para um dos tipos permitidos"**
</dt> <dd>

Erro semântico do módulo de invocação de macro do **tipo de objeto** . O tipo de um objeto na cláusula INDEX ou qualquer tipo especificado na cláusula INDEX, deve ser resolvido para um tipo escalar, ou seja, uma não sequência ou não sequência de tipo.

Esse erro pode ocorrer em SNMPv1 ou SNMPv2C.

</dd> </dl>

 

 



