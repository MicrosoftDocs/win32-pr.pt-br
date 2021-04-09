---
title: Estrutura de MPSIGUPDATE_DATA (MpClient. h)
description: Dados de notificação passados para a função de retorno de chamada de atualização de assinatura.
ms.assetid: E999ABC2-CC72-43CC-86D9-4F29E9128E1A
keywords:
- Recursos do ambiente Windows herdado da estrutura de MPSIGUPDATE_DATA
- Ponteiro de estrutura de PMPSIGUPDATE_DATA recursos de ambiente herdados do Windows
topic_type:
- apiref
api_name:
- MPSIGUPDATE_DATA
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 442b19da394043b6fc6b8693f51c5f150233f970
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085842"
---
# <a name="mpsigupdate_data-structure"></a><span data-ttu-id="eddce-105">\_Estrutura de dados MPSIGUPDATE</span><span class="sxs-lookup"><span data-stu-id="eddce-105">MPSIGUPDATE\_DATA structure</span></span>

<span data-ttu-id="eddce-106">Dados de notificação passados para a função de retorno de chamada de atualização de assinatura.</span><span class="sxs-lookup"><span data-stu-id="eddce-106">Notification data passed to the signature update callback function.</span></span>

## <a name="syntax"></a><span data-ttu-id="eddce-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="eddce-107">Syntax</span></span>


```C++
typedef struct tagMPSIGUPDATE_DATA {
  DWORD                 dwPercentComplete;
  DWORD                 dwTotalUpdates;
  DWORD                 dwCurrentUpdateIndex;
  MPSIGUPDATE_TYPE      eType;
  MP_UPDATE_STAGE       Stage;
  MP_MIDL_STRING LPWSTR Path;
} MPSIGUPDATE_DATA, *PMPSIGUPDATE_DATA;
```



## <a name="members"></a><span data-ttu-id="eddce-108">Membros</span><span class="sxs-lookup"><span data-stu-id="eddce-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="eddce-109">**dwPercentComplete**</span><span class="sxs-lookup"><span data-stu-id="eddce-109">**dwPercentComplete**</span></span>
</dt> <dd>

<span data-ttu-id="eddce-110">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="eddce-110">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="eddce-111">Uma estimativa da porcentagem em todas as atualizações que foram baixadas e/ou instaladas.</span><span class="sxs-lookup"><span data-stu-id="eddce-111">An estimate of the percentage across all the updates that have been downloaded and/or installed.</span></span>

</dd> <dt>

<span data-ttu-id="eddce-112">**dwTotalUpdates**</span><span class="sxs-lookup"><span data-stu-id="eddce-112">**dwTotalUpdates**</span></span>
</dt> <dd>

<span data-ttu-id="eddce-113">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="eddce-113">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="eddce-114">Número total de atualizações a serem baixadas e/ou instaladas.</span><span class="sxs-lookup"><span data-stu-id="eddce-114">Total number of updates to download and/or install.</span></span>

</dd> <dt>

<span data-ttu-id="eddce-115">**dwCurrentUpdateIndex**</span><span class="sxs-lookup"><span data-stu-id="eddce-115">**dwCurrentUpdateIndex**</span></span>
</dt> <dd>

<span data-ttu-id="eddce-116">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="eddce-116">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="eddce-117">Valor de índice com base em zero que especifica qual atualização entre esses necessários está sendo baixada e/ou instalada no momento.</span><span class="sxs-lookup"><span data-stu-id="eddce-117">Zero-based index value that specifies which update among those required is currently being downloaded and/or installed.</span></span>

</dd> <dt>

<span data-ttu-id="eddce-118">**eType**</span><span class="sxs-lookup"><span data-stu-id="eddce-118">**eType**</span></span>
</dt> <dd>

<span data-ttu-id="eddce-119">Tipo: **\_ tipo de MPSIGUPDATE**</span><span class="sxs-lookup"><span data-stu-id="eddce-119">Type: **MPSIGUPDATE\_TYPE**</span></span>

</dd> <dd>

<span data-ttu-id="eddce-120">Tipo de atualização.</span><span class="sxs-lookup"><span data-stu-id="eddce-120">Update type.</span></span> <span data-ttu-id="eddce-121">Um dos seguintes valores possíveis:</span><span class="sxs-lookup"><span data-stu-id="eddce-121">One of the following possible values:</span></span>



| <span data-ttu-id="eddce-122">Valor</span><span class="sxs-lookup"><span data-stu-id="eddce-122">Value</span></span>                                                                                                                                                                                                                             | <span data-ttu-id="eddce-123">Significado</span><span class="sxs-lookup"><span data-stu-id="eddce-123">Meaning</span></span>                                                                     |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <span id="MPSIGUPDATE_TYPE_NONE"></span><span id="mpsigupdate_type_none"></span><dl> <span data-ttu-id="eddce-124"><dt>**MPSIGUPDATE \_ tipo \_ nenhum**</dt></span><span class="sxs-lookup"><span data-stu-id="eddce-124"><dt>**MPSIGUPDATE\_TYPE\_NONE**</dt></span></span> </dl>                                            |                                                                             |
| <span id="MPSIGUPDATE_TYPE_MANAGED"></span><span id="mpsigupdate_type_managed"></span><dl> <span data-ttu-id="eddce-125"><dt>**tipo de MPSIGUPDATE \_ \_ gerenciado**</dt></span><span class="sxs-lookup"><span data-stu-id="eddce-125"><dt>**MPSIGUPDATE\_TYPE\_MANAGED**</dt></span></span> </dl>                                   | <span data-ttu-id="eddce-126">Atualização do WSUS.</span><span class="sxs-lookup"><span data-stu-id="eddce-126">WSUS update.</span></span> <span data-ttu-id="eddce-127">Cancelar requer direitos de administrador.</span><span class="sxs-lookup"><span data-stu-id="eddce-127">Cancel requires administrator rights.</span></span><br/>               |
| <span id="MPSIGUPDATE_TYPE_HTTP"></span><span id="mpsigupdate_type_http"></span><dl> <span data-ttu-id="eddce-128"><dt>**MPSIGUPDATE \_ tipo \_ http**</dt></span><span class="sxs-lookup"><span data-stu-id="eddce-128"><dt>**MPSIGUPDATE\_TYPE\_HTTP**</dt></span></span> </dl>                                            | <span data-ttu-id="eddce-129">Atualização de HTTP.</span><span class="sxs-lookup"><span data-stu-id="eddce-129">HTTP update.</span></span> <span data-ttu-id="eddce-130">Direitos de administrador não necessários para cancelar.</span><span class="sxs-lookup"><span data-stu-id="eddce-130">Administrator rights not needed to cancel.</span></span><br/>          |
| <span id="MPSIGUPDATE_TYPE_HTTP_SRV"></span><span id="mpsigupdate_type_http_srv"></span><dl> <span data-ttu-id="eddce-131"><dt>**MPSIGUPDATE \_ tipo \_ http \_ SRV**</dt></span><span class="sxs-lookup"><span data-stu-id="eddce-131"><dt>**MPSIGUPDATE\_TYPE\_HTTP\_SRV**</dt></span></span> </dl>                               | <span data-ttu-id="eddce-132">HTTP do serviço.</span><span class="sxs-lookup"><span data-stu-id="eddce-132">HTTP from service.</span></span> <span data-ttu-id="eddce-133">Cancelar requer direitos de administrador.</span><span class="sxs-lookup"><span data-stu-id="eddce-133">Cancel requires administrator rights.</span></span><br/>         |
| <span id="MPSIGUPDATE_TYPE_UNC"></span><span id="mpsigupdate_type_unc"></span><dl> <span data-ttu-id="eddce-134"><dt>**MPSIGUPDATE de \_ tipo \_ UNC**</dt></span><span class="sxs-lookup"><span data-stu-id="eddce-134"><dt>**MPSIGUPDATE\_TYPE\_UNC**</dt></span></span> </dl>                                               | <span data-ttu-id="eddce-135">Compartilhamento UNC.</span><span class="sxs-lookup"><span data-stu-id="eddce-135">UNC share.</span></span> <span data-ttu-id="eddce-136">Direitos de administrador não necessários para cancelar.</span><span class="sxs-lookup"><span data-stu-id="eddce-136">Administrator rights not needed to cancel.</span></span><br/>            |
| <span id="MPSIGUPDATE_TYPE_UNMANAGED"></span><span id="mpsigupdate_type_unmanaged"></span><dl> <span data-ttu-id="eddce-137"><dt>**tipo de MPSIGUPDATE \_ \_ não gerenciado**</dt></span><span class="sxs-lookup"><span data-stu-id="eddce-137"><dt>**MPSIGUPDATE\_TYPE\_UNMANAGED**</dt></span></span> </dl>                             | <span data-ttu-id="eddce-138">Atualização do MU/WU.</span><span class="sxs-lookup"><span data-stu-id="eddce-138">MU/WU update.</span></span> <span data-ttu-id="eddce-139">Cancelar requer direitos de administrador.</span><span class="sxs-lookup"><span data-stu-id="eddce-139">Cancel requires administrator rights.</span></span><br/>              |
| <span id="MPSIGUPDATE_TYPE_MANAGED_PLATFORM"></span><span id="mpsigupdate_type_managed_platform"></span><dl> <span data-ttu-id="eddce-140"><dt>**\_ \_ plataforma gerenciada do tipo MPSIGUPDATE \_**</dt></span><span class="sxs-lookup"><span data-stu-id="eddce-140"><dt>**MPSIGUPDATE\_TYPE\_MANAGED\_PLATFORM**</dt></span></span> </dl>       | <span data-ttu-id="eddce-141">Atualização do WSUS para plataforma.</span><span class="sxs-lookup"><span data-stu-id="eddce-141">WSUS update for PLATFORM.</span></span> <span data-ttu-id="eddce-142">Cancelar requer direitos de administrador.</span><span class="sxs-lookup"><span data-stu-id="eddce-142">Cancel requires administrator rights.</span></span><br/>  |
| <span id="MPSIGUPDATE_TYPE_UNMANAGED_PLATFORM"></span><span id="mpsigupdate_type_unmanaged_platform"></span><dl> <span data-ttu-id="eddce-143"><dt>**\_ \_ plataforma não gerenciada do tipo MPSIGUPDATE \_**</dt></span><span class="sxs-lookup"><span data-stu-id="eddce-143"><dt>**MPSIGUPDATE\_TYPE\_UNMANAGED\_PLATFORM**</dt></span></span> </dl> | <span data-ttu-id="eddce-144">Atualização do MU/WU para plataforma.</span><span class="sxs-lookup"><span data-stu-id="eddce-144">MU/WU update for PLATFORM.</span></span> <span data-ttu-id="eddce-145">Cancelar requer direitos de administrador.</span><span class="sxs-lookup"><span data-stu-id="eddce-145">Cancel requires administrator rights.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="eddce-146">**Estágio**</span><span class="sxs-lookup"><span data-stu-id="eddce-146">**Stage**</span></span>
</dt> <dd>

<span data-ttu-id="eddce-147">Tipo: **\_ \_ estágio de atualização do MP**</span><span class="sxs-lookup"><span data-stu-id="eddce-147">Type: **MP\_UPDATE\_STAGE**</span></span>

</dd> <dd>

<span data-ttu-id="eddce-148">Estágio de atualização.</span><span class="sxs-lookup"><span data-stu-id="eddce-148">Update stage.</span></span> <span data-ttu-id="eddce-149">Um dos seguintes valores possíveis:</span><span class="sxs-lookup"><span data-stu-id="eddce-149">One of the following possible values:</span></span>



| <span data-ttu-id="eddce-150">Valor</span><span class="sxs-lookup"><span data-stu-id="eddce-150">Value</span></span>                                                                                                                                                                         | <span data-ttu-id="eddce-151">Significado</span><span class="sxs-lookup"><span data-stu-id="eddce-151">Meaning</span></span>                           |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------|
| <span id="MP_STAGE_UNKNOWN"></span><span id="mp_stage_unknown"></span><dl> <span data-ttu-id="eddce-152"><dt>**\_estágio MP \_ desconhecido**</dt></span><span class="sxs-lookup"><span data-stu-id="eddce-152"><dt>**MP\_STAGE\_UNKNOWN**</dt></span></span> </dl>       | <span data-ttu-id="eddce-153">Estágio de atualização desconhecido.</span><span class="sxs-lookup"><span data-stu-id="eddce-153">Update stage unknown.</span></span><br/>  |
| <span id="MP_SEARCH_UPDATE"></span><span id="mp_search_update"></span><dl> <span data-ttu-id="eddce-154"><dt>**\_atualização de pesquisa de PG \_**</dt></span><span class="sxs-lookup"><span data-stu-id="eddce-154"><dt>**MP\_SEARCH\_UPDATE**</dt></span></span> </dl>       | <span data-ttu-id="eddce-155">Atualizar estágio de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="eddce-155">Update search stage.</span></span><br/>   |
| <span id="MP_DOWNLOAD_UPDATE"></span><span id="mp_download_update"></span><dl> <span data-ttu-id="eddce-156"><dt>**\_atualização de download do MP \_**</dt></span><span class="sxs-lookup"><span data-stu-id="eddce-156"><dt>**MP\_DOWNLOAD\_UPDATE**</dt></span></span> </dl> | <span data-ttu-id="eddce-157">Atualizar estágio de download.</span><span class="sxs-lookup"><span data-stu-id="eddce-157">Update download stage.</span></span><br/> |
| <span id="MP_INSTALL_UPDATE"></span><span id="mp_install_update"></span><dl> <span data-ttu-id="eddce-158"><dt>**\_atualização de instalação do MP \_**</dt></span><span class="sxs-lookup"><span data-stu-id="eddce-158"><dt>**MP\_INSTALL\_UPDATE**</dt></span></span> </dl>    | <span data-ttu-id="eddce-159">Atualizar estágio de instalação.</span><span class="sxs-lookup"><span data-stu-id="eddce-159">Update install stage.</span></span><br/>  |



 

</dd> <dt>

<span data-ttu-id="eddce-160">**Caminho**</span><span class="sxs-lookup"><span data-stu-id="eddce-160">**Path**</span></span>
</dt> <dd>

<span data-ttu-id="eddce-161">Tipo: **PG \_ MIDL \_ String LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="eddce-161">Type: **MP\_MIDL\_STRING LPWSTR**</span></span>

</dd> <dd>

<span data-ttu-id="eddce-162">Caminho de atualização.</span><span class="sxs-lookup"><span data-stu-id="eddce-162">Update path.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="eddce-163">Requisitos</span><span class="sxs-lookup"><span data-stu-id="eddce-163">Requirements</span></span>



| <span data-ttu-id="eddce-164">Requisito</span><span class="sxs-lookup"><span data-stu-id="eddce-164">Requirement</span></span> | <span data-ttu-id="eddce-165">Valor</span><span class="sxs-lookup"><span data-stu-id="eddce-165">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="eddce-166">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="eddce-166">Minimum supported client</span></span><br/> | <span data-ttu-id="eddce-167">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="eddce-167">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="eddce-168">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="eddce-168">Minimum supported server</span></span><br/> | <span data-ttu-id="eddce-169">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="eddce-169">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="eddce-170">parâmetro</span><span class="sxs-lookup"><span data-stu-id="eddce-170">Header</span></span><br/>                   | <dl> <span data-ttu-id="eddce-171"><dt>MpClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="eddce-171"><dt>MpClient.h</dt></span></span> </dl> |



 

 





