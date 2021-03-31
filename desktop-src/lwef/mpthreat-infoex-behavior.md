---
title: Estrutura de MPTHREAT_INFOEX_BEHAVIOR (MpClient. h)
description: Contém informações específicas de modificação de comportamento.
ms.assetid: 762E755F-5BA1-476D-B395-6617093309C5
keywords:
- Recursos do ambiente Windows herdado da estrutura de MPTHREAT_INFOEX_BEHAVIOR
- Ponteiro de estrutura de PMPTHREAT_INFOEX_BEHAVIOR recursos de ambiente herdados do Windows
topic_type:
- apiref
api_name:
- MPTHREAT_INFOEX_BEHAVIOR
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4cb0bc00aeb56aec38b88f2590211c705079834f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103645068"
---
# <a name="mpthreat_infoex_behavior-structure"></a><span data-ttu-id="f9837-105">Estrutura de comportamento do MPTHREAT \_ INFOEX \_</span><span class="sxs-lookup"><span data-stu-id="f9837-105">MPTHREAT\_INFOEX\_BEHAVIOR structure</span></span>

<span data-ttu-id="f9837-106">Contém informações específicas de modificação de comportamento.</span><span class="sxs-lookup"><span data-stu-id="f9837-106">Contains behavior modification-specific information.</span></span>

## <a name="syntax"></a><span data-ttu-id="f9837-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f9837-107">Syntax</span></span>


```C++
typedef struct tagMPTHREAT_INFOEX_BEHAVIOR {
  ULARGE_INTEGER         SignatureID;
  ULONGLONG              EngineVersion;
  ULONGLONG              ASDeltaSignatureVersion;
  ULONGLONG              AVDeltaSignatureVersion;
  MP_HASH_TYPE           HashType;
  DWORD                  FidelityValue;
  MP_MIDL_STRING  LPWSTR HashValue;
  MP_MIDL_STRING  LPWSTR TargetFileName;
  MP_MIDL_STRING  LPWSTR TargetFileHash;
} MPTHREAT_INFOEX_BEHAVIOR, *PMPTHREAT_INFOEX_BEHAVIOR;
```



## <a name="members"></a><span data-ttu-id="f9837-108">Membros</span><span class="sxs-lookup"><span data-stu-id="f9837-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="f9837-109">**SignatureId**</span><span class="sxs-lookup"><span data-stu-id="f9837-109">**SignatureID**</span></span>
</dt> <dd>

<span data-ttu-id="f9837-110">Tipo: **ULARGE \_ inteiro**</span><span class="sxs-lookup"><span data-stu-id="f9837-110">Type: **ULARGE\_INTEGER**</span></span>

</dd> <dd>

<span data-ttu-id="f9837-111">ID de assinatura de modificação de comportamento fornecida pelo mecanismo no momento da detecção.</span><span class="sxs-lookup"><span data-stu-id="f9837-111">Behavior modification signature ID given by the engine at the time of detection.</span></span>

</dd> <dt>

<span data-ttu-id="f9837-112">**EngineVersion**</span><span class="sxs-lookup"><span data-stu-id="f9837-112">**EngineVersion**</span></span>
</dt> <dd>

<span data-ttu-id="f9837-113">Tipo: **ULONGLONG**</span><span class="sxs-lookup"><span data-stu-id="f9837-113">Type: **ULONGLONG**</span></span>

</dd> <dd>

<span data-ttu-id="f9837-114">Versão do módulo do mecanismo.</span><span class="sxs-lookup"><span data-stu-id="f9837-114">Engine module version.</span></span>

</dd> <dt>

<span data-ttu-id="f9837-115">**ASDeltaSignatureVersion**</span><span class="sxs-lookup"><span data-stu-id="f9837-115">**ASDeltaSignatureVersion**</span></span>
</dt> <dd>

<span data-ttu-id="f9837-116">Tipo: **ULONGLONG**</span><span class="sxs-lookup"><span data-stu-id="f9837-116">Type: **ULONGLONG**</span></span>

</dd> <dd>

<span data-ttu-id="f9837-117">Versão da assinatura de AntiSpyware.</span><span class="sxs-lookup"><span data-stu-id="f9837-117">Antispyware signature version.</span></span>

</dd> <dt>

<span data-ttu-id="f9837-118">**AVDeltaSignatureVersion**</span><span class="sxs-lookup"><span data-stu-id="f9837-118">**AVDeltaSignatureVersion**</span></span>
</dt> <dd>

<span data-ttu-id="f9837-119">Tipo: **ULONGLONG**</span><span class="sxs-lookup"><span data-stu-id="f9837-119">Type: **ULONGLONG**</span></span>

</dd> <dd>

<span data-ttu-id="f9837-120">Versão da assinatura antivírus</span><span class="sxs-lookup"><span data-stu-id="f9837-120">Antivirus signature version</span></span>

</dd> <dt>

<span data-ttu-id="f9837-121">**Hashtype**</span><span class="sxs-lookup"><span data-stu-id="f9837-121">**HashType**</span></span>
</dt> <dd>

<span data-ttu-id="f9837-122">Tipo: **[ **\_ \_ tipo de hash do MP**](mp-hash-type.md)**</span><span class="sxs-lookup"><span data-stu-id="f9837-122">Type: **[**MP\_HASH\_TYPE**](mp-hash-type.md)**</span></span>

</dd> <dd>

<span data-ttu-id="f9837-123">Tipo de hash usado.</span><span class="sxs-lookup"><span data-stu-id="f9837-123">Hash type used.</span></span> <span data-ttu-id="f9837-124">Consulte [**\_ \_ tipo de hash MP**](mp-hash-type.md).</span><span class="sxs-lookup"><span data-stu-id="f9837-124">See [**MP\_HASH\_TYPE**](mp-hash-type.md).</span></span>

</dd> <dt>

<span data-ttu-id="f9837-125">**Fidelidadevalue**</span><span class="sxs-lookup"><span data-stu-id="f9837-125">**FidelityValue**</span></span>
</dt> <dd>

<span data-ttu-id="f9837-126">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="f9837-126">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="f9837-127">Valor de fidelidade.</span><span class="sxs-lookup"><span data-stu-id="f9837-127">Fidelity value.</span></span>

</dd> <dt>

<span data-ttu-id="f9837-128">**HashValue**</span><span class="sxs-lookup"><span data-stu-id="f9837-128">**HashValue**</span></span>
</dt> <dd>

<span data-ttu-id="f9837-129">Tipo: **PG \_ MIDL \_ String LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="f9837-129">Type: **MP\_MIDL\_STRING LPWSTR**</span></span>

</dd> <dd>

<span data-ttu-id="f9837-130">O hash do arquivo.</span><span class="sxs-lookup"><span data-stu-id="f9837-130">The hash of the file.</span></span>

</dd> <dt>

<span data-ttu-id="f9837-131">**TargetFileName**</span><span class="sxs-lookup"><span data-stu-id="f9837-131">**TargetFileName**</span></span>
</dt> <dd>

<span data-ttu-id="f9837-132">Tipo: **PG \_ MIDL \_ String LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="f9837-132">Type: **MP\_MIDL\_STRING LPWSTR**</span></span>

</dd> <dd>

<span data-ttu-id="f9837-133">O caminho e o nome do arquivo de destino.</span><span class="sxs-lookup"><span data-stu-id="f9837-133">The path and name of the targeted file.</span></span>

</dd> <dt>

<span data-ttu-id="f9837-134">**TargetFileHash**</span><span class="sxs-lookup"><span data-stu-id="f9837-134">**TargetFileHash**</span></span>
</dt> <dd>

<span data-ttu-id="f9837-135">Tipo: **PG \_ MIDL \_ String LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="f9837-135">Type: **MP\_MIDL\_STRING LPWSTR**</span></span>

</dd> <dd>

<span data-ttu-id="f9837-136">O hash do arquivo de destino.</span><span class="sxs-lookup"><span data-stu-id="f9837-136">The hash of the targeted file.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f9837-137">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f9837-137">Requirements</span></span>



| <span data-ttu-id="f9837-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="f9837-138">Requirement</span></span> | <span data-ttu-id="f9837-139">Valor</span><span class="sxs-lookup"><span data-stu-id="f9837-139">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f9837-140">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f9837-140">Minimum supported client</span></span><br/> | <span data-ttu-id="f9837-141">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="f9837-141">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="f9837-142">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f9837-142">Minimum supported server</span></span><br/> | <span data-ttu-id="f9837-143">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="f9837-143">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f9837-144">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f9837-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="f9837-145"><dt>MpClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="f9837-145"><dt>MpClient.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f9837-146">Consulte também</span><span class="sxs-lookup"><span data-stu-id="f9837-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f9837-147">**\_tipo de hash MP \_**</span><span class="sxs-lookup"><span data-stu-id="f9837-147">**MP\_HASH\_TYPE**</span></span>](mp-hash-type.md)
</dt> </dl>

 

 





