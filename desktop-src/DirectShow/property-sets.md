---
description: Conjuntos de propriedades
ms.assetid: 4b8a917f-7a6c-4433-83f4-b83ef6d26115
title: Conjuntos de Propriedades (DirectShow)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fcdc65efbc99eeed3a5f94ab33ce5ec982975852
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104370171"
---
# <a name="property-sets-directshow"></a><span data-ttu-id="aace0-103">Conjuntos de Propriedades (DirectShow)</span><span class="sxs-lookup"><span data-stu-id="aace0-103">Property Sets (DirectShow)</span></span>

<span data-ttu-id="aace0-104">O Microsoft DirectShow usa conjuntos de propriedades para dar suporte a serviços estendidos oferecidos por hardware e seus drivers e filtros associados.</span><span class="sxs-lookup"><span data-stu-id="aace0-104">Microsoft DirectShow uses property sets to support extended services offered by hardware and its associated drivers and filters.</span></span> <span data-ttu-id="aace0-105">Fornecedores de hardware e filtro podem definir novos recursos como propriedades, organizá-los em conjuntos de propriedades e publicar a especificação para esses conjuntos de propriedades.</span><span class="sxs-lookup"><span data-stu-id="aace0-105">Hardware and filter vendors can define new capabilities as properties, arrange them in property sets, and publish the specification for these property sets.</span></span> <span data-ttu-id="aace0-106">Como desenvolvedor do aplicativo, você pode usar os métodos da interface [**IKsPropertySet**](ikspropertyset.md) para determinar se um driver ou filtro dá suporte a um determinado conjunto de propriedades e recuperar ou definir essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="aace0-106">As the application developer, you can use the methods of the [**IKsPropertySet**](ikspropertyset.md) interface to determine whether a driver or filter supports a particular set of properties, and retrieve or set those properties.</span></span>

<span data-ttu-id="aace0-107">Todos os métodos expostos por **IKsPropertySet** exigem um **GUID** que identifica o conjunto de Propriedades (o parâmetro *guidPropSet* ) e um **DWORD** que identifica a propriedade dentro do conjunto de Propriedades (o parâmetro *dwPropId* ).</span><span class="sxs-lookup"><span data-stu-id="aace0-107">All the methods exposed by **IKsPropertySet** require a **GUID** that identifies the property set (the *guidPropSet* parameter) and a **DWORD** that identifies the property within the property set (the *dwPropID* parameter).</span></span> <span data-ttu-id="aace0-108">O parâmetro *dwPropId* normalmente é um membro de um tipo de dados enumerado.</span><span class="sxs-lookup"><span data-stu-id="aace0-108">The *dwPropID* parameter is typically a member of an enumerated data type.</span></span>

<span data-ttu-id="aace0-109">As propriedades individuais podem ter dados associados que você especifica no parâmetro *pPropData* nos métodos [**IKsPropertySet:: Set**](ikspropertyset-set.md) e [**IKsPropertySet:: Get**](ikspropertyset-get.md) .</span><span class="sxs-lookup"><span data-stu-id="aace0-109">Individual properties can have associated data that you specify in the *pPropData* parameter in the [**IKsPropertySet::Set**](ikspropertyset-set.md) and [**IKsPropertySet::Get**](ikspropertyset-get.md) methods.</span></span> <span data-ttu-id="aace0-110">Nesses métodos, os dados de propriedade são digitados como um ponteiro para `void` .</span><span class="sxs-lookup"><span data-stu-id="aace0-110">In these methods, the property data is typed as a pointer to `void`.</span></span> <span data-ttu-id="aace0-111">O tipo de dados e o significado dos dados são especificados na definição do conjunto de propriedades.</span><span class="sxs-lookup"><span data-stu-id="aace0-111">The data type and the meaning of the data are specified in the definition of the property set.</span></span>

<span data-ttu-id="aace0-112">As seções a seguir fornecem informações sobre os conjuntos de propriedades com suporte no DirectShow:</span><span class="sxs-lookup"><span data-stu-id="aace0-112">The following sections provide information about the property sets supported in DirectShow:</span></span>

-   [<span data-ttu-id="aace0-113">**Conjunto de propriedades da proteção contra cópia de DVD**</span><span class="sxs-lookup"><span data-stu-id="aace0-113">**DVD Copy Protection Property Set**</span></span>](dvd-copy-protection-property-set.md)
-   [<span data-ttu-id="aace0-114">**Conjunto de propriedades de karaokê de DVD**</span><span class="sxs-lookup"><span data-stu-id="aace0-114">**DVD Karaoke Property Set**</span></span>](dvd-karaoke-property-set.md)
-   [<span data-ttu-id="aace0-115">**Conjunto de propriedades de subimagem de DVD**</span><span class="sxs-lookup"><span data-stu-id="aace0-115">**DVD Subpicture Property Set**</span></span>](dvd-subpicture-property-set.md)
-   [<span data-ttu-id="aace0-116">Conjunto de propriedades de transporte de dispositivo externo</span><span class="sxs-lookup"><span data-stu-id="aace0-116">External Device Transport Property Set</span></span>](external-device-transport-property-set.md)
-   [<span data-ttu-id="aace0-117">Conjunto de propriedades de revisão do quadro</span><span class="sxs-lookup"><span data-stu-id="aace0-117">Frame Stepping Property Set</span></span>](frame-stepping-property-set.md)
-   [<span data-ttu-id="aace0-118">Conjunto de propriedades de PIN</span><span class="sxs-lookup"><span data-stu-id="aace0-118">Pin Property Set</span></span>](pin-property-set.md)
-   [<span data-ttu-id="aace0-119">**Conjunto de propriedades de alteração de taxa**</span><span class="sxs-lookup"><span data-stu-id="aace0-119">**Rate Change Property Set**</span></span>](rate-change-property-set.md)

 

 



