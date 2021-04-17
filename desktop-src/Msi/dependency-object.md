---
description: O objeto Dependency retorna um módulo no qual o módulo atual depende e que ainda não foi mesclado no banco de dados de instalação atual.
ms.assetid: 3157f07d-99de-4628-9b03-eb86eb4896a4
title: Objeto Dependency (Mergemod. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Dependency
- IMsmDependency
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 24b215b67d22d27639f3e002590e7d08dd54b0c6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105749591"
---
# <a name="dependency-object"></a><span data-ttu-id="c141a-103">Objeto de dependência</span><span class="sxs-lookup"><span data-stu-id="c141a-103">Dependency object</span></span>

<span data-ttu-id="c141a-104">O objeto **Dependency** retorna um módulo no qual o módulo atual depende e que ainda não foi mesclado no banco de dados de instalação atual.</span><span class="sxs-lookup"><span data-stu-id="c141a-104">The **Dependency** object returns a module that the current module is dependent upon and which has not yet been merged into the current installation database.</span></span>

## <a name="members"></a><span data-ttu-id="c141a-105">Membros</span><span class="sxs-lookup"><span data-stu-id="c141a-105">Members</span></span>

<span data-ttu-id="c141a-106">O objeto de **dependência** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="c141a-106">The **Dependency** object has these types of members:</span></span>

-   [<span data-ttu-id="c141a-107">Propriedades</span><span class="sxs-lookup"><span data-stu-id="c141a-107">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c141a-108">Propriedades</span><span class="sxs-lookup"><span data-stu-id="c141a-108">Properties</span></span>

<span data-ttu-id="c141a-109">O objeto de **dependência** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="c141a-109">The **Dependency** object has these properties.</span></span>



| <span data-ttu-id="c141a-110">Propriedade</span><span class="sxs-lookup"><span data-stu-id="c141a-110">Property</span></span>                                           | <span data-ttu-id="c141a-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="c141a-111">Description</span></span>                                             |
|:---------------------------------------------------|:--------------------------------------------------------|
| [<span data-ttu-id="c141a-112">**Idioma**</span><span class="sxs-lookup"><span data-stu-id="c141a-112">**Language**</span></span>](dependency-language.md)<br/> | <span data-ttu-id="c141a-113">Retorne o idioma do módulo.</span><span class="sxs-lookup"><span data-stu-id="c141a-113">Return the language of the module.</span></span><br/>           |
| [<span data-ttu-id="c141a-114">**Módulo**</span><span class="sxs-lookup"><span data-stu-id="c141a-114">**Module**</span></span>](dependency-module.md)<br/>     | <span data-ttu-id="c141a-115">Retornar a ID do módulo necessário.</span><span class="sxs-lookup"><span data-stu-id="c141a-115">Return the module ID of the required module.</span></span><br/> |
| [<span data-ttu-id="c141a-116">**Versão**</span><span class="sxs-lookup"><span data-stu-id="c141a-116">**Version**</span></span>](dependency-version.md)<br/>   | <span data-ttu-id="c141a-117">Retorne a versão do módulo necessário.</span><span class="sxs-lookup"><span data-stu-id="c141a-117">Return the version of the required module.</span></span><br/>   |



 

## <a name="c"></a><span data-ttu-id="c141a-118">C++</span><span class="sxs-lookup"><span data-stu-id="c141a-118">C++</span></span>

<span data-ttu-id="c141a-119">IMsmDependency de interface **: IDispatch**</span><span class="sxs-lookup"><span data-stu-id="c141a-119">interface **IMsmDependency : IDispatch**</span></span>

## <a name="interface-id"></a><span data-ttu-id="c141a-120">ID da interface</span><span class="sxs-lookup"><span data-stu-id="c141a-120">Interface ID</span></span>



| <span data-ttu-id="c141a-121">Constante</span><span class="sxs-lookup"><span data-stu-id="c141a-121">Constant</span></span>                | <span data-ttu-id="c141a-122">Valor</span><span class="sxs-lookup"><span data-stu-id="c141a-122">Value</span></span>                                  |
|-------------------------|----------------------------------------|
| <span data-ttu-id="c141a-123">**IMsmDependency de IID \_**</span><span class="sxs-lookup"><span data-stu-id="c141a-123">**IID\_IMsmDependency**</span></span> | <span data-ttu-id="c141a-124">{0ADDA82D-2C26-11D2-AD65-00A0C9AF11A6}</span><span class="sxs-lookup"><span data-stu-id="c141a-124">{0ADDA82D-2C26-11D2-AD65-00A0C9AF11A6}</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="c141a-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c141a-125">Requirements</span></span>



| <span data-ttu-id="c141a-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="c141a-126">Requirement</span></span> | <span data-ttu-id="c141a-127">Valor</span><span class="sxs-lookup"><span data-stu-id="c141a-127">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c141a-128">Versão</span><span class="sxs-lookup"><span data-stu-id="c141a-128">Version</span></span><br/> | <span data-ttu-id="c141a-129">Mergemod.dll 1,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="c141a-129">Mergemod.dll 1.0 or later</span></span><br/>                                                    |
| <span data-ttu-id="c141a-130">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c141a-130">Header</span></span><br/>  | <dl> <span data-ttu-id="c141a-131"><dt>Mergemod. h</dt></span><span class="sxs-lookup"><span data-stu-id="c141a-131"><dt>Mergemod.h</dt></span></span> </dl>   |
| <span data-ttu-id="c141a-132">DLL</span><span class="sxs-lookup"><span data-stu-id="c141a-132">DLL</span></span><br/>     | <dl> <span data-ttu-id="c141a-133"><dt>Mergemod.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c141a-133"><dt>Mergemod.dll</dt></span></span> </dl> |



 

 




