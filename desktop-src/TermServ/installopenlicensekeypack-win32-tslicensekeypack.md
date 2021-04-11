---
title: Método InstallOpenLicenseKeyPack da classe Win32_TSLicenseKeyPack
description: Instala uma licença aberta Serviços de Área de Trabalho Remota pacote de chaves de licença.
ms.assetid: be50e25c-cda3-408b-934b-51ce343f3271
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método InstallOpenLicenseKeyPack
- Método InstallOpenLicenseKeyPack Serviços de Área de Trabalho Remota, classe Win32_TSLicenseKeyPack
- Classe Win32_TSLicenseKeyPack Serviços de Área de Trabalho Remota, método InstallOpenLicenseKeyPack
topic_type:
- apiref
api_name:
- Win32_TSLicenseKeyPack.InstallOpenLicenseKeyPack
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7335f25d3118c14f8cd0d27f72fd6a8d4cf1e0ad
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454889"
---
# <a name="installopenlicensekeypack-method-of-the-win32_tslicensekeypack-class"></a><span data-ttu-id="fa6b1-106">Método InstallOpenLicenseKeyPack da classe Win32 \_ TSLicenseKeyPack</span><span class="sxs-lookup"><span data-stu-id="fa6b1-106">InstallOpenLicenseKeyPack method of the Win32\_TSLicenseKeyPack class</span></span>

<span data-ttu-id="fa6b1-107">Instala uma licença aberta Serviços de Área de Trabalho Remota pacote de chaves de licença.</span><span class="sxs-lookup"><span data-stu-id="fa6b1-107">Installs an Open License Remote Desktop Services license key pack.</span></span>

## <a name="syntax"></a><span data-ttu-id="fa6b1-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fa6b1-108">Syntax</span></span>


```mof
uint32 InstallOpenLicenseKeyPack(
  [in]  string sLicenseNumber,
  [in]  string sAuthorizationNumber,
  [in]  uint32 ProductVersion,
  [in]  uint32 ProductType,
  [in]  uint32 LicenseCount,
  [out] uint32 KeyPackId
);
```

## <a name="parameters"></a><span data-ttu-id="fa6b1-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fa6b1-109">Parameters</span></span>

<span data-ttu-id="fa6b1-110">*sLicenseNumber* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="fa6b1-110">*sLicenseNumber* \[in\]</span></span>

<span data-ttu-id="fa6b1-111">Cadeia de caracteres numérica de 8 caracteres fornecida com o pacote de chaves de licença.</span><span class="sxs-lookup"><span data-stu-id="fa6b1-111">8-character numeric string that is provided with the license key pack.</span></span> <span data-ttu-id="fa6b1-112">O parâmetro *sLicenseNumber* não pode conter hifens.</span><span class="sxs-lookup"><span data-stu-id="fa6b1-112">The *sLicenseNumber* parameter cannot contain hyphens.</span></span>

<span data-ttu-id="fa6b1-113">*sAuthorizationNumber* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="fa6b1-113">*sAuthorizationNumber* \[in\]</span></span>

<span data-ttu-id="fa6b1-114">Cadeia de caracteres alfanumérica de 15 caracteres que é fornecida com a chave de licença.</span><span class="sxs-lookup"><span data-stu-id="fa6b1-114">15-character alphanumeric string that is provided with the license key.</span></span> <span data-ttu-id="fa6b1-115">O parâmetro *sAuthorizationNumber* não pode conter hifens.</span><span class="sxs-lookup"><span data-stu-id="fa6b1-115">The *sAuthorizationNumber* parameter cannot contain hyphens.</span></span>

<span data-ttu-id="fa6b1-116">*ProductVersion* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="fa6b1-116">*ProductVersion* \[in\]</span></span>

<span data-ttu-id="fa6b1-117">Versão do produto.</span><span class="sxs-lookup"><span data-stu-id="fa6b1-117">Product version.</span></span>

| <span data-ttu-id="fa6b1-118">Valor</span><span class="sxs-lookup"><span data-stu-id="fa6b1-118">Value</span></span> | <span data-ttu-id="fa6b1-119">Descrição</span><span class="sxs-lookup"><span data-stu-id="fa6b1-119">Description</span></span> |
|-------|-------------|
| <span data-ttu-id="fa6b1-120">0</span><span class="sxs-lookup"><span data-stu-id="fa6b1-120">0</span></span> | <span data-ttu-id="fa6b1-121">Sem suporte</span><span class="sxs-lookup"><span data-stu-id="fa6b1-121">Not supported</span></span> |
| <span data-ttu-id="fa6b1-122">1</span><span class="sxs-lookup"><span data-stu-id="fa6b1-122">1</span></span> | <span data-ttu-id="fa6b1-123">Sem suporte</span><span class="sxs-lookup"><span data-stu-id="fa6b1-123">Not supported</span></span> |
| <span data-ttu-id="fa6b1-124">2</span><span class="sxs-lookup"><span data-stu-id="fa6b1-124">2</span></span> | <span data-ttu-id="fa6b1-125">Windows Server 2008/Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="fa6b1-125">Windows Server 2008/Windows Server 2008 R2</span></span> |
| <span data-ttu-id="fa6b1-126">4</span><span class="sxs-lookup"><span data-stu-id="fa6b1-126">4</span></span> | <span data-ttu-id="fa6b1-127">Windows Server 2012/Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="fa6b1-127">Windows Server 2012/Windows Server 2012 R2</span></span> |
| <span data-ttu-id="fa6b1-128">5</span><span class="sxs-lookup"><span data-stu-id="fa6b1-128">5</span></span> | <span data-ttu-id="fa6b1-129">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="fa6b1-129">Windows Server 2016</span></span> |
| <span data-ttu-id="fa6b1-130">6</span><span class="sxs-lookup"><span data-stu-id="fa6b1-130">6</span></span> | <span data-ttu-id="fa6b1-131">Windows Server 2019</span><span class="sxs-lookup"><span data-stu-id="fa6b1-131">Windows Server 2019</span></span> |

<span data-ttu-id="fa6b1-132">*ProductType* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="fa6b1-132">*ProductType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fa6b1-133">Tipo de produto.</span><span class="sxs-lookup"><span data-stu-id="fa6b1-133">Product type.</span></span>

| <span data-ttu-id="fa6b1-134">Valor</span><span class="sxs-lookup"><span data-stu-id="fa6b1-134">Value</span></span> | <span data-ttu-id="fa6b1-135">Descrição</span><span class="sxs-lookup"><span data-stu-id="fa6b1-135">Description</span></span> |
|-------|-------------|
| <span data-ttu-id="fa6b1-136">0</span><span class="sxs-lookup"><span data-stu-id="fa6b1-136">0</span></span> | <span data-ttu-id="fa6b1-137">O tipo de produto do pacote de chaves de licença Serviços de Área de Trabalho Remota é por dispositivo.</span><span class="sxs-lookup"><span data-stu-id="fa6b1-137">The Remote Desktop Services license key pack product type is per device.</span></span> <span data-ttu-id="fa6b1-138">Portanto, cada dispositivo que se conecta ao servidor de Host da Sessão RD deve ter uma licença.</span><span class="sxs-lookup"><span data-stu-id="fa6b1-138">Therefore, each device that connects to the RD Session Host server must have a license.</span></span> |
| <span data-ttu-id="fa6b1-139">1</span><span class="sxs-lookup"><span data-stu-id="fa6b1-139">1</span></span> | <span data-ttu-id="fa6b1-140">O tipo de produto do pacote de chaves de licença Serviços de Área de Trabalho Remota é por usuário.</span><span class="sxs-lookup"><span data-stu-id="fa6b1-140">The Remote Desktop Services license key pack product type is per user.</span></span> <span data-ttu-id="fa6b1-141">Portanto, cada usuário que se conecta ao servidor de Host da Sessão RD deve ter uma licença.</span><span class="sxs-lookup"><span data-stu-id="fa6b1-141">Therefore, each user who connects to the RD Session Host server must have a license.</span></span> |
| <span data-ttu-id="fa6b1-142">2</span><span class="sxs-lookup"><span data-stu-id="fa6b1-142">2</span></span> | <span data-ttu-id="fa6b1-143">Este tipo de produto não é válido.</span><span class="sxs-lookup"><span data-stu-id="fa6b1-143">This product type is not valid.</span></span> |

<span data-ttu-id="fa6b1-144">*LicenseCount* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="fa6b1-144">*LicenseCount* \[in\]</span></span>

<span data-ttu-id="fa6b1-145">O número de licenças a serem instaladas.</span><span class="sxs-lookup"><span data-stu-id="fa6b1-145">The number of licenses to install.</span></span>

<span data-ttu-id="fa6b1-146">*Pacote de chaves* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="fa6b1-146">*KeyPackId* \[out\]</span></span>

<span data-ttu-id="fa6b1-147">Recebe o identificador do pacote de chaves.</span><span class="sxs-lookup"><span data-stu-id="fa6b1-147">Receives the key pack identifier.</span></span>

## <a name="return-value"></a><span data-ttu-id="fa6b1-148">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="fa6b1-148">Return value</span></span>

<span data-ttu-id="fa6b1-149">Se o método tiver sucesso, ele retornará zero.</span><span class="sxs-lookup"><span data-stu-id="fa6b1-149">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="fa6b1-150">Se o método não for bem-sucedido, ele retornará um valor diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="fa6b1-150">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="fa6b1-151">Para obter uma lista de códigos de erro, consulte [serviços de área de trabalho remota códigos de erro do provedor WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="fa6b1-151">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="fa6b1-152">Comentários</span><span class="sxs-lookup"><span data-stu-id="fa6b1-152">Remarks</span></span>

<span data-ttu-id="fa6b1-153">Você deve ser um membro do grupo Administradores para chamar esse método.</span><span class="sxs-lookup"><span data-stu-id="fa6b1-153">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="fa6b1-154">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="fa6b1-154">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="fa6b1-155">Os arquivos MOF não são instalados como parte do SDK (Software Development Kit) do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="fa6b1-155">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="fa6b1-156">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="fa6b1-156">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="fa6b1-157">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="fa6b1-157">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="fa6b1-158">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fa6b1-158">Requirements</span></span>



| <span data-ttu-id="fa6b1-159">Requisito</span><span class="sxs-lookup"><span data-stu-id="fa6b1-159">Requirement</span></span> | <span data-ttu-id="fa6b1-160">Valor</span><span class="sxs-lookup"><span data-stu-id="fa6b1-160">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="fa6b1-161">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fa6b1-161">Minimum supported client</span></span><br/> | <span data-ttu-id="fa6b1-162">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="fa6b1-162">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="fa6b1-163">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fa6b1-163">Minimum supported server</span></span><br/> | <span data-ttu-id="fa6b1-164">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fa6b1-164">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="fa6b1-165">Namespace</span><span class="sxs-lookup"><span data-stu-id="fa6b1-165">Namespace</span></span><br/>                | <span data-ttu-id="fa6b1-166">Raiz\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="fa6b1-166">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="fa6b1-167">MOF</span><span class="sxs-lookup"><span data-stu-id="fa6b1-167">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fa6b1-168"><dt>TlsWmiProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="fa6b1-168"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="fa6b1-169">DLL</span><span class="sxs-lookup"><span data-stu-id="fa6b1-169">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fa6b1-170"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fa6b1-170"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fa6b1-171">Confira também</span><span class="sxs-lookup"><span data-stu-id="fa6b1-171">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fa6b1-172">**\_TSLicenseKeyPack Win32**</span><span class="sxs-lookup"><span data-stu-id="fa6b1-172">**Win32\_TSLicenseKeyPack**</span></span>](win32-tslicensekeypack.md)
</dt> </dl>

 

