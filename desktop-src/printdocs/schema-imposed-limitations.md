---
description: Saiba mais sobre as limitações impostas pelo esquema de PrintCapabilities. O provedor de PrintCapabilities deve detectar inválidas de configurações e resolvê-las.
ms.assetid: 420c5c84-abb8-495a-9b74-dc19a16034fb
title: Limitações de Schema-Imposed
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ee2911d4b90ebc194aa245f398f71575496c877
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112404919"
---
# <a name="schema-imposed-limitations"></a><span data-ttu-id="554d1-104">Limitações de Schema-Imposed</span><span class="sxs-lookup"><span data-stu-id="554d1-104">Schema-Imposed Limitations</span></span>

<span data-ttu-id="554d1-105">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="554d1-105">This topic is not current.</span></span> <span data-ttu-id="554d1-106">Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="554d1-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="554d1-107">O esquema de PrintCapabilities fornece aos autores de PrintCapabilities uma quantidade significativa de flexibilidade e expressividade que pode ser utilizada em descrições de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="554d1-107">The PrintCapabilities Schema provides PrintCapabilities authors with a substantial amount of flexibility and expressiveness that can be utilized in device descriptions.</span></span> <span data-ttu-id="554d1-108">No entanto, as dependências de configuração impõem uma limitação nessa flexibilidade e na expressividade.</span><span class="sxs-lookup"><span data-stu-id="554d1-108">However, configuration dependencies impose a limitation on this flexibility and expressiveness.</span></span> <span data-ttu-id="554d1-109">Instâncias de ParameterDef, a lista de elementos de recurso, a lista de instâncias de opção dentro de cada recurso e as instâncias de ScoredProperty dentro de cada opção não devem conter dependências de configuração.</span><span class="sxs-lookup"><span data-stu-id="554d1-109">ParameterDef instances, the list of Feature elements, the list of Option instances within each Feature, and the ScoredProperty instances within each Option must not contain configuration dependencies.</span></span> <span data-ttu-id="554d1-110">O provedor de documentos PrintCapabilities deve detectar combinações inválidas de configurações e deve resolvê-las.</span><span class="sxs-lookup"><span data-stu-id="554d1-110">The PrintCapabilities document provider must detect invalid combinations of configurations and must resolve them.</span></span>

## <a name="related-topics"></a><span data-ttu-id="554d1-111">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="554d1-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="554d1-112">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="554d1-112">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



