---
title: Enumeração dodownloadstate
description: Especifica a ID do estado de download atual, que faz parte da estrutura de **DO_DOWNLOAD_STATUS** .
keywords:
- Enumeração dodownloadstate, dodownloadstate
topic_type:
- apiref
api_name:
- DODownloadState
api_location:
- deliveryoptimizationdownloadtypes.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/02/2019
ms.openlocfilehash: 4fb882a26d20de3094aa46763d6e1538ccf0c643
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499630"
---
# <a name="dodownloadstate-enumeration"></a><span data-ttu-id="f236f-104">Enumeração dodownloadstate</span><span class="sxs-lookup"><span data-stu-id="f236f-104">DODownloadState enumeration</span></span>

<span data-ttu-id="f236f-105">A enumeração **Dodownloadstate** especifica a ID do estado de download atual, que faz parte da estrutura de **DO_DOWNLOAD_STATUS** .</span><span class="sxs-lookup"><span data-stu-id="f236f-105">The **DODownloadState** enumeration specifies the ID of the current download state, which is part of the **DO_DOWNLOAD_STATUS** structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="f236f-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="f236f-106">Syntax</span></span>

```cpp
typedef enum _DODownloadState
{
  DODownloadState_Created = 0, 
  DODownloadState_Transferring,
  DODownloadState_Transferred, 
  DODownloadState_Finalized,   
  DODownloadState_Aborted,     
  DODownloadState_Paused
} DODownloadState;
```

## <a name="constants"></a><span data-ttu-id="f236f-107">Constantes</span><span class="sxs-lookup"><span data-stu-id="f236f-107">Constants</span></span>

| <span data-ttu-id="f236f-108">Requisito</span><span class="sxs-lookup"><span data-stu-id="f236f-108">Requirement</span></span> | <span data-ttu-id="f236f-109">Valor</span><span class="sxs-lookup"><span data-stu-id="f236f-109">Value</span></span> |
|-|-|
| <span data-ttu-id="f236f-110">DODownloadState_Created</span><span class="sxs-lookup"><span data-stu-id="f236f-110">DODownloadState_Created</span></span> | <span data-ttu-id="f236f-111">O objeto de download foi criado, mas ainda não foi iniciado.</span><span class="sxs-lookup"><span data-stu-id="f236f-111">Download object is created but hasn't been started yet.</span></span> |
| <span data-ttu-id="f236f-112">DODownloadState_Transferring</span><span class="sxs-lookup"><span data-stu-id="f236f-112">DODownloadState_Transferring</span></span> | <span data-ttu-id="f236f-113">O download está em andamento.</span><span class="sxs-lookup"><span data-stu-id="f236f-113">Download is in progress.</span></span> |
| <span data-ttu-id="f236f-114">DODownloadState_Transferred</span><span class="sxs-lookup"><span data-stu-id="f236f-114">DODownloadState_Transferred</span></span> | <span data-ttu-id="f236f-115">O download é transferido e pode ser iniciado novamente baixando outra parte do arquivo.</span><span class="sxs-lookup"><span data-stu-id="f236f-115">Download is transferred and can start again by downloading another portion of the file.</span></span> |
| <span data-ttu-id="f236f-116">DODownloadState_Finalized</span><span class="sxs-lookup"><span data-stu-id="f236f-116">DODownloadState_Finalized</span></span> | <span data-ttu-id="f236f-117">O download foi finalizado e não pode ser iniciado novamente.</span><span class="sxs-lookup"><span data-stu-id="f236f-117">Download is finalized and cannot be started again.</span></span> |
| <span data-ttu-id="f236f-118">DODownloadState_Aborted</span><span class="sxs-lookup"><span data-stu-id="f236f-118">DODownloadState_Aborted</span></span> | <span data-ttu-id="f236f-119">O download foi anulado.</span><span class="sxs-lookup"><span data-stu-id="f236f-119">Download was aborted.</span></span> |
| <span data-ttu-id="f236f-120">DODownloadState_Paused</span><span class="sxs-lookup"><span data-stu-id="f236f-120">DODownloadState_Paused</span></span> | <span data-ttu-id="f236f-121">O download foi pausado sob demanda ou devido a um erro transitório.</span><span class="sxs-lookup"><span data-stu-id="f236f-121">Download has been paused on demand or due to transient error.</span></span> |

## <a name="requirements"></a><span data-ttu-id="f236f-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f236f-122">Requirements</span></span>

| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="f236f-123">**Cliente mínimo com suporte**</span><span class="sxs-lookup"><span data-stu-id="f236f-123">**Minimum supported client**</span></span> | <span data-ttu-id="f236f-124">Somente aplicativos do Windows 10, versão 1809 \[ Win32\]</span><span class="sxs-lookup"><span data-stu-id="f236f-124">Windows 10, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="f236f-125">**Servidor mínimo com suporte**</span><span class="sxs-lookup"><span data-stu-id="f236f-125">**Minimum supported server**</span></span> | <span data-ttu-id="f236f-126">Somente aplicativos do Windows Server, versão 1809 \[ Win32\]</span><span class="sxs-lookup"><span data-stu-id="f236f-126">Windows Server, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="f236f-127">**Cabeçalho**</span><span class="sxs-lookup"><span data-stu-id="f236f-127">**Header**</span></span> | <span data-ttu-id="f236f-128">DeliveryOptimizationDownloadTypes. h</span><span class="sxs-lookup"><span data-stu-id="f236f-128">DeliveryOptimizationDownloadTypes.h</span></span> |
