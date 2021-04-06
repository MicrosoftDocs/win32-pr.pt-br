---
description: Representa um estágio de pipeline, incluindo detalhes do sombreador usado.
MS-HAID: vspixengine.PipeLineStage
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Estrutura PipeLineStage
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 616103CB-777E-4AA8-8B70-E19B1A2D667C
api_name:
- PipeLineStage
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 5ddd0cbcf417da7967b135a10227ce6687cb2ea5
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103919856"
---
# <a name="span-idvspixenginepipelinestagespanpipelinestage-structure"></a><span data-ttu-id="bea41-103"><span id="vspixengine.pipelinestage"></span>Estrutura PipeLineStage</span><span class="sxs-lookup"><span data-stu-id="bea41-103"><span id="vspixengine.pipelinestage"></span>PipeLineStage structure</span></span>

<span data-ttu-id="bea41-104">Representa um estágio de pipeline, incluindo detalhes do sombreador usado.</span><span class="sxs-lookup"><span data-stu-id="bea41-104">Represents a pipeline stage, including details of the shader used.</span></span>

## <a name="syntax"></a><span data-ttu-id="bea41-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="bea41-105">Syntax</span></span>


```C++
} PipeLineStage;
```

## <a name="members"></a><span data-ttu-id="bea41-106">Membros</span><span class="sxs-lookup"><span data-stu-id="bea41-106">Members</span></span>

<span data-ttu-id="bea41-107">**Prepareid**</span><span class="sxs-lookup"><span data-stu-id="bea41-107">**StageId**</span></span>  
<span data-ttu-id="bea41-108">A ID do estágio do pipeline.</span><span class="sxs-lookup"><span data-stu-id="bea41-108">The ID of the pipeline stage.</span></span>

<span data-ttu-id="bea41-109">**Depurável**</span><span class="sxs-lookup"><span data-stu-id="bea41-109">**Debuggable**</span></span>  
<span data-ttu-id="bea41-110">true se o estágio do pipeline oferecer suporte à depuração; caso contrário, false.</span><span class="sxs-lookup"><span data-stu-id="bea41-110">true if the pipeline stage supports debugging; otherwise, false.</span></span>

<span data-ttu-id="bea41-111">**StageName**</span><span class="sxs-lookup"><span data-stu-id="bea41-111">**StageName**</span></span>  
<span data-ttu-id="bea41-112">Uma cadeia de caracteres COM que contém o nome do estágio do pipeline.</span><span class="sxs-lookup"><span data-stu-id="bea41-112">A COM string containing the name of the pipeline stage.</span></span>

<span data-ttu-id="bea41-113">**GuaranteedOutput**</span><span class="sxs-lookup"><span data-stu-id="bea41-113">**GuaranteedOutput**</span></span>  
<span data-ttu-id="bea41-114">true se o estágio do pipeline sempre tiver saída de pipeline; caso contrário, false.</span><span class="sxs-lookup"><span data-stu-id="bea41-114">true if the pipeline stage always has pipeline output; otherwise, false.</span></span>

<span data-ttu-id="bea41-115">**DebugEntryPoint**</span><span class="sxs-lookup"><span data-stu-id="bea41-115">**DebugEntryPoint**</span></span>  
<span data-ttu-id="bea41-116">Uma cadeia de caracteres COM que contém o nome do ponto de entrada do sombreador, se houver um.</span><span class="sxs-lookup"><span data-stu-id="bea41-116">A COM string containing the name of the shader entry point, if there is one.</span></span>

<span data-ttu-id="bea41-117">**Shaderfile**</span><span class="sxs-lookup"><span data-stu-id="bea41-117">**ShaderFile**</span></span>  
<span data-ttu-id="bea41-118">Uma cadeia de caracteres COM que contém o caminho de arquivo de origem do sombreador.</span><span class="sxs-lookup"><span data-stu-id="bea41-118">A COM string containing the filepath of the shader source file.</span></span>

<span data-ttu-id="bea41-119">**ShaderByteStreamPtr**</span><span class="sxs-lookup"><span data-stu-id="bea41-119">**ShaderByteStreamPtr**</span></span>  
<span data-ttu-id="bea41-120">Um FILEPTR para o fluxo de bytes do sombreador.</span><span class="sxs-lookup"><span data-stu-id="bea41-120">A FILEPTR for the shader byte stream.</span></span> <span data-ttu-id="bea41-121">Isso é passado de volta para depurar.</span><span class="sxs-lookup"><span data-stu-id="bea41-121">This is passed back in order to debug.</span></span>

## <a name="requirements"></a><span data-ttu-id="bea41-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bea41-122">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="bea41-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="bea41-123">Header</span></span></p></td><td><span data-ttu-id="bea41-124">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="bea41-124">Vspixengine.h</span></span></td></tr></tbody></table>

 

 



