---
title: Método ImportRetailPurchaseLicenseKeyPack da classe Win32_TSLicenseKeyPack
description: Importações, de outro servidor de licença Área de Trabalho Remota, um Serviços de Área de Trabalho Remota pacote de chaves de licença que foi adquirido por meio de um canal de varejo.
ms.assetid: B45C3263-216E-4284-89A1-BE2ADE3A8E84
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método ImportRetailPurchaseLicenseKeyPack
- Método ImportRetailPurchaseLicenseKeyPack Serviços de Área de Trabalho Remota, classe Win32_TSLicenseKeyPack
- Classe Win32_TSLicenseKeyPack Serviços de Área de Trabalho Remota, método ImportRetailPurchaseLicenseKeyPack
topic_type:
- apiref
api_name:
- Win32_TSLicenseKeyPack.ImportRetailPurchaseLicenseKeyPack
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2699d1f96827f9ace0f111a4c95adb64d5f8467e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644716"
---
# <a name="importretailpurchaselicensekeypack-method-of-the-win32_tslicensekeypack-class"></a><span data-ttu-id="08891-106">Método ImportRetailPurchaseLicenseKeyPack da classe Win32 \_ TSLicenseKeyPack</span><span class="sxs-lookup"><span data-stu-id="08891-106">ImportRetailPurchaseLicenseKeyPack method of the Win32\_TSLicenseKeyPack class</span></span>

<span data-ttu-id="08891-107">Importações, de outro servidor de licença Área de Trabalho Remota, um Serviços de Área de Trabalho Remota pacote de chaves de licença que foi adquirido por meio de um canal de varejo.</span><span class="sxs-lookup"><span data-stu-id="08891-107">Imports, from another Remote Desktop license server, a Remote Desktop Services license key pack that was purchased through a retail channel.</span></span>

## <a name="syntax"></a><span data-ttu-id="08891-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="08891-108">Syntax</span></span>


```mof
uint32 ImportRetailPurchaseLicenseKeyPack(
  [in]  string sLicenseCode,
  [in]  string sSourceLSName,
  [in]  string sSourceLSProductId,
  [out] uint32 KeyPackId
);
```



## <a name="parameters"></a><span data-ttu-id="08891-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="08891-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="08891-110">*sLicenseCode* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="08891-110">*sLicenseCode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="08891-111">Contém o código de licença de 25 caracteres.</span><span class="sxs-lookup"><span data-stu-id="08891-111">Contains the 25-character license code.</span></span> <span data-ttu-id="08891-112">Somente a cadeia de caracteres alfanumérica de 25 caracteres deve ser fornecida como entrada.</span><span class="sxs-lookup"><span data-stu-id="08891-112">Only the 25-character alphanumeric character string should be given as input.</span></span> <span data-ttu-id="08891-113">Nenhum hífen deve ser adicionado.</span><span class="sxs-lookup"><span data-stu-id="08891-113">No hyphens should be added.</span></span>

</dd> <dt>

<span data-ttu-id="08891-114">*sSourceLSName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="08891-114">*sSourceLSName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="08891-115">O nome do servidor de licença de Área de Trabalho Remota de origem.</span><span class="sxs-lookup"><span data-stu-id="08891-115">The name of the source Remote Desktop license server.</span></span> <span data-ttu-id="08891-116">Esse é o nome diferenciado totalmente qualificado ou o endereço IP do servidor.</span><span class="sxs-lookup"><span data-stu-id="08891-116">This is either the fully qualified distinguished name or the IP address of the server.</span></span>

</dd> <dt>

<span data-ttu-id="08891-117">*sSourceLSProductId* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="08891-117">*sSourceLSProductId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="08891-118">O identificador do servidor de licença Área de Trabalho Remota.</span><span class="sxs-lookup"><span data-stu-id="08891-118">The Remote Desktop license server identifier.</span></span> <span data-ttu-id="08891-119">O é uma cadeia de caracteres alfanumérica de 35 caracteres que não pode incluir hifens.</span><span class="sxs-lookup"><span data-stu-id="08891-119">The is a 35-character alphanumeric string that cannot include hyphens.</span></span>

</dd> <dt>

<span data-ttu-id="08891-120">*Pacote de chaves* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="08891-120">*KeyPackId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="08891-121">Recebe o identificador do pacote de chaves.</span><span class="sxs-lookup"><span data-stu-id="08891-121">Receives the key pack identifier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="08891-122">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="08891-122">Return value</span></span>

<span data-ttu-id="08891-123">Se o método tiver sucesso, ele retornará zero.</span><span class="sxs-lookup"><span data-stu-id="08891-123">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="08891-124">Se o método não for bem-sucedido, ele retornará um valor diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="08891-124">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="08891-125">Para obter uma lista de códigos de erro, consulte [serviços de área de trabalho remota códigos de erro do provedor WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="08891-125">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="08891-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="08891-126">Requirements</span></span>



| <span data-ttu-id="08891-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="08891-127">Requirement</span></span> | <span data-ttu-id="08891-128">Valor</span><span class="sxs-lookup"><span data-stu-id="08891-128">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="08891-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="08891-129">Minimum supported client</span></span><br/> | <span data-ttu-id="08891-130">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="08891-130">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="08891-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="08891-131">Minimum supported server</span></span><br/> | <span data-ttu-id="08891-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="08891-132">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="08891-133">Namespace</span><span class="sxs-lookup"><span data-stu-id="08891-133">Namespace</span></span><br/>                | <span data-ttu-id="08891-134">Raiz\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="08891-134">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="08891-135">MOF</span><span class="sxs-lookup"><span data-stu-id="08891-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="08891-136"><dt>TlsWmiProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="08891-136"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="08891-137">DLL</span><span class="sxs-lookup"><span data-stu-id="08891-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="08891-138"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="08891-138"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="08891-139">Consulte também</span><span class="sxs-lookup"><span data-stu-id="08891-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="08891-140">**\_TSLicenseKeyPack Win32**</span><span class="sxs-lookup"><span data-stu-id="08891-140">**Win32\_TSLicenseKeyPack**</span></span>](win32-tslicensekeypack.md)
</dt> </dl>

 

 





