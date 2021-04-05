---
title: Método AddLSToSpecifiedLicenseServerList da classe Win32_TerminalServiceSetting
description: Adiciona o servidor de licença fornecido ao final da lista de servidores de licença especificados.
ms.assetid: 2aebe7c0-5ec2-4c2d-9887-7ecd2d6ec02a
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método AddLSToSpecifiedLicenseServerList
- Método AddLSToSpecifiedLicenseServerList Serviços de Área de Trabalho Remota, classe Win32_TerminalServiceSetting
- Classe Win32_TerminalServiceSetting Serviços de Área de Trabalho Remota, método AddLSToSpecifiedLicenseServerList
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.AddLSToSpecifiedLicenseServerList
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c53a5279523405b760addabb03e381507775e6a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918204"
---
# <a name="addlstospecifiedlicenseserverlist-method-of-the-win32_terminalservicesetting-class"></a><span data-ttu-id="3a975-106">Método AddLSToSpecifiedLicenseServerList da classe Win32 \_ TerminalServiceSetting</span><span class="sxs-lookup"><span data-stu-id="3a975-106">AddLSToSpecifiedLicenseServerList method of the Win32\_TerminalServiceSetting class</span></span>

<span data-ttu-id="3a975-107">Adiciona o servidor de licença fornecido ao final da lista de servidores de licença especificados.</span><span class="sxs-lookup"><span data-stu-id="3a975-107">Adds the given license server to the end of the list of specified license servers.</span></span>

## <a name="syntax"></a><span data-ttu-id="3a975-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3a975-108">Syntax</span></span>


```mof
uint32 AddLSToSpecifiedLicenseServerList(
  [in] string LicenseServerName
);
```



## <a name="parameters"></a><span data-ttu-id="3a975-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3a975-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3a975-110">*LicenseServerName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="3a975-110">*LicenseServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3a975-111">O nome do servidor de licença a ser adicionado.</span><span class="sxs-lookup"><span data-stu-id="3a975-111">The name of the license server to add.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3a975-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3a975-112">Return value</span></span>

<span data-ttu-id="3a975-113">Retorna 0 em caso de êxito; caso contrário, retorna um código de erro WMI.</span><span class="sxs-lookup"><span data-stu-id="3a975-113">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="3a975-114">Consulte [serviços de área de trabalho remota códigos de erro do provedor WMI](terminal-services-wmi-provider-error-codes.md) para obter uma lista desses valores.</span><span class="sxs-lookup"><span data-stu-id="3a975-114">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="requirements"></a><span data-ttu-id="3a975-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3a975-115">Requirements</span></span>



| <span data-ttu-id="3a975-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="3a975-116">Requirement</span></span> | <span data-ttu-id="3a975-117">Valor</span><span class="sxs-lookup"><span data-stu-id="3a975-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3a975-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3a975-118">Minimum supported client</span></span><br/> | <span data-ttu-id="3a975-119">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="3a975-119">None supported</span></span><br/>                                                               |
| <span data-ttu-id="3a975-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3a975-120">Minimum supported server</span></span><br/> | <span data-ttu-id="3a975-121">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="3a975-121">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="3a975-122">Namespace</span><span class="sxs-lookup"><span data-stu-id="3a975-122">Namespace</span></span><br/>                | <span data-ttu-id="3a975-123">\\TerminalServices da CIMv2 raiz \\</span><span class="sxs-lookup"><span data-stu-id="3a975-123">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="3a975-124">MOF</span><span class="sxs-lookup"><span data-stu-id="3a975-124">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3a975-125"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3a975-125"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="3a975-126">DLL</span><span class="sxs-lookup"><span data-stu-id="3a975-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3a975-127"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3a975-127"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3a975-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="3a975-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3a975-129">**\_TerminalServiceSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="3a975-129">**Win32\_TerminalServiceSetting**</span></span>](win32-terminalservicesetting.md)
</dt> <dt>

[<span data-ttu-id="3a975-130">**EmptySpecifiedLicenseServerList**</span><span class="sxs-lookup"><span data-stu-id="3a975-130">**EmptySpecifiedLicenseServerList**</span></span>](emptyspecifiedlicenseserverlist-win32-terminalservicesetting.md)
</dt> <dt>

[<span data-ttu-id="3a975-131">**GetSpecifiedLicenseServerList**</span><span class="sxs-lookup"><span data-stu-id="3a975-131">**GetSpecifiedLicenseServerList**</span></span>](getspecifiedlicenseserverlist-win32-terminalservicesetting.md)
</dt> <dt>

[<span data-ttu-id="3a975-132">**RemoveLSFromSpecifiedLicenseServerList**</span><span class="sxs-lookup"><span data-stu-id="3a975-132">**RemoveLSFromSpecifiedLicenseServerList**</span></span>](removelsfromspecifiedlicenseserverlist-win32-terminalservicesetting.md)
</dt> <dt>

[<span data-ttu-id="3a975-133">**SetSpecifiedLicenseServerList**</span><span class="sxs-lookup"><span data-stu-id="3a975-133">**SetSpecifiedLicenseServerList**</span></span>](setspecifiedlicenseserverlist-win32-terminalservicesetting.md)
</dt> </dl>

 

 





