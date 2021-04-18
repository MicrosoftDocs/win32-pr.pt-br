---
title: Método InstallAgreementLicenseKeyPack da classe Win32_TSLicenseKeyPack
description: Instala um Serviços de Área de Trabalho Remota pacote de chaves de licença adquirido por meio de um contrato de licença e se conecta automaticamente pela Internet para validar a licença do pacote de chaves.
ms.assetid: 70a0aac3-2709-47ba-bf6a-549393c4c115
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método InstallAgreementLicenseKeyPack
- Método InstallAgreementLicenseKeyPack Serviços de Área de Trabalho Remota, classe Win32_TSLicenseKeyPack
- Classe Win32_TSLicenseKeyPack Serviços de Área de Trabalho Remota, método InstallAgreementLicenseKeyPack
topic_type:
- apiref
api_name:
- Win32_TSLicenseKeyPack.InstallAgreementLicenseKeyPack
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: beb891469feae169c1267c12c04af6d21415c309
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105759936"
---
# <a name="installagreementlicensekeypack-method-of-the-win32_tslicensekeypack-class"></a><span data-ttu-id="230d3-106">Método InstallAgreementLicenseKeyPack da classe Win32 \_ TSLicenseKeyPack</span><span class="sxs-lookup"><span data-stu-id="230d3-106">InstallAgreementLicenseKeyPack method of the Win32\_TSLicenseKeyPack class</span></span>

<span data-ttu-id="230d3-107">Instala um Serviços de Área de Trabalho Remota pacote de chaves de licença adquirido por meio de um contrato de licença e se conecta automaticamente pela Internet para validar a licença do pacote de chaves.</span><span class="sxs-lookup"><span data-stu-id="230d3-107">Installs a Remote Desktop Services license key pack that was purchased through a license agreement, and automatically connects over the Internet to validate the key pack license.</span></span>

## <a name="syntax"></a><span data-ttu-id="230d3-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="230d3-108">Syntax</span></span>


```mof
uint32 InstallAgreementLicenseKeyPack(
  [in]  uint32 AgreementType,
  [in]  string sAgreementNumber,
  [in]  uint32 ProductVersion,
  [in]  uint32 ProductType,
  [in]  uint32 LicenseCount,
  [out] uint32 KeyPackId
);
```

## <a name="parameters"></a><span data-ttu-id="230d3-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="230d3-109">Parameters</span></span>

<span data-ttu-id="230d3-110">*Agreementtype* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="230d3-110">*AgreementType* \[in\]</span></span>

<span data-ttu-id="230d3-111">Tipo de contrato.</span><span class="sxs-lookup"><span data-stu-id="230d3-111">Agreement type.</span></span>

| <span data-ttu-id="230d3-112">Valor</span><span class="sxs-lookup"><span data-stu-id="230d3-112">Value</span></span> | <span data-ttu-id="230d3-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="230d3-113">Description</span></span> |
|-------|-------------|
| <span data-ttu-id="230d3-114">0</span><span class="sxs-lookup"><span data-stu-id="230d3-114">0</span></span> | <span data-ttu-id="230d3-115">O pacote de chaves de licença é de um contrato de licença de volume selecionado (para clientes com 250 ou mais computadores).</span><span class="sxs-lookup"><span data-stu-id="230d3-115">The license key pack is from a Select volume license agreement (for customers with 250 or more computers).</span></span> <span data-ttu-id="230d3-116">O parâmetro *sAgreementNumber* é o número de registro (sete dígitos numéricos) encontrado no formulário de contrato assinado.</span><span class="sxs-lookup"><span data-stu-id="230d3-116">The *sAgreementNumber* parameter is the enrollment number (seven numeric digits) found on the signed agreement form.</span></span> |
| <span data-ttu-id="230d3-117">1</span><span class="sxs-lookup"><span data-stu-id="230d3-117">1</span></span> | <span data-ttu-id="230d3-118">O pacote de chaves de licença é de um contrato de licença de volume corporativo para clientes com 250 ou mais computadores.</span><span class="sxs-lookup"><span data-stu-id="230d3-118">The license key pack is from an Enterprise volume license agreement for customers with 250 or more computers.</span></span> <span data-ttu-id="230d3-119">O parâmetro *sAgreementNumber* é o número de registro (sete dígitos numéricos) encontrado no formulário de contrato assinado.</span><span class="sxs-lookup"><span data-stu-id="230d3-119">The *sAgreementNumber* parameter is the enrollment number (seven numeric digits) found on the signed agreement form.</span></span> |
| <span data-ttu-id="230d3-120">2</span><span class="sxs-lookup"><span data-stu-id="230d3-120">2</span></span> | <span data-ttu-id="230d3-121">O pacote de chaves de licença é de um contrato de licença por volume de campus para uma instituição de ensino superior.</span><span class="sxs-lookup"><span data-stu-id="230d3-121">The license key pack is from a Campus volume license agreement for a higher education institution.</span></span> <span data-ttu-id="230d3-122">O parâmetro *sAgreementNumber* é o número de registro (sete dígitos numéricos) encontrado no formulário de contrato assinado.</span><span class="sxs-lookup"><span data-stu-id="230d3-122">The *sAgreementNumber* parameter is the enrollment number (seven numeric digits) found on the signed agreement form.</span></span> |
| <span data-ttu-id="230d3-123">3</span><span class="sxs-lookup"><span data-stu-id="230d3-123">3</span></span> | <span data-ttu-id="230d3-124">O pacote de chaves de licença é de um contrato de licença por volume da escola para instituições primárias e secundárias.</span><span class="sxs-lookup"><span data-stu-id="230d3-124">The license key pack is from a School volume license agreement for primary and secondary institutions.</span></span> <span data-ttu-id="230d3-125">O parâmetro *sAgreementNumber* é o número de registro (sete dígitos numéricos) encontrado no formulário de contrato assinado.</span><span class="sxs-lookup"><span data-stu-id="230d3-125">The *sAgreementNumber* parameter is the enrollment number (seven numeric digits) found on the signed agreement form.</span></span> |
| <span data-ttu-id="230d3-126">4</span><span class="sxs-lookup"><span data-stu-id="230d3-126">4</span></span> | <span data-ttu-id="230d3-127">O pacote de chaves de licença é de um contrato de licença de provedor de serviços para provedores de serviços para licenciar softwares da Microsoft mensalmente.</span><span class="sxs-lookup"><span data-stu-id="230d3-127">The license key pack is from a Service Provider license agreement for service providers to license Microsoft software on a monthly basis.</span></span> <span data-ttu-id="230d3-128">O parâmetro *sAgreementNumber* é o número de registro (sete dígitos numéricos) encontrado no formulário de contrato assinado.</span><span class="sxs-lookup"><span data-stu-id="230d3-128">The *sAgreementNumber* parameter is the enrollment number (seven numeric digits) found on the signed agreement form.</span></span> |
| <span data-ttu-id="230d3-129">5</span><span class="sxs-lookup"><span data-stu-id="230d3-129">5</span></span> | <span data-ttu-id="230d3-130">O pacote de chaves de licença é de outro contrato de licença, como valor aberto, licença aberta de vários anos e licença de assinatura aberta.</span><span class="sxs-lookup"><span data-stu-id="230d3-130">The license key pack is from another license agreement, such as Open Value, Multi-Year Open License, and Open Subscription License.</span></span> <span data-ttu-id="230d3-131">O parâmetro *sAgreementNumber* é o número do contrato fornecido com as informações do programa.</span><span class="sxs-lookup"><span data-stu-id="230d3-131">The *sAgreementNumber* parameter is the agreement number provided with your program information.</span></span> |

<span data-ttu-id="230d3-132">*sAgreementNumber* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="230d3-132">*sAgreementNumber* \[in\]</span></span>

<span data-ttu-id="230d3-133">Número do contrato ou número de registro.</span><span class="sxs-lookup"><span data-stu-id="230d3-133">Agreement number or enrollment number.</span></span> <span data-ttu-id="230d3-134">O parâmetro *sAgreementNumber* é uma cadeia de caracteres numérica de sete dígitos sem hifens.</span><span class="sxs-lookup"><span data-stu-id="230d3-134">The *sAgreementNumber* parameter is a seven digit numeric string without hyphens.</span></span>

<span data-ttu-id="230d3-135">*ProductVersion* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="230d3-135">*ProductVersion* \[in\]</span></span>

<span data-ttu-id="230d3-136">Versão do produto.</span><span class="sxs-lookup"><span data-stu-id="230d3-136">Product version.</span></span>

| <span data-ttu-id="230d3-137">Valor</span><span class="sxs-lookup"><span data-stu-id="230d3-137">Value</span></span> | <span data-ttu-id="230d3-138">Descrição</span><span class="sxs-lookup"><span data-stu-id="230d3-138">Description</span></span> |
|-------|-------------|
| <span data-ttu-id="230d3-139">0</span><span class="sxs-lookup"><span data-stu-id="230d3-139">0</span></span> | <span data-ttu-id="230d3-140">Sem suporte</span><span class="sxs-lookup"><span data-stu-id="230d3-140">Not supported</span></span> |
| <span data-ttu-id="230d3-141">1</span><span class="sxs-lookup"><span data-stu-id="230d3-141">1</span></span> | <span data-ttu-id="230d3-142">Sem suporte</span><span class="sxs-lookup"><span data-stu-id="230d3-142">Not supported</span></span> |
| <span data-ttu-id="230d3-143">2</span><span class="sxs-lookup"><span data-stu-id="230d3-143">2</span></span> | <span data-ttu-id="230d3-144">Windows Server 2008/Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="230d3-144">Windows Server 2008/Windows Server 2008 R2</span></span> |
| <span data-ttu-id="230d3-145">4</span><span class="sxs-lookup"><span data-stu-id="230d3-145">4</span></span> | <span data-ttu-id="230d3-146">Windows Server 2012/Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="230d3-146">Windows Server 2012/Windows Server 2012 R2</span></span> |
| <span data-ttu-id="230d3-147">5</span><span class="sxs-lookup"><span data-stu-id="230d3-147">5</span></span> | <span data-ttu-id="230d3-148">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="230d3-148">Windows Server 2016</span></span> |
| <span data-ttu-id="230d3-149">6</span><span class="sxs-lookup"><span data-stu-id="230d3-149">6</span></span> | <span data-ttu-id="230d3-150">Windows Server 2019</span><span class="sxs-lookup"><span data-stu-id="230d3-150">Windows Server 2019</span></span> |

<span data-ttu-id="230d3-151">*ProductType* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="230d3-151">*ProductType* \[in\]</span></span>

<span data-ttu-id="230d3-152">Tipo de produto.</span><span class="sxs-lookup"><span data-stu-id="230d3-152">Product type.</span></span>

| <span data-ttu-id="230d3-153">Valor</span><span class="sxs-lookup"><span data-stu-id="230d3-153">Value</span></span> | <span data-ttu-id="230d3-154">Descrição</span><span class="sxs-lookup"><span data-stu-id="230d3-154">Description</span></span> |
|-------|-------------|
| <span data-ttu-id="230d3-155">0</span><span class="sxs-lookup"><span data-stu-id="230d3-155">0</span></span> | <span data-ttu-id="230d3-156">O tipo de produto do pacote de chaves de licença Serviços de Área de Trabalho Remota é por dispositivo.</span><span class="sxs-lookup"><span data-stu-id="230d3-156">The Remote Desktop Services license key pack product type is per device.</span></span> <span data-ttu-id="230d3-157">Portanto, cada dispositivo que se conecta ao servidor de Host da Sessão RD deve ter uma licença.</span><span class="sxs-lookup"><span data-stu-id="230d3-157">Therefore, each device that connects to the RD Session Host server must have a license.</span></span> |
| <span data-ttu-id="230d3-158">1</span><span class="sxs-lookup"><span data-stu-id="230d3-158">1</span></span> | <span data-ttu-id="230d3-159">O tipo de produto do pacote de chaves de licença Serviços de Área de Trabalho Remota é por usuário.</span><span class="sxs-lookup"><span data-stu-id="230d3-159">The Remote Desktop Services license key pack product type is per user.</span></span> <span data-ttu-id="230d3-160">Portanto, cada usuário que se conecta ao servidor de Host da Sessão RD deve ter uma licença.</span><span class="sxs-lookup"><span data-stu-id="230d3-160">Therefore, each user who connects to the RD Session Host server must have a license.</span></span> |
| <span data-ttu-id="230d3-161">2</span><span class="sxs-lookup"><span data-stu-id="230d3-161">2</span></span> | <span data-ttu-id="230d3-162">Este tipo de produto não é válido.</span><span class="sxs-lookup"><span data-stu-id="230d3-162">This product type is not valid.</span></span> |

<span data-ttu-id="230d3-163">*LicenseCount* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="230d3-163">*LicenseCount* \[in\]</span></span>

<span data-ttu-id="230d3-164">Número de licenças a serem instaladas.</span><span class="sxs-lookup"><span data-stu-id="230d3-164">Number of licenses to install.</span></span>

<span data-ttu-id="230d3-165">*Pacote de chaves* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="230d3-165">*KeyPackId* \[out\]</span></span>

<span data-ttu-id="230d3-166">Recebe o identificador do pacote de chaves.</span><span class="sxs-lookup"><span data-stu-id="230d3-166">Receives the key pack identifier.</span></span>

## <a name="return-value"></a><span data-ttu-id="230d3-167">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="230d3-167">Return value</span></span>

<span data-ttu-id="230d3-168">Se o método tiver sucesso, ele retornará zero.</span><span class="sxs-lookup"><span data-stu-id="230d3-168">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="230d3-169">Se o método não for bem-sucedido, ele retornará um valor diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="230d3-169">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="230d3-170">Para obter uma lista de códigos de erro, consulte [serviços de área de trabalho remota códigos de erro do provedor WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="230d3-170">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="230d3-171">Comentários</span><span class="sxs-lookup"><span data-stu-id="230d3-171">Remarks</span></span>

<span data-ttu-id="230d3-172">Você deve ser um membro do grupo Administradores para chamar esse método.</span><span class="sxs-lookup"><span data-stu-id="230d3-172">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="230d3-173">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="230d3-173">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="230d3-174">Os arquivos MOF não são instalados como parte do SDK (Software Development Kit) do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="230d3-174">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="230d3-175">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="230d3-175">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="230d3-176">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="230d3-176">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="230d3-177">Requisitos</span><span class="sxs-lookup"><span data-stu-id="230d3-177">Requirements</span></span>

| <span data-ttu-id="230d3-178">Requisito</span><span class="sxs-lookup"><span data-stu-id="230d3-178">Requirement</span></span> | <span data-ttu-id="230d3-179">Valor</span><span class="sxs-lookup"><span data-stu-id="230d3-179">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="230d3-180">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="230d3-180">Minimum supported client</span></span><br/> | <span data-ttu-id="230d3-181">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="230d3-181">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="230d3-182">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="230d3-182">Minimum supported server</span></span><br/> | <span data-ttu-id="230d3-183">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="230d3-183">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="230d3-184">Namespace</span><span class="sxs-lookup"><span data-stu-id="230d3-184">Namespace</span></span><br/>                | <span data-ttu-id="230d3-185">Raiz\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="230d3-185">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="230d3-186">MOF</span><span class="sxs-lookup"><span data-stu-id="230d3-186">MOF</span></span><br/>                      | <dl> <span data-ttu-id="230d3-187"><dt>TlsWmiProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="230d3-187"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="230d3-188">DLL</span><span class="sxs-lookup"><span data-stu-id="230d3-188">DLL</span></span><br/>                      | <dl> <span data-ttu-id="230d3-189"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="230d3-189"><dt>TlsWmiProv.dll</dt></span></span> </dl> |

## <a name="see-also"></a><span data-ttu-id="230d3-190">Confira também</span><span class="sxs-lookup"><span data-stu-id="230d3-190">See also</span></span>

<dl> <dt>

[<span data-ttu-id="230d3-191">**\_TSLicenseKeyPack Win32**</span><span class="sxs-lookup"><span data-stu-id="230d3-191">**Win32\_TSLicenseKeyPack**</span></span>](win32-tslicensekeypack.md)
</dt> </dl>

 

