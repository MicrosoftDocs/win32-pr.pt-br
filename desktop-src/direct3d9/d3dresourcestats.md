---
description: Estatísticas de recursos coletadas pelo \_ RESOURCEMANAGER D3DDEVINFO ao usar o mecanismo de consulta assíncrona.
ms.assetid: f4d9c6db-4002-439c-9a88-485763badc82
title: Estrutura D3DRESOURCESTATS (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DRESOURCESTATS
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: f6f549011b9750f69187c0e0cbf34ec94764c9ef
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105790381"
---
# <a name="d3dresourcestats-structure"></a><span data-ttu-id="a1981-103">Estrutura D3DRESOURCESTATS</span><span class="sxs-lookup"><span data-stu-id="a1981-103">D3DRESOURCESTATS structure</span></span>

<span data-ttu-id="a1981-104">Estatísticas de recursos coletadas [**pelo \_ ResourceManager D3DDEVINFO**](d3ddevinfo-resourcemanager.md) ao usar o mecanismo de consulta assíncrona.</span><span class="sxs-lookup"><span data-stu-id="a1981-104">Resource statistics gathered by the [**D3DDEVINFO\_ResourceManager**](d3ddevinfo-resourcemanager.md) when using the asynchronous query mechanism.</span></span>

## <a name="syntax"></a><span data-ttu-id="a1981-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a1981-105">Syntax</span></span>


```C++
typedef struct D3DRESOURCESTATS {
  BOOL  bThrashing;
  DWORD ApproxBytesDownloaded;
  DWORD NumEvicts;
  DWORD NumVidCreates;
  DWORD LastPri;
  DWORD NumUsed;
  DWORD NumUsedInVidMem;
  DWORD WorkingSet;
  DWORD WorkingSetBytes;
  DWORD TotalManaged;
  DWORD TotalBytes;
} D3DRESOURCESTATS, *LPD3DRESOURCESTATS;
```



## <a name="members"></a><span data-ttu-id="a1981-106">Membros</span><span class="sxs-lookup"><span data-stu-id="a1981-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="a1981-107">**bThrashing**</span><span class="sxs-lookup"><span data-stu-id="a1981-107">**bThrashing**</span></span>
</dt> <dd>

<span data-ttu-id="a1981-108">Tipo: **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a1981-108">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="a1981-109">Indica se ultrapaginação está ocorrendo.</span><span class="sxs-lookup"><span data-stu-id="a1981-109">Indicates if thrashing is occurring.</span></span>

</dd> <dt>

<span data-ttu-id="a1981-110">**ApproxBytesDownloaded**</span><span class="sxs-lookup"><span data-stu-id="a1981-110">**ApproxBytesDownloaded**</span></span>
</dt> <dd>

<span data-ttu-id="a1981-111">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a1981-111">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="a1981-112">Número aproximado de bytes baixados pelo Gerenciador de recursos.</span><span class="sxs-lookup"><span data-stu-id="a1981-112">Approximate number of bytes downloaded by the resource manager.</span></span>

</dd> <dt>

<span data-ttu-id="a1981-113">**NumEvicts**</span><span class="sxs-lookup"><span data-stu-id="a1981-113">**NumEvicts**</span></span>
</dt> <dd>

<span data-ttu-id="a1981-114">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a1981-114">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="a1981-115">Número de objetos removidos.</span><span class="sxs-lookup"><span data-stu-id="a1981-115">Number of objects evicted.</span></span>

</dd> <dt>

<span data-ttu-id="a1981-116">**NumVidCreates**</span><span class="sxs-lookup"><span data-stu-id="a1981-116">**NumVidCreates**</span></span>
</dt> <dd>

<span data-ttu-id="a1981-117">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a1981-117">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="a1981-118">Número de objetos criados na memória de vídeo.</span><span class="sxs-lookup"><span data-stu-id="a1981-118">Number of objects created in video memory.</span></span>

</dd> <dt>

<span data-ttu-id="a1981-119">**LastPri**</span><span class="sxs-lookup"><span data-stu-id="a1981-119">**LastPri**</span></span>
</dt> <dd>

<span data-ttu-id="a1981-120">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a1981-120">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="a1981-121">Prioridade do último objeto removido.</span><span class="sxs-lookup"><span data-stu-id="a1981-121">Priority of last object evicted.</span></span>

</dd> <dt>

<span data-ttu-id="a1981-122">**NumUsed**</span><span class="sxs-lookup"><span data-stu-id="a1981-122">**NumUsed**</span></span>
</dt> <dd>

<span data-ttu-id="a1981-123">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a1981-123">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="a1981-124">Número de objetos definidos para o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a1981-124">Number of objects set to the device.</span></span>

</dd> <dt>

<span data-ttu-id="a1981-125">**NumUsedInVidMem**</span><span class="sxs-lookup"><span data-stu-id="a1981-125">**NumUsedInVidMem**</span></span>
</dt> <dd>

<span data-ttu-id="a1981-126">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a1981-126">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="a1981-127">Número de objetos definidos para o dispositivo, que já estão na memória de vídeo.</span><span class="sxs-lookup"><span data-stu-id="a1981-127">Number of objects set to the device, which are already in video memory.</span></span>

</dd> <dt>

<span data-ttu-id="a1981-128">**WorkingSet**</span><span class="sxs-lookup"><span data-stu-id="a1981-128">**WorkingSet**</span></span>
</dt> <dd>

<span data-ttu-id="a1981-129">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a1981-129">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="a1981-130">Número de objetos na memória de vídeo.</span><span class="sxs-lookup"><span data-stu-id="a1981-130">Number of objects in video memory.</span></span>

</dd> <dt>

<span data-ttu-id="a1981-131">**WorkingSetBytes**</span><span class="sxs-lookup"><span data-stu-id="a1981-131">**WorkingSetBytes**</span></span>
</dt> <dd>

<span data-ttu-id="a1981-132">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a1981-132">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="a1981-133">Número de bytes na memória de vídeo.</span><span class="sxs-lookup"><span data-stu-id="a1981-133">Number of bytes in video memory.</span></span>

</dd> <dt>

<span data-ttu-id="a1981-134">**TotalManaged**</span><span class="sxs-lookup"><span data-stu-id="a1981-134">**TotalManaged**</span></span>
</dt> <dd>

<span data-ttu-id="a1981-135">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a1981-135">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="a1981-136">Número total de objetos gerenciados.</span><span class="sxs-lookup"><span data-stu-id="a1981-136">Total number of managed objects.</span></span>

</dd> <dt>

<span data-ttu-id="a1981-137">**TotalBytes**</span><span class="sxs-lookup"><span data-stu-id="a1981-137">**TotalBytes**</span></span>
</dt> <dd>

<span data-ttu-id="a1981-138">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a1981-138">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="a1981-139">Número total de bytes de objetos gerenciados.</span><span class="sxs-lookup"><span data-stu-id="a1981-139">Total number of bytes of managed objects.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a1981-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a1981-140">Requirements</span></span>



| <span data-ttu-id="a1981-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="a1981-141">Requirement</span></span> | <span data-ttu-id="a1981-142">Valor</span><span class="sxs-lookup"><span data-stu-id="a1981-142">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a1981-143">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a1981-143">Header</span></span><br/> | <dl> <span data-ttu-id="a1981-144"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="a1981-144"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a1981-145">Confira também</span><span class="sxs-lookup"><span data-stu-id="a1981-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a1981-146">Estruturas do Direct3D</span><span class="sxs-lookup"><span data-stu-id="a1981-146">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[<span data-ttu-id="a1981-147">Notificação assíncrona (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="a1981-147">Asynchronous Notification (Direct3D 9)</span></span>](asynchronous-notification.md)
</dt> </dl>

 

 
