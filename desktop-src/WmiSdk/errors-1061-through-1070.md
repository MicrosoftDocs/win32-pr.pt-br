---
description: Descreve os erros do provedor SNMP WMI 1061 a 1070.
ms.assetid: 1bbd6153-7241-4673-ae17-1caa92b2e6a6
ms.tgt_platform: multiple
title: Erros 1061 a 1070
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76a4bf0773ade1f62eb11f0c496aea340410c4a8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105760972"
---
# <a name="errors-1061-through-1070"></a>Erros 1061 a 1070

Descreve os erros do provedor SNMP WMI 1061 a 1070.

[Erro fatal 1063](#fatal-error-1063)

[Erro fatal 1064](#fatal-error-1064)

[Erro fatal 1070](#fatal-error-1070)

## <a name="fatal-error-1063"></a>Erro fatal 1063

<dl> <dt>

<span id="_1063__Fatal_____fileName__line____Upper_bound_of_SIZE_specification_is_less_than_the_lower_bound_"></span><span id="_1063__fatal_____filename__line____upper_bound_of_size_specification_is_less_than_the_lower_bound_"></span><span id="_1063__FATAL_____FILENAME__LINE____UPPER_BOUND_OF_SIZE_SPECIFICATION_IS_LESS_THAN_THE_LOWER_BOUND_"></span>**<1063,> fatal: " <fileName> linha de<\#>: o limite superior da especificação de tamanho é menor que o limite inferior"**
</dt> <dd>

Erro semântico de módulo em especificação de tamanho, específico para nem SNMPv1 nem SNMPv2C. O símbolo usado em uma especificação de tamanho deve ser resolvido para a cadeia de caracteres de OCTETO ou opaco. O limite inferior de uma especificação de intervalo ou tamanho não deve ser maior que o limite superior.

</dd> </dl>

## <a name="fatal-error-1064"></a>Erro fatal 1064

<dl> <dt>

<span id="_1064__Fatal_____fileName___line____SEQUENCE_item__identifier__does_not_resolve_to_an_OBJECT-TYPE_"></span><span id="_1064__fatal_____filename___line____sequence_item__identifier__does_not_resolve_to_an_object-type_"></span><span id="_1064__FATAL_____FILENAME___LINE____SEQUENCE_ITEM__IDENTIFIER__DOES_NOT_RESOLVE_TO_AN_OBJECT-TYPE_"></span>**<1064,> fatal: " <fileName> : <linha \#>: o item de sequência <identifier> não é resolvido para um tipo de objeto"**
</dt> <dd>

Erro semântico do módulo de atribuição de tipo, específico para nenhum SNMPv1 nem SNMPv2C. Todos os elementos individuais de uma declaração de sequência devem ser resolvidos para um tipo de objeto.

</dd> </dl>

## <a name="fatal-error-1070"></a>Erro fatal 1070

<dl> <dt>

<span id="_1070__Fatal_____fileName__line____MIB_Module__moduleName___from_which_symbol__symbolName__is_imported__is_not_present_in_input_"></span><span id="_1070__fatal_____filename__line____mib_module__modulename___from_which_symbol__symbolname__is_imported__is_not_present_in_input_"></span><span id="_1070__FATAL_____FILENAME__LINE____MIB_MODULE__MODULENAME___FROM_WHICH_SYMBOL__SYMBOLNAME__IS_IMPORTED__IS_NOT_PRESENT_IN_INPUT_"></span>**<1070,> fatal: " <fileName><linha \#>: módulo MIB <moduleName> , de onde o símbolo <symbolName> é importado, não está presente na entrada"**
</dt> <dd>

Erro semântico de módulo em referência cruzada, específico para nenhum SNMPv1 nem SNMPv2C. Se um dos módulos na seção Imports do módulo principal ou de um módulo subsidiária não existir e um ou mais símbolos desse módulo forem realmente referenciados, esse erro fatal ocorrerá.

</dd> </dl>

 

 



