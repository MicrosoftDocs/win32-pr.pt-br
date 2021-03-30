---
title: Estrutura LSLicense
description: Contém informações sobre uma licença de Serviços de Área de Trabalho Remota específica.
ms.assetid: 2c7f7b7a-e3b5-4f84-b49f-5f1d6960652d
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota estrutura LSLicense
- Serviços de Área de Trabalho Remota de ponteiro de estrutura de LPLSLicense
topic_type:
- apiref
api_name:
- LSLicense
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: dcb8551c1d1edfd9486d42df63de9a76fab38433
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455054"
---
# <a name="lslicense-structure"></a><span data-ttu-id="78b5b-105">Estrutura LSLicense</span><span class="sxs-lookup"><span data-stu-id="78b5b-105">LSLicense structure</span></span>

<span data-ttu-id="78b5b-106">Contém informações sobre uma licença de Serviços de Área de Trabalho Remota específica.</span><span class="sxs-lookup"><span data-stu-id="78b5b-106">Contains information about a specific Remote Desktop Services license.</span></span>

> [!Note]  
> <span data-ttu-id="78b5b-107">Essa estrutura não está definida em nenhum arquivo de cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="78b5b-107">This structure is not defined in any header file.</span></span> <span data-ttu-id="78b5b-108">Para usar essa estrutura, você deve defini-la por conta própria, conforme mostrado neste tópico.</span><span class="sxs-lookup"><span data-stu-id="78b5b-108">To use this structure, you must define it yourself as shown in this topic.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="78b5b-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="78b5b-109">Syntax</span></span>


```C++
typedef struct _LSLicense {
  DWORD dwVersion;
  DWORD dwLicenseId;
  DWORD dwKeyPackId;
  TCHAR szHWID[GUID_MAX_SIZE];
  TCHAR szMachineName[MAXCOMPUTERNAMELENGTH];
  TCHAR szUserName[MAXUSERNAMELENGTH];
  DWORD dwCertSerialLicense;
  DWORD dwLicenseSerialNumber;
  DWORD ftIssueDate;
  DWORD ftExpireDate;
  UCHAR ucLicenseStatus;
} LSLicense, *LPLSLicense;
```



## <a name="members"></a><span data-ttu-id="78b5b-110">Membros</span><span class="sxs-lookup"><span data-stu-id="78b5b-110">Members</span></span>

<dl> <dt>

<span data-ttu-id="78b5b-111">**DW**</span><span class="sxs-lookup"><span data-stu-id="78b5b-111">**dwVersion**</span></span>
</dt> <dd>

<span data-ttu-id="78b5b-112">Versão da licença.</span><span class="sxs-lookup"><span data-stu-id="78b5b-112">Version of the license.</span></span>

</dd> <dt>

<span data-ttu-id="78b5b-113">**dwLicenseId**</span><span class="sxs-lookup"><span data-stu-id="78b5b-113">**dwLicenseId**</span></span>
</dt> <dd>

<span data-ttu-id="78b5b-114">ID da licença.</span><span class="sxs-lookup"><span data-stu-id="78b5b-114">ID of the license.</span></span>

</dd> <dt>

<span data-ttu-id="78b5b-115">**dwKeyPackId**</span><span class="sxs-lookup"><span data-stu-id="78b5b-115">**dwKeyPackId**</span></span>
</dt> <dd>

<span data-ttu-id="78b5b-116">ID do [**LSKeyPack**](lskeypack.md) que contém a licença.</span><span class="sxs-lookup"><span data-stu-id="78b5b-116">ID of the [**LSKeyPack**](lskeypack.md) that contains the license.</span></span>

</dd> <dt>

<span data-ttu-id="78b5b-117">**szHWID**</span><span class="sxs-lookup"><span data-stu-id="78b5b-117">**szHWID**</span></span>
</dt> <dd>

<span data-ttu-id="78b5b-118">ID de hardware do cliente de Conexão de Área de Trabalho Remota (RDC) que emitiu a licença.</span><span class="sxs-lookup"><span data-stu-id="78b5b-118">Hardware ID of the Remote Desktop Connection (RDC) client that was issued the license.</span></span>

</dd> <dt>

<span data-ttu-id="78b5b-119">**szMachineName**</span><span class="sxs-lookup"><span data-stu-id="78b5b-119">**szMachineName**</span></span>
</dt> <dd>

<span data-ttu-id="78b5b-120">Nome do cliente de Conexão de Área de Trabalho Remota (RDC) que emitiu a licença.</span><span class="sxs-lookup"><span data-stu-id="78b5b-120">Name of the Remote Desktop Connection (RDC) client that was issued the license.</span></span>

</dd> <dt>

<span data-ttu-id="78b5b-121">**szUserName**</span><span class="sxs-lookup"><span data-stu-id="78b5b-121">**szUserName**</span></span>
</dt> <dd>

<span data-ttu-id="78b5b-122">Nome do usuário que emitiu a licença.</span><span class="sxs-lookup"><span data-stu-id="78b5b-122">Name of the user who was issued the license.</span></span>

</dd> <dt>

<span data-ttu-id="78b5b-123">**dwCertSerialLicense**</span><span class="sxs-lookup"><span data-stu-id="78b5b-123">**dwCertSerialLicense**</span></span>
</dt> <dd>

<span data-ttu-id="78b5b-124">Reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="78b5b-124">Reserved for future use.</span></span>

</dd> <dt>

<span data-ttu-id="78b5b-125">**dwLicenseSerialNumber**</span><span class="sxs-lookup"><span data-stu-id="78b5b-125">**dwLicenseSerialNumber**</span></span>
</dt> <dd>

<span data-ttu-id="78b5b-126">Número de série da licença.</span><span class="sxs-lookup"><span data-stu-id="78b5b-126">Serial number of the license.</span></span>

</dd> <dt>

<span data-ttu-id="78b5b-127">**ftIssueDate**</span><span class="sxs-lookup"><span data-stu-id="78b5b-127">**ftIssueDate**</span></span>
</dt> <dd>

<span data-ttu-id="78b5b-128">Data em que a licença foi emitida.</span><span class="sxs-lookup"><span data-stu-id="78b5b-128">Date that the license was issued.</span></span>

</dd> <dt>

<span data-ttu-id="78b5b-129">**ftExpireDate**</span><span class="sxs-lookup"><span data-stu-id="78b5b-129">**ftExpireDate**</span></span>
</dt> <dd>

<span data-ttu-id="78b5b-130">Data em que a licença irá expirar.</span><span class="sxs-lookup"><span data-stu-id="78b5b-130">Date that the license will expire.</span></span>

</dd> <dt>

<span data-ttu-id="78b5b-131">**ucLicenseStatus**</span><span class="sxs-lookup"><span data-stu-id="78b5b-131">**ucLicenseStatus**</span></span>
</dt> <dd>

<span data-ttu-id="78b5b-132">Status atual da licença.</span><span class="sxs-lookup"><span data-stu-id="78b5b-132">Current status of the license.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="78b5b-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="78b5b-133">Requirements</span></span>



| <span data-ttu-id="78b5b-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="78b5b-134">Requirement</span></span> | <span data-ttu-id="78b5b-135">Valor</span><span class="sxs-lookup"><span data-stu-id="78b5b-135">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="78b5b-136">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="78b5b-136">Minimum supported client</span></span><br/> | <span data-ttu-id="78b5b-137">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="78b5b-137">Windows Vista</span></span><br/>       |
| <span data-ttu-id="78b5b-138">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="78b5b-138">Minimum supported server</span></span><br/> | <span data-ttu-id="78b5b-139">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="78b5b-139">Windows Server 2008</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="78b5b-140">Consulte também</span><span class="sxs-lookup"><span data-stu-id="78b5b-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="78b5b-141">**LSKeyPack**</span><span class="sxs-lookup"><span data-stu-id="78b5b-141">**LSKeyPack**</span></span>](lskeypack.md)
</dt> <dt>

[<span data-ttu-id="78b5b-142">**TLSLicenseEnumBegin**</span><span class="sxs-lookup"><span data-stu-id="78b5b-142">**TLSLicenseEnumBegin**</span></span>](tlslicenseenumbegin.md)
</dt> <dt>

[<span data-ttu-id="78b5b-143">**TLSLicenseEnumNext**</span><span class="sxs-lookup"><span data-stu-id="78b5b-143">**TLSLicenseEnumNext**</span></span>](tlslicenseenumnext.md)
</dt> <dt>

[<span data-ttu-id="78b5b-144">**TLSLicenseEnumEnd**</span><span class="sxs-lookup"><span data-stu-id="78b5b-144">**TLSLicenseEnumEnd**</span></span>](tlslicenseenumend.md)
</dt> </dl>

 

 





