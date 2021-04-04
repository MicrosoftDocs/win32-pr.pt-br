---
description: Representa informações sobre uma única entrada no layout de buffer de uma malha.
MS-HAID: vspixengine.MeshDataBufferLayoutEntry
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Estrutura MeshDataBufferLayoutEntry
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: FE1D796C-DFD8-4C6E-9914-3063408FE565
api_name:
- MeshDataBufferLayoutEntry
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: bce67b8316e9eb9b96e641e2a90260fab6bfdaad
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103646168"
---
# <a name="span-idvspixenginemeshdatabufferlayoutentryspanmeshdatabufferlayoutentry-structure"></a><span data-ttu-id="a5651-103"><span id="vspixengine.meshdatabufferlayoutentry"></span>Estrutura MeshDataBufferLayoutEntry</span><span class="sxs-lookup"><span data-stu-id="a5651-103"><span id="vspixengine.meshdatabufferlayoutentry"></span>MeshDataBufferLayoutEntry structure</span></span>

<span data-ttu-id="a5651-104">Representa informações sobre uma única entrada no layout de buffer de uma malha.</span><span class="sxs-lookup"><span data-stu-id="a5651-104">Represents information about a single entry in the buffer layout of a mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="a5651-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a5651-105">Syntax</span></span>


```C++
} MeshDataBufferLayoutEntry;
```

## <a name="members"></a><span data-ttu-id="a5651-106">Membros</span><span class="sxs-lookup"><span data-stu-id="a5651-106">Members</span></span>

<span data-ttu-id="a5651-107">**pName**</span><span class="sxs-lookup"><span data-stu-id="a5651-107">**pName**</span></span>  
<span data-ttu-id="a5651-108">Uma cadeia de caracteres COM que contém o nome da entrada.</span><span class="sxs-lookup"><span data-stu-id="a5651-108">A COM string containing the name of the entry.</span></span>

<span data-ttu-id="a5651-109">**numComponents**</span><span class="sxs-lookup"><span data-stu-id="a5651-109">**numComponents**</span></span>  
<span data-ttu-id="a5651-110">O número de componentes homogêneos (valores) que compõem essa entrada.</span><span class="sxs-lookup"><span data-stu-id="a5651-110">The number of homogenous components (values) that make up this entry.</span></span>

<span data-ttu-id="a5651-111">**isposition**</span><span class="sxs-lookup"><span data-stu-id="a5651-111">**isPosition**</span></span>  
<span data-ttu-id="a5651-112">true se a entrada for uma posição; caso contrário, false.</span><span class="sxs-lookup"><span data-stu-id="a5651-112">true if the entry is a position; otherwise, false.</span></span>

<span data-ttu-id="a5651-113">**format**</span><span class="sxs-lookup"><span data-stu-id="a5651-113">**format**</span></span>  
<span data-ttu-id="a5651-114">O formato de dados da entrada (registro).</span><span class="sxs-lookup"><span data-stu-id="a5651-114">The data format of the entry (register).</span></span> <span data-ttu-id="a5651-115">Para obter mais informações, consulte a \_ enumeração de formato de registro.</span><span class="sxs-lookup"><span data-stu-id="a5651-115">For more information, see the REGISTER\_FORMAT enumeration.</span></span>

## <a name="requirements"></a><span data-ttu-id="a5651-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a5651-116">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="a5651-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a5651-117">Header</span></span></p></td><td><span data-ttu-id="a5651-118">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="a5651-118">Vspixengine.h</span></span></td></tr></tbody></table>

 

 



