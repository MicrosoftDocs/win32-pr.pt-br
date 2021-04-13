---
title: Método EmptySpecifiedLicenseServerList da classe Win32_TerminalServiceSetting
description: Remove todos os servidores de licença da lista de servidores de licença especificados.
ms.assetid: de1633ca-3f0b-4540-8b45-44303a4e72fe
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método EmptySpecifiedLicenseServerList
- Método EmptySpecifiedLicenseServerList Serviços de Área de Trabalho Remota, classe Win32_TerminalServiceSetting
- Classe Win32_TerminalServiceSetting Serviços de Área de Trabalho Remota, método EmptySpecifiedLicenseServerList
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.EmptySpecifiedLicenseServerList
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1392c05618860f742a13140167e423b312e49b0a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104456014"
---
# <a name="emptyspecifiedlicenseserverlist-method-of-the-win32_terminalservicesetting-class"></a><span data-ttu-id="2ec2b-106">Método EmptySpecifiedLicenseServerList da classe Win32 \_ TerminalServiceSetting</span><span class="sxs-lookup"><span data-stu-id="2ec2b-106">EmptySpecifiedLicenseServerList method of the Win32\_TerminalServiceSetting class</span></span>

<span data-ttu-id="2ec2b-107">Remove todos os servidores de licença da lista de servidores de licença especificados.</span><span class="sxs-lookup"><span data-stu-id="2ec2b-107">Removes all license servers from the list of specified license servers.</span></span>

## <a name="syntax"></a><span data-ttu-id="2ec2b-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2ec2b-108">Syntax</span></span>


```mof
uint32 EmptySpecifiedLicenseServerList();
```



## <a name="parameters"></a><span data-ttu-id="2ec2b-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2ec2b-109">Parameters</span></span>

<span data-ttu-id="2ec2b-110">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="2ec2b-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="2ec2b-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="2ec2b-111">Return value</span></span>

<span data-ttu-id="2ec2b-112">Retorna 0 em caso de êxito; caso contrário, retorna um código de erro WMI.</span><span class="sxs-lookup"><span data-stu-id="2ec2b-112">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="2ec2b-113">Consulte [serviços de área de trabalho remota códigos de erro do provedor WMI](terminal-services-wmi-provider-error-codes.md) para obter uma lista desses valores.</span><span class="sxs-lookup"><span data-stu-id="2ec2b-113">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="requirements"></a><span data-ttu-id="2ec2b-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2ec2b-114">Requirements</span></span>



| <span data-ttu-id="2ec2b-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="2ec2b-115">Requirement</span></span> | <span data-ttu-id="2ec2b-116">Valor</span><span class="sxs-lookup"><span data-stu-id="2ec2b-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2ec2b-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2ec2b-117">Minimum supported client</span></span><br/> | <span data-ttu-id="2ec2b-118">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="2ec2b-118">None supported</span></span><br/>                                                               |
| <span data-ttu-id="2ec2b-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2ec2b-119">Minimum supported server</span></span><br/> | <span data-ttu-id="2ec2b-120">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="2ec2b-120">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="2ec2b-121">Namespace</span><span class="sxs-lookup"><span data-stu-id="2ec2b-121">Namespace</span></span><br/>                | <span data-ttu-id="2ec2b-122">\\TerminalServices da CIMv2 raiz \\</span><span class="sxs-lookup"><span data-stu-id="2ec2b-122">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="2ec2b-123">MOF</span><span class="sxs-lookup"><span data-stu-id="2ec2b-123">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2ec2b-124"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2ec2b-124"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="2ec2b-125">DLL</span><span class="sxs-lookup"><span data-stu-id="2ec2b-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2ec2b-126"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2ec2b-126"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2ec2b-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="2ec2b-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2ec2b-128">**\_TerminalServiceSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="2ec2b-128">**Win32\_TerminalServiceSetting**</span></span>](win32-terminalservicesetting.md)
</dt> <dt>

[<span data-ttu-id="2ec2b-129">**AddLSToSpecifiedLicenseServerList**</span><span class="sxs-lookup"><span data-stu-id="2ec2b-129">**AddLSToSpecifiedLicenseServerList**</span></span>](addlstospecifiedlicenseserverlist-win32-terminalservicesetting.md)
</dt> <dt>

[<span data-ttu-id="2ec2b-130">**GetSpecifiedLicenseServerList**</span><span class="sxs-lookup"><span data-stu-id="2ec2b-130">**GetSpecifiedLicenseServerList**</span></span>](getspecifiedlicenseserverlist-win32-terminalservicesetting.md)
</dt> <dt>

[<span data-ttu-id="2ec2b-131">**RemoveLSFromSpecifiedLicenseServerList**</span><span class="sxs-lookup"><span data-stu-id="2ec2b-131">**RemoveLSFromSpecifiedLicenseServerList**</span></span>](removelsfromspecifiedlicenseserverlist-win32-terminalservicesetting.md)
</dt> <dt>

[<span data-ttu-id="2ec2b-132">**SetSpecifiedLicenseServerList**</span><span class="sxs-lookup"><span data-stu-id="2ec2b-132">**SetSpecifiedLicenseServerList**</span></span>](setspecifiedlicenseserverlist-win32-terminalservicesetting.md)
</dt> </dl>

 

 





