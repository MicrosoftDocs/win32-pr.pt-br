---
title: Método GetSpecifiedLicenseServerList da classe Win32_TerminalServiceSetting
description: Recupera a lista de servidores de licença especificados.
ms.assetid: 800be0ce-1002-48e1-be4e-88db22590f12
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método GetSpecifiedLicenseServerList
- Método GetSpecifiedLicenseServerList Serviços de Área de Trabalho Remota, classe Win32_TerminalServiceSetting
- Classe Win32_TerminalServiceSetting Serviços de Área de Trabalho Remota, método GetSpecifiedLicenseServerList
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.GetSpecifiedLicenseServerList
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f70c50281cad7072d420082db0e6916a631e2b1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369311"
---
# <a name="getspecifiedlicenseserverlist-method-of-the-win32_terminalservicesetting-class"></a><span data-ttu-id="6c9d7-106">Método GetSpecifiedLicenseServerList da classe Win32 \_ TerminalServiceSetting</span><span class="sxs-lookup"><span data-stu-id="6c9d7-106">GetSpecifiedLicenseServerList method of the Win32\_TerminalServiceSetting class</span></span>

<span data-ttu-id="6c9d7-107">Recupera a lista de servidores de licença especificados.</span><span class="sxs-lookup"><span data-stu-id="6c9d7-107">Retrieves the list of specified license servers.</span></span>

## <a name="syntax"></a><span data-ttu-id="6c9d7-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6c9d7-108">Syntax</span></span>


```mof
uint32 GetSpecifiedLicenseServerList(
  [out] string SpecifiedLSList[]
);
```



## <a name="parameters"></a><span data-ttu-id="6c9d7-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6c9d7-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6c9d7-110">*SpecifiedLSList* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="6c9d7-110">*SpecifiedLSList* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6c9d7-111">Uma matriz de cadeia de caracteres que recebe a lista de servidores de licença.</span><span class="sxs-lookup"><span data-stu-id="6c9d7-111">A string array that receives the list of license servers.</span></span> <span data-ttu-id="6c9d7-112">Se não houver servidores de licença, essa matriz estará vazia.</span><span class="sxs-lookup"><span data-stu-id="6c9d7-112">If there are no license servers, this array will be empty.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6c9d7-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6c9d7-113">Return value</span></span>

<span data-ttu-id="6c9d7-114">Retorna 0 em caso de êxito; caso contrário, retorna um código de erro WMI.</span><span class="sxs-lookup"><span data-stu-id="6c9d7-114">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="6c9d7-115">Consulte [serviços de área de trabalho remota códigos de erro do provedor WMI](terminal-services-wmi-provider-error-codes.md) para obter uma lista desses valores.</span><span class="sxs-lookup"><span data-stu-id="6c9d7-115">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="requirements"></a><span data-ttu-id="6c9d7-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6c9d7-116">Requirements</span></span>



| <span data-ttu-id="6c9d7-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="6c9d7-117">Requirement</span></span> | <span data-ttu-id="6c9d7-118">Valor</span><span class="sxs-lookup"><span data-stu-id="6c9d7-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6c9d7-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6c9d7-119">Minimum supported client</span></span><br/> | <span data-ttu-id="6c9d7-120">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="6c9d7-120">None supported</span></span><br/>                                                               |
| <span data-ttu-id="6c9d7-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6c9d7-121">Minimum supported server</span></span><br/> | <span data-ttu-id="6c9d7-122">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="6c9d7-122">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="6c9d7-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="6c9d7-123">Namespace</span></span><br/>                | <span data-ttu-id="6c9d7-124">\\TerminalServices da CIMv2 raiz \\</span><span class="sxs-lookup"><span data-stu-id="6c9d7-124">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="6c9d7-125">MOF</span><span class="sxs-lookup"><span data-stu-id="6c9d7-125">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6c9d7-126"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6c9d7-126"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="6c9d7-127">DLL</span><span class="sxs-lookup"><span data-stu-id="6c9d7-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6c9d7-128"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6c9d7-128"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6c9d7-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="6c9d7-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6c9d7-130">**\_TerminalServiceSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="6c9d7-130">**Win32\_TerminalServiceSetting**</span></span>](win32-terminalservicesetting.md)
</dt> <dt>

[<span data-ttu-id="6c9d7-131">**AddLSToSpecifiedLicenseServerList**</span><span class="sxs-lookup"><span data-stu-id="6c9d7-131">**AddLSToSpecifiedLicenseServerList**</span></span>](addlstospecifiedlicenseserverlist-win32-terminalservicesetting.md)
</dt> <dt>

[<span data-ttu-id="6c9d7-132">**EmptySpecifiedLicenseServerList**</span><span class="sxs-lookup"><span data-stu-id="6c9d7-132">**EmptySpecifiedLicenseServerList**</span></span>](emptyspecifiedlicenseserverlist-win32-terminalservicesetting.md)
</dt> <dt>

[<span data-ttu-id="6c9d7-133">**RemoveLSFromSpecifiedLicenseServerList**</span><span class="sxs-lookup"><span data-stu-id="6c9d7-133">**RemoveLSFromSpecifiedLicenseServerList**</span></span>](removelsfromspecifiedlicenseserverlist-win32-terminalservicesetting.md)
</dt> <dt>

[<span data-ttu-id="6c9d7-134">**SetSpecifiedLicenseServerList**</span><span class="sxs-lookup"><span data-stu-id="6c9d7-134">**SetSpecifiedLicenseServerList**</span></span>](setspecifiedlicenseserverlist-win32-terminalservicesetting.md)
</dt> </dl>

 

 





