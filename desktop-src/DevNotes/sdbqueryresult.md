---
description: Contém os resultados da consulta do banco de dados Shim para um executável correspondente.
ms.assetid: 6e6df118-fb64-4a97-9280-050e3b4e3a4b
title: Estrutura SDBQUERYRESULT
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SDBQUERYRESULT
api_type:
- NA
api_location: ''
ms.openlocfilehash: 9c631438d36116d47bfcb8675c390fb2974271c8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920263"
---
# <a name="sdbqueryresult-structure"></a><span data-ttu-id="fa07e-103">Estrutura SDBQUERYRESULT</span><span class="sxs-lookup"><span data-stu-id="fa07e-103">SDBQUERYRESULT structure</span></span>

<span data-ttu-id="fa07e-104">Contém os resultados da consulta do banco de dados Shim para um executável correspondente.</span><span class="sxs-lookup"><span data-stu-id="fa07e-104">Contains the results from querying the shim database for a matching executable.</span></span>

## <a name="syntax"></a><span data-ttu-id="fa07e-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fa07e-105">Syntax</span></span>


```C++
typedef struct tagSDBQUERYRESULT {
  TAGREF atrExes[SDB_MAX_EXES];
  DWORD  adwExeFlags[SDB_MAX_EXES];
  TAGREF atrLayers[SDB_MAX_LAYERS];
  DWORD  dwLayerFlags;
  TAGREF trApphelp;
  DWORD  dwExeCount;
  DWORD  dwLayerCount;
  GUID   guidID;
  DWORD  dwFlags;
  DWORD  dwCustomSDBMap;
  GUID   rgGuidDB[SDB_MAX_SDBS];
} SDBQUERYRESULT, *PSDBQUERYRESULT;
```



## <a name="members"></a><span data-ttu-id="fa07e-106">Membros</span><span class="sxs-lookup"><span data-stu-id="fa07e-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="fa07e-107">**atrExes**</span><span class="sxs-lookup"><span data-stu-id="fa07e-107">**atrExes**</span></span>
</dt> <dd>

<span data-ttu-id="fa07e-108">Os valores de **TAGREF** dos arquivos executáveis correspondentes.</span><span class="sxs-lookup"><span data-stu-id="fa07e-108">The **TAGREF** values of the matching executable files.</span></span> <span data-ttu-id="fa07e-109">Observe que **sdb \_ Max \_ EXES** é definido como 16.</span><span class="sxs-lookup"><span data-stu-id="fa07e-109">Note that **SDB\_MAX\_EXES** is defined as 16.</span></span>

</dd> <dt>

<span data-ttu-id="fa07e-110">**adwExeFlags**</span><span class="sxs-lookup"><span data-stu-id="fa07e-110">**adwExeFlags**</span></span>
</dt> <dd>

<span data-ttu-id="fa07e-111">Esse parâmetro pode ser um ou mais dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="fa07e-111">This parameter can be one or more of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="fa07e-112"><span id="SHIMREG_DISABLE_SHIM"></span><span id="shimreg_disable_shim"></span>**SHIMREG \_ DESABILITAR \_ Shim** (0x00000001)</span><span class="sxs-lookup"><span data-stu-id="fa07e-112"><span id="SHIMREG_DISABLE_SHIM"></span><span id="shimreg_disable_shim"></span>**SHIMREG\_DISABLE\_SHIM** (0x00000001)</span></span>
</dt> <dt>

<span data-ttu-id="fa07e-113"><span id="SHIMREG_DISABLE_APPHELP"></span><span id="shimreg_disable_apphelp"></span>**SHIMREG \_ DESABILITAR \_ APPHELP** (0x00000002)</span><span class="sxs-lookup"><span data-stu-id="fa07e-113"><span id="SHIMREG_DISABLE_APPHELP"></span><span id="shimreg_disable_apphelp"></span>**SHIMREG\_DISABLE\_APPHELP** (0x00000002)</span></span>
</dt> <dt>

<span data-ttu-id="fa07e-114"><span id="SHIMREG_APPHELP_NOUI"></span><span id="shimreg_apphelp_noui"></span>**SHIMREG \_ \_NOUI APPHELP** (0x00000004)</span><span class="sxs-lookup"><span data-stu-id="fa07e-114"><span id="SHIMREG_APPHELP_NOUI"></span><span id="shimreg_apphelp_noui"></span>**SHIMREG\_APPHELP\_NOUI** (0x00000004)</span></span>
</dt> <dt>

<span data-ttu-id="fa07e-115"><span id="SHIMREG_APPHELP_CANCEL"></span><span id="shimreg_apphelp_cancel"></span>**SHIMREG \_ \_Cancelamento de APPHELP** (0x10000000)</span><span class="sxs-lookup"><span data-stu-id="fa07e-115"><span id="SHIMREG_APPHELP_CANCEL"></span><span id="shimreg_apphelp_cancel"></span>**SHIMREG\_APPHELP\_CANCEL** (0x10000000)</span></span>
</dt> <dt>

<span data-ttu-id="fa07e-116"><span id="SHIMREG_DISABLE_SXS"></span><span id="shimreg_disable_sxs"></span>**SHIMREG \_ DESABILITAR \_ SxS** (0x00000010)</span><span class="sxs-lookup"><span data-stu-id="fa07e-116"><span id="SHIMREG_DISABLE_SXS"></span><span id="shimreg_disable_sxs"></span>**SHIMREG\_DISABLE\_SXS** (0x00000010)</span></span>
</dt> <dt>

<span data-ttu-id="fa07e-117"><span id="SHIMREG_DISABLE_LAYER"></span><span id="shimreg_disable_layer"></span>**SHIMREG \_ DESABILITAR \_ camada** (0x00000020)</span><span class="sxs-lookup"><span data-stu-id="fa07e-117"><span id="SHIMREG_DISABLE_LAYER"></span><span id="shimreg_disable_layer"></span>**SHIMREG\_DISABLE\_LAYER** (0x00000020)</span></span>
</dt> <dt>

<span data-ttu-id="fa07e-118"><span id="SHIMREG_DISABLE_DRIVER"></span><span id="shimreg_disable_driver"></span>**SHIMREG \_ DESABILITAR \_ Driver** (0x00000040)</span><span class="sxs-lookup"><span data-stu-id="fa07e-118"><span id="SHIMREG_DISABLE_DRIVER"></span><span id="shimreg_disable_driver"></span>**SHIMREG\_DISABLE\_DRIVER** (0x00000040)</span></span>
</dt> </dl> </dd> <dt>

<span data-ttu-id="fa07e-119">**atrLayers**</span><span class="sxs-lookup"><span data-stu-id="fa07e-119">**atrLayers**</span></span>
</dt> <dd>

<span data-ttu-id="fa07e-120">Os valores de **TAGREF** das camadas correspondentes.</span><span class="sxs-lookup"><span data-stu-id="fa07e-120">The **TAGREF** values of the matching layers.</span></span> <span data-ttu-id="fa07e-121">Observe que **as \_ \_ camadas sdb Max** são definidas como 8.</span><span class="sxs-lookup"><span data-stu-id="fa07e-121">Note that **SDB\_MAX\_LAYERS** is defined as 8.</span></span>

</dd> <dt>

<span data-ttu-id="fa07e-122">**dwLayerFlags**</span><span class="sxs-lookup"><span data-stu-id="fa07e-122">**dwLayerFlags**</span></span>
</dt> <dd>

<span data-ttu-id="fa07e-123">Esse parâmetro pode ser um ou mais dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="fa07e-123">This parameter can be one or more of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="fa07e-124"><span id="SHIMREG_DISABLE_SHIM"></span><span id="shimreg_disable_shim"></span>**SHIMREG \_ DESABILITAR \_ Shim** (0x00000001)</span><span class="sxs-lookup"><span data-stu-id="fa07e-124"><span id="SHIMREG_DISABLE_SHIM"></span><span id="shimreg_disable_shim"></span>**SHIMREG\_DISABLE\_SHIM** (0x00000001)</span></span>
</dt> <dt>

<span data-ttu-id="fa07e-125"><span id="SHIMREG_DISABLE_APPHELP"></span><span id="shimreg_disable_apphelp"></span>**SHIMREG \_ DESABILITAR \_ APPHELP** (0x00000002)</span><span class="sxs-lookup"><span data-stu-id="fa07e-125"><span id="SHIMREG_DISABLE_APPHELP"></span><span id="shimreg_disable_apphelp"></span>**SHIMREG\_DISABLE\_APPHELP** (0x00000002)</span></span>
</dt> <dt>

<span data-ttu-id="fa07e-126"><span id="SHIMREG_APPHELP_NOUI"></span><span id="shimreg_apphelp_noui"></span>**SHIMREG \_ \_NOUI APPHELP** (0x00000004)</span><span class="sxs-lookup"><span data-stu-id="fa07e-126"><span id="SHIMREG_APPHELP_NOUI"></span><span id="shimreg_apphelp_noui"></span>**SHIMREG\_APPHELP\_NOUI** (0x00000004)</span></span>
</dt> <dt>

<span data-ttu-id="fa07e-127"><span id="SHIMREG_APPHELP_CANCEL"></span><span id="shimreg_apphelp_cancel"></span>**SHIMREG \_ \_Cancelamento de APPHELP** (0x10000000)</span><span class="sxs-lookup"><span data-stu-id="fa07e-127"><span id="SHIMREG_APPHELP_CANCEL"></span><span id="shimreg_apphelp_cancel"></span>**SHIMREG\_APPHELP\_CANCEL** (0x10000000)</span></span>
</dt> <dt>

<span data-ttu-id="fa07e-128"><span id="SHIMREG_DISABLE_SXS"></span><span id="shimreg_disable_sxs"></span>**SHIMREG \_ DESABILITAR \_ SxS** (0x00000010)</span><span class="sxs-lookup"><span data-stu-id="fa07e-128"><span id="SHIMREG_DISABLE_SXS"></span><span id="shimreg_disable_sxs"></span>**SHIMREG\_DISABLE\_SXS** (0x00000010)</span></span>
</dt> <dt>

<span data-ttu-id="fa07e-129"><span id="SHIMREG_DISABLE_LAYER"></span><span id="shimreg_disable_layer"></span>**SHIMREG \_ DESABILITAR \_ camada** (0x00000020)</span><span class="sxs-lookup"><span data-stu-id="fa07e-129"><span id="SHIMREG_DISABLE_LAYER"></span><span id="shimreg_disable_layer"></span>**SHIMREG\_DISABLE\_LAYER** (0x00000020)</span></span>
</dt> <dt>

<span data-ttu-id="fa07e-130"><span id="SHIMREG_DISABLE_DRIVER"></span><span id="shimreg_disable_driver"></span>**SHIMREG \_ DESABILITAR \_ Driver** (0x00000040)</span><span class="sxs-lookup"><span data-stu-id="fa07e-130"><span id="SHIMREG_DISABLE_DRIVER"></span><span id="shimreg_disable_driver"></span>**SHIMREG\_DISABLE\_DRIVER** (0x00000040)</span></span>
</dt> </dl> </dd> <dt>

<span data-ttu-id="fa07e-131">**trApphelp**</span><span class="sxs-lookup"><span data-stu-id="fa07e-131">**trApphelp**</span></span>
</dt> <dd>

<span data-ttu-id="fa07e-132">O valor **TAGREF** da mensagem AppHelp do executável correspondente.</span><span class="sxs-lookup"><span data-stu-id="fa07e-132">The **TAGREF** value of the apphelp message of the corresponding executable.</span></span>

</dd> <dt>

<span data-ttu-id="fa07e-133">**dwExeCount**</span><span class="sxs-lookup"><span data-stu-id="fa07e-133">**dwExeCount**</span></span>
</dt> <dd>

<span data-ttu-id="fa07e-134">O número de elementos em **atrExes**.</span><span class="sxs-lookup"><span data-stu-id="fa07e-134">The number of elements in **atrExes**.</span></span>

</dd> <dt>

<span data-ttu-id="fa07e-135">**dwLayerCount**</span><span class="sxs-lookup"><span data-stu-id="fa07e-135">**dwLayerCount**</span></span>
</dt> <dd>

<span data-ttu-id="fa07e-136">O número de elementos em **atrLayers**.</span><span class="sxs-lookup"><span data-stu-id="fa07e-136">The number of elements in **atrLayers**.</span></span>

</dd> <dt>

<span data-ttu-id="fa07e-137">**guidID**</span><span class="sxs-lookup"><span data-stu-id="fa07e-137">**guidID**</span></span>
</dt> <dd>

<span data-ttu-id="fa07e-138">O GUID do último arquivo executável.</span><span class="sxs-lookup"><span data-stu-id="fa07e-138">The GUID of the last executable file.</span></span>

</dd> <dt>

<span data-ttu-id="fa07e-139">**dwFlags**</span><span class="sxs-lookup"><span data-stu-id="fa07e-139">**dwFlags**</span></span>
</dt> <dd>

<span data-ttu-id="fa07e-140">Esse parâmetro pode ser um ou mais dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="fa07e-140">This parameter can be one or more of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="fa07e-141"><span id="SHIMREG_DISABLE_SHIM"></span><span id="shimreg_disable_shim"></span>**SHIMREG \_ DESABILITAR \_ Shim** (0x00000001)</span><span class="sxs-lookup"><span data-stu-id="fa07e-141"><span id="SHIMREG_DISABLE_SHIM"></span><span id="shimreg_disable_shim"></span>**SHIMREG\_DISABLE\_SHIM** (0x00000001)</span></span>
</dt> <dt>

<span data-ttu-id="fa07e-142"><span id="SHIMREG_DISABLE_APPHELP"></span><span id="shimreg_disable_apphelp"></span>**SHIMREG \_ DESABILITAR \_ APPHELP** (0x00000002)</span><span class="sxs-lookup"><span data-stu-id="fa07e-142"><span id="SHIMREG_DISABLE_APPHELP"></span><span id="shimreg_disable_apphelp"></span>**SHIMREG\_DISABLE\_APPHELP** (0x00000002)</span></span>
</dt> <dt>

<span data-ttu-id="fa07e-143"><span id="SHIMREG_APPHELP_NOUI"></span><span id="shimreg_apphelp_noui"></span>**SHIMREG \_ \_NOUI APPHELP** (0x00000004)</span><span class="sxs-lookup"><span data-stu-id="fa07e-143"><span id="SHIMREG_APPHELP_NOUI"></span><span id="shimreg_apphelp_noui"></span>**SHIMREG\_APPHELP\_NOUI** (0x00000004)</span></span>
</dt> <dt>

<span data-ttu-id="fa07e-144"><span id="SHIMREG_APPHELP_CANCEL"></span><span id="shimreg_apphelp_cancel"></span>**SHIMREG \_ \_Cancelamento de APPHELP** (0x10000000)</span><span class="sxs-lookup"><span data-stu-id="fa07e-144"><span id="SHIMREG_APPHELP_CANCEL"></span><span id="shimreg_apphelp_cancel"></span>**SHIMREG\_APPHELP\_CANCEL** (0x10000000)</span></span>
</dt> <dt>

<span data-ttu-id="fa07e-145"><span id="SHIMREG_DISABLE_SXS"></span><span id="shimreg_disable_sxs"></span>**SHIMREG \_ DESABILITAR \_ SxS** (0x00000010)</span><span class="sxs-lookup"><span data-stu-id="fa07e-145"><span id="SHIMREG_DISABLE_SXS"></span><span id="shimreg_disable_sxs"></span>**SHIMREG\_DISABLE\_SXS** (0x00000010)</span></span>
</dt> <dt>

<span data-ttu-id="fa07e-146"><span id="SHIMREG_DISABLE_LAYER"></span><span id="shimreg_disable_layer"></span>**SHIMREG \_ DESABILITAR \_ camada** (0x00000020)</span><span class="sxs-lookup"><span data-stu-id="fa07e-146"><span id="SHIMREG_DISABLE_LAYER"></span><span id="shimreg_disable_layer"></span>**SHIMREG\_DISABLE\_LAYER** (0x00000020)</span></span>
</dt> <dt>

<span data-ttu-id="fa07e-147"><span id="SHIMREG_DISABLE_DRIVER"></span><span id="shimreg_disable_driver"></span>**SHIMREG \_ DESABILITAR \_ Driver** (0x00000040)</span><span class="sxs-lookup"><span data-stu-id="fa07e-147"><span id="SHIMREG_DISABLE_DRIVER"></span><span id="shimreg_disable_driver"></span>**SHIMREG\_DISABLE\_DRIVER** (0x00000040)</span></span>
</dt> </dl> </dd> <dt>

<span data-ttu-id="fa07e-148">**dwCustomSDBMap**</span><span class="sxs-lookup"><span data-stu-id="fa07e-148">**dwCustomSDBMap**</span></span>
</dt> <dd>

<span data-ttu-id="fa07e-149">Um mapa dos bancos de dados de shims personalizados.</span><span class="sxs-lookup"><span data-stu-id="fa07e-149">A map of the custom shim databases.</span></span> <span data-ttu-id="fa07e-150">Os bits correspondentes serão definidos se **rgGuidDB** for válido.</span><span class="sxs-lookup"><span data-stu-id="fa07e-150">The corresponding bits are set if **rgGuidDB** is valid.</span></span>

</dd> <dt>

<span data-ttu-id="fa07e-151">**rgGuidDB**</span><span class="sxs-lookup"><span data-stu-id="fa07e-151">**rgGuidDB**</span></span>
</dt> <dd>

<span data-ttu-id="fa07e-152">Os GUIDs dos bancos de dados de Shim.</span><span class="sxs-lookup"><span data-stu-id="fa07e-152">The GUIDs of the shim databases.</span></span> <span data-ttu-id="fa07e-153">Observe que **sdb \_ Max \_ SDBS** é definido como 16.</span><span class="sxs-lookup"><span data-stu-id="fa07e-153">Note that **SDB\_MAX\_SDBS** is defined as 16.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="fa07e-154">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fa07e-154">Requirements</span></span>



| <span data-ttu-id="fa07e-155">Requisito</span><span class="sxs-lookup"><span data-stu-id="fa07e-155">Requirement</span></span> | <span data-ttu-id="fa07e-156">Valor</span><span class="sxs-lookup"><span data-stu-id="fa07e-156">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="fa07e-157">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fa07e-157">Minimum supported client</span></span><br/> | <span data-ttu-id="fa07e-158">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="fa07e-158">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="fa07e-159">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fa07e-159">Minimum supported server</span></span><br/> | <span data-ttu-id="fa07e-160">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="fa07e-160">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="fa07e-161">Confira também</span><span class="sxs-lookup"><span data-stu-id="fa07e-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fa07e-162">**SdbGetMatchingExe**</span><span class="sxs-lookup"><span data-stu-id="fa07e-162">**SdbGetMatchingExe**</span></span>](sdbgetmatchingexe.md)
</dt> </dl>

 

 




