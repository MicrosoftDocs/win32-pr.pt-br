---
title: Método RemoveLicensesWithIdCount da classe Win32_TSLicenseKeyPack
description: Remove o número especificado de licenças de Serviços de Área de Trabalho Remota do pacote de chaves especificado.
ms.assetid: 36228659-7BE7-490A-A00C-A99FA66BFEB8
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método RemoveLicensesWithIdCount
- Método RemoveLicensesWithIdCount Serviços de Área de Trabalho Remota, classe Win32_TSLicenseKeyPack
- Classe Win32_TSLicenseKeyPack Serviços de Área de Trabalho Remota, método RemoveLicensesWithIdCount
topic_type:
- apiref
api_name:
- Win32_TSLicenseKeyPack.RemoveLicensesWithIdCount
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e3b2de1d1e0bfeed538e400436f8a88cd25ac563
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104008958"
---
# <a name="removelicenseswithidcount-method-of-the-win32_tslicensekeypack-class"></a><span data-ttu-id="5b0cb-106">Método RemoveLicensesWithIdCount da classe Win32 \_ TSLicenseKeyPack</span><span class="sxs-lookup"><span data-stu-id="5b0cb-106">RemoveLicensesWithIdCount method of the Win32\_TSLicenseKeyPack class</span></span>

<span data-ttu-id="5b0cb-107">Remove o número especificado de licenças de Serviços de Área de Trabalho Remota do pacote de chaves especificado.</span><span class="sxs-lookup"><span data-stu-id="5b0cb-107">Removes the specified number of Remote Desktop Services licenses from the specified key pack.</span></span>

## <a name="syntax"></a><span data-ttu-id="5b0cb-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5b0cb-108">Syntax</span></span>


```mof
uint32 RemoveLicensesWithIdCount(
  [in] uint32 KeyPackId,
  [in] uint32 LicenseCount
);
```



## <a name="parameters"></a><span data-ttu-id="5b0cb-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5b0cb-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5b0cb-110">*Pacote de chaves* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="5b0cb-110">*KeyPackId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5b0cb-111">O identificador do pacote de chaves que contém as licenças a serem removidas.</span><span class="sxs-lookup"><span data-stu-id="5b0cb-111">The identifier of the key pack that contains the licenses to remove.</span></span>

</dd> <dt>

<span data-ttu-id="5b0cb-112">*LicenseCount* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="5b0cb-112">*LicenseCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5b0cb-113">O número de licenças a desinstalar.</span><span class="sxs-lookup"><span data-stu-id="5b0cb-113">The number of licenses to uninstall.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5b0cb-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="5b0cb-114">Return value</span></span>

<span data-ttu-id="5b0cb-115">Se o método tiver sucesso, ele retornará zero.</span><span class="sxs-lookup"><span data-stu-id="5b0cb-115">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="5b0cb-116">Se o método não for bem-sucedido, ele retornará um valor diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="5b0cb-116">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="5b0cb-117">Para obter uma lista de códigos de erro, consulte [serviços de área de trabalho remota códigos de erro do provedor WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="5b0cb-117">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="5b0cb-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5b0cb-118">Requirements</span></span>



| <span data-ttu-id="5b0cb-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="5b0cb-119">Requirement</span></span> | <span data-ttu-id="5b0cb-120">Valor</span><span class="sxs-lookup"><span data-stu-id="5b0cb-120">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="5b0cb-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5b0cb-121">Minimum supported client</span></span><br/> | <span data-ttu-id="5b0cb-122">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="5b0cb-122">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="5b0cb-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5b0cb-123">Minimum supported server</span></span><br/> | <span data-ttu-id="5b0cb-124">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5b0cb-124">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="5b0cb-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="5b0cb-125">Namespace</span></span><br/>                | <span data-ttu-id="5b0cb-126">Raiz\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="5b0cb-126">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="5b0cb-127">MOF</span><span class="sxs-lookup"><span data-stu-id="5b0cb-127">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5b0cb-128"><dt>TlsWmiProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5b0cb-128"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="5b0cb-129">DLL</span><span class="sxs-lookup"><span data-stu-id="5b0cb-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5b0cb-130"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5b0cb-130"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5b0cb-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="5b0cb-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5b0cb-132">**\_TSLicenseKeyPack Win32**</span><span class="sxs-lookup"><span data-stu-id="5b0cb-132">**Win32\_TSLicenseKeyPack**</span></span>](win32-tslicensekeypack.md)
</dt> </dl>

 

 





