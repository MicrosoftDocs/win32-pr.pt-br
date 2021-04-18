---
description: Contém informações de dados AppHelp.
ms.assetid: 31b305e9-1f38-4952-b4fd-963df79b1346
title: Estrutura de APPHELP_DATA
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- APPHELP_DATA
api_type:
- NA
api_location: ''
ms.openlocfilehash: 20c66779dcb3d89746de5f90b2817ddcdb37b59f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105747630"
---
# <a name="apphelp_data-structure"></a><span data-ttu-id="cbab6-103">\_Estrutura de dados APPHELP</span><span class="sxs-lookup"><span data-stu-id="cbab6-103">APPHELP\_DATA structure</span></span>

<span data-ttu-id="cbab6-104">Contém informações de dados AppHelp.</span><span class="sxs-lookup"><span data-stu-id="cbab6-104">Contains Apphelp data information.</span></span>

## <a name="syntax"></a><span data-ttu-id="cbab6-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="cbab6-105">Syntax</span></span>


```C++
typedef struct tagAPPHELP_DATA {
  DWORD  dwFlags;
  DWORD  dwSeverity;
  DWORD  dwHTMLHelpID;
  LPTSTR szAppName;
  TAGREF trExe;
  LPTSTR szURL;
  LPTSTR szLink;
  LPTSTR szAppTitle;
  LPTSTR szContact;
  LPTSTR szDetails;
  DWORD  dwData;
  BOOL   bSPEntry;
} APPHELP_DATA, *PAPPHELP_DATA;
```



## <a name="members"></a><span data-ttu-id="cbab6-106">Membros</span><span class="sxs-lookup"><span data-stu-id="cbab6-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="cbab6-107">**dwFlags**</span><span class="sxs-lookup"><span data-stu-id="cbab6-107">**dwFlags**</span></span>
</dt> <dd>

<span data-ttu-id="cbab6-108">Esse parâmetro pode ser um ou mais dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="cbab6-108">This parameter can be one of more of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="cbab6-109"><span id="SHIMREG_DISABLE_SHIM"></span><span id="shimreg_disable_shim"></span>**SHIMREG \_ DESABILITAR \_ Shim** (0x00000001)</span><span class="sxs-lookup"><span data-stu-id="cbab6-109"><span id="SHIMREG_DISABLE_SHIM"></span><span id="shimreg_disable_shim"></span>**SHIMREG\_DISABLE\_SHIM** (0x00000001)</span></span>
</dt> <dt>

<span data-ttu-id="cbab6-110"><span id="SHIMREG_DISABLE_APPHELP"></span><span id="shimreg_disable_apphelp"></span>**SHIMREG \_ DESABILITAR \_ APPHELP** (0x00000002)</span><span class="sxs-lookup"><span data-stu-id="cbab6-110"><span id="SHIMREG_DISABLE_APPHELP"></span><span id="shimreg_disable_apphelp"></span>**SHIMREG\_DISABLE\_APPHELP** (0x00000002)</span></span>
</dt> <dt>

<span data-ttu-id="cbab6-111"><span id="SHIMREG_APPHELP_NOUI"></span><span id="shimreg_apphelp_noui"></span>**SHIMREG \_ \_NOUI APPHELP** (0x00000004)</span><span class="sxs-lookup"><span data-stu-id="cbab6-111"><span id="SHIMREG_APPHELP_NOUI"></span><span id="shimreg_apphelp_noui"></span>**SHIMREG\_APPHELP\_NOUI** (0x00000004)</span></span>
</dt> <dt>

<span data-ttu-id="cbab6-112"><span id="SHIMREG_APPHELP_CANCEL"></span><span id="shimreg_apphelp_cancel"></span>**SHIMREG \_ \_Cancelamento de APPHELP** (0x10000000)</span><span class="sxs-lookup"><span data-stu-id="cbab6-112"><span id="SHIMREG_APPHELP_CANCEL"></span><span id="shimreg_apphelp_cancel"></span>**SHIMREG\_APPHELP\_CANCEL** (0x10000000)</span></span>
</dt> <dt>

<span data-ttu-id="cbab6-113"><span id="SHIMREG_DISABLE_SXS"></span><span id="shimreg_disable_sxs"></span>**SHIMREG \_ DESABILITAR \_ SxS** (0x00000010)</span><span class="sxs-lookup"><span data-stu-id="cbab6-113"><span id="SHIMREG_DISABLE_SXS"></span><span id="shimreg_disable_sxs"></span>**SHIMREG\_DISABLE\_SXS** (0x00000010)</span></span>
</dt> <dt>

<span data-ttu-id="cbab6-114"><span id="SHIMREG_DISABLE_LAYER"></span><span id="shimreg_disable_layer"></span>**SHIMREG \_ DESABILITAR \_ camada** (0x00000020)</span><span class="sxs-lookup"><span data-stu-id="cbab6-114"><span id="SHIMREG_DISABLE_LAYER"></span><span id="shimreg_disable_layer"></span>**SHIMREG\_DISABLE\_LAYER** (0x00000020)</span></span>
</dt> <dt>

<span data-ttu-id="cbab6-115"><span id="SHIMREG_DISABLE_DRIVER"></span><span id="shimreg_disable_driver"></span>**SHIMREG \_ DESABILITAR \_ Driver** (0x00000040)</span><span class="sxs-lookup"><span data-stu-id="cbab6-115"><span id="SHIMREG_DISABLE_DRIVER"></span><span id="shimreg_disable_driver"></span>**SHIMREG\_DISABLE\_DRIVER** (0x00000040)</span></span>
</dt> </dl> </dd> <dt>

<span data-ttu-id="cbab6-116">**dwSeverity**</span><span class="sxs-lookup"><span data-stu-id="cbab6-116">**dwSeverity**</span></span>
</dt> <dd>

<span data-ttu-id="cbab6-117">Esse parâmetro pode ser APPTYPE \_ nenhum (0).</span><span class="sxs-lookup"><span data-stu-id="cbab6-117">This parameter can be APPTYPE\_NONE (0).</span></span>

</dd> <dt>

<span data-ttu-id="cbab6-118">**dwHTMLHelpID**</span><span class="sxs-lookup"><span data-stu-id="cbab6-118">**dwHTMLHelpID**</span></span>
</dt> <dd>

<span data-ttu-id="cbab6-119">O identificador da ajuda HTML.</span><span class="sxs-lookup"><span data-stu-id="cbab6-119">The HTML Help identifier.</span></span>

</dd> <dt>

<span data-ttu-id="cbab6-120">**szAppName**</span><span class="sxs-lookup"><span data-stu-id="cbab6-120">**szAppName**</span></span>
</dt> <dd>

<span data-ttu-id="cbab6-121">O nome do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="cbab6-121">The application name.</span></span>

</dd> <dt>

<span data-ttu-id="cbab6-122">**trExe**</span><span class="sxs-lookup"><span data-stu-id="cbab6-122">**trExe**</span></span>
</dt> <dd>

<span data-ttu-id="cbab6-123">O [**TAGREF**](tagref.md) do arquivo executável correspondente.</span><span class="sxs-lookup"><span data-stu-id="cbab6-123">The [**TAGREF**](tagref.md) of the corresponding executable file.</span></span>

</dd> <dt>

<span data-ttu-id="cbab6-124">**szURL**</span><span class="sxs-lookup"><span data-stu-id="cbab6-124">**szURL**</span></span>
</dt> <dd>

<span data-ttu-id="cbab6-125">A URL para o link online AppHelp.</span><span class="sxs-lookup"><span data-stu-id="cbab6-125">The URL for Apphelp online link.</span></span>

</dd> <dt>

<span data-ttu-id="cbab6-126">**szLink**</span><span class="sxs-lookup"><span data-stu-id="cbab6-126">**szLink**</span></span>
</dt> <dd>

<span data-ttu-id="cbab6-127">O texto do link para **szURL**.</span><span class="sxs-lookup"><span data-stu-id="cbab6-127">The link text for **szURL**.</span></span>

</dd> <dt>

<span data-ttu-id="cbab6-128">**szAppTitle**</span><span class="sxs-lookup"><span data-stu-id="cbab6-128">**szAppTitle**</span></span>
</dt> <dd>

<span data-ttu-id="cbab6-129">O título da mensagem AppHelp.</span><span class="sxs-lookup"><span data-stu-id="cbab6-129">The title for the Apphelp message.</span></span>

</dd> <dt>

<span data-ttu-id="cbab6-130">**szContact**</span><span class="sxs-lookup"><span data-stu-id="cbab6-130">**szContact**</span></span>
</dt> <dd>

<span data-ttu-id="cbab6-131">As informações de contato do fornecedor.</span><span class="sxs-lookup"><span data-stu-id="cbab6-131">The vendor contact information.</span></span>

</dd> <dt>

<span data-ttu-id="cbab6-132">**szDetails**</span><span class="sxs-lookup"><span data-stu-id="cbab6-132">**szDetails**</span></span>
</dt> <dd>

<span data-ttu-id="cbab6-133">A mensagem AppHelp detalhada.</span><span class="sxs-lookup"><span data-stu-id="cbab6-133">The detailed Apphelp message.</span></span>

</dd> <dt>

<span data-ttu-id="cbab6-134">**dwData**</span><span class="sxs-lookup"><span data-stu-id="cbab6-134">**dwData**</span></span>
</dt> <dd>

<span data-ttu-id="cbab6-135">Dados definidos pelo usuário gerenciados pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="cbab6-135">User-defined data managed by the application.</span></span>

</dd> <dt>

<span data-ttu-id="cbab6-136">**bSPEntry**</span><span class="sxs-lookup"><span data-stu-id="cbab6-136">**bSPEntry**</span></span>
</dt> <dd>

<span data-ttu-id="cbab6-137">Esse membro será **verdadeiro** se essa entrada estiver no banco de dados Service Pack e **false** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="cbab6-137">This member is **TRUE** if this entry is in the service pack database and **FALSE** otherwise.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="cbab6-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cbab6-138">Requirements</span></span>



| <span data-ttu-id="cbab6-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="cbab6-139">Requirement</span></span> | <span data-ttu-id="cbab6-140">Valor</span><span class="sxs-lookup"><span data-stu-id="cbab6-140">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="cbab6-141">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cbab6-141">Minimum supported client</span></span><br/> | <span data-ttu-id="cbab6-142">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="cbab6-142">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="cbab6-143">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cbab6-143">Minimum supported server</span></span><br/> | <span data-ttu-id="cbab6-144">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="cbab6-144">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="cbab6-145">Confira também</span><span class="sxs-lookup"><span data-stu-id="cbab6-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cbab6-146">**SdbReadApphelpDetailsData**</span><span class="sxs-lookup"><span data-stu-id="cbab6-146">**SdbReadApphelpDetailsData**</span></span>](sdbreadapphelpdetailsdata.md)
</dt> </dl>

 

 




