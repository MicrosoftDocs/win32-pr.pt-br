---
title: Método ImportAgreementLicenseKeyPack da classe Win32_TSLicenseKeyPack
description: Importações, de outro servidor de licença Área de Trabalho Remota, um Serviços de Área de Trabalho Remota pacote de chaves de licença que foi adquirido por meio de um contrato de licença e se conecta automaticamente pela Internet para validar a licença do pacote de chaves.
ms.assetid: 3C29E691-3734-4D39-A89F-F381F285DC9E
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método ImportAgreementLicenseKeyPack
- Método ImportAgreementLicenseKeyPack Serviços de Área de Trabalho Remota, classe Win32_TSLicenseKeyPack
- Classe Win32_TSLicenseKeyPack Serviços de Área de Trabalho Remota, método ImportAgreementLicenseKeyPack
topic_type:
- apiref
api_name:
- Win32_TSLicenseKeyPack.ImportAgreementLicenseKeyPack
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff61d022f9cf195eb357817f7733f4ec49e2986f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086354"
---
# <a name="importagreementlicensekeypack-method-of-the-win32_tslicensekeypack-class"></a><span data-ttu-id="aa9b2-106">Método ImportAgreementLicenseKeyPack da classe Win32 \_ TSLicenseKeyPack</span><span class="sxs-lookup"><span data-stu-id="aa9b2-106">ImportAgreementLicenseKeyPack method of the Win32\_TSLicenseKeyPack class</span></span>

<span data-ttu-id="aa9b2-107">Importações, de outro servidor de licença Área de Trabalho Remota, um Serviços de Área de Trabalho Remota pacote de chaves de licença que foi adquirido por meio de um contrato de licença e se conecta automaticamente pela Internet para validar a licença do pacote de chaves.</span><span class="sxs-lookup"><span data-stu-id="aa9b2-107">Imports, from another Remote Desktop license server, a Remote Desktop Services license key pack that was purchased through a license agreement, and automatically connects over the Internet to validate the key pack license.</span></span>

## <a name="syntax"></a><span data-ttu-id="aa9b2-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="aa9b2-108">Syntax</span></span>


```mof
uint32 ImportAgreementLicenseKeyPack(
  [in]  uint32 AgreementType,
  [in]  string sAgreementNumber,
  [in]  uint32 ProductVersion,
  [in]  uint32 ProductType,
  [in]  uint32 LicenseCount,
  [in]  string sSourceLSName,
  [in]  string sSourceLSProductId,
  [out] uint32 KeyPackId
);
```



## <a name="parameters"></a><span data-ttu-id="aa9b2-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="aa9b2-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aa9b2-110">*Agreementtype* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="aa9b2-110">*AgreementType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aa9b2-111">Tipo de contrato.</span><span class="sxs-lookup"><span data-stu-id="aa9b2-111">Agreement type.</span></span>

<dt>

<span data-ttu-id="aa9b2-112">0</span><span class="sxs-lookup"><span data-stu-id="aa9b2-112">0</span></span>
</dt> <dd>

<span data-ttu-id="aa9b2-113">O pacote de chaves de licença é de um contrato de licença de volume selecionado (para clientes com 250 ou mais computadores).</span><span class="sxs-lookup"><span data-stu-id="aa9b2-113">The license key pack is from a Select volume license agreement (for customers with 250 or more computers).</span></span> <span data-ttu-id="aa9b2-114">O parâmetro *sAgreementNumber* é o número de registro (sete dígitos numéricos) encontrado no formulário de contrato assinado.</span><span class="sxs-lookup"><span data-stu-id="aa9b2-114">The *sAgreementNumber* parameter is the enrollment number (seven numeric digits) found on the signed agreement form.</span></span>

</dd> <dt>

<span data-ttu-id="aa9b2-115">1</span><span class="sxs-lookup"><span data-stu-id="aa9b2-115">1</span></span>
</dt> <dd>

<span data-ttu-id="aa9b2-116">O pacote de chaves de licença é de um contrato de licença de volume corporativo para clientes com 250 ou mais computadores.</span><span class="sxs-lookup"><span data-stu-id="aa9b2-116">The license key pack is from an Enterprise volume license agreement for customers with 250 or more computers.</span></span> <span data-ttu-id="aa9b2-117">O parâmetro *sAgreementNumber* é o número de registro (sete dígitos numéricos) encontrado no formulário de contrato assinado.</span><span class="sxs-lookup"><span data-stu-id="aa9b2-117">The *sAgreementNumber* parameter is the enrollment number (seven numeric digits) found on the signed agreement form.</span></span>

</dd> <dt>

<span data-ttu-id="aa9b2-118">2</span><span class="sxs-lookup"><span data-stu-id="aa9b2-118">2</span></span>
</dt> <dd>

<span data-ttu-id="aa9b2-119">O pacote de chaves de licença é de um contrato de licença por volume de campus para uma instituição de ensino superior.</span><span class="sxs-lookup"><span data-stu-id="aa9b2-119">The license key pack is from a Campus volume license agreement for a higher education institution.</span></span> <span data-ttu-id="aa9b2-120">O parâmetro *sAgreementNumber* é o número de registro (sete dígitos numéricos) encontrado no formulário de contrato assinado.</span><span class="sxs-lookup"><span data-stu-id="aa9b2-120">The *sAgreementNumber* parameter is the enrollment number (seven numeric digits) found on the signed agreement form.</span></span>

</dd> <dt>

<span data-ttu-id="aa9b2-121">3</span><span class="sxs-lookup"><span data-stu-id="aa9b2-121">3</span></span>
</dt> <dd>

<span data-ttu-id="aa9b2-122">O pacote de chaves de licença é de um contrato de licença por volume da escola para instituições primárias e secundárias.</span><span class="sxs-lookup"><span data-stu-id="aa9b2-122">The license key pack is from a School volume license agreement for primary and secondary institutions.</span></span> <span data-ttu-id="aa9b2-123">O parâmetro *sAgreementNumber* é o número de registro (sete dígitos numéricos) encontrado no formulário de contrato assinado.</span><span class="sxs-lookup"><span data-stu-id="aa9b2-123">The *sAgreementNumber* parameter is the enrollment number (seven numeric digits) found on the signed agreement form.</span></span>

</dd> <dt>

<span data-ttu-id="aa9b2-124">4</span><span class="sxs-lookup"><span data-stu-id="aa9b2-124">4</span></span>
</dt> <dd>

<span data-ttu-id="aa9b2-125">O pacote de chaves de licença é de um contrato de licença de provedor de serviços para provedores de serviços para licenciar softwares da Microsoft mensalmente.</span><span class="sxs-lookup"><span data-stu-id="aa9b2-125">The license key pack is from a Service Provider license agreement for service providers to license Microsoft software on a monthly basis.</span></span> <span data-ttu-id="aa9b2-126">O parâmetro *sAgreementNumber* é o número de registro (sete dígitos numéricos) encontrado no formulário de contrato assinado.</span><span class="sxs-lookup"><span data-stu-id="aa9b2-126">The *sAgreementNumber* parameter is the enrollment number (seven numeric digits) found on the signed agreement form.</span></span>

</dd> <dt>

<span data-ttu-id="aa9b2-127">5</span><span class="sxs-lookup"><span data-stu-id="aa9b2-127">5</span></span>
</dt> <dd>

<span data-ttu-id="aa9b2-128">O pacote de chaves de licença é de outro contrato de licença, como valor aberto, licença aberta de vários anos e licença de assinatura aberta.</span><span class="sxs-lookup"><span data-stu-id="aa9b2-128">The license key pack is from another license agreement, such as Open Value, Multi-Year Open License, and Open Subscription License.</span></span> <span data-ttu-id="aa9b2-129">O parâmetro *sAgreementNumber* é o número do contrato fornecido com as informações do programa.</span><span class="sxs-lookup"><span data-stu-id="aa9b2-129">The *sAgreementNumber* parameter is the agreement number provided with your program information.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="aa9b2-130">*sAgreementNumber* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="aa9b2-130">*sAgreementNumber* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aa9b2-131">Número do contrato ou número de registro.</span><span class="sxs-lookup"><span data-stu-id="aa9b2-131">Agreement number or enrollment number.</span></span> <span data-ttu-id="aa9b2-132">O parâmetro *sAgreementNumber* é uma cadeia de caracteres numérica de sete dígitos sem hifens.</span><span class="sxs-lookup"><span data-stu-id="aa9b2-132">The *sAgreementNumber* parameter is a seven digit numeric string without hyphens.</span></span>

</dd> <dt>

<span data-ttu-id="aa9b2-133">*ProductVersion* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="aa9b2-133">*ProductVersion* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aa9b2-134">Versão do produto.</span><span class="sxs-lookup"><span data-stu-id="aa9b2-134">Product version.</span></span>

<dt>

<span data-ttu-id="aa9b2-135">0</span><span class="sxs-lookup"><span data-stu-id="aa9b2-135">0</span></span>
</dt> <dd>

<span data-ttu-id="aa9b2-136">Não há suporte.</span><span class="sxs-lookup"><span data-stu-id="aa9b2-136">Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="aa9b2-137">1</span><span class="sxs-lookup"><span data-stu-id="aa9b2-137">1</span></span>
</dt> <dd>

<span data-ttu-id="aa9b2-138">Não há suporte.</span><span class="sxs-lookup"><span data-stu-id="aa9b2-138">Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="aa9b2-139">2</span><span class="sxs-lookup"><span data-stu-id="aa9b2-139">2</span></span>
</dt> <dd>

<span data-ttu-id="aa9b2-140">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="aa9b2-140">Windows Server 2008</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="aa9b2-141">*ProductType* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="aa9b2-141">*ProductType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aa9b2-142">Tipo de produto.</span><span class="sxs-lookup"><span data-stu-id="aa9b2-142">Product type.</span></span>

<dt>

<span data-ttu-id="aa9b2-143">0</span><span class="sxs-lookup"><span data-stu-id="aa9b2-143">0</span></span>
</dt> <dd>

<span data-ttu-id="aa9b2-144">O tipo de produto do pacote de chaves de licença Serviços de Área de Trabalho Remota é por dispositivo.</span><span class="sxs-lookup"><span data-stu-id="aa9b2-144">The Remote Desktop Services license key pack product type is per device.</span></span> <span data-ttu-id="aa9b2-145">Portanto, cada dispositivo que se conecta ao servidor de Host da Sessão RD deve ter uma licença.</span><span class="sxs-lookup"><span data-stu-id="aa9b2-145">Therefore, each device that connects to the RD Session Host server must have a license.</span></span>

</dd> <dt>

<span data-ttu-id="aa9b2-146">1</span><span class="sxs-lookup"><span data-stu-id="aa9b2-146">1</span></span>
</dt> <dd>

<span data-ttu-id="aa9b2-147">O tipo de produto do pacote de chaves de licença Serviços de Área de Trabalho Remota é por usuário.</span><span class="sxs-lookup"><span data-stu-id="aa9b2-147">The Remote Desktop Services license key pack product type is per user.</span></span> <span data-ttu-id="aa9b2-148">Portanto, cada usuário que se conecta ao servidor de Host da Sessão RD deve ter uma licença.</span><span class="sxs-lookup"><span data-stu-id="aa9b2-148">Therefore, each user who connects to the RD Session Host server must have a license.</span></span>

</dd> <dt>

<span data-ttu-id="aa9b2-149">2</span><span class="sxs-lookup"><span data-stu-id="aa9b2-149">2</span></span>
</dt> <dd>

<span data-ttu-id="aa9b2-150">Este tipo de produto não é válido.</span><span class="sxs-lookup"><span data-stu-id="aa9b2-150">This product type is not valid.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="aa9b2-151">*LicenseCount* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="aa9b2-151">*LicenseCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aa9b2-152">Número de licenças a serem importadas.</span><span class="sxs-lookup"><span data-stu-id="aa9b2-152">Number of licenses to import.</span></span>

</dd> <dt>

<span data-ttu-id="aa9b2-153">*sSourceLSName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="aa9b2-153">*sSourceLSName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aa9b2-154">O nome do servidor de licença de Área de Trabalho Remota de origem.</span><span class="sxs-lookup"><span data-stu-id="aa9b2-154">The name of the source Remote Desktop license server.</span></span> <span data-ttu-id="aa9b2-155">Esse é o nome diferenciado totalmente qualificado ou o endereço IP do servidor.</span><span class="sxs-lookup"><span data-stu-id="aa9b2-155">This is either the fully qualified distinguished name or the IP address of the server.</span></span>

</dd> <dt>

<span data-ttu-id="aa9b2-156">*sSourceLSProductId* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="aa9b2-156">*sSourceLSProductId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aa9b2-157">O identificador do servidor de licença Área de Trabalho Remota.</span><span class="sxs-lookup"><span data-stu-id="aa9b2-157">The Remote Desktop license server identifier.</span></span> <span data-ttu-id="aa9b2-158">O é uma cadeia de caracteres alfanumérica de 35 caracteres que não pode incluir hifens.</span><span class="sxs-lookup"><span data-stu-id="aa9b2-158">The is a 35-character alphanumeric string that cannot include hyphens.</span></span>

</dd> <dt>

<span data-ttu-id="aa9b2-159">*Pacote de chaves* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="aa9b2-159">*KeyPackId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="aa9b2-160">Recebe o identificador do pacote de chaves.</span><span class="sxs-lookup"><span data-stu-id="aa9b2-160">Receives the key pack identifier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aa9b2-161">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="aa9b2-161">Return value</span></span>

<span data-ttu-id="aa9b2-162">Se o método tiver sucesso, ele retornará zero.</span><span class="sxs-lookup"><span data-stu-id="aa9b2-162">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="aa9b2-163">Se o método não for bem-sucedido, ele retornará um valor diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="aa9b2-163">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="aa9b2-164">Para obter uma lista de códigos de erro, consulte [serviços de área de trabalho remota códigos de erro do provedor WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="aa9b2-164">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="aa9b2-165">Requisitos</span><span class="sxs-lookup"><span data-stu-id="aa9b2-165">Requirements</span></span>



| <span data-ttu-id="aa9b2-166">Requisito</span><span class="sxs-lookup"><span data-stu-id="aa9b2-166">Requirement</span></span> | <span data-ttu-id="aa9b2-167">Valor</span><span class="sxs-lookup"><span data-stu-id="aa9b2-167">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="aa9b2-168">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="aa9b2-168">Minimum supported client</span></span><br/> | <span data-ttu-id="aa9b2-169">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="aa9b2-169">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="aa9b2-170">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="aa9b2-170">Minimum supported server</span></span><br/> | <span data-ttu-id="aa9b2-171">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="aa9b2-171">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="aa9b2-172">Namespace</span><span class="sxs-lookup"><span data-stu-id="aa9b2-172">Namespace</span></span><br/>                | <span data-ttu-id="aa9b2-173">Raiz\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="aa9b2-173">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="aa9b2-174">MOF</span><span class="sxs-lookup"><span data-stu-id="aa9b2-174">MOF</span></span><br/>                      | <dl> <span data-ttu-id="aa9b2-175"><dt>TlsWmiProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="aa9b2-175"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="aa9b2-176">DLL</span><span class="sxs-lookup"><span data-stu-id="aa9b2-176">DLL</span></span><br/>                      | <dl> <span data-ttu-id="aa9b2-177"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="aa9b2-177"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aa9b2-178">Confira também</span><span class="sxs-lookup"><span data-stu-id="aa9b2-178">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aa9b2-179">**\_TSLicenseKeyPack Win32**</span><span class="sxs-lookup"><span data-stu-id="aa9b2-179">**Win32\_TSLicenseKeyPack**</span></span>](win32-tslicensekeypack.md)
</dt> </dl>

 

 





