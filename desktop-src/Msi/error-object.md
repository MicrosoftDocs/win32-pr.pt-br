---
description: O objeto Error Retorna as informações de um único erro de mesclagem.
ms.assetid: 38025e21-2d31-40f8-a088-2d3912c2893e
title: Objeto de erro (Mergemod. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Error
- IMsmError
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 36fce310e6f75889ba5092f4fe43b6ca52ee2963
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105747981"
---
# <a name="error-object"></a><span data-ttu-id="5415c-103">Objeto de erro</span><span class="sxs-lookup"><span data-stu-id="5415c-103">Error object</span></span>

<span data-ttu-id="5415c-104">O objeto **Error** retorna as informações de um único erro de mesclagem.</span><span class="sxs-lookup"><span data-stu-id="5415c-104">The **Error** object returns the information of a single merge error.</span></span>

## <a name="members"></a><span data-ttu-id="5415c-105">Membros</span><span class="sxs-lookup"><span data-stu-id="5415c-105">Members</span></span>

<span data-ttu-id="5415c-106">O objeto de **erro** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="5415c-106">The **Error** object has these types of members:</span></span>

-   [<span data-ttu-id="5415c-107">Propriedades</span><span class="sxs-lookup"><span data-stu-id="5415c-107">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5415c-108">Propriedades</span><span class="sxs-lookup"><span data-stu-id="5415c-108">Properties</span></span>

<span data-ttu-id="5415c-109">O objeto de **erro** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="5415c-109">The **Error** object has these properties.</span></span>



| <span data-ttu-id="5415c-110">Propriedade</span><span class="sxs-lookup"><span data-stu-id="5415c-110">Property</span></span>                                                | <span data-ttu-id="5415c-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="5415c-111">Description</span></span>                                                                                 |
|:--------------------------------------------------------|:--------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5415c-112">**DatabaseKeys**</span><span class="sxs-lookup"><span data-stu-id="5415c-112">**DatabaseKeys**</span></span>](error-databasekeys.md)<br/>   | <span data-ttu-id="5415c-113">Retorna as chaves primárias da linha na tabela de banco de dados que causou o erro.</span><span class="sxs-lookup"><span data-stu-id="5415c-113">Returns the primary keys of the row in the database table that caused the error.</span></span><br/> |
| [<span data-ttu-id="5415c-114">**Banco de dados**</span><span class="sxs-lookup"><span data-stu-id="5415c-114">**DatabaseTable**</span></span>](error-databasetable.md)<br/> | <span data-ttu-id="5415c-115">Retorna o nome da tabela do banco de dados que está causando o erro.</span><span class="sxs-lookup"><span data-stu-id="5415c-115">Returns the table name of the table in the database causing the error.</span></span><br/>           |
| [<span data-ttu-id="5415c-116">**Idioma**</span><span class="sxs-lookup"><span data-stu-id="5415c-116">**Language**</span></span>](error-language.md)<br/>           | <span data-ttu-id="5415c-117">Retorne o idioma do erro.</span><span class="sxs-lookup"><span data-stu-id="5415c-117">Return the language of the error.</span></span><br/>                                                |
| [<span data-ttu-id="5415c-118">**ModuleKeys**</span><span class="sxs-lookup"><span data-stu-id="5415c-118">**ModuleKeys**</span></span>](error-modulekeys.md)<br/>       | <span data-ttu-id="5415c-119">Retorna as chaves primárias da linha na tabela de módulo que causou o erro.</span><span class="sxs-lookup"><span data-stu-id="5415c-119">Returns the primary keys of the row in the module table that caused the error.</span></span><br/>   |
| [<span data-ttu-id="5415c-120">**Módulotable**</span><span class="sxs-lookup"><span data-stu-id="5415c-120">**ModuleTable**</span></span>](error-moduletable.md)<br/>     | <span data-ttu-id="5415c-121">Retorna o nome da tabela do módulo que está causando o erro.</span><span class="sxs-lookup"><span data-stu-id="5415c-121">Returns the table name of the table in the module causing the error.</span></span><br/>             |
| [<span data-ttu-id="5415c-122">**Caminho**</span><span class="sxs-lookup"><span data-stu-id="5415c-122">**Path**</span></span>](error-path.md)<br/>                   | <span data-ttu-id="5415c-123">Retorne o caminho para o arquivo ou diretório causando o erro.</span><span class="sxs-lookup"><span data-stu-id="5415c-123">Return the path to the file or directory causing the error.</span></span> <span data-ttu-id="5415c-124">Atualmente não utilizado.</span><span class="sxs-lookup"><span data-stu-id="5415c-124">Currently unused.</span></span><br/>    |
| [<span data-ttu-id="5415c-125">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="5415c-125">**Type**</span></span>](error-type.md)<br/>                   | <span data-ttu-id="5415c-126">Retornar o tipo de erro.</span><span class="sxs-lookup"><span data-stu-id="5415c-126">Return the type of error.</span></span><br/>                                                        |



 

## <a name="c"></a><span data-ttu-id="5415c-127">C++</span><span class="sxs-lookup"><span data-stu-id="5415c-127">C++</span></span>

<span data-ttu-id="5415c-128">IMsmError de interface **: IDispatch**</span><span class="sxs-lookup"><span data-stu-id="5415c-128">interface **IMsmError : IDispatch**</span></span>

## <a name="interface-id"></a><span data-ttu-id="5415c-129">ID da interface</span><span class="sxs-lookup"><span data-stu-id="5415c-129">Interface ID</span></span>



| <span data-ttu-id="5415c-130">Constante</span><span class="sxs-lookup"><span data-stu-id="5415c-130">Constant</span></span>           | <span data-ttu-id="5415c-131">Valor</span><span class="sxs-lookup"><span data-stu-id="5415c-131">Value</span></span>                                  |
|--------------------|----------------------------------------|
| <span data-ttu-id="5415c-132">**IMsmError de IID \_**</span><span class="sxs-lookup"><span data-stu-id="5415c-132">**IID\_IMsmError**</span></span> | <span data-ttu-id="5415c-133">{0ADDA828-2C26-11D2-AD65-00A0C9AF11A6}</span><span class="sxs-lookup"><span data-stu-id="5415c-133">{0ADDA828-2C26-11D2-AD65-00A0C9AF11A6}</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="5415c-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5415c-134">Requirements</span></span>



| <span data-ttu-id="5415c-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="5415c-135">Requirement</span></span> | <span data-ttu-id="5415c-136">Valor</span><span class="sxs-lookup"><span data-stu-id="5415c-136">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5415c-137">Versão</span><span class="sxs-lookup"><span data-stu-id="5415c-137">Version</span></span><br/> | <span data-ttu-id="5415c-138">Mergemod.dll 1,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="5415c-138">Mergemod.dll 1.0 or later</span></span><br/>                                                    |
| <span data-ttu-id="5415c-139">parâmetro</span><span class="sxs-lookup"><span data-stu-id="5415c-139">Header</span></span><br/>  | <dl> <span data-ttu-id="5415c-140"><dt>Mergemod. h</dt></span><span class="sxs-lookup"><span data-stu-id="5415c-140"><dt>Mergemod.h</dt></span></span> </dl>   |
| <span data-ttu-id="5415c-141">DLL</span><span class="sxs-lookup"><span data-stu-id="5415c-141">DLL</span></span><br/>     | <dl> <span data-ttu-id="5415c-142"><dt>Mergemod.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5415c-142"><dt>Mergemod.dll</dt></span></span> </dl> |



 

 




