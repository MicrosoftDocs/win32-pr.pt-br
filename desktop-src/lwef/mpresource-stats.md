---
title: Estrutura de MPRESOURCE_STATS (MpClient. h)
description: Estatísticas relacionadas a recursos.
ms.assetid: D1DC4BC9-911D-448C-A421-11D2F51F0A61
keywords:
- Recursos do ambiente Windows herdado da estrutura de MPRESOURCE_STATS
- Ponteiro de estrutura de PMPRESOURCE_STATS recursos de ambiente herdados do Windows
topic_type:
- apiref
api_name:
- MPRESOURCE_STATS
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: afbe1ce6734aabd1093f7acd886af757c51ed83e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455460"
---
# <a name="mpresource_stats-structure"></a><span data-ttu-id="09094-105">\_Estrutura de estatísticas MPRESOURCE</span><span class="sxs-lookup"><span data-stu-id="09094-105">MPRESOURCE\_STATS structure</span></span>

<span data-ttu-id="09094-106">Estatísticas relacionadas a recursos.</span><span class="sxs-lookup"><span data-stu-id="09094-106">Resource-related statistics.</span></span>

## <a name="syntax"></a><span data-ttu-id="09094-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="09094-107">Syntax</span></span>


```C++
typedef struct tagMPRESOURCE_STATS {
  DWORD  PPMProgress;
  UINT64 ProcessCount;
  UINT64 FileCount;
  UINT64 FileBytesCount;
  UINT64 RegKeyCount;
  UINT64 Reserved[4];
} MPRESOURCE_STATS, *PMPRESOURCE_STATS;
```



## <a name="members"></a><span data-ttu-id="09094-108">Membros</span><span class="sxs-lookup"><span data-stu-id="09094-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="09094-109">**PPMProgress**</span><span class="sxs-lookup"><span data-stu-id="09094-109">**PPMProgress**</span></span>
</dt> <dd>

<span data-ttu-id="09094-110">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="09094-110">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="09094-111">Progresso aproximado para verificação em ppm (partes por milhão).</span><span class="sxs-lookup"><span data-stu-id="09094-111">Approximate progress for scan in ppm (parts per million).</span></span> <span data-ttu-id="09094-112">Defina como **MPPROGRESS \_ inválido** se as informações de progresso não estiverem disponíveis.</span><span class="sxs-lookup"><span data-stu-id="09094-112">Set to **MPPROGRESS\_INVALID** if progress information is not available.</span></span>

</dd> <dt>

<span data-ttu-id="09094-113">**ProcessCount**</span><span class="sxs-lookup"><span data-stu-id="09094-113">**ProcessCount**</span></span>
</dt> <dd>

<span data-ttu-id="09094-114">Tipo: **UINT64**</span><span class="sxs-lookup"><span data-stu-id="09094-114">Type: **UINT64**</span></span>

</dd> <dd>

<span data-ttu-id="09094-115">Número de processos verificados.</span><span class="sxs-lookup"><span data-stu-id="09094-115">Number of processes scanned.</span></span>

</dd> <dt>

<span data-ttu-id="09094-116">**FileCount**</span><span class="sxs-lookup"><span data-stu-id="09094-116">**FileCount**</span></span>
</dt> <dd>

<span data-ttu-id="09094-117">Tipo: **UINT64**</span><span class="sxs-lookup"><span data-stu-id="09094-117">Type: **UINT64**</span></span>

</dd> <dd>

<span data-ttu-id="09094-118">Número de arquivos verificados.</span><span class="sxs-lookup"><span data-stu-id="09094-118">Number of files scanned.</span></span>

</dd> <dt>

<span data-ttu-id="09094-119">**FileBytesCount**</span><span class="sxs-lookup"><span data-stu-id="09094-119">**FileBytesCount**</span></span>
</dt> <dd>

<span data-ttu-id="09094-120">Tipo: **UINT64**</span><span class="sxs-lookup"><span data-stu-id="09094-120">Type: **UINT64**</span></span>

</dd> <dd>

<span data-ttu-id="09094-121">Número de bytes verificados em busca de arquivos.</span><span class="sxs-lookup"><span data-stu-id="09094-121">Number of bytes scanned for files.</span></span>

</dd> <dt>

<span data-ttu-id="09094-122">**RegKeyCount**</span><span class="sxs-lookup"><span data-stu-id="09094-122">**RegKeyCount**</span></span>
</dt> <dd>

<span data-ttu-id="09094-123">Tipo: **UINT64**</span><span class="sxs-lookup"><span data-stu-id="09094-123">Type: **UINT64**</span></span>

</dd> <dd>

<span data-ttu-id="09094-124">Número de RegKeys verificados.</span><span class="sxs-lookup"><span data-stu-id="09094-124">Number of RegKeys scanned.</span></span>

</dd> <dt>

<span data-ttu-id="09094-125">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="09094-125">**Reserved**</span></span>
</dt> <dd>

<span data-ttu-id="09094-126">Tipo: **UINT64 \[ 4 \]**</span><span class="sxs-lookup"><span data-stu-id="09094-126">Type: **UINT64\[4\]**</span></span>

</dd> <dd>

<span data-ttu-id="09094-127">Campos reservados para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="09094-127">Fields reserved for future use.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="09094-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="09094-128">Requirements</span></span>



| <span data-ttu-id="09094-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="09094-129">Requirement</span></span> | <span data-ttu-id="09094-130">Valor</span><span class="sxs-lookup"><span data-stu-id="09094-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="09094-131">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="09094-131">Minimum supported client</span></span><br/> | <span data-ttu-id="09094-132">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="09094-132">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="09094-133">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="09094-133">Minimum supported server</span></span><br/> | <span data-ttu-id="09094-134">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="09094-134">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="09094-135">parâmetro</span><span class="sxs-lookup"><span data-stu-id="09094-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="09094-136"><dt>MpClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="09094-136"><dt>MpClient.h</dt></span></span> </dl> |



 

 





