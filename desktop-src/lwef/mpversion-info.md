---
title: Estrutura de MPVERSION_INFO (MpClient. h)
description: Informações de versão dos componentes do Malware Protection Manager.
ms.assetid: C18EE6FE-57E1-4814-85CA-19C3ACE275D2
keywords:
- Recursos do ambiente Windows herdado da estrutura de MPVERSION_INFO
- Ponteiro de estrutura de PMPVERSION_INFO recursos de ambiente herdados do Windows
topic_type:
- apiref
api_name:
- MPVERSION_INFO
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f30153c427b880600a3d8aeb3c411a8679cd64b1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104295857"
---
# <a name="mpversion_info-structure"></a><span data-ttu-id="3e59b-105">Estrutura de informações do MPVERSION \_</span><span class="sxs-lookup"><span data-stu-id="3e59b-105">MPVERSION\_INFO structure</span></span>

<span data-ttu-id="3e59b-106">Informações de versão dos componentes do Malware Protection Manager.</span><span class="sxs-lookup"><span data-stu-id="3e59b-106">Version information for the malware protection manager's components.</span></span>

## <a name="syntax"></a><span data-ttu-id="3e59b-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3e59b-107">Syntax</span></span>


```C++
typedef struct tagMPVERSION_INFO {
  MPCOMPONENT_VERSION Product;
  MPCOMPONENT_VERSION Service;
  MPCOMPONENT_VERSION FileSystemFilter;
  MPCOMPONENT_VERSION Engine;
  MPCOMPONENT_VERSION ASSignature;
  MPCOMPONENT_VERSION AVSignature;
  MPCOMPONENT_VERSION NISEngine;
  MPCOMPONENT_VERSION NISSignature;
  MPCOMPONENT_VERSION Reserved[4];
} MPVERSION_INFO, *PMPVERSION_INFO;
```



## <a name="members"></a><span data-ttu-id="3e59b-108">Membros</span><span class="sxs-lookup"><span data-stu-id="3e59b-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="3e59b-109">**Product**</span><span class="sxs-lookup"><span data-stu-id="3e59b-109">**Product**</span></span>
</dt> <dd>

<span data-ttu-id="3e59b-110">Tipo: **[ **\_ versão de MPCOMPONENT**](mpcomponent-version.md)**</span><span class="sxs-lookup"><span data-stu-id="3e59b-110">Type: **[**MPCOMPONENT\_VERSION**](mpcomponent-version.md)**</span></span>

</dd> <dd>

<span data-ttu-id="3e59b-111">Versão do produto.</span><span class="sxs-lookup"><span data-stu-id="3e59b-111">Product version.</span></span>

</dd> <dt>

<span data-ttu-id="3e59b-112">**Serviço**</span><span class="sxs-lookup"><span data-stu-id="3e59b-112">**Service**</span></span>
</dt> <dd>

<span data-ttu-id="3e59b-113">Tipo: **[ **\_ versão de MPCOMPONENT**](mpcomponent-version.md)**</span><span class="sxs-lookup"><span data-stu-id="3e59b-113">Type: **[**MPCOMPONENT\_VERSION**](mpcomponent-version.md)**</span></span>

</dd> <dd>

<span data-ttu-id="3e59b-114">Versão do componente de serviço.</span><span class="sxs-lookup"><span data-stu-id="3e59b-114">Service component version.</span></span>

</dd> <dt>

<span data-ttu-id="3e59b-115">**FileSystemFilter**</span><span class="sxs-lookup"><span data-stu-id="3e59b-115">**FileSystemFilter**</span></span>
</dt> <dd>

<span data-ttu-id="3e59b-116">Tipo: **[ **\_ versão de MPCOMPONENT**](mpcomponent-version.md)**</span><span class="sxs-lookup"><span data-stu-id="3e59b-116">Type: **[**MPCOMPONENT\_VERSION**](mpcomponent-version.md)**</span></span>

</dd> <dd>

<span data-ttu-id="3e59b-117">Versão do componente de filtro do sistema de arquivos.</span><span class="sxs-lookup"><span data-stu-id="3e59b-117">File system filter component version.</span></span>

</dd> <dt>

<span data-ttu-id="3e59b-118">**Mecanismo**</span><span class="sxs-lookup"><span data-stu-id="3e59b-118">**Engine**</span></span>
</dt> <dd>

<span data-ttu-id="3e59b-119">Tipo: **[ **\_ versão de MPCOMPONENT**](mpcomponent-version.md)**</span><span class="sxs-lookup"><span data-stu-id="3e59b-119">Type: **[**MPCOMPONENT\_VERSION**](mpcomponent-version.md)**</span></span>

</dd> <dd>

<span data-ttu-id="3e59b-120">Versão do componente do mecanismo.</span><span class="sxs-lookup"><span data-stu-id="3e59b-120">Engine component version.</span></span>

</dd> <dt>

<span data-ttu-id="3e59b-121">**Assignature**</span><span class="sxs-lookup"><span data-stu-id="3e59b-121">**ASSignature**</span></span>
</dt> <dd>

<span data-ttu-id="3e59b-122">Tipo: **[ **\_ versão de MPCOMPONENT**](mpcomponent-version.md)**</span><span class="sxs-lookup"><span data-stu-id="3e59b-122">Type: **[**MPCOMPONENT\_VERSION**](mpcomponent-version.md)**</span></span>

</dd> <dd>

<span data-ttu-id="3e59b-123">Versão do componente de assinatura de AntiSpyware.</span><span class="sxs-lookup"><span data-stu-id="3e59b-123">Antispyware signature component version.</span></span>

</dd> <dt>

<span data-ttu-id="3e59b-124">**AVSignature**</span><span class="sxs-lookup"><span data-stu-id="3e59b-124">**AVSignature**</span></span>
</dt> <dd>

<span data-ttu-id="3e59b-125">Tipo: **[ **\_ versão de MPCOMPONENT**](mpcomponent-version.md)**</span><span class="sxs-lookup"><span data-stu-id="3e59b-125">Type: **[**MPCOMPONENT\_VERSION**](mpcomponent-version.md)**</span></span>

</dd> <dd>

<span data-ttu-id="3e59b-126">Versão do componente de assinatura antivírus.</span><span class="sxs-lookup"><span data-stu-id="3e59b-126">Antivirus signature component version.</span></span>

</dd> <dt>

<span data-ttu-id="3e59b-127">**NISEngine**</span><span class="sxs-lookup"><span data-stu-id="3e59b-127">**NISEngine**</span></span>
</dt> <dd>

<span data-ttu-id="3e59b-128">Tipo: **[ **\_ versão de MPCOMPONENT**](mpcomponent-version.md)**</span><span class="sxs-lookup"><span data-stu-id="3e59b-128">Type: **[**MPCOMPONENT\_VERSION**](mpcomponent-version.md)**</span></span>

</dd> <dd>

<span data-ttu-id="3e59b-129">Versão do mecanismo NIS.</span><span class="sxs-lookup"><span data-stu-id="3e59b-129">NIS engine version.</span></span>

</dd> <dt>

<span data-ttu-id="3e59b-130">**NISSignature**</span><span class="sxs-lookup"><span data-stu-id="3e59b-130">**NISSignature**</span></span>
</dt> <dd>

<span data-ttu-id="3e59b-131">Tipo: **[ **\_ versão de MPCOMPONENT**](mpcomponent-version.md)**</span><span class="sxs-lookup"><span data-stu-id="3e59b-131">Type: **[**MPCOMPONENT\_VERSION**](mpcomponent-version.md)**</span></span>

</dd> <dd>

<span data-ttu-id="3e59b-132">Versão do componente de assinatura de assinatura NIS.</span><span class="sxs-lookup"><span data-stu-id="3e59b-132">NIS Signature signature component version.</span></span>

</dd> <dt>

<span data-ttu-id="3e59b-133">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="3e59b-133">**Reserved**</span></span>
</dt> <dd>

<span data-ttu-id="3e59b-134">Tipo: **[**MPCOMPONENT \_ versão**](mpcomponent-version.md) \[ 4\]**</span><span class="sxs-lookup"><span data-stu-id="3e59b-134">Type: **[**MPCOMPONENT\_VERSION**](mpcomponent-version.md)\[4\]**</span></span>

</dd> <dd>

<span data-ttu-id="3e59b-135">Campos reservados.</span><span class="sxs-lookup"><span data-stu-id="3e59b-135">Reserved fields.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3e59b-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3e59b-136">Requirements</span></span>



| <span data-ttu-id="3e59b-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="3e59b-137">Requirement</span></span> | <span data-ttu-id="3e59b-138">Valor</span><span class="sxs-lookup"><span data-stu-id="3e59b-138">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3e59b-139">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3e59b-139">Minimum supported client</span></span><br/> | <span data-ttu-id="3e59b-140">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="3e59b-140">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="3e59b-141">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3e59b-141">Minimum supported server</span></span><br/> | <span data-ttu-id="3e59b-142">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="3e59b-142">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="3e59b-143">parâmetro</span><span class="sxs-lookup"><span data-stu-id="3e59b-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="3e59b-144"><dt>MpClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="3e59b-144"><dt>MpClient.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3e59b-145">Confira também</span><span class="sxs-lookup"><span data-stu-id="3e59b-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3e59b-146">**versão do MPCOMPONENT \_**</span><span class="sxs-lookup"><span data-stu-id="3e59b-146">**MPCOMPONENT\_VERSION**</span></span>](mpcomponent-version.md)
</dt> </dl>

 

 





