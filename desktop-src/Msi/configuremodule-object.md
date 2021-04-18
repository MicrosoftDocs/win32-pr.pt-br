---
description: O objeto ConfigureModule é uma interface implementada pelo cliente.
ms.assetid: f6240837-7685-4bfe-8a2f-b4428014702a
title: Objeto ConfigureModule (Mergemod. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ConfigureModule
- IMsmConfigureModule
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 0c99f8932d1d3c0e7ba7d7df5e14fc0738e8b81c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751446"
---
# <a name="configuremodule-object"></a><span data-ttu-id="ce899-103">Objeto ConfigureModule</span><span class="sxs-lookup"><span data-stu-id="ce899-103">ConfigureModule object</span></span>

<span data-ttu-id="ce899-104">O **objeto ConfigureModule** é uma interface implementada pelo cliente.</span><span class="sxs-lookup"><span data-stu-id="ce899-104">The **ConfigureModule object** is an interface implemented by the client.</span></span> <span data-ttu-id="ce899-105">Mergemod.dllchama métodos na interface **IMsmConfigureModule** para solicitar que a ferramenta cliente forneça informações de configuração.</span><span class="sxs-lookup"><span data-stu-id="ce899-105">Mergemod.dllcalls methods on the **IMsmConfigureModule** interface to request that the client tool provide configuration information.</span></span> <span data-ttu-id="ce899-106">O módulo é configurado com base nas respostas do cliente a chamadas nesta interface.</span><span class="sxs-lookup"><span data-stu-id="ce899-106">The module is configured based on the client's responses to calls on this interface.</span></span>

## <a name="members"></a><span data-ttu-id="ce899-107">Membros</span><span class="sxs-lookup"><span data-stu-id="ce899-107">Members</span></span>

<span data-ttu-id="ce899-108">O objeto **ConfigureModule** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="ce899-108">The **ConfigureModule** object has these types of members:</span></span>

-   [<span data-ttu-id="ce899-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="ce899-109">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="ce899-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="ce899-110">Methods</span></span>

<span data-ttu-id="ce899-111">O objeto **ConfigureModule** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="ce899-111">The **ConfigureModule** object has these methods.</span></span>



| <span data-ttu-id="ce899-112">Método</span><span class="sxs-lookup"><span data-stu-id="ce899-112">Method</span></span>                                                           | <span data-ttu-id="ce899-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="ce899-113">Description</span></span>                                                                        |
|:-----------------------------------------------------------------|:-----------------------------------------------------------------------------------|
| [<span data-ttu-id="ce899-114">**ProvideIntegerData**</span><span class="sxs-lookup"><span data-stu-id="ce899-114">**ProvideIntegerData**</span></span>](configuremodule-provideintegerdata.md) | <span data-ttu-id="ce899-115">Chamado por Mergemod.dll para obter números inteiros usados para configurar o módulo.</span><span class="sxs-lookup"><span data-stu-id="ce899-115">Called by Mergemod.dll to obtain integers used to configure the module.</span></span><br/> |
| [<span data-ttu-id="ce899-116">**ProvideTextData**</span><span class="sxs-lookup"><span data-stu-id="ce899-116">**ProvideTextData**</span></span>](configuremodule-providetextdata.md)       | <span data-ttu-id="ce899-117">Chamado por Mergemod.dll para obter o texto usado para configurar o módulo.</span><span class="sxs-lookup"><span data-stu-id="ce899-117">Called by Mergemod.dll to obtain text used to configure the module.</span></span><br/>     |



 

## <a name="remarks"></a><span data-ttu-id="ce899-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="ce899-118">Remarks</span></span>

### <a name="c"></a><span data-ttu-id="ce899-119">C++</span><span class="sxs-lookup"><span data-stu-id="ce899-119">C++</span></span>

<span data-ttu-id="ce899-120">IMsmConfigureModule de interface **: IDispatch**</span><span class="sxs-lookup"><span data-stu-id="ce899-120">interface **IMsmConfigureModule : IDispatch**</span></span>

### <a name="interface-id"></a><span data-ttu-id="ce899-121">ID da interface</span><span class="sxs-lookup"><span data-stu-id="ce899-121">Interface ID</span></span>



| <span data-ttu-id="ce899-122">Constante</span><span class="sxs-lookup"><span data-stu-id="ce899-122">Constant</span></span>                     | <span data-ttu-id="ce899-123">Valor</span><span class="sxs-lookup"><span data-stu-id="ce899-123">Value</span></span>                                  |
|------------------------------|----------------------------------------|
| <span data-ttu-id="ce899-124">**IMsmConfigureModule de IID \_**</span><span class="sxs-lookup"><span data-stu-id="ce899-124">**IID\_IMsmConfigureModule**</span></span> | <span data-ttu-id="ce899-125">{AC013209-18A7-4851-8A21-2353443D70A0}</span><span class="sxs-lookup"><span data-stu-id="ce899-125">{AC013209-18A7-4851-8A21-2353443D70A0}</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="ce899-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ce899-126">Requirements</span></span>



| <span data-ttu-id="ce899-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="ce899-127">Requirement</span></span> | <span data-ttu-id="ce899-128">Valor</span><span class="sxs-lookup"><span data-stu-id="ce899-128">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ce899-129">Versão</span><span class="sxs-lookup"><span data-stu-id="ce899-129">Version</span></span><br/> | <span data-ttu-id="ce899-130">Mergemod.dll 2,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="ce899-130">Mergemod.dll 2.0 or later</span></span><br/>                                                    |
| <span data-ttu-id="ce899-131">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ce899-131">Header</span></span><br/>  | <dl> <span data-ttu-id="ce899-132"><dt>Mergemod. h</dt></span><span class="sxs-lookup"><span data-stu-id="ce899-132"><dt>Mergemod.h</dt></span></span> </dl>   |
| <span data-ttu-id="ce899-133">DLL</span><span class="sxs-lookup"><span data-stu-id="ce899-133">DLL</span></span><br/>     | <dl> <span data-ttu-id="ce899-134"><dt>Mergemod.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ce899-134"><dt>Mergemod.dll</dt></span></span> </dl> |



 

 




