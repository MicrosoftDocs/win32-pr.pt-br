---
description: Este tópico não é atual. Para obter as informações mais atuais, consulte a especificação do esquema de impressão.
ms.assetid: 7f08747f-f7ff-4381-b2b9-1917e4708ee3
title: Palavras-chave públicas de PrintCapabilities
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81d5e7b001a8106f95c830f0af5e99ee9821af64
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/05/2021
ms.locfileid: "105753686"
---
# <a name="printcapabilities-public-keywords"></a><span data-ttu-id="6b096-104">Palavras-chave públicas de PrintCapabilities</span><span class="sxs-lookup"><span data-stu-id="6b096-104">PrintCapabilities Public Keywords</span></span>

<span data-ttu-id="6b096-105">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="6b096-105">This topic is not current.</span></span> <span data-ttu-id="6b096-106">Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="6b096-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="6b096-107">A seção a seguir especifica os elementos configuráveis pelo usuário e as definições de parâmetro que podem ser aplicáveis a um documento de PrintCapabilities.</span><span class="sxs-lookup"><span data-stu-id="6b096-107">The following section specifies both user configurable elements and parameter definitions which may be applicable to a PrintCapabilities document.</span></span>

## <a name="user-configurable-elements-usage"></a><span data-ttu-id="6b096-108">Uso de elementos configuráveis pelo usuário</span><span class="sxs-lookup"><span data-stu-id="6b096-108">User Configurable Elements Usage</span></span>

<span data-ttu-id="6b096-109">Os elementos configuráveis pelo usuário representam as palavras-chave públicas do esquema de impressão que podem aparecer em um documento de PrintCapabilities ou em um PrintTicket.</span><span class="sxs-lookup"><span data-stu-id="6b096-109">User Configurable Elements represent Print Schema Public Keywords which may appear in either a PrintCapabilities document or a PrintTicket.</span></span> <span data-ttu-id="6b096-110">Eles têm a finalidade de representar os atributos de dispositivo configuráveis com suporte em um dispositivo específico ou comunicar a intenção de configuração de impressão por um aplicativo ou usuário.</span><span class="sxs-lookup"><span data-stu-id="6b096-110">They are intended to represent configurable device attributes supported by a specific device or communicate print setting intent by an application or user.</span></span>

<span data-ttu-id="6b096-111">Elementos configuráveis pelo usuário podem referenciar elementos de referência de parâmetro.</span><span class="sxs-lookup"><span data-stu-id="6b096-111">User Configurable Elements may reference Parameter Reference Elements.</span></span> <span data-ttu-id="6b096-112">Para obter mais informações, consulte a seção [elementos de referência de parâmetro](parameter-reference-elements.md) .</span><span class="sxs-lookup"><span data-stu-id="6b096-112">For more information, please refer to [Parameter Reference Elements](parameter-reference-elements.md) section.</span></span>

## <a name="parameter-definitions-usage"></a><span data-ttu-id="6b096-113">Uso de definições de parâmetro</span><span class="sxs-lookup"><span data-stu-id="6b096-113">Parameter Definitions Usage</span></span>

<span data-ttu-id="6b096-114">As definições de parâmetros assumem a forma de tipos de elementos ParameterDef em um documento de recursos de impressão.</span><span class="sxs-lookup"><span data-stu-id="6b096-114">Parameters definitions take the form of ParameterDef element types in a Print Capabilities document.</span></span> <span data-ttu-id="6b096-115">Os tipos de elementos ParameterDef são inicializados em um PrintTicket usando o tipo de elemento ParameterInit.</span><span class="sxs-lookup"><span data-stu-id="6b096-115">ParameterDef element types are initialized in a PrintTicket using the ParameterInit element type.</span></span> <span data-ttu-id="6b096-116">O valor do parâmetro será especificado usando o elemento ParameterInit.</span><span class="sxs-lookup"><span data-stu-id="6b096-116">The value of the parameter will be specified using the ParameterInit element.</span></span> <span data-ttu-id="6b096-117">Uma palavra-chave configurável pelo usuário pode fazer referência a uma definição de parâmetro usando o tipo de elemento ParameterRef.</span><span class="sxs-lookup"><span data-stu-id="6b096-117">A user configurable keyword may reference a parameter definition using the ParameterRef element type.</span></span> <span data-ttu-id="6b096-118">Para obter mais informações, consulte a seção [construções de parâmetro](parameter-constructs.md) .</span><span class="sxs-lookup"><span data-stu-id="6b096-118">For more information, please refer to [Parameter Constructs](parameter-constructs.md) section.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6b096-119">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="6b096-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6b096-120">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="6b096-120">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



