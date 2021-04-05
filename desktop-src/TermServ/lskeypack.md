---
title: Estrutura LSKeyPack
description: Contém informações sobre um pacote de chaves de licenciamento Serviços de Área de Trabalho Remota específico.
ms.assetid: c26d27ee-7dd3-49f0-a79c-752d23693a2a
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota estrutura LSKeyPack
- Serviços de Área de Trabalho Remota de ponteiro de estrutura de LPLSKeyPack
topic_type:
- apiref
api_name:
- LSKeyPack
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2b1ac1f51e66a0a3c15c33f2535bc02f1fd3528f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103919040"
---
# <a name="lskeypack-structure"></a><span data-ttu-id="82899-105">Estrutura LSKeyPack</span><span class="sxs-lookup"><span data-stu-id="82899-105">LSKeyPack structure</span></span>

<span data-ttu-id="82899-106">Contém informações sobre um pacote de chaves de licenciamento Serviços de Área de Trabalho Remota específico.</span><span class="sxs-lookup"><span data-stu-id="82899-106">Contains information about a specific Remote Desktop Services licensing key pack.</span></span>

> [!Note]  
> <span data-ttu-id="82899-107">Essa estrutura não está definida em nenhum arquivo de cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="82899-107">This structure is not defined in any header file.</span></span> <span data-ttu-id="82899-108">Para usar essa estrutura, você deve defini-la por conta própria, conforme mostrado neste tópico.</span><span class="sxs-lookup"><span data-stu-id="82899-108">To use this structure, you must define it yourself as shown in this topic.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="82899-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="82899-109">Syntax</span></span>


```C++
typedef struct _LSKeyPack {
  DWORD dwVersion;
  UCHAR ucKeyPackType;
  TCHAR szCompanyName[256];
  TCHAR szKeyPackId[256];
  TCHAR szProductName[256];
  TCHAR szProductId[256];
  TCHAR szProductDesc[256];
  WORD  wMajorVersion;
  WORD  wMinorVersion;
  DWORD dwPlatformType;
  UCHAR ucLicenseType;
  DWORD dwLanguageId;
  UCHAR ucChannelOfPurchase;
  TCHAR szBeginSerialNumber[256];
  DWORD dwTotalLicenseInKeyPack;
  DWORD dwProductFlags;
  DWORD dwKeyPackId;
  UCHAR ucKeyPackStatus;
  DWORD dwActivateDate;
  DWORD dwExpirationDate;
  DWORD dwNumberOfLicenses;
} LSKeyPack, *LPLSKeyPack;
```



## <a name="members"></a><span data-ttu-id="82899-110">Membros</span><span class="sxs-lookup"><span data-stu-id="82899-110">Members</span></span>

<dl> <dt>

<span data-ttu-id="82899-111">**DW**</span><span class="sxs-lookup"><span data-stu-id="82899-111">**dwVersion**</span></span>
</dt> <dd>

<span data-ttu-id="82899-112">Versão do pacote de chaves.</span><span class="sxs-lookup"><span data-stu-id="82899-112">Version of the key pack.</span></span>

</dd> <dt>

<span data-ttu-id="82899-113">**ucKeyPackType**</span><span class="sxs-lookup"><span data-stu-id="82899-113">**ucKeyPackType**</span></span>
</dt> <dd>

<span data-ttu-id="82899-114">Tipo de pacote de chaves.</span><span class="sxs-lookup"><span data-stu-id="82899-114">Type of key pack.</span></span>

</dd> <dt>

<span data-ttu-id="82899-115">**szCompanyName**</span><span class="sxs-lookup"><span data-stu-id="82899-115">**szCompanyName**</span></span>
</dt> <dd>

<span data-ttu-id="82899-116">Nome da empresa que emitiu o pacote de chaves.</span><span class="sxs-lookup"><span data-stu-id="82899-116">Name of the company that issued the key pack.</span></span>

</dd> <dt>

<span data-ttu-id="82899-117">**szKeyPackId**</span><span class="sxs-lookup"><span data-stu-id="82899-117">**szKeyPackId**</span></span>
</dt> <dd>

<span data-ttu-id="82899-118">ID do pacote de chaves.</span><span class="sxs-lookup"><span data-stu-id="82899-118">ID of the key pack.</span></span>

</dd> <dt>

<span data-ttu-id="82899-119">**szProductName**</span><span class="sxs-lookup"><span data-stu-id="82899-119">**szProductName**</span></span>
</dt> <dd>

<span data-ttu-id="82899-120">Nome do produto ao qual este pacote de chaves pertence.</span><span class="sxs-lookup"><span data-stu-id="82899-120">Name of the product to which this key pack belongs.</span></span>

</dd> <dt>

<span data-ttu-id="82899-121">**szProductId**</span><span class="sxs-lookup"><span data-stu-id="82899-121">**szProductId**</span></span>
</dt> <dd>

<span data-ttu-id="82899-122">ID do produto ao qual este pacote de chaves pertence.</span><span class="sxs-lookup"><span data-stu-id="82899-122">ID of the product to which this key pack belongs.</span></span>

</dd> <dt>

<span data-ttu-id="82899-123">**szProductDesc**</span><span class="sxs-lookup"><span data-stu-id="82899-123">**szProductDesc**</span></span>
</dt> <dd>

<span data-ttu-id="82899-124">Descrição do produto ao qual este pacote de chaves pertence.</span><span class="sxs-lookup"><span data-stu-id="82899-124">Description of the product to which this key pack belongs.</span></span>

</dd> <dt>

<span data-ttu-id="82899-125">**wMajorVersion**</span><span class="sxs-lookup"><span data-stu-id="82899-125">**wMajorVersion**</span></span>
</dt> <dd>

<span data-ttu-id="82899-126">Versão principal do produto ao qual este pacote de chaves pertence.</span><span class="sxs-lookup"><span data-stu-id="82899-126">Major version of the product to which this key pack belongs.</span></span>

</dd> <dt>

<span data-ttu-id="82899-127">**wMinorVersion**</span><span class="sxs-lookup"><span data-stu-id="82899-127">**wMinorVersion**</span></span>
</dt> <dd>

<span data-ttu-id="82899-128">Versão secundária do produto ao qual este pacote de chaves pertence.</span><span class="sxs-lookup"><span data-stu-id="82899-128">Minor version of the product to which this key pack belongs.</span></span>

</dd> <dt>

<span data-ttu-id="82899-129">**dwPlatformType**</span><span class="sxs-lookup"><span data-stu-id="82899-129">**dwPlatformType**</span></span>
</dt> <dd>

<span data-ttu-id="82899-130">Tipo de plataforma.</span><span class="sxs-lookup"><span data-stu-id="82899-130">Platform type.</span></span>

</dd> <dt>

<span data-ttu-id="82899-131">**ucLicenseType**</span><span class="sxs-lookup"><span data-stu-id="82899-131">**ucLicenseType**</span></span>
</dt> <dd>

<span data-ttu-id="82899-132">Tipo de licenças no pacote de chaves.</span><span class="sxs-lookup"><span data-stu-id="82899-132">Type of licenses in the key pack.</span></span>

</dd> <dt>

<span data-ttu-id="82899-133">**dwLanguageId**</span><span class="sxs-lookup"><span data-stu-id="82899-133">**dwLanguageId**</span></span>
</dt> <dd>

<span data-ttu-id="82899-134">Identificação de idioma</span><span class="sxs-lookup"><span data-stu-id="82899-134">Language ID.</span></span>

</dd> <dt>

<span data-ttu-id="82899-135">**ucChannelOfPurchase**</span><span class="sxs-lookup"><span data-stu-id="82899-135">**ucChannelOfPurchase**</span></span>
</dt> <dd>

<span data-ttu-id="82899-136">Canal de compra.</span><span class="sxs-lookup"><span data-stu-id="82899-136">Channel of purchase.</span></span>

</dd> <dt>

<span data-ttu-id="82899-137">**szBeginSerialNumber**</span><span class="sxs-lookup"><span data-stu-id="82899-137">**szBeginSerialNumber**</span></span>
</dt> <dd>

<span data-ttu-id="82899-138">Número de série da primeira licença.</span><span class="sxs-lookup"><span data-stu-id="82899-138">Serial number for the first license.</span></span>

</dd> <dt>

<span data-ttu-id="82899-139">**dwTotalLicenseInKeyPack**</span><span class="sxs-lookup"><span data-stu-id="82899-139">**dwTotalLicenseInKeyPack**</span></span>
</dt> <dd>

<span data-ttu-id="82899-140">Número total de licenças no pacote de chaves.</span><span class="sxs-lookup"><span data-stu-id="82899-140">Total number of licenses in the key pack.</span></span>

</dd> <dt>

<span data-ttu-id="82899-141">**dwProductFlags**</span><span class="sxs-lookup"><span data-stu-id="82899-141">**dwProductFlags**</span></span>
</dt> <dd>

<span data-ttu-id="82899-142">Flags.</span><span class="sxs-lookup"><span data-stu-id="82899-142">Flags.</span></span>

</dd> <dt>

<span data-ttu-id="82899-143">**dwKeyPackId**</span><span class="sxs-lookup"><span data-stu-id="82899-143">**dwKeyPackId**</span></span>
</dt> <dd>

<span data-ttu-id="82899-144">ID do pacote de chaves.</span><span class="sxs-lookup"><span data-stu-id="82899-144">ID of the key pack.</span></span>

</dd> <dt>

<span data-ttu-id="82899-145">**ucKeyPackStatus**</span><span class="sxs-lookup"><span data-stu-id="82899-145">**ucKeyPackStatus**</span></span>
</dt> <dd>

<span data-ttu-id="82899-146">Status do pacote de chaves.</span><span class="sxs-lookup"><span data-stu-id="82899-146">Status of the key pack.</span></span>

</dd> <dt>

<span data-ttu-id="82899-147">**dwActivateDate**</span><span class="sxs-lookup"><span data-stu-id="82899-147">**dwActivateDate**</span></span>
</dt> <dd>

<span data-ttu-id="82899-148">Data de ativação do pacote de chaves.</span><span class="sxs-lookup"><span data-stu-id="82899-148">Activation date for the key pack.</span></span>

</dd> <dt>

<span data-ttu-id="82899-149">**dwExpirationDate**</span><span class="sxs-lookup"><span data-stu-id="82899-149">**dwExpirationDate**</span></span>
</dt> <dd>

<span data-ttu-id="82899-150">Data de validade do pacote de chaves.</span><span class="sxs-lookup"><span data-stu-id="82899-150">Expiration date for the key pack.</span></span>

</dd> <dt>

<span data-ttu-id="82899-151">**dwNumberOfLicenses**</span><span class="sxs-lookup"><span data-stu-id="82899-151">**dwNumberOfLicenses**</span></span>
</dt> <dd>

<span data-ttu-id="82899-152">Número de licenças.</span><span class="sxs-lookup"><span data-stu-id="82899-152">Number of licenses.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="82899-153">Requisitos</span><span class="sxs-lookup"><span data-stu-id="82899-153">Requirements</span></span>



| <span data-ttu-id="82899-154">Requisito</span><span class="sxs-lookup"><span data-stu-id="82899-154">Requirement</span></span> | <span data-ttu-id="82899-155">Valor</span><span class="sxs-lookup"><span data-stu-id="82899-155">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="82899-156">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="82899-156">Minimum supported client</span></span><br/> | <span data-ttu-id="82899-157">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="82899-157">Windows Vista</span></span><br/>       |
| <span data-ttu-id="82899-158">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="82899-158">Minimum supported server</span></span><br/> | <span data-ttu-id="82899-159">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="82899-159">Windows Server 2008</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="82899-160">Confira também</span><span class="sxs-lookup"><span data-stu-id="82899-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="82899-161">**TLSKeyPackEnumBegin**</span><span class="sxs-lookup"><span data-stu-id="82899-161">**TLSKeyPackEnumBegin**</span></span>](tlskeypackenumbegin.md)
</dt> <dt>

[<span data-ttu-id="82899-162">**TLSKeyPackEnumNext**</span><span class="sxs-lookup"><span data-stu-id="82899-162">**TLSKeyPackEnumNext**</span></span>](tlskeypackenumnext.md)
</dt> <dt>

[<span data-ttu-id="82899-163">**TLSKeyPackEnumEnd**</span><span class="sxs-lookup"><span data-stu-id="82899-163">**TLSKeyPackEnumEnd**</span></span>](tlskeypackenumend.md)
</dt> </dl>

 

 





