---
title: Enumeração DODownloadPropertyEx
description: Especifica a ID das propriedades estendidas para a operação de download.
keywords:
- Enumeração DODownloadPropertyEx, DODownloadPropertyEx
topic_type:
- apiref
api_name:
- DODownloadPropertyEx
api_location:
- deliveryoptimizationdownloadtypes.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/29/2019
ms.openlocfilehash: 5df0f53778d9059ef8767f5b8052940847e36c00
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824480"
---
# <a name="dodownloadpropertyex-enumeration"></a><span data-ttu-id="051d3-104">Enumeração DODownloadPropertyEx</span><span class="sxs-lookup"><span data-stu-id="051d3-104">DODownloadPropertyEx enumeration</span></span>

> [!IMPORTANT]
> <span data-ttu-id="051d3-105">A enumeração **DODownloadPropertyEx** foi preterida.</span><span class="sxs-lookup"><span data-stu-id="051d3-105">The **DODownloadPropertyEx** enumeration is deprecated.</span></span> <span data-ttu-id="051d3-106">Em vez disso, use a enumeração [Dobaixeproperty](../deliveryoptimizationdownloadtypes/ne-deliveryoptimizationdownloadtypes-dodownloadproperty.md) com [IDODownload:: GetProperty](../do/nf-do-idodownload-getproperty.md) e [IDODownload:: SetProperty](../do/nf-do-idodownload-setproperty.md).</span><span class="sxs-lookup"><span data-stu-id="051d3-106">Instead, use the [DODownloadProperty](../deliveryoptimizationdownloadtypes/ne-deliveryoptimizationdownloadtypes-dodownloadproperty.md) enumeration with [IDODownload::GetProperty](../do/nf-do-idodownload-getproperty.md) and [IDODownload::SetProperty](../do/nf-do-idodownload-setproperty.md).</span></span>

<span data-ttu-id="051d3-107">A enumeração **DODownloadPropertyEx** especifica a ID das propriedades estendidas para a operação fazer download.</span><span class="sxs-lookup"><span data-stu-id="051d3-107">The **DODownloadPropertyEx** enumeration specifies the ID of extended properties for the DO download operation.</span></span> <span data-ttu-id="051d3-108">Essa enumeração é usada pela interface **IDODownloadInternal** e um valor **Variant** é usado para obter e definir o valor da propriedade.</span><span class="sxs-lookup"><span data-stu-id="051d3-108">This enumeration is used by the **IDODownloadInternal** interface, and a **VARIANT** value is used to get and set the property value.</span></span>

## <a name="syntax"></a><span data-ttu-id="051d3-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="051d3-109">Syntax</span></span>

```cpp
typedef enum _DODownloadPropertyEx
{
  DODownloadPropertyEx_UpdateId = 0,
  DODownloadPropertyEx_CorrelationVector,
  DODownloadPropertyEx_DecryptionInfo,    
  DODownloadPropertyEx_IntegrityCheckInfo,   
  DODownloadPropertyEx_IntegrityCheckMandatory, 
  DODownloadPropertyEx_TotalSizeBytes, 
  DODownloadPropertyEx_TempLocalFileUsage 
} DODownloadPropertyEx;
```
## <a name="constants"></a><span data-ttu-id="051d3-110">Constantes</span><span class="sxs-lookup"><span data-stu-id="051d3-110">Constants</span></span>

| <span data-ttu-id="051d3-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="051d3-111">Requirement</span></span> | <span data-ttu-id="051d3-112">Valor</span><span class="sxs-lookup"><span data-stu-id="051d3-112">Value</span></span> |
|-|-|
| <span data-ttu-id="051d3-113">DODownloadPropertyEx_UpdateId</span><span class="sxs-lookup"><span data-stu-id="051d3-113">DODownloadPropertyEx_UpdateId</span></span> | <span data-ttu-id="051d3-114">Reservado.</span><span class="sxs-lookup"><span data-stu-id="051d3-114">Reserved.</span></span> <span data-ttu-id="051d3-115">Não use.</span><span class="sxs-lookup"><span data-stu-id="051d3-115">Do not use.</span></span> |
| <span data-ttu-id="051d3-116">DODownloadPropertyEx_CorrelationVector</span><span class="sxs-lookup"><span data-stu-id="051d3-116">DODownloadPropertyEx_CorrelationVector</span></span> | <span data-ttu-id="051d3-117">Opcional.</span><span class="sxs-lookup"><span data-stu-id="051d3-117">Optional.</span></span> <span data-ttu-id="051d3-118">Define um vetor de correlação específico para fins de telemetria.</span><span class="sxs-lookup"><span data-stu-id="051d3-118">Sets a specific correlation vector for telemetry purposes.</span></span> <span data-ttu-id="051d3-119">O tipo de variante é VT_BSTR.</span><span class="sxs-lookup"><span data-stu-id="051d3-119">VARIANT type is VT_BSTR.</span></span> |
| <span data-ttu-id="051d3-120">DODownloadPropertyEx_DecryptionInfo</span><span class="sxs-lookup"><span data-stu-id="051d3-120">DODownloadPropertyEx_DecryptionInfo</span></span> | <span data-ttu-id="051d3-121">Reservado.</span><span class="sxs-lookup"><span data-stu-id="051d3-121">Reserved.</span></span> <span data-ttu-id="051d3-122">Não use.</span><span class="sxs-lookup"><span data-stu-id="051d3-122">Do not use.</span></span> |
| <span data-ttu-id="051d3-123">DODownloadPropertyEx_IntegrityCheckInfo</span><span class="sxs-lookup"><span data-stu-id="051d3-123">DODownloadPropertyEx_IntegrityCheckInfo</span></span> | <span data-ttu-id="051d3-124">Opcional somente gravação.</span><span class="sxs-lookup"><span data-stu-id="051d3-124">Optional write-only.</span></span> <span data-ttu-id="051d3-125">Define o local do arquivo de hash da parte (PHF), que é usado pelo para executar verificações de integridade de tempo de execução no conteúdo baixado.</span><span class="sxs-lookup"><span data-stu-id="051d3-125">Sets the piece hash file (PHF) location, which is used by DO to perform runtime integrity checks on the downloaded content.</span></span> <span data-ttu-id="051d3-126">O tipo de variante é VT_BSTR.</span><span class="sxs-lookup"><span data-stu-id="051d3-126">VARIANT type is VT_BSTR.</span></span> |
| <span data-ttu-id="051d3-127">DODownloadPropertyEx_IntegrityCheckMandatory</span><span class="sxs-lookup"><span data-stu-id="051d3-127">DODownloadPropertyEx_IntegrityCheckMandatory</span></span> | <span data-ttu-id="051d3-128">Opcional.</span><span class="sxs-lookup"><span data-stu-id="051d3-128">Optional.</span></span> <span data-ttu-id="051d3-129">Define um sinalizador booliano que indica se o uso do arquivo de hash da parte (PHF) é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="051d3-129">Sets a boolean flag indicating whether usage of the piece hash file (PHF) is mandatory.</span></span> <span data-ttu-id="051d3-130">Se VARIANT_TRUE, o download será anulado quando a verificação de integridade falhar.</span><span class="sxs-lookup"><span data-stu-id="051d3-130">If VARIANT_TRUE, the download will be aborted once the integrity check is failed.</span></span> <span data-ttu-id="051d3-131">O tipo de variante é VT_BOOL.</span><span class="sxs-lookup"><span data-stu-id="051d3-131">VARIANT type is VT_BOOL.</span></span> |
| <span data-ttu-id="051d3-132">DODownloadPropertyEx_TotalSizeBytes</span><span class="sxs-lookup"><span data-stu-id="051d3-132">DODownloadPropertyEx_TotalSizeBytes</span></span> | <span data-ttu-id="051d3-133">Reservado.</span><span class="sxs-lookup"><span data-stu-id="051d3-133">Reserved.</span></span> <span data-ttu-id="051d3-134">Não use.</span><span class="sxs-lookup"><span data-stu-id="051d3-134">Do not use.</span></span> |
| <span data-ttu-id="051d3-135">DODownloadPropertyEx_TempLocalFileUsage</span><span class="sxs-lookup"><span data-stu-id="051d3-135">DODownloadPropertyEx_TempLocalFileUsage</span></span> | <span data-ttu-id="051d3-136">Reservado.</span><span class="sxs-lookup"><span data-stu-id="051d3-136">Reserved.</span></span> <span data-ttu-id="051d3-137">Não use.</span><span class="sxs-lookup"><span data-stu-id="051d3-137">Do not use.</span></span> |

## <a name="requirements"></a><span data-ttu-id="051d3-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="051d3-138">Requirements</span></span>

| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="051d3-139">**Cliente mínimo com suporte**</span><span class="sxs-lookup"><span data-stu-id="051d3-139">**Minimum supported client**</span></span> | <span data-ttu-id="051d3-140">Somente aplicativos do Windows 10, versão 1809 \[ Win32\]</span><span class="sxs-lookup"><span data-stu-id="051d3-140">Windows 10, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="051d3-141">**Servidor mínimo com suporte**</span><span class="sxs-lookup"><span data-stu-id="051d3-141">**Minimum supported server**</span></span> | <span data-ttu-id="051d3-142">Somente aplicativos do Windows Server, versão 1809 \[ Win32\]</span><span class="sxs-lookup"><span data-stu-id="051d3-142">Windows Server, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="051d3-143">**Cabeçalho**</span><span class="sxs-lookup"><span data-stu-id="051d3-143">**Header**</span></span> | <span data-ttu-id="051d3-144">DODownloadInternal. h</span><span class="sxs-lookup"><span data-stu-id="051d3-144">DODownloadInternal.h</span></span> |
