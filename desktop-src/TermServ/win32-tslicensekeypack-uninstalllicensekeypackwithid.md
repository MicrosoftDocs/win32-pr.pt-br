---
title: Método UninstallLicenseKeyPackWithId da classe Win32_TSLicenseKeyPack
description: Desinstala o pacote de chaves de licença Serviços de Área de Trabalho Remota com o identificador de pacote de chaves especificado.
ms.assetid: ECB622AB-FAB4-4C5D-A007-E3ABA8E1D3E7
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método UninstallLicenseKeyPackWithId
- Método UninstallLicenseKeyPackWithId Serviços de Área de Trabalho Remota, classe Win32_TSLicenseKeyPack
- Classe Win32_TSLicenseKeyPack Serviços de Área de Trabalho Remota, método UninstallLicenseKeyPackWithId
topic_type:
- apiref
api_name:
- Win32_TSLicenseKeyPack.UninstallLicenseKeyPackWithId
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 583c7d56f5aacde57a1b683e988646e7e30b62d4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454731"
---
# <a name="uninstalllicensekeypackwithid-method-of-the-win32_tslicensekeypack-class"></a><span data-ttu-id="c260c-106">Método UninstallLicenseKeyPackWithId da classe Win32 \_ TSLicenseKeyPack</span><span class="sxs-lookup"><span data-stu-id="c260c-106">UninstallLicenseKeyPackWithId method of the Win32\_TSLicenseKeyPack class</span></span>

<span data-ttu-id="c260c-107">Desinstala o pacote de chaves de licença Serviços de Área de Trabalho Remota com o identificador de pacote de chaves especificado.</span><span class="sxs-lookup"><span data-stu-id="c260c-107">Uninstalls the Remote Desktop Services license key pack with the specified key pack identifier.</span></span>

## <a name="syntax"></a><span data-ttu-id="c260c-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c260c-108">Syntax</span></span>


```mof
uint32 UninstallLicenseKeyPackWithId(
  [in] uint32 KeyPackId
);
```



## <a name="parameters"></a><span data-ttu-id="c260c-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c260c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c260c-110">*Pacote de chaves* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c260c-110">*KeyPackId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c260c-111">O identificador do pacote de chaves a ser desinstalado.</span><span class="sxs-lookup"><span data-stu-id="c260c-111">The identifier of the key pack to uninstall.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c260c-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c260c-112">Return value</span></span>

<span data-ttu-id="c260c-113">Se o método tiver sucesso, ele retornará zero.</span><span class="sxs-lookup"><span data-stu-id="c260c-113">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="c260c-114">Se o método não for bem-sucedido, ele retornará um valor diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="c260c-114">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="c260c-115">Para obter uma lista de códigos de erro, consulte [serviços de área de trabalho remota códigos de erro do provedor WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="c260c-115">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c260c-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c260c-116">Requirements</span></span>



| <span data-ttu-id="c260c-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="c260c-117">Requirement</span></span> | <span data-ttu-id="c260c-118">Valor</span><span class="sxs-lookup"><span data-stu-id="c260c-118">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="c260c-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c260c-119">Minimum supported client</span></span><br/> | <span data-ttu-id="c260c-120">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="c260c-120">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="c260c-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c260c-121">Minimum supported server</span></span><br/> | <span data-ttu-id="c260c-122">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c260c-122">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="c260c-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="c260c-123">Namespace</span></span><br/>                | <span data-ttu-id="c260c-124">Raiz\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="c260c-124">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="c260c-125">MOF</span><span class="sxs-lookup"><span data-stu-id="c260c-125">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c260c-126"><dt>TlsWmiProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c260c-126"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="c260c-127">DLL</span><span class="sxs-lookup"><span data-stu-id="c260c-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c260c-128"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c260c-128"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c260c-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="c260c-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c260c-130">**\_TSLicenseKeyPack Win32**</span><span class="sxs-lookup"><span data-stu-id="c260c-130">**Win32\_TSLicenseKeyPack**</span></span>](win32-tslicensekeypack.md)
</dt> </dl>

 

 





