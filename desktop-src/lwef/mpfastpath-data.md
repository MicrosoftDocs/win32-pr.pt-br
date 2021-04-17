---
title: Estrutura de MPFASTPATH_DATA (MpClient. h)
description: Notificação de atualização do FastPath.
ms.assetid: E19F153D-DD46-4E27-9A4B-33586794DAC2
keywords:
- Recursos do ambiente Windows herdado da estrutura de MPFASTPATH_DATA
- Ponteiro de estrutura de PMPFASTPATH_DATA recursos de ambiente herdados do Windows
topic_type:
- apiref
api_name:
- MPFASTPATH_DATA
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2850a48074fee6984564550683c7fe595d0779ff
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105791591"
---
# <a name="mpfastpath_data-structure"></a><span data-ttu-id="be321-105">\_Estrutura de dados MPFASTPATH</span><span class="sxs-lookup"><span data-stu-id="be321-105">MPFASTPATH\_DATA structure</span></span>

<span data-ttu-id="be321-106">Notificação de atualização do FastPath.</span><span class="sxs-lookup"><span data-stu-id="be321-106">FastPath update notification.</span></span>

## <a name="syntax"></a><span data-ttu-id="be321-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="be321-107">Syntax</span></span>


```C++
typedef struct tagMPFASTPATH_DATA {
  MP_SIGNATURE_TYPE         SignatureType;
  MP_FASTPATH_TYPE          FastPathSignatureType;
  MP_MIDL_STRING LPWSTR     FastPathSignatureVersion;
  ULARGE_INTEGER            CompilationTimestamp;
  MP_PERSISTENCE_LIMIT_TYPE PersistenceType;
  MP_MIDL_STRING LPWSTR     PersistenceValue;
  MP_MIDL_STRING LPWSTR     PersistencePath;
  MP_REMOVAL_REASON         Reason;
} MPFASTPATH_DATA, *PMPFASTPATH_DATA;
```



## <a name="members"></a><span data-ttu-id="be321-108">Membros</span><span class="sxs-lookup"><span data-stu-id="be321-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="be321-109">**SignatureType**</span><span class="sxs-lookup"><span data-stu-id="be321-109">**SignatureType**</span></span>
</dt> <dd>

<span data-ttu-id="be321-110">Tipo: **[ **\_ \_ tipo de assinatura MP**](mp-signature-type.md)**</span><span class="sxs-lookup"><span data-stu-id="be321-110">Type: **[**MP\_SIGNATURE\_TYPE**](mp-signature-type.md)**</span></span>

</dd> <dd>

<span data-ttu-id="be321-111">Tipo de assinatura.</span><span class="sxs-lookup"><span data-stu-id="be321-111">Signature type.</span></span>

</dd> <dt>

<span data-ttu-id="be321-112">**FastPathSignatureType**</span><span class="sxs-lookup"><span data-stu-id="be321-112">**FastPathSignatureType**</span></span>
</dt> <dd>

<span data-ttu-id="be321-113">Tipo: **[ **\_ \_ tipo de FASTPATH do MP**](mp-fastpath-type.md)**</span><span class="sxs-lookup"><span data-stu-id="be321-113">Type: **[**MP\_FASTPATH\_TYPE**](mp-fastpath-type.md)**</span></span>

</dd> <dd>

<span data-ttu-id="be321-114">Tipo de assinatura FastPath.</span><span class="sxs-lookup"><span data-stu-id="be321-114">FastPath signature type.</span></span>

</dd> <dt>

<span data-ttu-id="be321-115">**FastPathSignatureVersion**</span><span class="sxs-lookup"><span data-stu-id="be321-115">**FastPathSignatureVersion**</span></span>
</dt> <dd>

<span data-ttu-id="be321-116">Tipo: **PG \_ MIDL \_ String LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="be321-116">Type: **MP\_MIDL\_STRING LPWSTR**</span></span>

</dd> <dd>

<span data-ttu-id="be321-117">Versão da assinatura FastPath (opcional).</span><span class="sxs-lookup"><span data-stu-id="be321-117">FastPath signature version (optional).</span></span>

</dd> <dt>

<span data-ttu-id="be321-118">**CompilationTimestamp**</span><span class="sxs-lookup"><span data-stu-id="be321-118">**CompilationTimestamp**</span></span>
</dt> <dd>

<span data-ttu-id="be321-119">Tipo: **ULARGE \_ inteiro**</span><span class="sxs-lookup"><span data-stu-id="be321-119">Type: **ULARGE\_INTEGER**</span></span>

</dd> <dd>

<span data-ttu-id="be321-120">Carimbo de data/hora de compilação (UTC).</span><span class="sxs-lookup"><span data-stu-id="be321-120">Compilation timestamp (UTC).</span></span>

</dd> <dt>

<span data-ttu-id="be321-121">**PersistenceType**</span><span class="sxs-lookup"><span data-stu-id="be321-121">**PersistenceType**</span></span>
</dt> <dd>

<span data-ttu-id="be321-122">Tipo: **[ **\_ tipo de \_ limite \_ de persistência MP**](mp-persistence-limit-type.md)**</span><span class="sxs-lookup"><span data-stu-id="be321-122">Type: **[**MP\_PERSISTENCE\_LIMIT\_TYPE**](mp-persistence-limit-type.md)**</span></span>

</dd> <dd>

<span data-ttu-id="be321-123">Tipo de persistência (opcional).</span><span class="sxs-lookup"><span data-stu-id="be321-123">Persistence type (optional).</span></span>

</dd> <dt>

<span data-ttu-id="be321-124">**Persistencevalue**</span><span class="sxs-lookup"><span data-stu-id="be321-124">**PersistenceValue**</span></span>
</dt> <dd>

<span data-ttu-id="be321-125">Tipo: **PG \_ MIDL \_ String LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="be321-125">Type: **MP\_MIDL\_STRING LPWSTR**</span></span>

</dd> <dd>

<span data-ttu-id="be321-126">Valor de persistência (opcional).</span><span class="sxs-lookup"><span data-stu-id="be321-126">Persistence value (optional).</span></span>

</dd> <dt>

<span data-ttu-id="be321-127">**PersistencePath**</span><span class="sxs-lookup"><span data-stu-id="be321-127">**PersistencePath**</span></span>
</dt> <dd>

<span data-ttu-id="be321-128">Tipo: **PG \_ MIDL \_ String LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="be321-128">Type: **MP\_MIDL\_STRING LPWSTR**</span></span>

</dd> <dd>

<span data-ttu-id="be321-129">Caminho de persistência (opcional).</span><span class="sxs-lookup"><span data-stu-id="be321-129">Persistence path (optional).</span></span>

</dd> <dt>

<span data-ttu-id="be321-130">**Motivo**</span><span class="sxs-lookup"><span data-stu-id="be321-130">**Reason**</span></span>
</dt> <dd>

<span data-ttu-id="be321-131">Tipo: **[ **\_ \_ motivo da remoção de MP**](mp-removal-reason.md)**</span><span class="sxs-lookup"><span data-stu-id="be321-131">Type: **[**MP\_REMOVAL\_REASON**](mp-removal-reason.md)**</span></span>

</dd> <dd>

<span data-ttu-id="be321-132">Motivo para remoção de assinatura.</span><span class="sxs-lookup"><span data-stu-id="be321-132">Reason for signature removal.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="be321-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="be321-133">Requirements</span></span>



| <span data-ttu-id="be321-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="be321-134">Requirement</span></span> | <span data-ttu-id="be321-135">Valor</span><span class="sxs-lookup"><span data-stu-id="be321-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="be321-136">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="be321-136">Minimum supported client</span></span><br/> | <span data-ttu-id="be321-137">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="be321-137">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="be321-138">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="be321-138">Minimum supported server</span></span><br/> | <span data-ttu-id="be321-139">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="be321-139">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="be321-140">parâmetro</span><span class="sxs-lookup"><span data-stu-id="be321-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="be321-141"><dt>MpClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="be321-141"><dt>MpClient.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="be321-142">Confira também</span><span class="sxs-lookup"><span data-stu-id="be321-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="be321-143">**\_tipo de FASTPATH MP \_**</span><span class="sxs-lookup"><span data-stu-id="be321-143">**MP\_FASTPATH\_TYPE**</span></span>](mp-fastpath-type.md)
</dt> <dt>

[<span data-ttu-id="be321-144">**\_tipo de \_ limite de persistência MP \_**</span><span class="sxs-lookup"><span data-stu-id="be321-144">**MP\_PERSISTENCE\_LIMIT\_TYPE**</span></span>](mp-persistence-limit-type.md)
</dt> <dt>

[<span data-ttu-id="be321-145">**\_tipo de assinatura MP \_**</span><span class="sxs-lookup"><span data-stu-id="be321-145">**MP\_SIGNATURE\_TYPE**</span></span>](mp-signature-type.md)
</dt> </dl>

 

 





