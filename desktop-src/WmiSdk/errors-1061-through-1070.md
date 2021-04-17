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
# <a name="errors-1061-through-1070"></a><span data-ttu-id="42025-103">Erros 1061 a 1070</span><span class="sxs-lookup"><span data-stu-id="42025-103">Errors 1061 through 1070</span></span>

<span data-ttu-id="42025-104">Descreve os erros do provedor SNMP WMI 1061 a 1070.</span><span class="sxs-lookup"><span data-stu-id="42025-104">Describes WMI SNMP provider errors 1061 through 1070.</span></span>

[<span data-ttu-id="42025-105">Erro fatal 1063</span><span class="sxs-lookup"><span data-stu-id="42025-105">Fatal Error 1063</span></span>](#fatal-error-1063)

[<span data-ttu-id="42025-106">Erro fatal 1064</span><span class="sxs-lookup"><span data-stu-id="42025-106">Fatal Error 1064</span></span>](#fatal-error-1064)

[<span data-ttu-id="42025-107">Erro fatal 1070</span><span class="sxs-lookup"><span data-stu-id="42025-107">Fatal Error 1070</span></span>](#fatal-error-1070)

## <a name="fatal-error-1063"></a><span data-ttu-id="42025-108">Erro fatal 1063</span><span class="sxs-lookup"><span data-stu-id="42025-108">Fatal Error 1063</span></span>

<dl> <dt>

<span data-ttu-id="42025-109"><span id="_1063__Fatal_____fileName__line____Upper_bound_of_SIZE_specification_is_less_than_the_lower_bound_"></span><span id="_1063__fatal_____filename__line____upper_bound_of_size_specification_is_less_than_the_lower_bound_"></span><span id="_1063__FATAL_____FILENAME__LINE____UPPER_BOUND_OF_SIZE_SPECIFICATION_IS_LESS_THAN_THE_LOWER_BOUND_"></span>**<1063,> fatal: " <fileName> linha de<\#>: o limite superior da especificação de tamanho é menor que o limite inferior"**</span><span class="sxs-lookup"><span data-stu-id="42025-109"><span id="_1063__Fatal_____fileName__line____Upper_bound_of_SIZE_specification_is_less_than_the_lower_bound_"></span><span id="_1063__fatal_____filename__line____upper_bound_of_size_specification_is_less_than_the_lower_bound_"></span><span id="_1063__FATAL_____FILENAME__LINE____UPPER_BOUND_OF_SIZE_SPECIFICATION_IS_LESS_THAN_THE_LOWER_BOUND_"></span>**<1063, Fatal>: "<fileName><line\#>: Upper bound of SIZE specification is less than the lower bound"**</span></span>
</dt> <dd>

<span data-ttu-id="42025-110">Erro semântico de módulo em especificação de tamanho, específico para nem SNMPv1 nem SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="42025-110">Module semantic error in SIZE specification, specific to neither SNMPv1 nor SNMPv2C.</span></span> <span data-ttu-id="42025-111">O símbolo usado em uma especificação de tamanho deve ser resolvido para a cadeia de caracteres de OCTETO ou opaco.</span><span class="sxs-lookup"><span data-stu-id="42025-111">The symbol used in a SIZE specification must resolve to OCTET STRING or Opaque.</span></span> <span data-ttu-id="42025-112">O limite inferior de uma especificação de intervalo ou tamanho não deve ser maior que o limite superior.</span><span class="sxs-lookup"><span data-stu-id="42025-112">The lower bound of a range or SIZE specification must be no greater than the upper bound.</span></span>

</dd> </dl>

## <a name="fatal-error-1064"></a><span data-ttu-id="42025-113">Erro fatal 1064</span><span class="sxs-lookup"><span data-stu-id="42025-113">Fatal Error 1064</span></span>

<dl> <dt>

<span data-ttu-id="42025-114"><span id="_1064__Fatal_____fileName___line____SEQUENCE_item__identifier__does_not_resolve_to_an_OBJECT-TYPE_"></span><span id="_1064__fatal_____filename___line____sequence_item__identifier__does_not_resolve_to_an_object-type_"></span><span id="_1064__FATAL_____FILENAME___LINE____SEQUENCE_ITEM__IDENTIFIER__DOES_NOT_RESOLVE_TO_AN_OBJECT-TYPE_"></span>**<1064,> fatal: " <fileName> : <linha \#>: o item de sequência <identifier> não é resolvido para um tipo de objeto"**</span><span class="sxs-lookup"><span data-stu-id="42025-114"><span id="_1064__Fatal_____fileName___line____SEQUENCE_item__identifier__does_not_resolve_to_an_OBJECT-TYPE_"></span><span id="_1064__fatal_____filename___line____sequence_item__identifier__does_not_resolve_to_an_object-type_"></span><span id="_1064__FATAL_____FILENAME___LINE____SEQUENCE_ITEM__IDENTIFIER__DOES_NOT_RESOLVE_TO_AN_OBJECT-TYPE_"></span>**<1064, Fatal>: "<fileName>:<line\#>: SEQUENCE item <identifier> does not resolve to an OBJECT-TYPE"**</span></span>
</dt> <dd>

<span data-ttu-id="42025-115">Erro semântico do módulo de atribuição de tipo, específico para nenhum SNMPv1 nem SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="42025-115">Type assignment module semantic error, specific to neither SNMPv1 nor SNMPv2C.</span></span> <span data-ttu-id="42025-116">Todos os elementos individuais de uma declaração de sequência devem ser resolvidos para um tipo de objeto.</span><span class="sxs-lookup"><span data-stu-id="42025-116">All of the individual elements of a SEQUENCE declaration must resolve to an OBJECT-TYPE.</span></span>

</dd> </dl>

## <a name="fatal-error-1070"></a><span data-ttu-id="42025-117">Erro fatal 1070</span><span class="sxs-lookup"><span data-stu-id="42025-117">Fatal Error 1070</span></span>

<dl> <dt>

<span data-ttu-id="42025-118"><span id="_1070__Fatal_____fileName__line____MIB_Module__moduleName___from_which_symbol__symbolName__is_imported__is_not_present_in_input_"></span><span id="_1070__fatal_____filename__line____mib_module__modulename___from_which_symbol__symbolname__is_imported__is_not_present_in_input_"></span><span id="_1070__FATAL_____FILENAME__LINE____MIB_MODULE__MODULENAME___FROM_WHICH_SYMBOL__SYMBOLNAME__IS_IMPORTED__IS_NOT_PRESENT_IN_INPUT_"></span>**<1070,> fatal: " <fileName><linha \#>: módulo MIB <moduleName> , de onde o símbolo <symbolName> é importado, não está presente na entrada"**</span><span class="sxs-lookup"><span data-stu-id="42025-118"><span id="_1070__Fatal_____fileName__line____MIB_Module__moduleName___from_which_symbol__symbolName__is_imported__is_not_present_in_input_"></span><span id="_1070__fatal_____filename__line____mib_module__modulename___from_which_symbol__symbolname__is_imported__is_not_present_in_input_"></span><span id="_1070__FATAL_____FILENAME__LINE____MIB_MODULE__MODULENAME___FROM_WHICH_SYMBOL__SYMBOLNAME__IS_IMPORTED__IS_NOT_PRESENT_IN_INPUT_"></span>**<1070, Fatal>: "<fileName><line\#>: MIB Module <moduleName>, from which symbol <symbolName> is imported, is not present in input"**</span></span>
</dt> <dd>

<span data-ttu-id="42025-119">Erro semântico de módulo em referência cruzada, específico para nenhum SNMPv1 nem SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="42025-119">Module semantic error in cross-referencing, specific to neither SNMPv1 nor SNMPv2C.</span></span> <span data-ttu-id="42025-120">Se um dos módulos na seção Imports do módulo principal ou de um módulo subsidiária não existir e um ou mais símbolos desse módulo forem realmente referenciados, esse erro fatal ocorrerá.</span><span class="sxs-lookup"><span data-stu-id="42025-120">If one of the modules in the IMPORTS section of the main module or a subsidiary module does not exist and one or more symbols from this module are actually referenced, this fatal error occurs.</span></span>

</dd> </dl>

 

 



