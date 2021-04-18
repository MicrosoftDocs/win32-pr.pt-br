---
title: Método SetSpecifiedLicenseServerList da classe Win32_TerminalServiceSetting
description: Atualiza a lista de servidores de licença especificados, substituindo quaisquer servidores de licença especificados existentes.
ms.assetid: afd7ca11-9db5-4cf3-9706-3c6984789ecd
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método SetSpecifiedLicenseServerList
- Método SetSpecifiedLicenseServerList Serviços de Área de Trabalho Remota, classe Win32_TerminalServiceSetting
- Classe Win32_TerminalServiceSetting Serviços de Área de Trabalho Remota, método SetSpecifiedLicenseServerList
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.SetSpecifiedLicenseServerList
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d10fde34e490f26c287e63dcddae3c62761670bc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105784060"
---
# <a name="setspecifiedlicenseserverlist-method-of-the-win32_terminalservicesetting-class"></a><span data-ttu-id="540f2-106">Método SetSpecifiedLicenseServerList da classe Win32 \_ TerminalServiceSetting</span><span class="sxs-lookup"><span data-stu-id="540f2-106">SetSpecifiedLicenseServerList method of the Win32\_TerminalServiceSetting class</span></span>

<span data-ttu-id="540f2-107">Atualiza a lista de servidores de licença especificados, substituindo quaisquer servidores de licença especificados existentes.</span><span class="sxs-lookup"><span data-stu-id="540f2-107">Updates the list of specified license servers, replacing any existing specified license servers.</span></span>

## <a name="syntax"></a><span data-ttu-id="540f2-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="540f2-108">Syntax</span></span>


```mof
uint32 SetSpecifiedLicenseServerList(
  [in] string SpecifiedLSList[]
);
```



## <a name="parameters"></a><span data-ttu-id="540f2-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="540f2-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="540f2-110">*SpecifiedLSList* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="540f2-110">*SpecifiedLSList* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="540f2-111">Uma matriz de cadeia de caracteres que contém a nova lista de servidores de licença especificados.</span><span class="sxs-lookup"><span data-stu-id="540f2-111">A string array that contains the new list of specified license servers.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="540f2-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="540f2-112">Return value</span></span>

<span data-ttu-id="540f2-113">Retorna 0 em caso de êxito; caso contrário, retorna um código de erro WMI.</span><span class="sxs-lookup"><span data-stu-id="540f2-113">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="540f2-114">Consulte [serviços de área de trabalho remota códigos de erro do provedor WMI](terminal-services-wmi-provider-error-codes.md) para obter uma lista desses valores.</span><span class="sxs-lookup"><span data-stu-id="540f2-114">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="requirements"></a><span data-ttu-id="540f2-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="540f2-115">Requirements</span></span>



| <span data-ttu-id="540f2-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="540f2-116">Requirement</span></span> | <span data-ttu-id="540f2-117">Valor</span><span class="sxs-lookup"><span data-stu-id="540f2-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="540f2-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="540f2-118">Minimum supported client</span></span><br/> | <span data-ttu-id="540f2-119">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="540f2-119">None supported</span></span><br/>                                                               |
| <span data-ttu-id="540f2-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="540f2-120">Minimum supported server</span></span><br/> | <span data-ttu-id="540f2-121">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="540f2-121">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="540f2-122">Namespace</span><span class="sxs-lookup"><span data-stu-id="540f2-122">Namespace</span></span><br/>                | <span data-ttu-id="540f2-123">\\TerminalServices da CIMv2 raiz \\</span><span class="sxs-lookup"><span data-stu-id="540f2-123">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="540f2-124">MOF</span><span class="sxs-lookup"><span data-stu-id="540f2-124">MOF</span></span><br/>                      | <dl> <span data-ttu-id="540f2-125"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="540f2-125"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="540f2-126">DLL</span><span class="sxs-lookup"><span data-stu-id="540f2-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="540f2-127"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="540f2-127"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="540f2-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="540f2-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="540f2-129">**\_TerminalServiceSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="540f2-129">**Win32\_TerminalServiceSetting**</span></span>](win32-terminalservicesetting.md)
</dt> <dt>

[<span data-ttu-id="540f2-130">**AddLSToSpecifiedLicenseServerList**</span><span class="sxs-lookup"><span data-stu-id="540f2-130">**AddLSToSpecifiedLicenseServerList**</span></span>](addlstospecifiedlicenseserverlist-win32-terminalservicesetting.md)
</dt> <dt>

[<span data-ttu-id="540f2-131">**GetSpecifiedLicenseServerList**</span><span class="sxs-lookup"><span data-stu-id="540f2-131">**GetSpecifiedLicenseServerList**</span></span>](getspecifiedlicenseserverlist-win32-terminalservicesetting.md)
</dt> <dt>

[<span data-ttu-id="540f2-132">**EmptySpecifiedLicenseServerList**</span><span class="sxs-lookup"><span data-stu-id="540f2-132">**EmptySpecifiedLicenseServerList**</span></span>](emptyspecifiedlicenseserverlist-win32-terminalservicesetting.md)
</dt> <dt>

[<span data-ttu-id="540f2-133">**RemoveLSFromSpecifiedLicenseServerList**</span><span class="sxs-lookup"><span data-stu-id="540f2-133">**RemoveLSFromSpecifiedLicenseServerList**</span></span>](removelsfromspecifiedlicenseserverlist-win32-terminalservicesetting.md)
</dt> </dl>

 

 





