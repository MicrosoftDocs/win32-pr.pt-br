---
description: Este tópico não é atual. Para obter as informações mais atuais, consulte a especificação do esquema de impressão.
ms.assetid: 055e502d-631f-49d2-8577-65396373d478
title: Representando atributos como construções de recurso/opção ou como parâmetros
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2c24843a175337f40a84dcdacc41e1a2ab1e15e
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/05/2021
ms.locfileid: "104011970"
---
# <a name="representing-attributes-as-featureoption-constructs-or-as-parameters"></a><span data-ttu-id="11697-104">Representando atributos como construções de recurso/opção ou como parâmetros</span><span class="sxs-lookup"><span data-stu-id="11697-104">Representing Attributes as Feature/Option Constructs or as Parameters</span></span>

<span data-ttu-id="11697-105">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="11697-105">This topic is not current.</span></span> <span data-ttu-id="11697-106">Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="11697-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="11697-107">O autor de um documento de PrintCapabilities define os atributos de dispositivo que compõem a configuração.</span><span class="sxs-lookup"><span data-stu-id="11697-107">The author of a PrintCapabilities document defines device attributes that make up the configuration.</span></span> <span data-ttu-id="11697-108">No documento PrintCapabilities, o autor pode optar por representar um atributo de dispositivo como um constructo de recurso/opção ou como uma construção de parâmetro.</span><span class="sxs-lookup"><span data-stu-id="11697-108">In the PrintCapabilities document, the author can choose to represent a device attribute either as a Feature/Option construct or as a parameter construct.</span></span>

<span data-ttu-id="11697-109">Se um atributo de dispositivo tiver um número relativamente pequeno de Estados possíveis que não se enquadram em nenhum tipo de padrão óbvio, um constructo de recurso/opção será geralmente a melhor opção.</span><span class="sxs-lookup"><span data-stu-id="11697-109">If a device attribute has a relatively small number of possible states that do not fall into any sort of obvious pattern, a Feature/Option construct is usually the better choice.</span></span> <span data-ttu-id="11697-110">Por exemplo, se os valores permitidos para o atributo de dispositivo PageMediaSize forem os valores letra, ofício, A4ISO, tablóide e Envelope10, um constructo de recurso/opção seria a melhor opção para representação.</span><span class="sxs-lookup"><span data-stu-id="11697-110">For example, if the allowed values for the PageMediaSize device attribute are the values Letter, Legal, A4ISO, Tabloid, and Envelope10, a Feature/Option construct would be the better choice for representation.</span></span> <span data-ttu-id="11697-111">Devido à dificuldade e à ambiguidade associada à expressar os valores permitidos sem Enumeração explícita, a construção do parâmetro não é apropriada para o atributo PageMediaSize.</span><span class="sxs-lookup"><span data-stu-id="11697-111">Because of the difficulty and ambiguity associated with expressing the allowable values without explicit enumeration, the parameter construct is not appropriate for the PageMediaSize attribute.</span></span>

<span data-ttu-id="11697-112">Se um atributo de dispositivo puder ser representado por um intervalo de inteiros, a representação de parâmetro geralmente é a melhor opção, especialmente para intervalos que incluem muitos valores.</span><span class="sxs-lookup"><span data-stu-id="11697-112">If a device attribute can be represented by a range of integers, parameter representation is usually the better choice, especially for ranges that include many values.</span></span> <span data-ttu-id="11697-113">Por exemplo, se o atributo de dispositivo CopyCount para um modelo específico de impressora puder variar de 1 a 99.999, esse atributo deverá ser Categorizado como um parâmetro, definindo uma instância de ParameterDef.</span><span class="sxs-lookup"><span data-stu-id="11697-113">For example, if the CopyCount device attribute for a particular model of printer can range from 1 through 99,999, then this attribute should be categorized as a parameter, by defining a ParameterDef instance.</span></span> <span data-ttu-id="11697-114">Atribua valores às instâncias de propriedade padrão MinValue e MaxValue do elemento ParameterDef para definir o intervalo de valores para o atributo JobCopyCount.</span><span class="sxs-lookup"><span data-stu-id="11697-114">Assign values to the MinValue and MaxValue standard Property instances of the ParameterDef element to define the range of values for the JobCopyCount attribute.</span></span> <span data-ttu-id="11697-115">Devido ao grande número de valores que devem ser explicitamente listados como elementos de opção, a representação de recurso/opção não é apropriada para o atributo de dispositivo JobCopyCount.</span><span class="sxs-lookup"><span data-stu-id="11697-115">Because of the large number of values that must be explicitly listed as Option elements, Feature/Option representation is not appropriate for the JobCopyCount device attribute.</span></span>

## <a name="related-topics"></a><span data-ttu-id="11697-116">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="11697-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="11697-117">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="11697-117">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



