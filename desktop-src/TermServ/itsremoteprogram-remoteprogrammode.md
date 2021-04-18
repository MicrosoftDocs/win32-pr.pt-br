---
title: Propriedade ITSRemoteProgram RemoteProgramMode
description: O modo RemoteApp do Windows Server 2008 R2.
ms.assetid: 9ebdf966-db9c-4a14-8469-f8b153c6ea78
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade RemoteProgramMode
- Propriedade RemoteProgramMode Serviços de Área de Trabalho Remota, interface ITSRemoteProgram
- Serviços de Área de Trabalho Remota de interface ITSRemoteProgram, Propriedade RemoteProgramMode
- Propriedade RemoteProgramMode Serviços de Área de Trabalho Remota, interface ITSRemoteProgram2
- Serviços de Área de Trabalho Remota de interface ITSRemoteProgram2, Propriedade RemoteProgramMode
- Propriedade RemoteProgramMode Serviços de Área de Trabalho Remota, interface ITSRemoteProgram3
- Serviços de Área de Trabalho Remota de interface ITSRemoteProgram3, Propriedade RemoteProgramMode
topic_type:
- apiref
api_name:
- ITSRemoteProgram.RemoteProgramMode
- ITSRemoteProgram.get_RemoteProgramMode
- ITSRemoteProgram.put_RemoteProgramMode
- ITSRemoteProgram2.RemoteProgramMode
- ITSRemoteProgram2.get_RemoteProgramMode
- ITSRemoteProgram2.put_RemoteProgramMode
- ITSRemoteProgram3.RemoteProgramMode
- ITSRemoteProgram3.get_RemoteProgramMode
- ITSRemoteProgram3.put_RemoteProgramMode
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e8582824e2f6349e37b125ffd974847b602ad6fa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105810979"
---
# <a name="itsremoteprogramremoteprogrammode-property"></a><span data-ttu-id="fb12c-110">Propriedade ITSRemoteProgram:: RemoteProgramMode</span><span class="sxs-lookup"><span data-stu-id="fb12c-110">ITSRemoteProgram::RemoteProgramMode property</span></span>

<span data-ttu-id="fb12c-111">O modo RemoteApp do Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="fb12c-111">The Windows Server 2008 R2 RemoteApp mode.</span></span>

<span data-ttu-id="fb12c-112">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="fb12c-112">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="fb12c-113">Syntax</span><span class="sxs-lookup"><span data-stu-id="fb12c-113">Syntax</span></span>


```C++
HRESULT put_RemoteProgramMode(
  [in]  VARIANT_BOOL vboolRemoteProgramMode
);

HRESULT get_RemoteProgramMode(
  [out] VARIANT_BOOL *pvboolRemoteProgramMode
);
```



## <a name="property-value"></a><span data-ttu-id="fb12c-114">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="fb12c-114">Property value</span></span>

<span data-ttu-id="fb12c-115">O modo do RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="fb12c-115">The RemoteApp mode.</span></span> <span data-ttu-id="fb12c-116">Se definido como **Variant \_ true**, o modo RemoteApp será habilitado e a sessão remota hospedará os programas do RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="fb12c-116">If set to **VARIANT\_TRUE**, RemoteApp mode is enabled, and the remote session will host RemoteApp programs.</span></span> <span data-ttu-id="fb12c-117">Se definido como **Variant \_ false** (o padrão), o modo RemoteApp não está habilitado.</span><span class="sxs-lookup"><span data-stu-id="fb12c-117">If set to **VARIANT\_FALSE** (the default), RemoteApp mode is not enabled.</span></span> <span data-ttu-id="fb12c-118">A sessão remota irá hospedar uma área de trabalho remota.</span><span class="sxs-lookup"><span data-stu-id="fb12c-118">The remote session will host a remote desktop.</span></span>

## <a name="error-codes"></a><span data-ttu-id="fb12c-119">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="fb12c-119">Error codes</span></span>

<span data-ttu-id="fb12c-120">Retornará **S \_ OK** se for bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="fb12c-120">Returns **S\_OK** if successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="fb12c-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fb12c-121">Requirements</span></span>



| <span data-ttu-id="fb12c-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="fb12c-122">Requirement</span></span> | <span data-ttu-id="fb12c-123">Valor</span><span class="sxs-lookup"><span data-stu-id="fb12c-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="fb12c-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fb12c-124">Minimum supported client</span></span><br/> | <span data-ttu-id="fb12c-125">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="fb12c-125">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="fb12c-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fb12c-126">Minimum supported server</span></span><br/> | <span data-ttu-id="fb12c-127">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fb12c-127">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="fb12c-128">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="fb12c-128">Type library</span></span><br/>             | <dl> <span data-ttu-id="fb12c-129"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fb12c-129"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="fb12c-130">DLL</span><span class="sxs-lookup"><span data-stu-id="fb12c-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fb12c-131"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fb12c-131"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="fb12c-132">IID</span><span class="sxs-lookup"><span data-stu-id="fb12c-132">IID</span></span><br/>                      | <span data-ttu-id="fb12c-133">IID \_ ITSRemoteProgram é definido como FDD029F9-467A-4c49-8529-64B521DBD1B4</span><span class="sxs-lookup"><span data-stu-id="fb12c-133">IID\_ITSRemoteProgram is defined as FDD029F9-467A-4c49-8529-64B521DBD1B4</span></span><br/>    |



## <a name="see-also"></a><span data-ttu-id="fb12c-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="fb12c-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fb12c-135">**ITSRemoteProgram2**</span><span class="sxs-lookup"><span data-stu-id="fb12c-135">**ITSRemoteProgram2**</span></span>](itsremoteprogram2.md)
</dt> <dt>

[<span data-ttu-id="fb12c-136">**ITSRemoteProgram3**</span><span class="sxs-lookup"><span data-stu-id="fb12c-136">**ITSRemoteProgram3**</span></span>](itsremoteprogram3.md)
</dt> <dt>

[<span data-ttu-id="fb12c-137">**ITSRemoteProgram**</span><span class="sxs-lookup"><span data-stu-id="fb12c-137">**ITSRemoteProgram**</span></span>](itsremoteprogram.md)
</dt> </dl>

 

 





