---
title: Método SetPrimaryLicenseServer da classe Win32_TerminalServiceSetting
description: Define o servidor de licença fornecido como a primeira entrada na lista de servidores de licença especificados.
ms.assetid: 8921e861-3b9a-49c5-a691-ded7be18ca0a
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método SetPrimaryLicenseServer
- Método SetPrimaryLicenseServer Serviços de Área de Trabalho Remota, classe Win32_TerminalServiceSetting
- Classe Win32_TerminalServiceSetting Serviços de Área de Trabalho Remota, método SetPrimaryLicenseServer
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.SetPrimaryLicenseServer
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 61d73212230d1ca69e0a0809c48b8f2985920045
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824248"
---
# <a name="setprimarylicenseserver-method-of-the-win32_terminalservicesetting-class"></a><span data-ttu-id="d545f-106">Método SetPrimaryLicenseServer da classe Win32 \_ TerminalServiceSetting</span><span class="sxs-lookup"><span data-stu-id="d545f-106">SetPrimaryLicenseServer method of the Win32\_TerminalServiceSetting class</span></span>

<span data-ttu-id="d545f-107">Define o servidor de licença fornecido como a primeira entrada na lista de servidores de licença especificados.</span><span class="sxs-lookup"><span data-stu-id="d545f-107">Sets the given license server as the first entry in the list of specified license servers.</span></span>

## <a name="syntax"></a><span data-ttu-id="d545f-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d545f-108">Syntax</span></span>


```mof
uint32 SetPrimaryLicenseServer(
  [in] string LicenseServerName
);
```



## <a name="parameters"></a><span data-ttu-id="d545f-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d545f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d545f-110">*LicenseServerName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d545f-110">*LicenseServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d545f-111">O nome do servidor de licença.</span><span class="sxs-lookup"><span data-stu-id="d545f-111">The name of the license server.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d545f-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d545f-112">Return value</span></span>

<span data-ttu-id="d545f-113">Retorna 0 em caso de êxito; caso contrário, retorna um código de erro WMI.</span><span class="sxs-lookup"><span data-stu-id="d545f-113">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="d545f-114">Consulte [serviços de área de trabalho remota códigos de erro do provedor WMI](terminal-services-wmi-provider-error-codes.md) para obter uma lista desses valores.</span><span class="sxs-lookup"><span data-stu-id="d545f-114">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="requirements"></a><span data-ttu-id="d545f-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d545f-115">Requirements</span></span>



| <span data-ttu-id="d545f-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="d545f-116">Requirement</span></span> | <span data-ttu-id="d545f-117">Valor</span><span class="sxs-lookup"><span data-stu-id="d545f-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d545f-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d545f-118">Minimum supported client</span></span><br/> | <span data-ttu-id="d545f-119">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="d545f-119">None supported</span></span><br/>                                                               |
| <span data-ttu-id="d545f-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d545f-120">Minimum supported server</span></span><br/> | <span data-ttu-id="d545f-121">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="d545f-121">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="d545f-122">Namespace</span><span class="sxs-lookup"><span data-stu-id="d545f-122">Namespace</span></span><br/>                | <span data-ttu-id="d545f-123">\\TerminalServices da CIMv2 raiz \\</span><span class="sxs-lookup"><span data-stu-id="d545f-123">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="d545f-124">MOF</span><span class="sxs-lookup"><span data-stu-id="d545f-124">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d545f-125"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d545f-125"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="d545f-126">DLL</span><span class="sxs-lookup"><span data-stu-id="d545f-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d545f-127"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d545f-127"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d545f-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="d545f-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d545f-129">**\_TerminalServiceSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="d545f-129">**Win32\_TerminalServiceSetting**</span></span>](win32-terminalservicesetting.md)
</dt> </dl>

 

 





