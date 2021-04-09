---
title: Método ReinstallRetailPurchaseLicenseKeyPack da classe Win32_TSLicenseKeyPack
description: Reinstala um Serviços de Área de Trabalho Remota pacote de chaves de licença que foi adquirido por meio de um canal de varejo.
ms.assetid: 19528726-8DEB-4D03-BFA6-647C8A612FA2
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método ReinstallRetailPurchaseLicenseKeyPack
- Método ReinstallRetailPurchaseLicenseKeyPack Serviços de Área de Trabalho Remota, classe Win32_TSLicenseKeyPack
- Classe Win32_TSLicenseKeyPack Serviços de Área de Trabalho Remota, método ReinstallRetailPurchaseLicenseKeyPack
topic_type:
- apiref
api_name:
- Win32_TSLicenseKeyPack.ReinstallRetailPurchaseLicenseKeyPack
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4caa8635eaf28ad823add500883832a7fe885b22
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104008959"
---
# <a name="reinstallretailpurchaselicensekeypack-method-of-the-win32_tslicensekeypack-class"></a><span data-ttu-id="69ed3-106">Método ReinstallRetailPurchaseLicenseKeyPack da classe Win32 \_ TSLicenseKeyPack</span><span class="sxs-lookup"><span data-stu-id="69ed3-106">ReinstallRetailPurchaseLicenseKeyPack method of the Win32\_TSLicenseKeyPack class</span></span>

<span data-ttu-id="69ed3-107">Reinstala um Serviços de Área de Trabalho Remota pacote de chaves de licença que foi adquirido por meio de um canal de varejo.</span><span class="sxs-lookup"><span data-stu-id="69ed3-107">Reinstalls a Remote Desktop Services license key pack that was purchased through a retail channel.</span></span>

## <a name="syntax"></a><span data-ttu-id="69ed3-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="69ed3-108">Syntax</span></span>


```mof
uint32 ReinstallRetailPurchaseLicenseKeyPack(
  [in]  string sLicenseCode,
  [out] uint32 KeyPackId
);
```



## <a name="parameters"></a><span data-ttu-id="69ed3-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="69ed3-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="69ed3-110">*sLicenseCode* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="69ed3-110">*sLicenseCode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="69ed3-111">Contém o código de licença de 25 caracteres.</span><span class="sxs-lookup"><span data-stu-id="69ed3-111">Contains the 25-character license code.</span></span> <span data-ttu-id="69ed3-112">Somente a cadeia de caracteres alfanumérica de 25 caracteres deve ser fornecida como entrada.</span><span class="sxs-lookup"><span data-stu-id="69ed3-112">Only the 25-character alphanumeric character string should be given as input.</span></span> <span data-ttu-id="69ed3-113">Nenhum hífen deve ser adicionado.</span><span class="sxs-lookup"><span data-stu-id="69ed3-113">No hyphens should be added.</span></span>

</dd> <dt>

<span data-ttu-id="69ed3-114">*Pacote de chaves* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="69ed3-114">*KeyPackId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="69ed3-115">Recebe o identificador do pacote de chaves.</span><span class="sxs-lookup"><span data-stu-id="69ed3-115">Receives the key pack identifier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="69ed3-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="69ed3-116">Return value</span></span>

<span data-ttu-id="69ed3-117">Se o método tiver sucesso, ele retornará zero.</span><span class="sxs-lookup"><span data-stu-id="69ed3-117">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="69ed3-118">Se o método não for bem-sucedido, ele retornará um valor diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="69ed3-118">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="69ed3-119">Para obter uma lista de códigos de erro, consulte [serviços de área de trabalho remota códigos de erro do provedor WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="69ed3-119">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="69ed3-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="69ed3-120">Requirements</span></span>



| <span data-ttu-id="69ed3-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="69ed3-121">Requirement</span></span> | <span data-ttu-id="69ed3-122">Valor</span><span class="sxs-lookup"><span data-stu-id="69ed3-122">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="69ed3-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="69ed3-123">Minimum supported client</span></span><br/> | <span data-ttu-id="69ed3-124">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="69ed3-124">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="69ed3-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="69ed3-125">Minimum supported server</span></span><br/> | <span data-ttu-id="69ed3-126">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="69ed3-126">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="69ed3-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="69ed3-127">Namespace</span></span><br/>                | <span data-ttu-id="69ed3-128">Raiz\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="69ed3-128">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="69ed3-129">MOF</span><span class="sxs-lookup"><span data-stu-id="69ed3-129">MOF</span></span><br/>                      | <dl> <span data-ttu-id="69ed3-130"><dt>TlsWmiProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="69ed3-130"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="69ed3-131">DLL</span><span class="sxs-lookup"><span data-stu-id="69ed3-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="69ed3-132"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="69ed3-132"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="69ed3-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="69ed3-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="69ed3-134">**\_TSLicenseKeyPack Win32**</span><span class="sxs-lookup"><span data-stu-id="69ed3-134">**Win32\_TSLicenseKeyPack**</span></span>](win32-tslicensekeypack.md)
</dt> </dl>

 

 





