---
description: Especifica uma versão localizada do nome do dispositivo.
ms.assetid: 67ebbca0-bdb2-4a6e-98d8-3d8d1029884f
title: elemento modelNameLS
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e47d2f83d1b636efc30e98dff8c46600bcee555d
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107995493"
---
# <a name="modelnamels-element"></a><span data-ttu-id="7277f-103">elemento modelNameLS</span><span class="sxs-lookup"><span data-stu-id="7277f-103">modelNameLS element</span></span>

<span data-ttu-id="7277f-104">Especifica uma versão localizada do nome do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7277f-104">Specifies a localized version of the device name.</span></span>

## <a name="usage"></a><span data-ttu-id="7277f-105">Uso</span><span class="sxs-lookup"><span data-stu-id="7277f-105">Usage</span></span>

``` syntax
<modelNameLS
  Language = "language identifier string"
  Data = "localized model name string"/>
```

## <a name="attributes"></a><span data-ttu-id="7277f-106">Atributos</span><span class="sxs-lookup"><span data-stu-id="7277f-106">Attributes</span></span>



| <span data-ttu-id="7277f-107">Atributo</span><span class="sxs-lookup"><span data-stu-id="7277f-107">Attribute</span></span>               | <span data-ttu-id="7277f-108">Type</span><span class="sxs-lookup"><span data-stu-id="7277f-108">Type</span></span>                                   | <span data-ttu-id="7277f-109">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="7277f-109">Required</span></span>       | <span data-ttu-id="7277f-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="7277f-110">Description</span></span>                                                      |
|-------------------------|----------------------------------------|----------------|------------------------------------------------------------------|
| <span data-ttu-id="7277f-111">**Dados**</span><span class="sxs-lookup"><span data-stu-id="7277f-111">**Data**</span></span><br/>     | <span data-ttu-id="7277f-112">Cadeia de caracteres de nome de modelo localizado</span><span class="sxs-lookup"><span data-stu-id="7277f-112">localized model name string</span></span><br/> | <span data-ttu-id="7277f-113">Sim</span><span class="sxs-lookup"><span data-stu-id="7277f-113">Yes</span></span><br/> | <span data-ttu-id="7277f-114">O nome do modelo localizado.</span><span class="sxs-lookup"><span data-stu-id="7277f-114">The localized model name.</span></span><br/> <br/>                 |
| <span data-ttu-id="7277f-115">**Linguagem**</span><span class="sxs-lookup"><span data-stu-id="7277f-115">**Language**</span></span><br/> | <span data-ttu-id="7277f-116">Cadeia de caracteres do identificador de idioma</span><span class="sxs-lookup"><span data-stu-id="7277f-116">language identifier string</span></span><br/>  | <span data-ttu-id="7277f-117">Sim</span><span class="sxs-lookup"><span data-stu-id="7277f-117">Yes</span></span><br/> | <span data-ttu-id="7277f-118">O idioma do nome do modelo localizado.</span><span class="sxs-lookup"><span data-stu-id="7277f-118">The language of the localized model name.</span></span><br/> <br/> |



## <a name="child-elements"></a><span data-ttu-id="7277f-119">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="7277f-119">Child elements</span></span>

<span data-ttu-id="7277f-120">Não há elementos filho.</span><span class="sxs-lookup"><span data-stu-id="7277f-120">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="7277f-121">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="7277f-121">Parent elements</span></span>



| <span data-ttu-id="7277f-122">Elemento</span><span class="sxs-lookup"><span data-stu-id="7277f-122">Element</span></span>                                                   | <span data-ttu-id="7277f-123">Descrição</span><span class="sxs-lookup"><span data-stu-id="7277f-123">Description</span></span>                                                                                          |
|-----------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7277f-124">**thisModelMetadata**</span><span class="sxs-lookup"><span data-stu-id="7277f-124">**thisModelMetadata**</span></span>](thismodelmetadata.md)<br/> | <span data-ttu-id="7277f-125">Define os metadados de modelo e fabricante para o dispositivo a ser implementado.</span><span class="sxs-lookup"><span data-stu-id="7277f-125">Defines the manufacturer and model metadata for the device to be implemented.</span></span><br/> <br/> |



## <a name="element-information"></a><span data-ttu-id="7277f-126">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="7277f-126">Element information</span></span>



| <span data-ttu-id="7277f-127">Label</span><span class="sxs-lookup"><span data-stu-id="7277f-127">Label</span></span> | <span data-ttu-id="7277f-128">Valor</span><span class="sxs-lookup"><span data-stu-id="7277f-128">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="7277f-129">Sistema mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7277f-129">Minimum supported system</span></span><br/> | <span data-ttu-id="7277f-130">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7277f-130">Windows Vista</span></span> |
| <span data-ttu-id="7277f-131">Pode estar vazio</span><span class="sxs-lookup"><span data-stu-id="7277f-131">Can be empty</span></span>                        | <span data-ttu-id="7277f-132">Sim</span><span class="sxs-lookup"><span data-stu-id="7277f-132">Yes</span></span>           |



 

 




