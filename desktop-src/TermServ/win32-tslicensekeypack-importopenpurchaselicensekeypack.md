---
title: Método ImportOpenPurchaseLicenseKeyPack da classe Win32_TSLicenseKeyPack
description: Importações, de outro servidor de licença Área de Trabalho Remota, uma licença aberta Serviços de Área de Trabalho Remota pacote de chaves de licença.
ms.assetid: FE1923FF-5292-4080-AB51-88B8A6B2322C
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método ImportOpenPurchaseLicenseKeyPack
- Método ImportOpenPurchaseLicenseKeyPack Serviços de Área de Trabalho Remota, classe Win32_TSLicenseKeyPack
- Classe Win32_TSLicenseKeyPack Serviços de Área de Trabalho Remota, método ImportOpenPurchaseLicenseKeyPack
topic_type:
- apiref
api_name:
- Win32_TSLicenseKeyPack.ImportOpenPurchaseLicenseKeyPack
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 944bb1ce63150caece2cbc247af24542fde2d4f4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105783331"
---
# <a name="importopenpurchaselicensekeypack-method-of-the-win32_tslicensekeypack-class"></a><span data-ttu-id="953f8-106">Método ImportOpenPurchaseLicenseKeyPack da classe Win32 \_ TSLicenseKeyPack</span><span class="sxs-lookup"><span data-stu-id="953f8-106">ImportOpenPurchaseLicenseKeyPack method of the Win32\_TSLicenseKeyPack class</span></span>

<span data-ttu-id="953f8-107">Importações, de outro servidor de licença Área de Trabalho Remota, uma licença aberta Serviços de Área de Trabalho Remota pacote de chaves de licença.</span><span class="sxs-lookup"><span data-stu-id="953f8-107">Imports, from another Remote Desktop license server, an Open License Remote Desktop Services license key pack.</span></span>

## <a name="syntax"></a><span data-ttu-id="953f8-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="953f8-108">Syntax</span></span>


```mof
uint32 ImportOpenPurchaseLicenseKeyPack(
  [in]  string sLicenseNumber,
  [in]  string sAuthorizationNumber,
  [in]  uint32 ProductVersion,
  [in]  uint32 ProductType,
  [in]  uint32 LicenseCount,
  [in]  string sSourceLSName,
  [in]  string sSourceLSProductId,
  [out] uint32 KeyPackId
);
```



## <a name="parameters"></a><span data-ttu-id="953f8-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="953f8-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="953f8-110">*sLicenseNumber* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="953f8-110">*sLicenseNumber* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="953f8-111">Cadeia de caracteres numérica de 8 caracteres fornecida com o pacote de chaves de licença.</span><span class="sxs-lookup"><span data-stu-id="953f8-111">8-character numeric string that is provided with the license key pack.</span></span> <span data-ttu-id="953f8-112">O parâmetro *sLicenseNumber* não pode conter hifens.</span><span class="sxs-lookup"><span data-stu-id="953f8-112">The *sLicenseNumber* parameter cannot contain hyphens.</span></span>

</dd> <dt>

<span data-ttu-id="953f8-113">*sAuthorizationNumber* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="953f8-113">*sAuthorizationNumber* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="953f8-114">Cadeia de caracteres alfanumérica de 15 caracteres que é fornecida com a chave de licença.</span><span class="sxs-lookup"><span data-stu-id="953f8-114">15-character alphanumeric string that is provided with the license key.</span></span> <span data-ttu-id="953f8-115">O parâmetro *sAuthorizationNumber* não pode conter hifens.</span><span class="sxs-lookup"><span data-stu-id="953f8-115">The *sAuthorizationNumber* parameter cannot contain hyphens.</span></span>

</dd> <dt>

<span data-ttu-id="953f8-116">*ProductVersion* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="953f8-116">*ProductVersion* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="953f8-117">Versão do produto.</span><span class="sxs-lookup"><span data-stu-id="953f8-117">Product version.</span></span>

<dt>

<span data-ttu-id="953f8-118">0</span><span class="sxs-lookup"><span data-stu-id="953f8-118">0</span></span>
</dt> <dd>

<span data-ttu-id="953f8-119">Não há suporte.</span><span class="sxs-lookup"><span data-stu-id="953f8-119">Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="953f8-120">1</span><span class="sxs-lookup"><span data-stu-id="953f8-120">1</span></span>
</dt> <dd>

<span data-ttu-id="953f8-121">Não há suporte.</span><span class="sxs-lookup"><span data-stu-id="953f8-121">Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="953f8-122">2</span><span class="sxs-lookup"><span data-stu-id="953f8-122">2</span></span>
</dt> <dd>

<span data-ttu-id="953f8-123">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="953f8-123">Windows Server 2008</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="953f8-124">*ProductType* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="953f8-124">*ProductType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="953f8-125">Tipo de produto.</span><span class="sxs-lookup"><span data-stu-id="953f8-125">Product type.</span></span>

<dt>

<span data-ttu-id="953f8-126">0</span><span class="sxs-lookup"><span data-stu-id="953f8-126">0</span></span>
</dt> <dd>

<span data-ttu-id="953f8-127">O tipo de produto do pacote de chaves de licença Serviços de Área de Trabalho Remota é por dispositivo.</span><span class="sxs-lookup"><span data-stu-id="953f8-127">The Remote Desktop Services license key pack product type is per device.</span></span> <span data-ttu-id="953f8-128">Portanto, cada dispositivo que se conecta ao servidor de Host da Sessão RD deve ter uma licença.</span><span class="sxs-lookup"><span data-stu-id="953f8-128">Therefore, each device that connects to the RD Session Host server must have a license.</span></span>

</dd> <dt>

<span data-ttu-id="953f8-129">1</span><span class="sxs-lookup"><span data-stu-id="953f8-129">1</span></span>
</dt> <dd>

<span data-ttu-id="953f8-130">O tipo de produto do pacote de chaves de licença Serviços de Área de Trabalho Remota é por usuário.</span><span class="sxs-lookup"><span data-stu-id="953f8-130">The Remote Desktop Services license key pack product type is per user.</span></span> <span data-ttu-id="953f8-131">Portanto, cada usuário que se conecta ao servidor de Host da Sessão RD deve ter uma licença.</span><span class="sxs-lookup"><span data-stu-id="953f8-131">Therefore, each user who connects to the RD Session Host server must have a license.</span></span>

</dd> <dt>

<span data-ttu-id="953f8-132">2</span><span class="sxs-lookup"><span data-stu-id="953f8-132">2</span></span>
</dt> <dd>

<span data-ttu-id="953f8-133">Este tipo de produto não é válido.</span><span class="sxs-lookup"><span data-stu-id="953f8-133">This product type is not valid.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="953f8-134">*LicenseCount* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="953f8-134">*LicenseCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="953f8-135">O número de licenças a serem importadas</span><span class="sxs-lookup"><span data-stu-id="953f8-135">The number of licenses to import</span></span>

</dd> <dt>

<span data-ttu-id="953f8-136">*sSourceLSName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="953f8-136">*sSourceLSName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="953f8-137">O nome do servidor de licença de Área de Trabalho Remota de origem.</span><span class="sxs-lookup"><span data-stu-id="953f8-137">The name of the source Remote Desktop license server.</span></span> <span data-ttu-id="953f8-138">Esse é o nome diferenciado totalmente qualificado ou o endereço IP do servidor.</span><span class="sxs-lookup"><span data-stu-id="953f8-138">This is either the fully qualified distinguished name or the IP address of the server.</span></span>

</dd> <dt>

<span data-ttu-id="953f8-139">*sSourceLSProductId* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="953f8-139">*sSourceLSProductId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="953f8-140">O identificador do servidor de licença Área de Trabalho Remota.</span><span class="sxs-lookup"><span data-stu-id="953f8-140">The Remote Desktop license server identifier.</span></span> <span data-ttu-id="953f8-141">O é uma cadeia de caracteres alfanumérica de 35 caracteres que não pode incluir hifens.</span><span class="sxs-lookup"><span data-stu-id="953f8-141">The is a 35-character alphanumeric string that cannot include hyphens.</span></span>

</dd> <dt>

<span data-ttu-id="953f8-142">*Pacote de chaves* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="953f8-142">*KeyPackId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="953f8-143">Recebe o identificador do pacote de chaves.</span><span class="sxs-lookup"><span data-stu-id="953f8-143">Receives the key pack identifier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="953f8-144">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="953f8-144">Return value</span></span>

<span data-ttu-id="953f8-145">Se o método tiver sucesso, ele retornará zero.</span><span class="sxs-lookup"><span data-stu-id="953f8-145">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="953f8-146">Se o método não for bem-sucedido, ele retornará um valor diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="953f8-146">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="953f8-147">Para obter uma lista de códigos de erro, consulte [serviços de área de trabalho remota códigos de erro do provedor WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="953f8-147">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="953f8-148">Requisitos</span><span class="sxs-lookup"><span data-stu-id="953f8-148">Requirements</span></span>



| <span data-ttu-id="953f8-149">Requisito</span><span class="sxs-lookup"><span data-stu-id="953f8-149">Requirement</span></span> | <span data-ttu-id="953f8-150">Valor</span><span class="sxs-lookup"><span data-stu-id="953f8-150">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="953f8-151">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="953f8-151">Minimum supported client</span></span><br/> | <span data-ttu-id="953f8-152">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="953f8-152">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="953f8-153">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="953f8-153">Minimum supported server</span></span><br/> | <span data-ttu-id="953f8-154">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="953f8-154">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="953f8-155">Namespace</span><span class="sxs-lookup"><span data-stu-id="953f8-155">Namespace</span></span><br/>                | <span data-ttu-id="953f8-156">Raiz\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="953f8-156">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="953f8-157">MOF</span><span class="sxs-lookup"><span data-stu-id="953f8-157">MOF</span></span><br/>                      | <dl> <span data-ttu-id="953f8-158"><dt>TlsWmiProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="953f8-158"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="953f8-159">DLL</span><span class="sxs-lookup"><span data-stu-id="953f8-159">DLL</span></span><br/>                      | <dl> <span data-ttu-id="953f8-160"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="953f8-160"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="953f8-161">Confira também</span><span class="sxs-lookup"><span data-stu-id="953f8-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="953f8-162">**\_TSLicenseKeyPack Win32**</span><span class="sxs-lookup"><span data-stu-id="953f8-162">**Win32\_TSLicenseKeyPack**</span></span>](win32-tslicensekeypack.md)
</dt> </dl>

 

 





