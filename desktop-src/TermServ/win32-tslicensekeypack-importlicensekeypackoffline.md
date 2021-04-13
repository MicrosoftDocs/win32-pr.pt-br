---
title: Método ImportLicenseKeyPackOffline da classe Win32_TSLicenseKeyPack
description: Importações, de outro servidor de licença Área de Trabalho Remota, um pacote de chaves de licença Serviços de Área de Trabalho Remota que usa um identificador de licença que foi recebido pela Internet ou pelo telefone.
ms.assetid: 69D65917-8B82-4C24-AFFA-BBE529D3883C
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método ImportLicenseKeyPackOffline
- Método ImportLicenseKeyPackOffline Serviços de Área de Trabalho Remota, classe Win32_TSLicenseKeyPack
- Classe Win32_TSLicenseKeyPack Serviços de Área de Trabalho Remota, método ImportLicenseKeyPackOffline
topic_type:
- apiref
api_name:
- Win32_TSLicenseKeyPack.ImportLicenseKeyPackOffline
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0de474cce6eb91cdc605588f7f4a63d97f985769
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499405"
---
# <a name="importlicensekeypackoffline-method-of-the-win32_tslicensekeypack-class"></a><span data-ttu-id="ceb45-106">Método ImportLicenseKeyPackOffline da classe Win32 \_ TSLicenseKeyPack</span><span class="sxs-lookup"><span data-stu-id="ceb45-106">ImportLicenseKeyPackOffline method of the Win32\_TSLicenseKeyPack class</span></span>

<span data-ttu-id="ceb45-107">Importações, de outro servidor de licença Área de Trabalho Remota, um pacote de chaves de licença Serviços de Área de Trabalho Remota que usa um identificador de licença que foi recebido pela Internet ou pelo telefone.</span><span class="sxs-lookup"><span data-stu-id="ceb45-107">Imports, from another Remote Desktop license server, a Remote Desktop Services license key pack that uses a license identifier that was received over the Internet or the phone.</span></span>

## <a name="syntax"></a><span data-ttu-id="ceb45-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ceb45-108">Syntax</span></span>


```mof
uint32 ImportLicenseKeyPackOffline(
  [in]  string sLicenseKeyPackId,
  [in]  string sSourceLSName,
  [in]  string sSourceLSProductId,
  [out] uint32 KeyPackId
);
```



## <a name="parameters"></a><span data-ttu-id="ceb45-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ceb45-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ceb45-110">*sLicenseKeyPackId* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ceb45-110">*sLicenseKeyPackId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ceb45-111">Contém o código de licença de 35 caracteres.</span><span class="sxs-lookup"><span data-stu-id="ceb45-111">Contains the 35-character license code.</span></span> <span data-ttu-id="ceb45-112">Somente a cadeia de caracteres alfanumérica de 35 caracteres deve ser fornecida como entrada.</span><span class="sxs-lookup"><span data-stu-id="ceb45-112">Only the 35-character alphanumeric character string should be given as input.</span></span> <span data-ttu-id="ceb45-113">Nenhum hífen deve ser adicionado.</span><span class="sxs-lookup"><span data-stu-id="ceb45-113">No hyphens should be added.</span></span>

</dd> <dt>

<span data-ttu-id="ceb45-114">*sSourceLSName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ceb45-114">*sSourceLSName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ceb45-115">O nome do servidor de licença de Área de Trabalho Remota de origem.</span><span class="sxs-lookup"><span data-stu-id="ceb45-115">The name of the source Remote Desktop license server.</span></span> <span data-ttu-id="ceb45-116">Esse é o nome diferenciado totalmente qualificado ou o endereço IP do servidor.</span><span class="sxs-lookup"><span data-stu-id="ceb45-116">This is either the fully qualified distinguished name or the IP address of the server.</span></span>

</dd> <dt>

<span data-ttu-id="ceb45-117">*sSourceLSProductId* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ceb45-117">*sSourceLSProductId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ceb45-118">O identificador do servidor de licença Área de Trabalho Remota.</span><span class="sxs-lookup"><span data-stu-id="ceb45-118">The Remote Desktop license server identifier.</span></span> <span data-ttu-id="ceb45-119">O é uma cadeia de caracteres alfanumérica de 35 caracteres que não pode incluir hifens.</span><span class="sxs-lookup"><span data-stu-id="ceb45-119">The is a 35-character alphanumeric string that cannot include hyphens.</span></span>

</dd> <dt>

<span data-ttu-id="ceb45-120">*Pacote de chaves* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="ceb45-120">*KeyPackId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ceb45-121">Recebe o identificador do pacote de chaves.</span><span class="sxs-lookup"><span data-stu-id="ceb45-121">Receives the key pack identifier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ceb45-122">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ceb45-122">Return value</span></span>

<span data-ttu-id="ceb45-123">Se o método tiver sucesso, ele retornará zero.</span><span class="sxs-lookup"><span data-stu-id="ceb45-123">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="ceb45-124">Se o método não for bem-sucedido, ele retornará um valor diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="ceb45-124">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="ceb45-125">Para obter uma lista de códigos de erro, consulte [serviços de área de trabalho remota códigos de erro do provedor WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="ceb45-125">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ceb45-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ceb45-126">Requirements</span></span>



| <span data-ttu-id="ceb45-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="ceb45-127">Requirement</span></span> | <span data-ttu-id="ceb45-128">Valor</span><span class="sxs-lookup"><span data-stu-id="ceb45-128">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="ceb45-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ceb45-129">Minimum supported client</span></span><br/> | <span data-ttu-id="ceb45-130">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="ceb45-130">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="ceb45-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ceb45-131">Minimum supported server</span></span><br/> | <span data-ttu-id="ceb45-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ceb45-132">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="ceb45-133">Namespace</span><span class="sxs-lookup"><span data-stu-id="ceb45-133">Namespace</span></span><br/>                | <span data-ttu-id="ceb45-134">Raiz\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="ceb45-134">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="ceb45-135">MOF</span><span class="sxs-lookup"><span data-stu-id="ceb45-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ceb45-136"><dt>TlsWmiProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ceb45-136"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="ceb45-137">DLL</span><span class="sxs-lookup"><span data-stu-id="ceb45-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ceb45-138"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ceb45-138"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ceb45-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="ceb45-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ceb45-140">**\_TSLicenseKeyPack Win32**</span><span class="sxs-lookup"><span data-stu-id="ceb45-140">**Win32\_TSLicenseKeyPack**</span></span>](win32-tslicensekeypack.md)
</dt> </dl>

 

 





