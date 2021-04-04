---
title: Método ReinstallLicenseKeyPackOffline da classe Win32_TSLicenseKeyPack
description: Reinstala um pacote de chaves de licença Serviços de Área de Trabalho Remota que usa o identificador de licença que foi recebido pela Internet ou pelo telefone.
ms.assetid: CFDB4C3B-C7C1-4670-BC87-92727057A500
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método ReinstallLicenseKeyPackOffline
- Método ReinstallLicenseKeyPackOffline Serviços de Área de Trabalho Remota, classe Win32_TSLicenseKeyPack
- Classe Win32_TSLicenseKeyPack Serviços de Área de Trabalho Remota, método ReinstallLicenseKeyPackOffline
topic_type:
- apiref
api_name:
- Win32_TSLicenseKeyPack.ReinstallLicenseKeyPackOffline
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e805521ea750c018ab2e7965e7fbfba05a92d8d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824212"
---
# <a name="reinstalllicensekeypackoffline-method-of-the-win32_tslicensekeypack-class"></a><span data-ttu-id="c4d1a-106">Método ReinstallLicenseKeyPackOffline da classe Win32 \_ TSLicenseKeyPack</span><span class="sxs-lookup"><span data-stu-id="c4d1a-106">ReinstallLicenseKeyPackOffline method of the Win32\_TSLicenseKeyPack class</span></span>

<span data-ttu-id="c4d1a-107">Reinstala um pacote de chaves de licença Serviços de Área de Trabalho Remota que usa o identificador de licença que foi recebido pela Internet ou pelo telefone.</span><span class="sxs-lookup"><span data-stu-id="c4d1a-107">Reinstalls a Remote Desktop Services license key pack that uses the license identifier that was received over the Internet or the phone.</span></span>

## <a name="syntax"></a><span data-ttu-id="c4d1a-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c4d1a-108">Syntax</span></span>


```mof
uint32 ReinstallLicenseKeyPackOffline(
  [in]  string sLicenseKeyPackId,
  [out] uint32 KeyPackId
);
```



## <a name="parameters"></a><span data-ttu-id="c4d1a-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c4d1a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c4d1a-110">*sLicenseKeyPackId* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c4d1a-110">*sLicenseKeyPackId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c4d1a-111">Contém o código de licença de 35 caracteres.</span><span class="sxs-lookup"><span data-stu-id="c4d1a-111">Contains the 35-character license code.</span></span> <span data-ttu-id="c4d1a-112">Somente a cadeia de caracteres alfanumérica de 35 caracteres deve ser fornecida como entrada.</span><span class="sxs-lookup"><span data-stu-id="c4d1a-112">Only the 35-character alphanumeric character string should be given as input.</span></span> <span data-ttu-id="c4d1a-113">Nenhum hífen deve ser adicionado.</span><span class="sxs-lookup"><span data-stu-id="c4d1a-113">No hyphens should be added.</span></span>

</dd> <dt>

<span data-ttu-id="c4d1a-114">*Pacote de chaves* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="c4d1a-114">*KeyPackId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c4d1a-115">Recebe o identificador do pacote de chaves.</span><span class="sxs-lookup"><span data-stu-id="c4d1a-115">Receives the key pack identifier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c4d1a-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c4d1a-116">Return value</span></span>

<span data-ttu-id="c4d1a-117">Se o método tiver sucesso, ele retornará zero.</span><span class="sxs-lookup"><span data-stu-id="c4d1a-117">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="c4d1a-118">Se o método não for bem-sucedido, ele retornará um valor diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="c4d1a-118">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="c4d1a-119">Para obter uma lista de códigos de erro, consulte [serviços de área de trabalho remota códigos de erro do provedor WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="c4d1a-119">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c4d1a-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c4d1a-120">Requirements</span></span>



| <span data-ttu-id="c4d1a-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="c4d1a-121">Requirement</span></span> | <span data-ttu-id="c4d1a-122">Valor</span><span class="sxs-lookup"><span data-stu-id="c4d1a-122">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="c4d1a-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c4d1a-123">Minimum supported client</span></span><br/> | <span data-ttu-id="c4d1a-124">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="c4d1a-124">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="c4d1a-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c4d1a-125">Minimum supported server</span></span><br/> | <span data-ttu-id="c4d1a-126">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c4d1a-126">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="c4d1a-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="c4d1a-127">Namespace</span></span><br/>                | <span data-ttu-id="c4d1a-128">Raiz\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="c4d1a-128">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="c4d1a-129">MOF</span><span class="sxs-lookup"><span data-stu-id="c4d1a-129">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c4d1a-130"><dt>TlsWmiProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c4d1a-130"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="c4d1a-131">DLL</span><span class="sxs-lookup"><span data-stu-id="c4d1a-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c4d1a-132"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c4d1a-132"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c4d1a-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="c4d1a-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c4d1a-134">**\_TSLicenseKeyPack Win32**</span><span class="sxs-lookup"><span data-stu-id="c4d1a-134">**Win32\_TSLicenseKeyPack**</span></span>](win32-tslicensekeypack.md)
</dt> </dl>

 

 





