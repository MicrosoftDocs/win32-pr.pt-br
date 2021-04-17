---
description: Contém o cabeçalho do GRL (lista de revogação global).
ms.assetid: 806ae550-5106-47ec-8466-f967598d3e61
title: Estrutura de GRL_HEADER
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GRL_HEADER
api_type:
- NA
api_location: ''
ms.openlocfilehash: c20c9323ac627f9f1d6c63ae893d1633fb3cd96f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105753842"
---
# <a name="grl_header-structure"></a><span data-ttu-id="0325f-103">\_Estrutura do cabeçalho grl</span><span class="sxs-lookup"><span data-stu-id="0325f-103">GRL\_HEADER structure</span></span>

<span data-ttu-id="0325f-104">Contém o cabeçalho do GRL (lista de revogação global).</span><span class="sxs-lookup"><span data-stu-id="0325f-104">Contains the global revocation list (GRL) header.</span></span>

## <a name="syntax"></a><span data-ttu-id="0325f-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0325f-105">Syntax</span></span>


```C++
typedef struct _GRL_HEADER {
  WCHAR    wszIdentifier[6];
  WORD     wFormatMajor;
  WORD     wFormatMinor;
  FILETIME CreationTime;
  DWORD    dwSequenceNumber;
  DWORD    dwForceRebootVersion;
  DWORD    dwForceProcessRestartVersion;
  DWORD    cbRevocationSectionOffset;
  DWORD    cRevokedKernelBinaries;
  DWORD    cRevokedUserBinaries;
  DWORD    cRevokedCertificates;
  DWORD    cTrustedRoots;
  DWORD    cbExtensibleSectionOffset;
  DWORD    cExtensibleEntries;
  DWORD    cbRenewalSectionOffset;
  DWORD    cRevokedKernelBinaryRenewals;
  DWORD    cRevokedUserBinaryRenewals;
  DWORD    cRevokedCertificateRenewals;
  DWORD    cbSignatureCoreOffset;
  DWORD    cbSignatureExtOffset;
} GRL_HEADER;
```



## <a name="members"></a><span data-ttu-id="0325f-106">Membros</span><span class="sxs-lookup"><span data-stu-id="0325f-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="0325f-107">**wszIdentifier**</span><span class="sxs-lookup"><span data-stu-id="0325f-107">**wszIdentifier**</span></span>
</dt> <dd>

<span data-ttu-id="0325f-108">O identificador GRL.</span><span class="sxs-lookup"><span data-stu-id="0325f-108">The GRL identifier.</span></span> <span data-ttu-id="0325f-109">O valor é sempre L "MSGRL".</span><span class="sxs-lookup"><span data-stu-id="0325f-109">The value is always L"MSGRL".</span></span>

</dd> <dt>

<span data-ttu-id="0325f-110">**wFormatMajor**</span><span class="sxs-lookup"><span data-stu-id="0325f-110">**wFormatMajor**</span></span>
</dt> <dd>

<span data-ttu-id="0325f-111">O número da versão principal.</span><span class="sxs-lookup"><span data-stu-id="0325f-111">The major version number.</span></span> <span data-ttu-id="0325f-112">No momento, o valor deve ser 1.</span><span class="sxs-lookup"><span data-stu-id="0325f-112">Currently the value must be 1.</span></span>

</dd> <dt>

<span data-ttu-id="0325f-113">**wFormatMinor**</span><span class="sxs-lookup"><span data-stu-id="0325f-113">**wFormatMinor**</span></span>
</dt> <dd>

<span data-ttu-id="0325f-114">O número da versão secundária.</span><span class="sxs-lookup"><span data-stu-id="0325f-114">The minor version number.</span></span> <span data-ttu-id="0325f-115">No momento, o valor deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="0325f-115">Currently the value must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="0325f-116">**CreationTime**</span><span class="sxs-lookup"><span data-stu-id="0325f-116">**CreationTime**</span></span>
</dt> <dd>

<span data-ttu-id="0325f-117">Um valor **FILETIME** que especifica quando o arquivo foi criado.</span><span class="sxs-lookup"><span data-stu-id="0325f-117">A **FILETIME** value that specifies when the file was created.</span></span>

</dd> <dt>

<span data-ttu-id="0325f-118">**dwSequenceNumber**</span><span class="sxs-lookup"><span data-stu-id="0325f-118">**dwSequenceNumber**</span></span>
</dt> <dd>

<span data-ttu-id="0325f-119">O número de versão do GRL.</span><span class="sxs-lookup"><span data-stu-id="0325f-119">The GRL version number.</span></span> <span data-ttu-id="0325f-120">No momento, o valor deve ser pelo menos 3</span><span class="sxs-lookup"><span data-stu-id="0325f-120">Currently the value must be at least 3</span></span>

</dd> <dt>

<span data-ttu-id="0325f-121">**dwForceRebootVersion**</span><span class="sxs-lookup"><span data-stu-id="0325f-121">**dwForceRebootVersion**</span></span>
</dt> <dd>

<span data-ttu-id="0325f-122">Reservado.</span><span class="sxs-lookup"><span data-stu-id="0325f-122">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="0325f-123">**dwForceProcessRestartVersion**</span><span class="sxs-lookup"><span data-stu-id="0325f-123">**dwForceProcessRestartVersion**</span></span>
</dt> <dd>

<span data-ttu-id="0325f-124">Reservado.</span><span class="sxs-lookup"><span data-stu-id="0325f-124">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="0325f-125">**cbRevocationSectionOffset**</span><span class="sxs-lookup"><span data-stu-id="0325f-125">**cbRevocationSectionOffset**</span></span>
</dt> <dd>

<span data-ttu-id="0325f-126">O deslocamento, em bytes, do início do GRL para a seção principal.</span><span class="sxs-lookup"><span data-stu-id="0325f-126">The offset, in bytes, from the start of the GRL to the Core section.</span></span>

</dd> <dt>

<span data-ttu-id="0325f-127">**cRevokedKernelBinaries**</span><span class="sxs-lookup"><span data-stu-id="0325f-127">**cRevokedKernelBinaries**</span></span>
</dt> <dd>

<span data-ttu-id="0325f-128">O número de binários de kernel revogados listados no GRL.</span><span class="sxs-lookup"><span data-stu-id="0325f-128">The number of revoked kernel binaries listed in the GRL.</span></span>

</dd> <dt>

<span data-ttu-id="0325f-129">**cRevokedUserBinaries**</span><span class="sxs-lookup"><span data-stu-id="0325f-129">**cRevokedUserBinaries**</span></span>
</dt> <dd>

<span data-ttu-id="0325f-130">O número de binários de modo de usuário revogados listados no GRL.</span><span class="sxs-lookup"><span data-stu-id="0325f-130">The number of revoked user-mode binaries listed in the GRL.</span></span>

</dd> <dt>

<span data-ttu-id="0325f-131">**cRevokedCertificates**</span><span class="sxs-lookup"><span data-stu-id="0325f-131">**cRevokedCertificates**</span></span>
</dt> <dd>

<span data-ttu-id="0325f-132">O número de certificados revogados listados no GRL.</span><span class="sxs-lookup"><span data-stu-id="0325f-132">The number of revoked certificates listed in the GRL.</span></span>

</dd> <dt>

<span data-ttu-id="0325f-133">**cTrustedRoots**</span><span class="sxs-lookup"><span data-stu-id="0325f-133">**cTrustedRoots**</span></span>
</dt> <dd>

<span data-ttu-id="0325f-134">O número de raízes confiáveis listadas no GRL.</span><span class="sxs-lookup"><span data-stu-id="0325f-134">The number of trusted roots listed in the GRL.</span></span>

</dd> <dt>

<span data-ttu-id="0325f-135">**cbExtensibleSectionOffset**</span><span class="sxs-lookup"><span data-stu-id="0325f-135">**cbExtensibleSectionOffset**</span></span>
</dt> <dd>

<span data-ttu-id="0325f-136">O deslocamento, em bytes, do início do GRL para a seção extensível.</span><span class="sxs-lookup"><span data-stu-id="0325f-136">The offset, in bytes, from the start of the GRL to the Extensible section.</span></span>

</dd> <dt>

<span data-ttu-id="0325f-137">**cExtensibleEntries**</span><span class="sxs-lookup"><span data-stu-id="0325f-137">**cExtensibleEntries**</span></span>
</dt> <dd>

<span data-ttu-id="0325f-138">O número de entradas na seção extensível.</span><span class="sxs-lookup"><span data-stu-id="0325f-138">The number of entries in the Extensible section.</span></span>

</dd> <dt>

<span data-ttu-id="0325f-139">**cbRenewalSectionOffset**</span><span class="sxs-lookup"><span data-stu-id="0325f-139">**cbRenewalSectionOffset**</span></span>
</dt> <dd>

<span data-ttu-id="0325f-140">O deslocamento, em bytes, do início do GRL para a seção renovações.</span><span class="sxs-lookup"><span data-stu-id="0325f-140">The offset, in bytes, from the start of the GRL to the Renewals section.</span></span>

</dd> <dt>

<span data-ttu-id="0325f-141">**cRevokedKernelBinaryRenewals**</span><span class="sxs-lookup"><span data-stu-id="0325f-141">**cRevokedKernelBinaryRenewals**</span></span>
</dt> <dd>

<span data-ttu-id="0325f-142">O número de renovações binárias de kernel listadas no GRL.</span><span class="sxs-lookup"><span data-stu-id="0325f-142">The number of kernel binary renewals listed in the GRL.</span></span>

</dd> <dt>

<span data-ttu-id="0325f-143">**cRevokedUserBinaryRenewals**</span><span class="sxs-lookup"><span data-stu-id="0325f-143">**cRevokedUserBinaryRenewals**</span></span>
</dt> <dd>

<span data-ttu-id="0325f-144">O número de renovações binárias de modo de usuário listadas no GRL.</span><span class="sxs-lookup"><span data-stu-id="0325f-144">The number of user-mode binary renewals listed in the GRL.</span></span>

</dd> <dt>

<span data-ttu-id="0325f-145">**cRevokedCertificateRenewals**</span><span class="sxs-lookup"><span data-stu-id="0325f-145">**cRevokedCertificateRenewals**</span></span>
</dt> <dd>

<span data-ttu-id="0325f-146">O número de renovações de certificado listadas no GRL.</span><span class="sxs-lookup"><span data-stu-id="0325f-146">The number of certificate renewals listed in the GRL.</span></span>

</dd> <dt>

<span data-ttu-id="0325f-147">**cbSignatureCoreOffset**</span><span class="sxs-lookup"><span data-stu-id="0325f-147">**cbSignatureCoreOffset**</span></span>
</dt> <dd>

<span data-ttu-id="0325f-148">O deslocamento, em bytes, do início do GRL para a assinatura da seção principal.</span><span class="sxs-lookup"><span data-stu-id="0325f-148">The offset, in bytes, from the start of the GRL to the Core section signature.</span></span>

</dd> <dt>

<span data-ttu-id="0325f-149">**cbSignatureExtOffset**</span><span class="sxs-lookup"><span data-stu-id="0325f-149">**cbSignatureExtOffset**</span></span>
</dt> <dd>

<span data-ttu-id="0325f-150">O deslocamento, em bytes, do início do GRL para a assinatura da seção extensível.</span><span class="sxs-lookup"><span data-stu-id="0325f-150">The offset, in bytes, from the start of the GRL to the Extensible section signature.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0325f-151">Comentários</span><span class="sxs-lookup"><span data-stu-id="0325f-151">Remarks</span></span>

<span data-ttu-id="0325f-152">Todos os inteiros no GRL têm ordenação de byte little-endian.</span><span class="sxs-lookup"><span data-stu-id="0325f-152">All integers in the GRL have little-endian byte ordering.</span></span> <span data-ttu-id="0325f-153">Todas as estruturas são alinhadas a limites de 1 byte.</span><span class="sxs-lookup"><span data-stu-id="0325f-153">All structures are aligned to 1-byte boundaries.</span></span>

<span data-ttu-id="0325f-154">Essa estrutura não é declarada em um cabeçalho do SDK.</span><span class="sxs-lookup"><span data-stu-id="0325f-154">This structure is not declared in an SDK header.</span></span> <span data-ttu-id="0325f-155">Para usar essa estrutura, adicione a declaração mostrada aqui ao seu código-fonte.</span><span class="sxs-lookup"><span data-stu-id="0325f-155">To use this structure, add the declaration shown here to your source code.</span></span>

## <a name="requirements"></a><span data-ttu-id="0325f-156">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0325f-156">Requirements</span></span>



| <span data-ttu-id="0325f-157">Requisito</span><span class="sxs-lookup"><span data-stu-id="0325f-157">Requirement</span></span> | <span data-ttu-id="0325f-158">Valor</span><span class="sxs-lookup"><span data-stu-id="0325f-158">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="0325f-159">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0325f-159">Minimum supported client</span></span><br/> | <span data-ttu-id="0325f-160">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="0325f-160">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="0325f-161">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0325f-161">Minimum supported server</span></span><br/> | <span data-ttu-id="0325f-162">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="0325f-162">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="0325f-163">Confira também</span><span class="sxs-lookup"><span data-stu-id="0325f-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0325f-164">Revogação de certificado OPM</span><span class="sxs-lookup"><span data-stu-id="0325f-164">OPM Certificate Revocation</span></span>](opm-certificate-revocation.md)
</dt> <dt>

[<span data-ttu-id="0325f-165">Estruturas OPM</span><span class="sxs-lookup"><span data-stu-id="0325f-165">OPM Structures</span></span>](opm-structures.md)
</dt> </dl>

 

 




