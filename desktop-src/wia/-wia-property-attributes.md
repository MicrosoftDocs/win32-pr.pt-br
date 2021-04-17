---
description: Todos os objetos de item têm propriedades.
ms.assetid: 00e04790-e319-41b3-b88f-8064912b91b1
title: Atributos de propriedade (WIA)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47c635cb0d4e21fe2a1d65a3f21254f8e9c04d64
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104461144"
---
# <a name="property-attributes-wia"></a><span data-ttu-id="ba582-103">Atributos de propriedade (WIA)</span><span class="sxs-lookup"><span data-stu-id="ba582-103">Property Attributes (WIA)</span></span>

<span data-ttu-id="ba582-104">Todos os objetos de item têm propriedades.</span><span class="sxs-lookup"><span data-stu-id="ba582-104">All item objects have properties.</span></span> <span data-ttu-id="ba582-105">As propriedades têm atributos.</span><span class="sxs-lookup"><span data-stu-id="ba582-105">The properties have attributes.</span></span> <span data-ttu-id="ba582-106">Por exemplo, atributos de propriedade indicam se uma propriedade é lida, gravada ou excluída.</span><span class="sxs-lookup"><span data-stu-id="ba582-106">For instance, property attributes indicate whether a property is read from, written to, or deleted.</span></span> <span data-ttu-id="ba582-107">Eles também indicam os valores de propriedade válidos.</span><span class="sxs-lookup"><span data-stu-id="ba582-107">They also indicate the valid property values.</span></span> <span data-ttu-id="ba582-108">As constantes a seguir são atributos de propriedade válidos:</span><span class="sxs-lookup"><span data-stu-id="ba582-108">The following constants are valid property attributes:</span></span> 

| <span data-ttu-id="ba582-109">Atributo de propriedade</span><span class="sxs-lookup"><span data-stu-id="ba582-109">Property Attribute</span></span>        | <span data-ttu-id="ba582-110">Significado</span><span class="sxs-lookup"><span data-stu-id="ba582-110">Meaning</span></span>                                                                                                  |
|---------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ba582-111">\_propproperty \_ armazenável em cache</span><span class="sxs-lookup"><span data-stu-id="ba582-111">WIA\_PROP\_CACHEABLE</span></span>      | <span data-ttu-id="ba582-112">O dispositivo pode armazenar em cache o valor da propriedade.</span><span class="sxs-lookup"><span data-stu-id="ba582-112">The device can cache the property's value.</span></span>                                                               |
| <span data-ttu-id="ba582-113">\_sinalizador de prop WIA \_</span><span class="sxs-lookup"><span data-stu-id="ba582-113">WIA\_PROP\_FLAG</span></span>           | <span data-ttu-id="ba582-114">A propriedade tem uma lista de valores de sinalizador legais.</span><span class="sxs-lookup"><span data-stu-id="ba582-114">The property has a list of legal flag values.</span></span> <span data-ttu-id="ba582-115">Os valores de sinalizador são combinados por meio de uma operação **or** .</span><span class="sxs-lookup"><span data-stu-id="ba582-115">Flag values are combined using a bitwise **OR** operation.</span></span> |
| <span data-ttu-id="ba582-116">\_lista de propriedades do WIA \_</span><span class="sxs-lookup"><span data-stu-id="ba582-116">WIA\_PROP\_LIST</span></span>           | <span data-ttu-id="ba582-117">A propriedade tem uma lista de valores válidos.</span><span class="sxs-lookup"><span data-stu-id="ba582-117">The property has a list of legal values.</span></span>                                                                 |
| <span data-ttu-id="ba582-118">PROP. do WIA \_ \_</span><span class="sxs-lookup"><span data-stu-id="ba582-118">WIA\_PROP\_NONE</span></span>           | <span data-ttu-id="ba582-119">A propriedade não tem nenhum valor válido associado a ela.</span><span class="sxs-lookup"><span data-stu-id="ba582-119">The property does not have any valid values associated with it.</span></span>                                          |
| <span data-ttu-id="ba582-120">\_intervalo de prop WIA \_</span><span class="sxs-lookup"><span data-stu-id="ba582-120">WIA\_PROP\_RANGE</span></span>          | <span data-ttu-id="ba582-121">A propriedade tem um intervalo de valores válidos.</span><span class="sxs-lookup"><span data-stu-id="ba582-121">The property has a range of valid values.</span></span>                                                                |
| <span data-ttu-id="ba582-122">\_leitura de prop WIA \_</span><span class="sxs-lookup"><span data-stu-id="ba582-122">WIA\_PROP\_READ</span></span>           | <span data-ttu-id="ba582-123">O aplicativo pode ler o valor da propriedade.</span><span class="sxs-lookup"><span data-stu-id="ba582-123">The application can read the property's value.</span></span>                                                           |
| <span data-ttu-id="ba582-124">\_RW prop do WIA \_</span><span class="sxs-lookup"><span data-stu-id="ba582-124">WIA\_PROP\_RW</span></span>             | <span data-ttu-id="ba582-125">O aplicativo pode ler e gravar o valor da propriedade.</span><span class="sxs-lookup"><span data-stu-id="ba582-125">The application can read and write the property's value.</span></span>                                                 |
| <span data-ttu-id="ba582-126">sincronização de prop do WIA \_ \_ \_ necessária</span><span class="sxs-lookup"><span data-stu-id="ba582-126">WIA\_PROP\_SYNC\_REQUIRED</span></span> | <span data-ttu-id="ba582-127">Não use.</span><span class="sxs-lookup"><span data-stu-id="ba582-127">Do not use.</span></span>                                                                                              |
| <span data-ttu-id="ba582-128">\_gravação de prop WIA \_</span><span class="sxs-lookup"><span data-stu-id="ba582-128">WIA\_PROP\_WRITE</span></span>          | <span data-ttu-id="ba582-129">O aplicativo pode gravar o valor da propriedade.</span><span class="sxs-lookup"><span data-stu-id="ba582-129">The application can write the property's value.</span></span>                                                          |



 

 

 



