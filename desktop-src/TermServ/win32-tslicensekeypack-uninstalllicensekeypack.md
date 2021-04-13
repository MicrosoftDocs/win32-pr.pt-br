---
title: Método UninstallLicenseKeyPack da classe Win32_TSLicenseKeyPack
description: Desinstala um pacote de chaves de licença Serviços de Área de Trabalho Remota.
ms.assetid: AF429AD7-C0DB-40AC-A4C6-591699FBF7E7
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método UninstallLicenseKeyPack
- Método UninstallLicenseKeyPack Serviços de Área de Trabalho Remota, classe Win32_TSLicenseKeyPack
- Classe Win32_TSLicenseKeyPack Serviços de Área de Trabalho Remota, método UninstallLicenseKeyPack
topic_type:
- apiref
api_name:
- Win32_TSLicenseKeyPack.UninstallLicenseKeyPack
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 64754ea9ef2a32676b36821cf20c4f6871396415
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369264"
---
# <a name="uninstalllicensekeypack-method-of-the-win32_tslicensekeypack-class"></a><span data-ttu-id="20eb7-106">Método UninstallLicenseKeyPack da classe Win32 \_ TSLicenseKeyPack</span><span class="sxs-lookup"><span data-stu-id="20eb7-106">UninstallLicenseKeyPack method of the Win32\_TSLicenseKeyPack class</span></span>

<span data-ttu-id="20eb7-107">Desinstala um pacote de chaves de licença Serviços de Área de Trabalho Remota.</span><span class="sxs-lookup"><span data-stu-id="20eb7-107">Uninstalls a Remote Desktop Services license key pack.</span></span>

## <a name="syntax"></a><span data-ttu-id="20eb7-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="20eb7-108">Syntax</span></span>


```mof
uint32 UninstallLicenseKeyPack(
  [in] unit32 ProductVersion,
  [in] unit32 ProductType,
  [in] uint32 LicenseCount
);
```



## <a name="parameters"></a><span data-ttu-id="20eb7-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="20eb7-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="20eb7-110">*ProductVersion* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="20eb7-110">*ProductVersion* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="20eb7-111">Identificador de versão do produto para o pacote de chaves de licença Serviços de Área de Trabalho Remota.</span><span class="sxs-lookup"><span data-stu-id="20eb7-111">Product version identifier for the Remote Desktop Services license key pack.</span></span>

<dt>

<span data-ttu-id="20eb7-112">0</span><span class="sxs-lookup"><span data-stu-id="20eb7-112">0</span></span>
</dt> <dd>

<span data-ttu-id="20eb7-113">Não há suporte.</span><span class="sxs-lookup"><span data-stu-id="20eb7-113">Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="20eb7-114">1</span><span class="sxs-lookup"><span data-stu-id="20eb7-114">1</span></span>
</dt> <dd>

<span data-ttu-id="20eb7-115">Não há suporte.</span><span class="sxs-lookup"><span data-stu-id="20eb7-115">Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="20eb7-116">2</span><span class="sxs-lookup"><span data-stu-id="20eb7-116">2</span></span>
</dt> <dd>

<span data-ttu-id="20eb7-117">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="20eb7-117">Windows Server 2008</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="20eb7-118">*ProductType* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="20eb7-118">*ProductType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="20eb7-119">Tipo de produto do Serviços de Área de Trabalho Remota pacote de chaves de licença.</span><span class="sxs-lookup"><span data-stu-id="20eb7-119">Product type of the Remote Desktop Services license key pack.</span></span>

<dt>

<span data-ttu-id="20eb7-120">0</span><span class="sxs-lookup"><span data-stu-id="20eb7-120">0</span></span>
</dt> <dd>

<span data-ttu-id="20eb7-121">O tipo de produto do pacote de chaves de licença Serviços de Área de Trabalho Remota é por dispositivo.</span><span class="sxs-lookup"><span data-stu-id="20eb7-121">The Remote Desktop Services license key pack product type is per device.</span></span> <span data-ttu-id="20eb7-122">Portanto, cada dispositivo que se conecta ao servidor de Host da Sessão RD deve ter uma licença.</span><span class="sxs-lookup"><span data-stu-id="20eb7-122">Therefore, each device that connects to the RD Session Host server must have a license.</span></span>

</dd> <dt>

<span data-ttu-id="20eb7-123">1</span><span class="sxs-lookup"><span data-stu-id="20eb7-123">1</span></span>
</dt> <dd>

<span data-ttu-id="20eb7-124">O tipo de produto do pacote de chaves de licença Serviços de Área de Trabalho Remota é por usuário.</span><span class="sxs-lookup"><span data-stu-id="20eb7-124">The Remote Desktop Services license key pack product type is per user.</span></span> <span data-ttu-id="20eb7-125">Portanto, cada usuário que se conecta ao servidor de Host da Sessão RD deve ter uma licença.</span><span class="sxs-lookup"><span data-stu-id="20eb7-125">Therefore, each user who connects to the RD Session Host server must have a license.</span></span>

</dd> <dt>

<span data-ttu-id="20eb7-126">2</span><span class="sxs-lookup"><span data-stu-id="20eb7-126">2</span></span>
</dt> <dd>

<span data-ttu-id="20eb7-127">Este tipo de produto não é válido.</span><span class="sxs-lookup"><span data-stu-id="20eb7-127">This product type is not valid.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="20eb7-128">*LicenseCount* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="20eb7-128">*LicenseCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="20eb7-129">O número de licenças a desinstalar.</span><span class="sxs-lookup"><span data-stu-id="20eb7-129">The number of licenses to uninstall.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="20eb7-130">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="20eb7-130">Return value</span></span>

<span data-ttu-id="20eb7-131">Se o método tiver sucesso, ele retornará zero.</span><span class="sxs-lookup"><span data-stu-id="20eb7-131">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="20eb7-132">Se o método não for bem-sucedido, ele retornará um valor diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="20eb7-132">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="20eb7-133">Para obter uma lista de códigos de erro, consulte [serviços de área de trabalho remota códigos de erro do provedor WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="20eb7-133">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="20eb7-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="20eb7-134">Requirements</span></span>



| <span data-ttu-id="20eb7-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="20eb7-135">Requirement</span></span> | <span data-ttu-id="20eb7-136">Valor</span><span class="sxs-lookup"><span data-stu-id="20eb7-136">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="20eb7-137">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="20eb7-137">Minimum supported client</span></span><br/> | <span data-ttu-id="20eb7-138">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="20eb7-138">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="20eb7-139">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="20eb7-139">Minimum supported server</span></span><br/> | <span data-ttu-id="20eb7-140">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="20eb7-140">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="20eb7-141">Namespace</span><span class="sxs-lookup"><span data-stu-id="20eb7-141">Namespace</span></span><br/>                | <span data-ttu-id="20eb7-142">Raiz\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="20eb7-142">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="20eb7-143">MOF</span><span class="sxs-lookup"><span data-stu-id="20eb7-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="20eb7-144"><dt>TlsWmiProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="20eb7-144"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="20eb7-145">DLL</span><span class="sxs-lookup"><span data-stu-id="20eb7-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="20eb7-146"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="20eb7-146"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="20eb7-147">Confira também</span><span class="sxs-lookup"><span data-stu-id="20eb7-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="20eb7-148">**\_TSLicenseKeyPack Win32**</span><span class="sxs-lookup"><span data-stu-id="20eb7-148">**Win32\_TSLicenseKeyPack**</span></span>](win32-tslicensekeypack.md)
</dt> </dl>

 

 





