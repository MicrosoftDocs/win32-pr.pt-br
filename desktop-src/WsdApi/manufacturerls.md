---
description: Especifica uma versão localizada do nome do fabricante.
ms.assetid: e87de50f-60ec-4c18-b21c-81f7b6928752
title: elemento manufacturerLS
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5d24950355c5439d9a99c4ef451f1330772f3459
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107993673"
---
# <a name="manufacturerls-element"></a><span data-ttu-id="cfc17-103">elemento manufacturerLS</span><span class="sxs-lookup"><span data-stu-id="cfc17-103">manufacturerLS element</span></span>

<span data-ttu-id="cfc17-104">Especifica uma versão localizada do nome do fabricante.</span><span class="sxs-lookup"><span data-stu-id="cfc17-104">Specifies a localized version of the manufacturer name.</span></span>

## <a name="usage"></a><span data-ttu-id="cfc17-105">Uso</span><span class="sxs-lookup"><span data-stu-id="cfc17-105">Usage</span></span>

``` syntax
<manufacturerLS
  Language = "language identifier string"
  Data = "localized manufacturer name string"/>
```

## <a name="attributes"></a><span data-ttu-id="cfc17-106">Atributos</span><span class="sxs-lookup"><span data-stu-id="cfc17-106">Attributes</span></span>



| <span data-ttu-id="cfc17-107">Atributo</span><span class="sxs-lookup"><span data-stu-id="cfc17-107">Attribute</span></span>               | <span data-ttu-id="cfc17-108">Type</span><span class="sxs-lookup"><span data-stu-id="cfc17-108">Type</span></span>                                          | <span data-ttu-id="cfc17-109">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="cfc17-109">Required</span></span>       | <span data-ttu-id="cfc17-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="cfc17-110">Description</span></span>                                                             |
|-------------------------|-----------------------------------------------|----------------|-------------------------------------------------------------------------|
| <span data-ttu-id="cfc17-111">**Dados**</span><span class="sxs-lookup"><span data-stu-id="cfc17-111">**Data**</span></span><br/>     | <span data-ttu-id="cfc17-112">Cadeia de caracteres do nome do fabricante localizado</span><span class="sxs-lookup"><span data-stu-id="cfc17-112">localized manufacturer name string</span></span><br/> | <span data-ttu-id="cfc17-113">Sim</span><span class="sxs-lookup"><span data-stu-id="cfc17-113">Yes</span></span><br/> | <span data-ttu-id="cfc17-114">O nome do fabricante localizado.</span><span class="sxs-lookup"><span data-stu-id="cfc17-114">The localized manufacturer name.</span></span><br/> <br/>                 |
| <span data-ttu-id="cfc17-115">**Linguagem**</span><span class="sxs-lookup"><span data-stu-id="cfc17-115">**Language**</span></span><br/> | <span data-ttu-id="cfc17-116">Cadeia de caracteres do identificador de idioma</span><span class="sxs-lookup"><span data-stu-id="cfc17-116">language identifier string</span></span><br/>         | <span data-ttu-id="cfc17-117">Sim</span><span class="sxs-lookup"><span data-stu-id="cfc17-117">Yes</span></span><br/> | <span data-ttu-id="cfc17-118">O idioma do nome do fabricante localizado.</span><span class="sxs-lookup"><span data-stu-id="cfc17-118">The language of the localized manufacturer name.</span></span><br/> <br/> |



## <a name="child-elements"></a><span data-ttu-id="cfc17-119">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="cfc17-119">Child elements</span></span>

<span data-ttu-id="cfc17-120">Não há elementos filho.</span><span class="sxs-lookup"><span data-stu-id="cfc17-120">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="cfc17-121">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="cfc17-121">Parent elements</span></span>



| <span data-ttu-id="cfc17-122">Elemento</span><span class="sxs-lookup"><span data-stu-id="cfc17-122">Element</span></span>                                                   | <span data-ttu-id="cfc17-123">Descrição</span><span class="sxs-lookup"><span data-stu-id="cfc17-123">Description</span></span>                                                                                          |
|-----------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="cfc17-124">**thisModelMetadata**</span><span class="sxs-lookup"><span data-stu-id="cfc17-124">**thisModelMetadata**</span></span>](thismodelmetadata.md)<br/> | <span data-ttu-id="cfc17-125">Define os metadados de modelo e fabricante para o dispositivo a ser implementado.</span><span class="sxs-lookup"><span data-stu-id="cfc17-125">Defines the manufacturer and model metadata for the device to be implemented.</span></span><br/> <br/> |



## <a name="element-information"></a><span data-ttu-id="cfc17-126">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="cfc17-126">Element information</span></span>



| <span data-ttu-id="cfc17-127">Label</span><span class="sxs-lookup"><span data-stu-id="cfc17-127">Label</span></span> | <span data-ttu-id="cfc17-128">Valor</span><span class="sxs-lookup"><span data-stu-id="cfc17-128">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="cfc17-129">Sistema mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cfc17-129">Minimum supported system</span></span><br/> | <span data-ttu-id="cfc17-130">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="cfc17-130">Windows Vista</span></span> |
| <span data-ttu-id="cfc17-131">Pode estar vazio</span><span class="sxs-lookup"><span data-stu-id="cfc17-131">Can be empty</span></span>                        | <span data-ttu-id="cfc17-132">Sim</span><span class="sxs-lookup"><span data-stu-id="cfc17-132">Yes</span></span>           |



 

 




