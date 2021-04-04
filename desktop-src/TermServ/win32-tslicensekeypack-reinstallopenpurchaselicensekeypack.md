---
title: Método ReinstallOpenPurchaseLicenseKeyPack da classe Win32_TSLicenseKeyPack
description: Reinstala uma licença aberta Serviços de Área de Trabalho Remota pacote de chaves de licença.
ms.assetid: 3E70711E-284A-466E-A733-1219F5E0B741
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método ReinstallOpenPurchaseLicenseKeyPack
- Método ReinstallOpenPurchaseLicenseKeyPack Serviços de Área de Trabalho Remota, classe Win32_TSLicenseKeyPack
- Classe Win32_TSLicenseKeyPack Serviços de Área de Trabalho Remota, método ReinstallOpenPurchaseLicenseKeyPack
topic_type:
- apiref
api_name:
- Win32_TSLicenseKeyPack.ReinstallOpenPurchaseLicenseKeyPack
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d1eae765b74feed98760ef30c2b89a1090c4200
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103645092"
---
# <a name="reinstallopenpurchaselicensekeypack-method-of-the-win32_tslicensekeypack-class"></a><span data-ttu-id="2903b-106">Método ReinstallOpenPurchaseLicenseKeyPack da classe Win32 \_ TSLicenseKeyPack</span><span class="sxs-lookup"><span data-stu-id="2903b-106">ReinstallOpenPurchaseLicenseKeyPack method of the Win32\_TSLicenseKeyPack class</span></span>

<span data-ttu-id="2903b-107">Reinstala uma licença aberta Serviços de Área de Trabalho Remota pacote de chaves de licença.</span><span class="sxs-lookup"><span data-stu-id="2903b-107">Reinstalls an Open License Remote Desktop Services license key pack.</span></span>

## <a name="syntax"></a><span data-ttu-id="2903b-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2903b-108">Syntax</span></span>


```mof
uint32 ReinstallOpenPurchaseLicenseKeyPack(
  [in]  string sLicenseNumber,
  [in]  string sAuthorizationNumber,
  [in]  uint32 ProductVersion,
  [in]  uint32 ProductType,
  [in]  uint32 LicenseCount,
  [out] uint32 KeyPackId
);
```



## <a name="parameters"></a><span data-ttu-id="2903b-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2903b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2903b-110">*sLicenseNumber* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="2903b-110">*sLicenseNumber* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2903b-111">Cadeia de caracteres numérica de 8 caracteres fornecida com o pacote de chaves de licença.</span><span class="sxs-lookup"><span data-stu-id="2903b-111">8-character numeric string that is provided with the license key pack.</span></span> <span data-ttu-id="2903b-112">O parâmetro *sLicenseNumber* não pode conter hifens.</span><span class="sxs-lookup"><span data-stu-id="2903b-112">The *sLicenseNumber* parameter cannot contain hyphens.</span></span>

</dd> <dt>

<span data-ttu-id="2903b-113">*sAuthorizationNumber* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="2903b-113">*sAuthorizationNumber* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2903b-114">Cadeia de caracteres alfanumérica de 15 caracteres que é fornecida com a chave de licença.</span><span class="sxs-lookup"><span data-stu-id="2903b-114">15-character alphanumeric string that is provided with the license key.</span></span> <span data-ttu-id="2903b-115">O parâmetro *sAuthorizationNumber* não pode conter hifens.</span><span class="sxs-lookup"><span data-stu-id="2903b-115">The *sAuthorizationNumber* parameter cannot contain hyphens.</span></span>

</dd> <dt>

<span data-ttu-id="2903b-116">*ProductVersion* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="2903b-116">*ProductVersion* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2903b-117">Versão do produto.</span><span class="sxs-lookup"><span data-stu-id="2903b-117">Product version.</span></span>

<dt>

<span data-ttu-id="2903b-118">0</span><span class="sxs-lookup"><span data-stu-id="2903b-118">0</span></span>
</dt> <dd>

<span data-ttu-id="2903b-119">Não há suporte.</span><span class="sxs-lookup"><span data-stu-id="2903b-119">Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="2903b-120">1</span><span class="sxs-lookup"><span data-stu-id="2903b-120">1</span></span>
</dt> <dd>

<span data-ttu-id="2903b-121">Não há suporte.</span><span class="sxs-lookup"><span data-stu-id="2903b-121">Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="2903b-122">2</span><span class="sxs-lookup"><span data-stu-id="2903b-122">2</span></span>
</dt> <dd>

<span data-ttu-id="2903b-123">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2903b-123">Windows Server 2008</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="2903b-124">*ProductType* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="2903b-124">*ProductType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2903b-125">Tipo de produto.</span><span class="sxs-lookup"><span data-stu-id="2903b-125">Product type.</span></span>

<dt>

<span data-ttu-id="2903b-126">0</span><span class="sxs-lookup"><span data-stu-id="2903b-126">0</span></span>
</dt> <dd>

<span data-ttu-id="2903b-127">O tipo de produto do pacote de chaves de licença Serviços de Área de Trabalho Remota é por dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2903b-127">The Remote Desktop Services license key pack product type is per device.</span></span> <span data-ttu-id="2903b-128">Portanto, cada dispositivo que se conecta ao servidor de Host da Sessão RD deve ter uma licença.</span><span class="sxs-lookup"><span data-stu-id="2903b-128">Therefore, each device that connects to the RD Session Host server must have a license.</span></span>

</dd> <dt>

<span data-ttu-id="2903b-129">1</span><span class="sxs-lookup"><span data-stu-id="2903b-129">1</span></span>
</dt> <dd>

<span data-ttu-id="2903b-130">O tipo de produto do pacote de chaves de licença Serviços de Área de Trabalho Remota é por usuário.</span><span class="sxs-lookup"><span data-stu-id="2903b-130">The Remote Desktop Services license key pack product type is per user.</span></span> <span data-ttu-id="2903b-131">Portanto, cada usuário que se conecta ao servidor de Host da Sessão RD deve ter uma licença.</span><span class="sxs-lookup"><span data-stu-id="2903b-131">Therefore, each user who connects to the RD Session Host server must have a license.</span></span>

</dd> <dt>

<span data-ttu-id="2903b-132">2</span><span class="sxs-lookup"><span data-stu-id="2903b-132">2</span></span>
</dt> <dd>

<span data-ttu-id="2903b-133">Este tipo de produto não é válido.</span><span class="sxs-lookup"><span data-stu-id="2903b-133">This product type is not valid.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="2903b-134">*LicenseCount* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="2903b-134">*LicenseCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2903b-135">O número de licenças a serem instaladas.</span><span class="sxs-lookup"><span data-stu-id="2903b-135">The number of licenses to install.</span></span>

</dd> <dt>

<span data-ttu-id="2903b-136">*Pacote de chaves* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="2903b-136">*KeyPackId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2903b-137">Recebe o identificador do pacote de chaves.</span><span class="sxs-lookup"><span data-stu-id="2903b-137">Receives the key pack identifier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2903b-138">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="2903b-138">Return value</span></span>

<span data-ttu-id="2903b-139">Se o método tiver sucesso, ele retornará zero.</span><span class="sxs-lookup"><span data-stu-id="2903b-139">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="2903b-140">Se o método não for bem-sucedido, ele retornará um valor diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="2903b-140">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="2903b-141">Para obter uma lista de códigos de erro, consulte [serviços de área de trabalho remota códigos de erro do provedor WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="2903b-141">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="2903b-142">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2903b-142">Requirements</span></span>



| <span data-ttu-id="2903b-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="2903b-143">Requirement</span></span> | <span data-ttu-id="2903b-144">Valor</span><span class="sxs-lookup"><span data-stu-id="2903b-144">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="2903b-145">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2903b-145">Minimum supported client</span></span><br/> | <span data-ttu-id="2903b-146">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="2903b-146">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="2903b-147">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2903b-147">Minimum supported server</span></span><br/> | <span data-ttu-id="2903b-148">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2903b-148">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="2903b-149">Namespace</span><span class="sxs-lookup"><span data-stu-id="2903b-149">Namespace</span></span><br/>                | <span data-ttu-id="2903b-150">Raiz\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="2903b-150">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="2903b-151">MOF</span><span class="sxs-lookup"><span data-stu-id="2903b-151">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2903b-152"><dt>TlsWmiProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2903b-152"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="2903b-153">DLL</span><span class="sxs-lookup"><span data-stu-id="2903b-153">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2903b-154"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2903b-154"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2903b-155">Confira também</span><span class="sxs-lookup"><span data-stu-id="2903b-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2903b-156">**\_TSLicenseKeyPack Win32**</span><span class="sxs-lookup"><span data-stu-id="2903b-156">**Win32\_TSLicenseKeyPack**</span></span>](win32-tslicensekeypack.md)
</dt> </dl>

 

 





