---
title: Método ConvertLicenses da classe Win32_TSLicenseKeyPack
description: Converte as licenças no pacote de chaves atual.
ms.assetid: 38600144-8fa2-4f9a-b7a4-7fafc304e7cb
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método ConvertLicenses
- Método ConvertLicenses Serviços de Área de Trabalho Remota, classe Win32_TSLicenseKeyPack
- Classe Win32_TSLicenseKeyPack Serviços de Área de Trabalho Remota, método ConvertLicenses
topic_type:
- apiref
api_name:
- Win32_TSLicenseKeyPack.ConvertLicenses
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 54f37b1d9804c5f14f89a7ff6b48f5f8fcbdc60b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369327"
---
# <a name="convertlicenses-method-of-the-win32_tslicensekeypack-class"></a><span data-ttu-id="f6d7a-106">Método ConvertLicenses da classe Win32 \_ TSLicenseKeyPack</span><span class="sxs-lookup"><span data-stu-id="f6d7a-106">ConvertLicenses method of the Win32\_TSLicenseKeyPack class</span></span>

<span data-ttu-id="f6d7a-107">Converte as licenças no pacote de chaves atual.</span><span class="sxs-lookup"><span data-stu-id="f6d7a-107">Converts the licenses in the current key pack.</span></span> <span data-ttu-id="f6d7a-108">Se a licença for uma licença por usuário, ela será convertida em uma licença por dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f6d7a-108">If the license is a per-user license, it is converted to a per-device license.</span></span> <span data-ttu-id="f6d7a-109">Se a licença for uma licença por dispositivo, ela será convertida em uma licença por usuário.</span><span class="sxs-lookup"><span data-stu-id="f6d7a-109">If the license is a per-device license, it is converted to a per-user license.</span></span>

## <a name="syntax"></a><span data-ttu-id="f6d7a-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f6d7a-110">Syntax</span></span>


```mof
uint32 ConvertLicenses(
  [in]  uint32 Count,
  [out] uint32 KeypackID
);
```



## <a name="parameters"></a><span data-ttu-id="f6d7a-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f6d7a-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f6d7a-112">*Contagem* \[ de no\]</span><span class="sxs-lookup"><span data-stu-id="f6d7a-112">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f6d7a-113">O número de licenças a serem convertidas.</span><span class="sxs-lookup"><span data-stu-id="f6d7a-113">The number of licenses to be converted.</span></span>

</dd> <dt>

<span data-ttu-id="f6d7a-114">*Pacote de chaves* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="f6d7a-114">*KeypackID* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f6d7a-115">O identificador do pacote de chaves resultante.</span><span class="sxs-lookup"><span data-stu-id="f6d7a-115">The identifier of the resultant key pack.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f6d7a-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f6d7a-116">Return value</span></span>

<span data-ttu-id="f6d7a-117">Se o método tiver sucesso, ele retornará zero.</span><span class="sxs-lookup"><span data-stu-id="f6d7a-117">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="f6d7a-118">Se o método não for bem-sucedido, ele retornará um valor diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="f6d7a-118">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="f6d7a-119">Para obter uma lista de códigos de erro, consulte [serviços de área de trabalho remota códigos de erro do provedor WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="f6d7a-119">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f6d7a-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f6d7a-120">Requirements</span></span>



| <span data-ttu-id="f6d7a-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="f6d7a-121">Requirement</span></span> | <span data-ttu-id="f6d7a-122">Valor</span><span class="sxs-lookup"><span data-stu-id="f6d7a-122">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="f6d7a-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f6d7a-123">Minimum supported client</span></span><br/> | <span data-ttu-id="f6d7a-124">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="f6d7a-124">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="f6d7a-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f6d7a-125">Minimum supported server</span></span><br/> | <span data-ttu-id="f6d7a-126">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="f6d7a-126">Windows Server 2012</span></span><br/>                                                            |
| <span data-ttu-id="f6d7a-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="f6d7a-127">Namespace</span></span><br/>                | <span data-ttu-id="f6d7a-128">Raiz\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="f6d7a-128">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="f6d7a-129">MOF</span><span class="sxs-lookup"><span data-stu-id="f6d7a-129">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f6d7a-130"><dt>TlsWmiProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f6d7a-130"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="f6d7a-131">DLL</span><span class="sxs-lookup"><span data-stu-id="f6d7a-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f6d7a-132"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f6d7a-132"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f6d7a-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="f6d7a-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f6d7a-134">**\_TSLicenseKeyPack Win32**</span><span class="sxs-lookup"><span data-stu-id="f6d7a-134">**Win32\_TSLicenseKeyPack**</span></span>](win32-tslicensekeypack.md)
</dt> </dl>

 

 





