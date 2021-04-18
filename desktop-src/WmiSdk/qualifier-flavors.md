---
description: Os tipos de qualificador fornecem mais informações sobre um qualificador, como se uma classe ou instância derivada pode substituir o valor original dos qualificadores.
ms.assetid: 6a0769ac-e16c-45e1-92b6-26e4969bf23d
ms.tgt_platform: multiple
title: Tipos de qualificadores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec8ddf6c2daea59931e533174c532e3d07b147a4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105773008"
---
# <a name="qualifier-flavors"></a><span data-ttu-id="eae91-103">Tipos de qualificadores</span><span class="sxs-lookup"><span data-stu-id="eae91-103">Qualifier Flavors</span></span>

<span data-ttu-id="eae91-104">Os tipos de qualificador fornecem mais informações sobre um qualificador, como se uma classe ou instância derivada pode substituir o valor original do qualificador.</span><span class="sxs-lookup"><span data-stu-id="eae91-104">Qualifier flavors provide more information about a qualifier, such as whether a derived class or instance can override the qualifier's original value.</span></span>

<span data-ttu-id="eae91-105">Os tipos de qualificador podem ser adicionados à parte superior do arquivo MOF, usando a sintaxe a seguir, fazendo com que eles sejam aplicados em toda a definição.</span><span class="sxs-lookup"><span data-stu-id="eae91-105">Qualifier flavors may be added to the top of the MOF file, using the following syntax, causing them to be applied throughout the definition.</span></span> <span data-ttu-id="eae91-106">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="eae91-106">For example:</span></span>

``` syntax
Qualifier Description : ToSubClass Amended;
```

<span data-ttu-id="eae91-107">Os tipos **ToSubClass** e **emendados** se aplicam a todos os qualificadores de **Descrição** no MOF.</span><span class="sxs-lookup"><span data-stu-id="eae91-107">The **ToSubClass** and **Amended** flavors applies to all the **Description** qualifiers in the MOF.</span></span>

<span data-ttu-id="eae91-108">A tabela a seguir lista os tipos de qualificador.</span><span class="sxs-lookup"><span data-stu-id="eae91-108">The following table lists the qualifier flavors.</span></span>



| <span data-ttu-id="eae91-109">Tipo de qualificador</span><span class="sxs-lookup"><span data-stu-id="eae91-109">Qualifier Flavor</span></span>    | <span data-ttu-id="eae91-110">Significado</span><span class="sxs-lookup"><span data-stu-id="eae91-110">Meaning</span></span>                                                                                                                                                                                                                                         |
|---------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eae91-111">**Adicionados**</span><span class="sxs-lookup"><span data-stu-id="eae91-111">**Amended**</span></span>         | <span data-ttu-id="eae91-112">O qualificador não é necessário na definição de classe básica e pode ser movido para o aditamento a ser localizado.</span><span class="sxs-lookup"><span data-stu-id="eae91-112">The qualifier is not required in the basic class definition and can be moved to the amendment to be localized.</span></span>                                                                                                                                  |
| <span data-ttu-id="eae91-113">**DisableOverride**</span><span class="sxs-lookup"><span data-stu-id="eae91-113">**DisableOverride**</span></span> | <span data-ttu-id="eae91-114">O qualificador não pode ser substituído em uma instância ou classe derivada.</span><span class="sxs-lookup"><span data-stu-id="eae91-114">The qualifier cannot be overridden in a derived class or instance.</span></span> <span data-ttu-id="eae91-115">Observe que a capacidade de substituir um qualificador propagado é o padrão.</span><span class="sxs-lookup"><span data-stu-id="eae91-115">Note that being able to override a propagated qualifier is the default.</span></span>                                                                                                      |
| <span data-ttu-id="eae91-116">**EnableOverride**</span><span class="sxs-lookup"><span data-stu-id="eae91-116">**EnableOverride**</span></span>  | <span data-ttu-id="eae91-117">Quando propagada para uma classe ou instância derivada, o valor do qualificador pode ser substituído.</span><span class="sxs-lookup"><span data-stu-id="eae91-117">When propagated to a derived class or instance, the value of the qualifier can be overridden.</span></span> <span data-ttu-id="eae91-118">A configuração de **EnableOverride** é opcional porque a capacidade de substituir o valor do qualificador é a funcionalidade padrão para qualificadores propagados.</span><span class="sxs-lookup"><span data-stu-id="eae91-118">Setting **EnableOverride** is optional because being able to override the qualifier value is the default functionality for propagated qualifiers.</span></span> |
| <span data-ttu-id="eae91-119">**NotToInstance**</span><span class="sxs-lookup"><span data-stu-id="eae91-119">**NotToInstance**</span></span>   | <span data-ttu-id="eae91-120">O qualificador não é propagado para instâncias de classe.</span><span class="sxs-lookup"><span data-stu-id="eae91-120">The qualifier is not propagated to class instances.</span></span>                                                                                                                                                                                             |
| <span data-ttu-id="eae91-121">**NotToSubClass**</span><span class="sxs-lookup"><span data-stu-id="eae91-121">**NotToSubClass**</span></span>   | <span data-ttu-id="eae91-122">O qualificador não é propagado para classes derivadas.</span><span class="sxs-lookup"><span data-stu-id="eae91-122">The qualifier is not propagated to derived classes.</span></span>                                                                                                                                                                                             |
| <span data-ttu-id="eae91-123">**Restricted**</span><span class="sxs-lookup"><span data-stu-id="eae91-123">**Restricted**</span></span>      | <span data-ttu-id="eae91-124">O qualificador não é propagado para instâncias ou classes derivadas.</span><span class="sxs-lookup"><span data-stu-id="eae91-124">The qualifier is not propagated to instances or derived classes.</span></span>                                                                                                                                                                                |
| <span data-ttu-id="eae91-125">**ToInstance**</span><span class="sxs-lookup"><span data-stu-id="eae91-125">**ToInstance**</span></span>      | <span data-ttu-id="eae91-126">O qualificador é propagado para instâncias.</span><span class="sxs-lookup"><span data-stu-id="eae91-126">The qualifier is propagated to instances.</span></span>                                                                                                                                                                                                       |
| <span data-ttu-id="eae91-127">**ToSubClass**</span><span class="sxs-lookup"><span data-stu-id="eae91-127">**ToSubClass**</span></span>      | <span data-ttu-id="eae91-128">O qualificador é propagado para classes derivadas.</span><span class="sxs-lookup"><span data-stu-id="eae91-128">The qualifier is propagated to derived classes.</span></span> <span data-ttu-id="eae91-129">Esse tipo é apropriado apenas para qualificadores definidos para uma classe e não pode ser anexado a um qualificador que descreve uma instância de classe.</span><span class="sxs-lookup"><span data-stu-id="eae91-129">This flavor is only appropriate for qualifiers defined for a class and cannot be attached to a qualifier describing a class instance.</span></span>                                                           |



 

 

 



