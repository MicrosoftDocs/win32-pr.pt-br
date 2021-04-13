---
title: Método GetCurrentRedirectableAddresses da classe Win32_TSSessionDirectory
description: Obtém a lista atualmente configurada de endereços DNS qualificados que podem ser usados para redirecionamento.
ms.assetid: 79f35d8f-b5f9-4b0f-bb7d-0d1ee3f02346
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método GetCurrentRedirectableAddresses
- Método GetCurrentRedirectableAddresses Serviços de Área de Trabalho Remota, classe Win32_TSSessionDirectory
- Classe Win32_TSSessionDirectory Serviços de Área de Trabalho Remota, método GetCurrentRedirectableAddresses
topic_type:
- apiref
api_name:
- Win32_TSSessionDirectory.GetCurrentRedirectableAddresses
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e6b4a859c77f449fb5a8f436be6e18c058ca59f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455872"
---
# <a name="getcurrentredirectableaddresses-method-of-the-win32_tssessiondirectory-class"></a><span data-ttu-id="42892-106">Método GetCurrentRedirectableAddresses da classe Win32 \_ TSSessionDirectory</span><span class="sxs-lookup"><span data-stu-id="42892-106">GetCurrentRedirectableAddresses method of the Win32\_TSSessionDirectory class</span></span>

<span data-ttu-id="42892-107">Obtém a lista atualmente configurada de endereços DNS qualificados que podem ser usados para redirecionamento.</span><span class="sxs-lookup"><span data-stu-id="42892-107">Obtains the currently configured list of DNS eligible addresses that can be used for redirection.</span></span>

## <a name="syntax"></a><span data-ttu-id="42892-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="42892-108">Syntax</span></span>


```mof
uint32 GetCurrentRedirectableAddresses(
  [out] uint32 fTokenRedirection,
  [out] string IPAddresses[]
);
```



## <a name="parameters"></a><span data-ttu-id="42892-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="42892-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="42892-110">*fTokenRedirection* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="42892-110">*fTokenRedirection* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="42892-111">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="42892-111">Type: **uint32**</span></span>

<span data-ttu-id="42892-112">Um sinalizador que indica se o redirecionamento de token deve ser usado.</span><span class="sxs-lookup"><span data-stu-id="42892-112">A flag that indicates whether token redirection should be used.</span></span>

</dd> <dt>

<span data-ttu-id="42892-113">*IPAddresses* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="42892-113">*IPAddresses* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="42892-114">Tipo: **cadeia \[ \] de caracteres**</span><span class="sxs-lookup"><span data-stu-id="42892-114">Type: **string\[\]**</span></span>

<span data-ttu-id="42892-115">Uma matriz dos endereços IP qualificados do DNS atualmente configurados que podem ser usados para redirecionamento.</span><span class="sxs-lookup"><span data-stu-id="42892-115">An array of the currently configured DNS eligible IP addresses that can be used for redirection.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="42892-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="42892-116">Return value</span></span>

<span data-ttu-id="42892-117">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="42892-117">Type: **uint32**</span></span>

<span data-ttu-id="42892-118">Retorna 0 em caso de êxito; caso contrário, retorna um código de erro WMI.</span><span class="sxs-lookup"><span data-stu-id="42892-118">Returns 0 on success; otherwise, returns a WMI error code.</span></span> <span data-ttu-id="42892-119">Consulte [serviços de área de trabalho remota códigos de erro do provedor WMI](terminal-services-wmi-provider-error-codes.md) para obter uma lista desses valores.</span><span class="sxs-lookup"><span data-stu-id="42892-119">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="remarks"></a><span data-ttu-id="42892-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="42892-120">Remarks</span></span>

<span data-ttu-id="42892-121">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="42892-121">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="42892-122">Os arquivos MOF não são instalados como parte do SDK (Software Development Kit) do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="42892-122">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="42892-123">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="42892-123">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="42892-124">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="42892-124">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="42892-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="42892-125">Requirements</span></span>



| <span data-ttu-id="42892-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="42892-126">Requirement</span></span> | <span data-ttu-id="42892-127">Valor</span><span class="sxs-lookup"><span data-stu-id="42892-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="42892-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="42892-128">Minimum supported client</span></span><br/> | <span data-ttu-id="42892-129">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="42892-129">None supported</span></span><br/>                                                               |
| <span data-ttu-id="42892-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="42892-130">Minimum supported server</span></span><br/> | <span data-ttu-id="42892-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="42892-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="42892-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="42892-132">Namespace</span></span><br/>                | <span data-ttu-id="42892-133">\\TerminalServices da CIMv2 raiz \\</span><span class="sxs-lookup"><span data-stu-id="42892-133">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="42892-134">MOF</span><span class="sxs-lookup"><span data-stu-id="42892-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="42892-135"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="42892-135"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="42892-136">DLL</span><span class="sxs-lookup"><span data-stu-id="42892-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="42892-137"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="42892-137"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="42892-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="42892-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="42892-139">**\_TSSessionDirectory Win32**</span><span class="sxs-lookup"><span data-stu-id="42892-139">**Win32\_TSSessionDirectory**</span></span>](win32-tssessiondirectory.md)
</dt> </dl>

 

