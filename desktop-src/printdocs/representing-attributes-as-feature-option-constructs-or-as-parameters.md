---
description: Representa atributos como construções de recurso/opção ou como parâmetros. Este tópico não é atual. Para obter as informações mais atuais, consulte a especificação do esquema de impressão.
ms.assetid: 055e502d-631f-49d2-8577-65396373d478
title: Representando atributos como construções de recurso/opção ou como parâmetros
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c93f4de56709ed310a7f0aa259b1dbfd3377ed42
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120051"
---
# <a name="representing-attributes-as-featureoption-constructs-or-as-parameters"></a><span data-ttu-id="0d9e7-105">Representando atributos como construções de recurso/opção ou como parâmetros</span><span class="sxs-lookup"><span data-stu-id="0d9e7-105">Representing Attributes as Feature/Option Constructs or as Parameters</span></span>

<span data-ttu-id="0d9e7-106">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="0d9e7-106">This topic is not current.</span></span> <span data-ttu-id="0d9e7-107">Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="0d9e7-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="0d9e7-108">O autor de um documento de PrintCapabilities define os atributos de dispositivo que compõem a configuração.</span><span class="sxs-lookup"><span data-stu-id="0d9e7-108">The author of a PrintCapabilities document defines device attributes that make up the configuration.</span></span> <span data-ttu-id="0d9e7-109">No documento PrintCapabilities, o autor pode optar por representar um atributo de dispositivo como um constructo de recurso/opção ou como uma construção de parâmetro.</span><span class="sxs-lookup"><span data-stu-id="0d9e7-109">In the PrintCapabilities document, the author can choose to represent a device attribute either as a Feature/Option construct or as a parameter construct.</span></span>

<span data-ttu-id="0d9e7-110">Se um atributo de dispositivo tiver um número relativamente pequeno de Estados possíveis que não se enquadram em nenhum tipo de padrão óbvio, um constructo de recurso/opção será geralmente a melhor opção.</span><span class="sxs-lookup"><span data-stu-id="0d9e7-110">If a device attribute has a relatively small number of possible states that do not fall into any sort of obvious pattern, a Feature/Option construct is usually the better choice.</span></span> <span data-ttu-id="0d9e7-111">Por exemplo, se os valores permitidos para o atributo de dispositivo PageMediaSize forem os valores letra, ofício, A4ISO, tablóide e Envelope10, um constructo de recurso/opção seria a melhor opção para representação.</span><span class="sxs-lookup"><span data-stu-id="0d9e7-111">For example, if the allowed values for the PageMediaSize device attribute are the values Letter, Legal, A4ISO, Tabloid, and Envelope10, a Feature/Option construct would be the better choice for representation.</span></span> <span data-ttu-id="0d9e7-112">Devido à dificuldade e à ambiguidade associada à expressar os valores permitidos sem Enumeração explícita, a construção do parâmetro não é apropriada para o atributo PageMediaSize.</span><span class="sxs-lookup"><span data-stu-id="0d9e7-112">Because of the difficulty and ambiguity associated with expressing the allowable values without explicit enumeration, the parameter construct is not appropriate for the PageMediaSize attribute.</span></span>

<span data-ttu-id="0d9e7-113">Se um atributo de dispositivo puder ser representado por um intervalo de inteiros, a representação de parâmetro geralmente é a melhor opção, especialmente para intervalos que incluem muitos valores.</span><span class="sxs-lookup"><span data-stu-id="0d9e7-113">If a device attribute can be represented by a range of integers, parameter representation is usually the better choice, especially for ranges that include many values.</span></span> <span data-ttu-id="0d9e7-114">Por exemplo, se o atributo de dispositivo CopyCount para um modelo específico de impressora puder variar de 1 a 99.999, esse atributo deverá ser Categorizado como um parâmetro, definindo uma instância de ParameterDef.</span><span class="sxs-lookup"><span data-stu-id="0d9e7-114">For example, if the CopyCount device attribute for a particular model of printer can range from 1 through 99,999, then this attribute should be categorized as a parameter, by defining a ParameterDef instance.</span></span> <span data-ttu-id="0d9e7-115">Atribua valores às instâncias de propriedade padrão MinValue e MaxValue do elemento ParameterDef para definir o intervalo de valores para o atributo JobCopyCount.</span><span class="sxs-lookup"><span data-stu-id="0d9e7-115">Assign values to the MinValue and MaxValue standard Property instances of the ParameterDef element to define the range of values for the JobCopyCount attribute.</span></span> <span data-ttu-id="0d9e7-116">Devido ao grande número de valores que devem ser explicitamente listados como elementos de opção, a representação de recurso/opção não é apropriada para o atributo de dispositivo JobCopyCount.</span><span class="sxs-lookup"><span data-stu-id="0d9e7-116">Because of the large number of values that must be explicitly listed as Option elements, Feature/Option representation is not appropriate for the JobCopyCount device attribute.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0d9e7-117">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="0d9e7-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0d9e7-118">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="0d9e7-118">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



