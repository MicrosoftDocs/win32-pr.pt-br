---
title: Estrutura DOSwarmStats (Deliveryoptimization. h)
description: Contém campos para baixar e carregar estatísticas para um arquivo.
ms.assetid: 66B2498A-38E0-44E4-96C1-F778BD9AA593
keywords:
- Estrutura DOSwarmStats
topic_type:
- apiref
api_name:
- DOSwarmStats
api_location:
- deliveryoptimization.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 53d1702c25716ffe90c35727a258134311d5f427
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105793934"
---
# <a name="doswarmstats-structure"></a><span data-ttu-id="2aec8-104">Estrutura DOSwarmStats</span><span class="sxs-lookup"><span data-stu-id="2aec8-104">DOSwarmStats structure</span></span>

<span data-ttu-id="2aec8-105">Contém campos para baixar e carregar estatísticas para um arquivo.</span><span class="sxs-lookup"><span data-stu-id="2aec8-105">Contains fields for download and upload statistics for a file.</span></span>

## <a name="syntax"></a><span data-ttu-id="2aec8-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2aec8-106">Syntax</span></span>


```C++
typedef struct _DOSwarmStats {
  LPWSTR       fileId;
  LPWSTR       sourceURL;
  UINT64       fileSize;
  UINT64       totalBytesDownloaded;
  UINT64       bytesFromLanPeers;
  UINT64       bytesFromGroupPeers;
  UINT64       bytesFromInternetPeers;
  UINT64       bytesFromHttp;
  UINT64       bytesFromDoinc;
  UINT64       bytesToLanPeers;
  UINT64       bytesToGroupPeers;
  UINT64       bytesToInternetPeers;
  UINT         httpConnectionCount;
  UINT         doincConnectionCount;
  UINT         lanConnectionCount;
  UINT         groupConnectionCount;
  UINT         internetConnectionCount;
  UINT         downloadDuration;
  DownloadMode downloadMode;
  SwarmStatus  status;
  BOOL         isBackground;
} DOSwarmStats;
```



## <a name="members"></a><span data-ttu-id="2aec8-107">Membros</span><span class="sxs-lookup"><span data-stu-id="2aec8-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="2aec8-108">**fileId**</span><span class="sxs-lookup"><span data-stu-id="2aec8-108">**fileId**</span></span>
</dt> <dd>

<span data-ttu-id="2aec8-109">Cadeia de caracteres terminada em nulo que foi especificada com a chamada **AddFileWithRanges** .</span><span class="sxs-lookup"><span data-stu-id="2aec8-109">Null-terminated string that was specified with the **AddFileWithRanges** call.</span></span>

</dd> <dt>

<span data-ttu-id="2aec8-110">**sourceURL**</span><span class="sxs-lookup"><span data-stu-id="2aec8-110">**sourceURL**</span></span>
</dt> <dd>

<span data-ttu-id="2aec8-111">Cadeia de caracteres terminada em nulo que contém o nome do arquivo no servidor (por exemplo, https:// &lt; Server &gt; / &lt; Path &gt; /File.ext).</span><span class="sxs-lookup"><span data-stu-id="2aec8-111">Null-terminated string that contains the name of the file on the server (for example, https://&lt;server&gt;/&lt;path&gt;/file.ext).</span></span>

</dd> <dt>

<span data-ttu-id="2aec8-112">**Tamanho**</span><span class="sxs-lookup"><span data-stu-id="2aec8-112">**fileSize**</span></span>
</dt> <dd>

<span data-ttu-id="2aec8-113">Tamanho do arquivo em bytes.</span><span class="sxs-lookup"><span data-stu-id="2aec8-113">Size of the file in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="2aec8-114">**totalBytesDownloaded**</span><span class="sxs-lookup"><span data-stu-id="2aec8-114">**totalBytesDownloaded**</span></span>
</dt> <dd>

<span data-ttu-id="2aec8-115">Número total de bytes transferidos.</span><span class="sxs-lookup"><span data-stu-id="2aec8-115">Total number of bytes transferred.</span></span>

</dd> <dt>

<span data-ttu-id="2aec8-116">**bytesFromLanPeers**</span><span class="sxs-lookup"><span data-stu-id="2aec8-116">**bytesFromLanPeers**</span></span>
</dt> <dd>

<span data-ttu-id="2aec8-117">Número de bytes transferidos de pares de LAN.</span><span class="sxs-lookup"><span data-stu-id="2aec8-117">Number of bytes transferred from LAN peers.</span></span>

</dd> <dt>

<span data-ttu-id="2aec8-118">**bytesFromGroupPeers**</span><span class="sxs-lookup"><span data-stu-id="2aec8-118">**bytesFromGroupPeers**</span></span>
</dt> <dd>

<span data-ttu-id="2aec8-119">Número de bytes transferidos de pares de grupo.</span><span class="sxs-lookup"><span data-stu-id="2aec8-119">Number of bytes transferred from group peers.</span></span>

</dd> <dt>

<span data-ttu-id="2aec8-120">**bytesFromInternetPeers**</span><span class="sxs-lookup"><span data-stu-id="2aec8-120">**bytesFromInternetPeers**</span></span>
</dt> <dd>

<span data-ttu-id="2aec8-121">Número de bytes transferidos de pares da Internet.</span><span class="sxs-lookup"><span data-stu-id="2aec8-121">Number of bytes transferred from Internet peers.</span></span>

</dd> <dt>

<span data-ttu-id="2aec8-122">**bytesFromHttp**</span><span class="sxs-lookup"><span data-stu-id="2aec8-122">**bytesFromHttp**</span></span>
</dt> <dd>

<span data-ttu-id="2aec8-123">Número de bytes transferidos do http.</span><span class="sxs-lookup"><span data-stu-id="2aec8-123">Number of bytes transferred from http.</span></span>

</dd> <dt>

<span data-ttu-id="2aec8-124">**bytesFromDoinc**</span><span class="sxs-lookup"><span data-stu-id="2aec8-124">**bytesFromDoinc**</span></span>
</dt> <dd>

<span data-ttu-id="2aec8-125">Somente para uso interno.</span><span class="sxs-lookup"><span data-stu-id="2aec8-125">For internal use only.</span></span>

</dd> <dt>

<span data-ttu-id="2aec8-126">**bytesToLanPeers**</span><span class="sxs-lookup"><span data-stu-id="2aec8-126">**bytesToLanPeers**</span></span>
</dt> <dd>

<span data-ttu-id="2aec8-127">Número de bytes transferidos para pares de LAN.</span><span class="sxs-lookup"><span data-stu-id="2aec8-127">Number of bytes transferred to LAN peers.</span></span>

</dd> <dt>

<span data-ttu-id="2aec8-128">**bytesToGroupPeers**</span><span class="sxs-lookup"><span data-stu-id="2aec8-128">**bytesToGroupPeers**</span></span>
</dt> <dd>

<span data-ttu-id="2aec8-129">Número de bytes transferidos para pares de grupos.</span><span class="sxs-lookup"><span data-stu-id="2aec8-129">Number of bytes transferred to group peers.</span></span>

</dd> <dt>

<span data-ttu-id="2aec8-130">**bytesToInternetPeers**</span><span class="sxs-lookup"><span data-stu-id="2aec8-130">**bytesToInternetPeers**</span></span>
</dt> <dd>

<span data-ttu-id="2aec8-131">Número de bytes transferidos para pares da Internet.</span><span class="sxs-lookup"><span data-stu-id="2aec8-131">Number of bytes transferred to Internet peers.</span></span>

</dd> <dt>

<span data-ttu-id="2aec8-132">**httpConnectionCount**</span><span class="sxs-lookup"><span data-stu-id="2aec8-132">**httpConnectionCount**</span></span>
</dt> <dd>

<span data-ttu-id="2aec8-133">Contagem de conexões http.</span><span class="sxs-lookup"><span data-stu-id="2aec8-133">Count of http connections.</span></span>

</dd> <dt>

<span data-ttu-id="2aec8-134">**doincConnectionCount**</span><span class="sxs-lookup"><span data-stu-id="2aec8-134">**doincConnectionCount**</span></span>
</dt> <dd>

<span data-ttu-id="2aec8-135">Somente para uso interno.</span><span class="sxs-lookup"><span data-stu-id="2aec8-135">For internal use only.</span></span>

</dd> <dt>

<span data-ttu-id="2aec8-136">**lanConnectionCount**</span><span class="sxs-lookup"><span data-stu-id="2aec8-136">**lanConnectionCount**</span></span>
</dt> <dd>

<span data-ttu-id="2aec8-137">Contagem de conexões de LAN.</span><span class="sxs-lookup"><span data-stu-id="2aec8-137">Count of LAN connections.</span></span>

</dd> <dt>

<span data-ttu-id="2aec8-138">**groupConnectionCount**</span><span class="sxs-lookup"><span data-stu-id="2aec8-138">**groupConnectionCount**</span></span>
</dt> <dd>

<span data-ttu-id="2aec8-139">Contagem de conexões de grupo.</span><span class="sxs-lookup"><span data-stu-id="2aec8-139">Count of group connections.</span></span>

</dd> <dt>

<span data-ttu-id="2aec8-140">**internetConnectionCount**</span><span class="sxs-lookup"><span data-stu-id="2aec8-140">**internetConnectionCount**</span></span>
</dt> <dd>

<span data-ttu-id="2aec8-141">Contagem de conexões com a Internet.</span><span class="sxs-lookup"><span data-stu-id="2aec8-141">Count of Internet connections.</span></span>

</dd> <dt>

<span data-ttu-id="2aec8-142">**downloadDuration**</span><span class="sxs-lookup"><span data-stu-id="2aec8-142">**downloadDuration**</span></span>
</dt> <dd>

<span data-ttu-id="2aec8-143">Duração da transferência de arquivo em milissegundos.</span><span class="sxs-lookup"><span data-stu-id="2aec8-143">Duration of the file transfer in milliseconds.</span></span>

</dd> <dt>

<span data-ttu-id="2aec8-144">**downloadMode**</span><span class="sxs-lookup"><span data-stu-id="2aec8-144">**downloadMode**</span></span>
</dt> <dd>

<span data-ttu-id="2aec8-145">O modo de download usado, consulte [**downloadmode**](downloadmode.md).</span><span class="sxs-lookup"><span data-stu-id="2aec8-145">The download mode used, see [**DownloadMode**](downloadmode.md).</span></span>

</dd> <dt>

<span data-ttu-id="2aec8-146">**status**</span><span class="sxs-lookup"><span data-stu-id="2aec8-146">**status**</span></span>
</dt> <dd>

<span data-ttu-id="2aec8-147">O status de uma transferência de arquivo, consulte [**SwarmStatus**](swarmstatus.md).</span><span class="sxs-lookup"><span data-stu-id="2aec8-147">The status of a file transfer, see [**SwarmStatus**](swarmstatus.md).</span></span>

</dd> <dt>

<span data-ttu-id="2aec8-148">**IsBackground**</span><span class="sxs-lookup"><span data-stu-id="2aec8-148">**isBackground**</span></span>
</dt> <dd>

<span data-ttu-id="2aec8-149">True, se esta for uma transferência em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="2aec8-149">True, if this is a background transfer.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2aec8-150">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2aec8-150">Requirements</span></span>



| <span data-ttu-id="2aec8-151">Requisito</span><span class="sxs-lookup"><span data-stu-id="2aec8-151">Requirement</span></span> | <span data-ttu-id="2aec8-152">Valor</span><span class="sxs-lookup"><span data-stu-id="2aec8-152">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2aec8-153">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2aec8-153">Minimum supported client</span></span><br/> | <span data-ttu-id="2aec8-154">\[Somente aplicativos da área de trabalho do Windows 10, versão 1709\]</span><span class="sxs-lookup"><span data-stu-id="2aec8-154">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="2aec8-155">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2aec8-155">Minimum supported server</span></span><br/> | <span data-ttu-id="2aec8-156">Windows Server, \[ somente aplicativos da área de trabalho da versão 1709\]</span><span class="sxs-lookup"><span data-stu-id="2aec8-156">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="2aec8-157">parâmetro</span><span class="sxs-lookup"><span data-stu-id="2aec8-157">Header</span></span><br/>                   | <dl> <span data-ttu-id="2aec8-158"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="2aec8-158"><dt>Deliveryoptimization.h</dt></span></span> </dl> |



 

 





