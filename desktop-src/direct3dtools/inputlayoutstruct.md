---
description: Representa os campos de layout de entrada de um buffer de vértice, um por campo no buffer de vértice.
MS-HAID: vspixengine.InputLayoutStruct
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Estrutura InputLayoutStruct
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: CC7AAC2F-FDB1-4AD8-9B87-A97EE557FEAC
api_name:
- InputLayoutStruct
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 1369d80d202682b67eacbb184b215d9da1711874
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105762145"
---
# <a name="span-idvspixengineinputlayoutstructspaninputlayoutstruct-structure"></a><span data-ttu-id="cf4bd-103"><span id="vspixengine.inputlayoutstruct"></span>Estrutura InputLayoutStruct</span><span class="sxs-lookup"><span data-stu-id="cf4bd-103"><span id="vspixengine.inputlayoutstruct"></span>InputLayoutStruct structure</span></span>

<span data-ttu-id="cf4bd-104">Representa os campos de layout de entrada de um buffer de vértice, um por campo no buffer de vértice.</span><span class="sxs-lookup"><span data-stu-id="cf4bd-104">Represents the input layout fields of a vertex buffer, one per field in the vertex buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="cf4bd-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="cf4bd-105">Syntax</span></span>


```C++
} InputLayoutStruct;
```

## <a name="members"></a><span data-ttu-id="cf4bd-106">Membros</span><span class="sxs-lookup"><span data-stu-id="cf4bd-106">Members</span></span>

<span data-ttu-id="cf4bd-107">**Semânticaname**</span><span class="sxs-lookup"><span data-stu-id="cf4bd-107">**SemanticName**</span></span>  
<span data-ttu-id="cf4bd-108">Uma cadeia de caracteres COM que contém o nome da semântica associada.</span><span class="sxs-lookup"><span data-stu-id="cf4bd-108">A COM string containing the name of the associated semantic.</span></span>

<span data-ttu-id="cf4bd-109">**SemanticIndex**</span><span class="sxs-lookup"><span data-stu-id="cf4bd-109">**SemanticIndex**</span></span>  
<span data-ttu-id="cf4bd-110">O índice da semântica associada.</span><span class="sxs-lookup"><span data-stu-id="cf4bd-110">The index of the associated semantic.</span></span>

<span data-ttu-id="cf4bd-111">**Formato**</span><span class="sxs-lookup"><span data-stu-id="cf4bd-111">**Format**</span></span>  
<span data-ttu-id="cf4bd-112">O formato do campo.</span><span class="sxs-lookup"><span data-stu-id="cf4bd-112">The format of the field.</span></span> <span data-ttu-id="cf4bd-113">Para obter mais informações, consulte a \_ enumeração de formato dxgi.</span><span class="sxs-lookup"><span data-stu-id="cf4bd-113">For more information see the DXGI\_FORMAT enumeration.</span></span>

<span data-ttu-id="cf4bd-114">**InputSlot**</span><span class="sxs-lookup"><span data-stu-id="cf4bd-114">**InputSlot**</span></span>  
<span data-ttu-id="cf4bd-115">O slot de entrada associado.</span><span class="sxs-lookup"><span data-stu-id="cf4bd-115">The associated input slot.</span></span>

<span data-ttu-id="cf4bd-116">**AlignedByteOffset**</span><span class="sxs-lookup"><span data-stu-id="cf4bd-116">**AlignedByteOffset**</span></span>  

<span data-ttu-id="cf4bd-117">**InputSlotClass**</span><span class="sxs-lookup"><span data-stu-id="cf4bd-117">**InputSlotClass**</span></span>  

<span data-ttu-id="cf4bd-118">**InstanceDataStepRate**</span><span class="sxs-lookup"><span data-stu-id="cf4bd-118">**InstanceDataStepRate**</span></span>  

## <a name="requirements"></a><span data-ttu-id="cf4bd-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cf4bd-119">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="cf4bd-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="cf4bd-120">Header</span></span></p></td><td><span data-ttu-id="cf4bd-121">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="cf4bd-121">Vspixengine.h</span></span></td></tr></tbody></table>

 

 



