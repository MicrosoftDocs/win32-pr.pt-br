---
title: Método RemoveLSFromSpecifiedLicenseServerList da classe Win32_TerminalServiceSetting
description: Remove o servidor de licença fornecido da lista de servidores de licença especificados.
ms.assetid: c25eebf9-3a21-41a0-bb7d-c3f909cd8087
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método RemoveLSFromSpecifiedLicenseServerList
- Método RemoveLSFromSpecifiedLicenseServerList Serviços de Área de Trabalho Remota, classe Win32_TerminalServiceSetting
- Classe Win32_TerminalServiceSetting Serviços de Área de Trabalho Remota, método RemoveLSFromSpecifiedLicenseServerList
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.RemoveLSFromSpecifiedLicenseServerList
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 901c2676748e819290855df2de51e5d7936dc793
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824414"
---
# <a name="removelsfromspecifiedlicenseserverlist-method-of-the-win32_terminalservicesetting-class"></a><span data-ttu-id="bb36d-106">Método RemoveLSFromSpecifiedLicenseServerList da classe Win32 \_ TerminalServiceSetting</span><span class="sxs-lookup"><span data-stu-id="bb36d-106">RemoveLSFromSpecifiedLicenseServerList method of the Win32\_TerminalServiceSetting class</span></span>

<span data-ttu-id="bb36d-107">Remove o servidor de licença fornecido da lista de servidores de licença especificados.</span><span class="sxs-lookup"><span data-stu-id="bb36d-107">Removes the given license server from the list of specified license servers.</span></span>

## <a name="syntax"></a><span data-ttu-id="bb36d-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="bb36d-108">Syntax</span></span>


```mof
uint32 RemoveLSFromSpecifiedLicenseServerList(
  [in] string LicenseServerName
);
```



## <a name="parameters"></a><span data-ttu-id="bb36d-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="bb36d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bb36d-110">*LicenseServerName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="bb36d-110">*LicenseServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bb36d-111">O nome do servidor de licença a ser removido.</span><span class="sxs-lookup"><span data-stu-id="bb36d-111">The name of the license server to remove.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bb36d-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="bb36d-112">Return value</span></span>

<span data-ttu-id="bb36d-113">Retorna 0 em caso de êxito; caso contrário, retorna um código de erro WMI.</span><span class="sxs-lookup"><span data-stu-id="bb36d-113">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="bb36d-114">Consulte [serviços de área de trabalho remota códigos de erro do provedor WMI](terminal-services-wmi-provider-error-codes.md) para obter uma lista desses valores.</span><span class="sxs-lookup"><span data-stu-id="bb36d-114">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="requirements"></a><span data-ttu-id="bb36d-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bb36d-115">Requirements</span></span>



| <span data-ttu-id="bb36d-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="bb36d-116">Requirement</span></span> | <span data-ttu-id="bb36d-117">Valor</span><span class="sxs-lookup"><span data-stu-id="bb36d-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bb36d-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bb36d-118">Minimum supported client</span></span><br/> | <span data-ttu-id="bb36d-119">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="bb36d-119">None supported</span></span><br/>                                                               |
| <span data-ttu-id="bb36d-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bb36d-120">Minimum supported server</span></span><br/> | <span data-ttu-id="bb36d-121">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="bb36d-121">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="bb36d-122">Namespace</span><span class="sxs-lookup"><span data-stu-id="bb36d-122">Namespace</span></span><br/>                | <span data-ttu-id="bb36d-123">\\TerminalServices da CIMv2 raiz \\</span><span class="sxs-lookup"><span data-stu-id="bb36d-123">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="bb36d-124">MOF</span><span class="sxs-lookup"><span data-stu-id="bb36d-124">MOF</span></span><br/>                      | <dl> <span data-ttu-id="bb36d-125"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="bb36d-125"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="bb36d-126">DLL</span><span class="sxs-lookup"><span data-stu-id="bb36d-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bb36d-127"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bb36d-127"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bb36d-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="bb36d-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bb36d-129">**\_TerminalServiceSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="bb36d-129">**Win32\_TerminalServiceSetting**</span></span>](win32-terminalservicesetting.md)
</dt> <dt>

[<span data-ttu-id="bb36d-130">**AddLSToSpecifiedLicenseServerList**</span><span class="sxs-lookup"><span data-stu-id="bb36d-130">**AddLSToSpecifiedLicenseServerList**</span></span>](addlstospecifiedlicenseserverlist-win32-terminalservicesetting.md)
</dt> <dt>

[<span data-ttu-id="bb36d-131">**EmptySpecifiedLicenseServerList**</span><span class="sxs-lookup"><span data-stu-id="bb36d-131">**EmptySpecifiedLicenseServerList**</span></span>](emptyspecifiedlicenseserverlist-win32-terminalservicesetting.md)
</dt> <dt>

[<span data-ttu-id="bb36d-132">**GetSpecifiedLicenseServerList**</span><span class="sxs-lookup"><span data-stu-id="bb36d-132">**GetSpecifiedLicenseServerList**</span></span>](getspecifiedlicenseserverlist-win32-terminalservicesetting.md)
</dt> <dt>

[<span data-ttu-id="bb36d-133">**SetSpecifiedLicenseServerList**</span><span class="sxs-lookup"><span data-stu-id="bb36d-133">**SetSpecifiedLicenseServerList**</span></span>](setspecifiedlicenseserverlist-win32-terminalservicesetting.md)
</dt> </dl>

 

 





