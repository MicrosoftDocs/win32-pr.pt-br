---
description: O objeto GetFiles recupera os arquivos necessários em um idioma específico do módulo. Requer que determinadas ações sejam executadas por meio do objeto de mesclagem antes que todas as partes desta interface retornem resultados válidos.
ms.assetid: f3bf64ec-75f7-43a6-bbd8-a51508c57002
title: Objeto GetFiles (Mergemod. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetFiles
- IMsmGetFiles
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 8a26bb072b0b4a1f048ded76fbd52ffc6d42de62
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748160"
---
# <a name="getfiles-object"></a><span data-ttu-id="04ef0-104">Objeto GetFiles</span><span class="sxs-lookup"><span data-stu-id="04ef0-104">GetFiles object</span></span>

<span data-ttu-id="04ef0-105">O objeto **GetFiles** recupera os arquivos necessários em um idioma específico do módulo.</span><span class="sxs-lookup"><span data-stu-id="04ef0-105">The **GetFiles** object retrieves the files needed in a particular language of the module.</span></span> <span data-ttu-id="04ef0-106">Requer que determinadas ações sejam executadas por meio do [objeto de mesclagem](merge-object.md) antes que todas as partes desta interface retornem resultados válidos.</span><span class="sxs-lookup"><span data-stu-id="04ef0-106">Requires certain actions be performed through the [Merge object](merge-object.md) before all parts of this interface returns valid results.</span></span>

## <a name="members"></a><span data-ttu-id="04ef0-107">Membros</span><span class="sxs-lookup"><span data-stu-id="04ef0-107">Members</span></span>

<span data-ttu-id="04ef0-108">O objeto **GetFiles** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="04ef0-108">The **GetFiles** object has these types of members:</span></span>

-   [<span data-ttu-id="04ef0-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="04ef0-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="04ef0-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="04ef0-110">Properties</span></span>

<span data-ttu-id="04ef0-111">O objeto **GetFiles** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="04ef0-111">The **GetFiles** object has these properties.</span></span>



| <span data-ttu-id="04ef0-112">Propriedade</span><span class="sxs-lookup"><span data-stu-id="04ef0-112">Property</span></span>                                               | <span data-ttu-id="04ef0-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="04ef0-113">Description</span></span>                                                                                                                                                     |
|:-------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="04ef0-114">**ModuleFiles**</span><span class="sxs-lookup"><span data-stu-id="04ef0-114">**ModuleFiles**</span></span>](getfiles-modulefiles.md)<br/> | <span data-ttu-id="04ef0-115">A propriedade [**ModuleFiles**](getfiles-modulefiles.md) retorna todas as chaves primárias da [tabela de arquivos](file-table.md) para o módulo aberto no momento.</span><span class="sxs-lookup"><span data-stu-id="04ef0-115">[**ModuleFiles**](getfiles-modulefiles.md) property returns all the primary keys of the [File table](file-table.md) for the currently open module.</span></span><br/> |



 

## <a name="c"></a><span data-ttu-id="04ef0-116">C++</span><span class="sxs-lookup"><span data-stu-id="04ef0-116">C++</span></span>

<span data-ttu-id="04ef0-117">IMsmGetFiles de interface **: IDispatch**</span><span class="sxs-lookup"><span data-stu-id="04ef0-117">interface **IMsmGetFiles : IDispatch**</span></span>

## <a name="interface-id"></a><span data-ttu-id="04ef0-118">ID da interface</span><span class="sxs-lookup"><span data-stu-id="04ef0-118">Interface ID</span></span>



| <span data-ttu-id="04ef0-119">Constante</span><span class="sxs-lookup"><span data-stu-id="04ef0-119">Constant</span></span>              | <span data-ttu-id="04ef0-120">Valor</span><span class="sxs-lookup"><span data-stu-id="04ef0-120">Value</span></span>                                  |
|-----------------------|----------------------------------------|
| <span data-ttu-id="04ef0-121">**IMsmGetFiles de IID \_**</span><span class="sxs-lookup"><span data-stu-id="04ef0-121">**IID\_IMsmGetFiles**</span></span> | <span data-ttu-id="04ef0-122">{7041AE26-2D78-11D2-888A-00A0C981B015}</span><span class="sxs-lookup"><span data-stu-id="04ef0-122">{7041AE26-2D78-11D2-888A-00A0C981B015}</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="04ef0-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="04ef0-123">Requirements</span></span>



| <span data-ttu-id="04ef0-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="04ef0-124">Requirement</span></span> | <span data-ttu-id="04ef0-125">Valor</span><span class="sxs-lookup"><span data-stu-id="04ef0-125">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="04ef0-126">Versão</span><span class="sxs-lookup"><span data-stu-id="04ef0-126">Version</span></span><br/> | <span data-ttu-id="04ef0-127">Mergemod.dll 1,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="04ef0-127">Mergemod.dll 1.0 or later</span></span><br/>                                                    |
| <span data-ttu-id="04ef0-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="04ef0-128">Header</span></span><br/>  | <dl> <span data-ttu-id="04ef0-129"><dt>Mergemod. h</dt></span><span class="sxs-lookup"><span data-stu-id="04ef0-129"><dt>Mergemod.h</dt></span></span> </dl>   |
| <span data-ttu-id="04ef0-130">DLL</span><span class="sxs-lookup"><span data-stu-id="04ef0-130">DLL</span></span><br/>     | <dl> <span data-ttu-id="04ef0-131"><dt>Mergemod.dll</dt></span><span class="sxs-lookup"><span data-stu-id="04ef0-131"><dt>Mergemod.dll</dt></span></span> </dl> |



 

 




