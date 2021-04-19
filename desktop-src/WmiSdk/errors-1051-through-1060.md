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
# <a name="errors-1051-through-1060"></a><span data-ttu-id="f5494-103">Erros 1051 a 1060</span><span class="sxs-lookup"><span data-stu-id="f5494-103">Errors 1051 through 1060</span></span>

<span data-ttu-id="f5494-104">Descreve os erros do provedor SNMP WMI 1051 a 1060.</span><span class="sxs-lookup"><span data-stu-id="f5494-104">Describes WMI SNMP provider errors 1051 through 1060.</span></span>

[<span data-ttu-id="f5494-105">Erro fatal 1051</span><span class="sxs-lookup"><span data-stu-id="f5494-105">Fatal Error 1051</span></span>](#fatal-error-1051)

[<span data-ttu-id="f5494-106">Erro fatal 1054</span><span class="sxs-lookup"><span data-stu-id="f5494-106">Fatal Error 1054</span></span>](#fatal-error-1054)

[<span data-ttu-id="f5494-107">Erro fatal 1055</span><span class="sxs-lookup"><span data-stu-id="f5494-107">Fatal Error 1055</span></span>](#fatal-error-1055)

## <a name="fatal-error-1051"></a><span data-ttu-id="f5494-108">Erro fatal 1051</span><span class="sxs-lookup"><span data-stu-id="f5494-108">Fatal Error 1051</span></span>

<dl> <dt>

<span data-ttu-id="f5494-109"><span id="_1051__Fatal_____fileName___line____Ambiguous_reference_to_symbol__identifier__"></span><span id="_1051__fatal_____filename___line____ambiguous_reference_to_symbol__identifier__"></span><span id="_1051__FATAL_____FILENAME___LINE____AMBIGUOUS_REFERENCE_TO_SYMBOL__IDENTIFIER__"></span>**<1051,> fatal: " <fileName> : <linha \#>: referência ambígua ao símbolo <identifier> "**</span><span class="sxs-lookup"><span data-stu-id="f5494-109"><span id="_1051__Fatal_____fileName___line____Ambiguous_reference_to_symbol__identifier__"></span><span id="_1051__fatal_____filename___line____ambiguous_reference_to_symbol__identifier__"></span><span id="_1051__FATAL_____FILENAME___LINE____AMBIGUOUS_REFERENCE_TO_SYMBOL__IDENTIFIER__"></span>**<1051, Fatal>: "<fileName>:<line\#>: Ambiguous reference to symbol <identifier>"**</span></span>
</dt> <dd>

<span data-ttu-id="f5494-110">Erro semântico de módulo de seção Imports, específico para nem SNMPv1 nem SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="f5494-110">IMPORTS section module semantic error, specific to neither SNMPv1 nor SNMPv2C.</span></span> <span data-ttu-id="f5494-111">Cada descritor de objeto correspondente a um objeto em uma MIB padrão da Internet deve ser exclusivo.</span><span class="sxs-lookup"><span data-stu-id="f5494-111">Each object descriptor corresponding to an object in an Internet Standard MIB must be unique.</span></span> <span data-ttu-id="f5494-112">Como os MIBs corporativos podem ter descritores de objeto comuns, tais descritores importados de dois módulos devem ser usados de forma não ambígua no módulo MIB usando a notação "Module. Descriptor".</span><span class="sxs-lookup"><span data-stu-id="f5494-112">Since enterprise MIBs can have common object descriptors, such descriptors imported from two modules must be used unambiguously in the MIB module by using the notation "module.descriptor."</span></span>

</dd> </dl>

## <a name="fatal-error-1054"></a><span data-ttu-id="f5494-113">Erro fatal 1054</span><span class="sxs-lookup"><span data-stu-id="f5494-113">Fatal Error 1054</span></span>

<dl> <dt>

<span data-ttu-id="f5494-114"><span id="_1054__Fatal_____fileName___line_____identifier__in_INDEX_clause_does_not_resolve_to_one_of_the_allowed_types_"></span><span id="_1054__fatal_____filename___line_____identifier__in_index_clause_does_not_resolve_to_one_of_the_allowed_types_"></span><span id="_1054__FATAL_____FILENAME___LINE_____IDENTIFIER__IN_INDEX_CLAUSE_DOES_NOT_RESOLVE_TO_ONE_OF_THE_ALLOWED_TYPES_"></span>**<1054,> fatal: " <fileName> : <linha \#>: <identifier> na cláusula index não é resolvida para um dos tipos permitidos"**</span><span class="sxs-lookup"><span data-stu-id="f5494-114"><span id="_1054__Fatal_____fileName___line_____identifier__in_INDEX_clause_does_not_resolve_to_one_of_the_allowed_types_"></span><span id="_1054__fatal_____filename___line_____identifier__in_index_clause_does_not_resolve_to_one_of_the_allowed_types_"></span><span id="_1054__FATAL_____FILENAME___LINE_____IDENTIFIER__IN_INDEX_CLAUSE_DOES_NOT_RESOLVE_TO_ONE_OF_THE_ALLOWED_TYPES_"></span>**<1054, Fatal>: "<fileName>:<line\#>: <identifier> in INDEX clause does not resolve to one of the allowed types"**</span></span>
</dt> <dd>

<span data-ttu-id="f5494-115">Erro semântico do módulo de invocação de macro do **tipo de objeto** .</span><span class="sxs-lookup"><span data-stu-id="f5494-115">**OBJECT-TYPE** macro invocation module semantic error.</span></span> <span data-ttu-id="f5494-116">O tipo de um objeto na cláusula INDEX ou qualquer tipo especificado na cláusula INDEX, deve ser resolvido para um tipo escalar, ou seja, uma não sequência ou não sequência de tipo.</span><span class="sxs-lookup"><span data-stu-id="f5494-116">The type of an object in the INDEX clause, or any type specified in the INDEX clause, must resolve to a scalar type, that is, a non-SEQUENCE or non-SEQUENCE OF type.</span></span> <span data-ttu-id="f5494-117">Qualquer tipo especificado na cláusula INDEX também deve ser resolvido para um deles.</span><span class="sxs-lookup"><span data-stu-id="f5494-117">Any type specified in the INDEX clause must also resolve to one of these.</span></span>

<span data-ttu-id="f5494-118">Esse erro pode ocorrer em SNMPv1 ou SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="f5494-118">This error can occur in either SNMPv1 or SNMPv2C.</span></span>

</dd> </dl>

## <a name="fatal-error-1055"></a><span data-ttu-id="f5494-119">Erro fatal 1055</span><span class="sxs-lookup"><span data-stu-id="f5494-119">Fatal Error 1055</span></span>

<dl> <dt>

<span data-ttu-id="f5494-120"><span id="_1055__Fatal____fileName___line____SYNTAX_of_INDEX_OBJECT-TYPE__identifier___does_not_resolve_to_one_of_the_allowed_types_"></span><span id="_1055__fatal____filename___line____syntax_of_index_object-type__identifier___does_not_resolve_to_one_of_the_allowed_types_"></span><span id="_1055__FATAL____FILENAME___LINE____SYNTAX_OF_INDEX_OBJECT-TYPE__IDENTIFIER___DOES_NOT_RESOLVE_TO_ONE_OF_THE_ALLOWED_TYPES_"></span>**<1055, fatal>: " <fileName> : <linha \#>: a sintaxe do tipo de objeto de índice <identifier> , não é resolvida para um dos tipos permitidos"**</span><span class="sxs-lookup"><span data-stu-id="f5494-120"><span id="_1055__Fatal____fileName___line____SYNTAX_of_INDEX_OBJECT-TYPE__identifier___does_not_resolve_to_one_of_the_allowed_types_"></span><span id="_1055__fatal____filename___line____syntax_of_index_object-type__identifier___does_not_resolve_to_one_of_the_allowed_types_"></span><span id="_1055__FATAL____FILENAME___LINE____SYNTAX_OF_INDEX_OBJECT-TYPE__IDENTIFIER___DOES_NOT_RESOLVE_TO_ONE_OF_THE_ALLOWED_TYPES_"></span>**<1055, Fatal>:"<fileName>:<line\#>: SYNTAX of INDEX OBJECT-TYPE <identifier>, does not resolve to one of the allowed types"**</span></span>
</dt> <dd>

<span data-ttu-id="f5494-121">Erro semântico do módulo de invocação de macro do **tipo de objeto** .</span><span class="sxs-lookup"><span data-stu-id="f5494-121">**OBJECT-TYPE** macro invocation module semantic error.</span></span> <span data-ttu-id="f5494-122">O tipo de um objeto na cláusula INDEX ou qualquer tipo especificado na cláusula INDEX, deve ser resolvido para um tipo escalar, ou seja, uma não sequência ou não sequência de tipo.</span><span class="sxs-lookup"><span data-stu-id="f5494-122">The type of an object in the INDEX clause, or any type specified in the INDEX clause, must resolve to a scalar type, that is, a non-SEQUENCE or non-SEQUENCE OF type.</span></span>

<span data-ttu-id="f5494-123">Esse erro pode ocorrer em SNMPv1 ou SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="f5494-123">This error can occur in either SNMPv1 or SNMPv2C.</span></span>

</dd> </dl>

 

 



