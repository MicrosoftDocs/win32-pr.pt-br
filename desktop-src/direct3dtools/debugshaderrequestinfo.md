---
description: Representa informações sobre uma solicitação de depurador de sombreador.
MS-HAID: vspixengine.DebugShaderRequestInfo
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Estrutura DebugShaderRequestInfo
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: DEFFAEE4-6C53-4C89-A533-A5BE73B80DEA
api_name:
- DebugShaderRequestInfo
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: a59bfb84bb7d4e8644c0cfadc4475be7d7da4a54
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104500434"
---
# <a name="span-idvspixenginedebugshaderrequestinfospandebugshaderrequestinfo-structure"></a><span data-ttu-id="d07a7-103"><span id="vspixengine.debugshaderrequestinfo"></span>Estrutura DebugShaderRequestInfo</span><span class="sxs-lookup"><span data-stu-id="d07a7-103"><span id="vspixengine.debugshaderrequestinfo"></span>DebugShaderRequestInfo structure</span></span>

<span data-ttu-id="d07a7-104">Representa informações sobre uma solicitação de depurador de sombreador.</span><span class="sxs-lookup"><span data-stu-id="d07a7-104">Represents information about a shader debugger request.</span></span>

## <a name="syntax"></a><span data-ttu-id="d07a7-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d07a7-105">Syntax</span></span>


```C++
} DebugShaderRequestInfo;
```

## <a name="members"></a><span data-ttu-id="d07a7-106">Membros</span><span class="sxs-lookup"><span data-stu-id="d07a7-106">Members</span></span>

<span data-ttu-id="d07a7-107">**Test**</span><span class="sxs-lookup"><span data-stu-id="d07a7-107">**stage**</span></span>  
<span data-ttu-id="d07a7-108">O estágio do pipeline a ser depurado.</span><span class="sxs-lookup"><span data-stu-id="d07a7-108">The pipeline stage to debug.</span></span>

<span data-ttu-id="d07a7-109">**1008**</span><span class="sxs-lookup"><span data-stu-id="d07a7-109">**eventID**</span></span>  
<span data-ttu-id="d07a7-110">A ID do evento de gráficos a ser depurado.</span><span class="sxs-lookup"><span data-stu-id="d07a7-110">The ID of the graphics event to debug.</span></span>

<span data-ttu-id="d07a7-111">**frameNumber**</span><span class="sxs-lookup"><span data-stu-id="d07a7-111">**frameNumber**</span></span>  
<span data-ttu-id="d07a7-112">O quadro a ser depurado.</span><span class="sxs-lookup"><span data-stu-id="d07a7-112">The frame to debug.</span></span>

<span data-ttu-id="d07a7-113">**deles**</span><span class="sxs-lookup"><span data-stu-id="d07a7-113">**vertex**</span></span>  
<span data-ttu-id="d07a7-114">O vértice a ser depurado.</span><span class="sxs-lookup"><span data-stu-id="d07a7-114">The vertex to debug.</span></span>

<span data-ttu-id="d07a7-115">**pixel**</span><span class="sxs-lookup"><span data-stu-id="d07a7-115">**pixel**</span></span>  
<span data-ttu-id="d07a7-116">O pixel a ser depurado.</span><span class="sxs-lookup"><span data-stu-id="d07a7-116">The pixel to debug.</span></span>

<span data-ttu-id="d07a7-117">**groupCoordinates**</span><span class="sxs-lookup"><span data-stu-id="d07a7-117">**groupCoordinates**</span></span>  
<span data-ttu-id="d07a7-118">As coordenadas do grupo a ser depurado.</span><span class="sxs-lookup"><span data-stu-id="d07a7-118">The coordinates of the group to debug.</span></span>

<span data-ttu-id="d07a7-119">**threadCoordinates**</span><span class="sxs-lookup"><span data-stu-id="d07a7-119">**threadCoordinates**</span></span>  
<span data-ttu-id="d07a7-120">As coordenadas do thread a ser depurado</span><span class="sxs-lookup"><span data-stu-id="d07a7-120">The coordinates of the thread to debug</span></span>

## <a name="requirements"></a><span data-ttu-id="d07a7-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d07a7-121">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="d07a7-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d07a7-122">Header</span></span></p></td><td><span data-ttu-id="d07a7-123">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="d07a7-123">Vspixengine.h</span></span></td></tr></tbody></table>

 

 



