---
title: Método GetRegisteredLicenseServerList da classe Win32_TerminalServiceSetting
description: Obtém a lista de servidores de licença registrados.
ms.assetid: 32e06b4b-652f-4977-be1f-6d52983d2605
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método GetRegisteredLicenseServerList
- Método GetRegisteredLicenseServerList Serviços de Área de Trabalho Remota, classe Win32_TerminalServiceSetting
- Classe Win32_TerminalServiceSetting Serviços de Área de Trabalho Remota, método GetRegisteredLicenseServerList
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.GetRegisteredLicenseServerList
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5336910956a0d281fbfc8fbc65e1d3b8d5018cb2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105784066"
---
# <a name="getregisteredlicenseserverlist-method-of-the-win32_terminalservicesetting-class"></a><span data-ttu-id="f87ea-106">Método GetRegisteredLicenseServerList da classe Win32 \_ TerminalServiceSetting</span><span class="sxs-lookup"><span data-stu-id="f87ea-106">GetRegisteredLicenseServerList method of the Win32\_TerminalServiceSetting class</span></span>

<span data-ttu-id="f87ea-107">Obtém a lista de servidores de licença registrados.</span><span class="sxs-lookup"><span data-stu-id="f87ea-107">Gets the list of registered license servers.</span></span>

## <a name="syntax"></a><span data-ttu-id="f87ea-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f87ea-108">Syntax</span></span>


```mof
uint32 GetRegisteredLicenseServerList(
  [out] string RegisteredLSList[]
);
```



## <a name="parameters"></a><span data-ttu-id="f87ea-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f87ea-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f87ea-110">*RegisteredLSList* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="f87ea-110">*RegisteredLSList* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f87ea-111">Uma matriz de cadeia de caracteres que recebe a lista de servidores de licença registrados.</span><span class="sxs-lookup"><span data-stu-id="f87ea-111">A string array that receives the list of registered license servers.</span></span> <span data-ttu-id="f87ea-112">Se não houver nenhum servidor de licença registrado, essa matriz estará vazia.</span><span class="sxs-lookup"><span data-stu-id="f87ea-112">If there are no registered license servers, this array will be empty.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f87ea-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f87ea-113">Return value</span></span>

<span data-ttu-id="f87ea-114">Retorna 0 em caso de êxito; caso contrário, retorna um código de erro WMI.</span><span class="sxs-lookup"><span data-stu-id="f87ea-114">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="f87ea-115">Consulte [serviços de área de trabalho remota códigos de erro do provedor WMI](terminal-services-wmi-provider-error-codes.md) para obter uma lista desses valores.</span><span class="sxs-lookup"><span data-stu-id="f87ea-115">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="requirements"></a><span data-ttu-id="f87ea-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f87ea-116">Requirements</span></span>



| <span data-ttu-id="f87ea-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="f87ea-117">Requirement</span></span> | <span data-ttu-id="f87ea-118">Valor</span><span class="sxs-lookup"><span data-stu-id="f87ea-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f87ea-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f87ea-119">Minimum supported client</span></span><br/> | <span data-ttu-id="f87ea-120">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="f87ea-120">None supported</span></span><br/>                                                               |
| <span data-ttu-id="f87ea-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f87ea-121">Minimum supported server</span></span><br/> | <span data-ttu-id="f87ea-122">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="f87ea-122">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="f87ea-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="f87ea-123">Namespace</span></span><br/>                | <span data-ttu-id="f87ea-124">\\TerminalServices da CIMv2 raiz \\</span><span class="sxs-lookup"><span data-stu-id="f87ea-124">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="f87ea-125">MOF</span><span class="sxs-lookup"><span data-stu-id="f87ea-125">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f87ea-126"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f87ea-126"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="f87ea-127">DLL</span><span class="sxs-lookup"><span data-stu-id="f87ea-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f87ea-128"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f87ea-128"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f87ea-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="f87ea-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f87ea-130">**\_TerminalServiceSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="f87ea-130">**Win32\_TerminalServiceSetting**</span></span>](win32-terminalservicesetting.md)
</dt> </dl>

 

 





