---
title: Método GetRedirectableAddresses da classe Win32_TSSessionDirectory
description: Obtém a lista completa de endereços do DNS qualificados.
ms.assetid: 828079e7-472c-4428-97a0-2d5dedcdae91
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método GetRedirectableAddresses
- Método GetRedirectableAddresses Serviços de Área de Trabalho Remota, classe Win32_TSSessionDirectory
- Classe Win32_TSSessionDirectory Serviços de Área de Trabalho Remota, método GetRedirectableAddresses
topic_type:
- apiref
api_name:
- Win32_TSSessionDirectory.GetRedirectableAddresses
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bd5348c11b5f2aba442f7f13ef06488c6d849be3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104008886"
---
# <a name="getredirectableaddresses-method-of-the-win32_tssessiondirectory-class"></a><span data-ttu-id="f12f1-106">Método GetRedirectableAddresses da classe Win32 \_ TSSessionDirectory</span><span class="sxs-lookup"><span data-stu-id="f12f1-106">GetRedirectableAddresses method of the Win32\_TSSessionDirectory class</span></span>

<span data-ttu-id="f12f1-107">Obtém a lista completa de endereços do DNS qualificados.</span><span class="sxs-lookup"><span data-stu-id="f12f1-107">Obtains the entire list of DNS eligible addresses.</span></span>

## <a name="syntax"></a><span data-ttu-id="f12f1-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f12f1-108">Syntax</span></span>


```mof
uint32 GetRedirectableAddresses(
  [in]  uint32 fTokenRedirection,
  [out] string IPAddresses[],
  [out] string AdapterNames[],
  [out] string NetConName[]
);
```



## <a name="parameters"></a><span data-ttu-id="f12f1-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f12f1-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f12f1-110">*fTokenRedirection* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f12f1-110">*fTokenRedirection* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f12f1-111">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f12f1-111">Type: **uint32**</span></span>

<span data-ttu-id="f12f1-112">Um sinalizador que indica se o redirecionamento de token deve ser usado.</span><span class="sxs-lookup"><span data-stu-id="f12f1-112">A flag that indicates whether token redirection should be used.</span></span>

</dd> <dt>

<span data-ttu-id="f12f1-113">*IPAddresses* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="f12f1-113">*IPAddresses* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f12f1-114">Tipo: **cadeia \[ \] de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f12f1-114">Type: **string\[\]**</span></span>

<span data-ttu-id="f12f1-115">A lista completa de endereços IP que estão disponíveis para redirecionamento.</span><span class="sxs-lookup"><span data-stu-id="f12f1-115">The entire list of IP addresses that are available for redirection.</span></span>

</dd> <dt>

<span data-ttu-id="f12f1-116">*Adaptadores* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="f12f1-116">*AdapterNames* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f12f1-117">Tipo: **cadeia \[ \] de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f12f1-117">Type: **string\[\]**</span></span>

<span data-ttu-id="f12f1-118">A lista de nomes de adaptadores de rede que estão associados aos endereços que estão disponíveis para redirecionamento.</span><span class="sxs-lookup"><span data-stu-id="f12f1-118">The list of network adapter names that are associated with the addresses that are available for redirection.</span></span>

</dd> <dt>

<span data-ttu-id="f12f1-119">*NetConName* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="f12f1-119">*NetConName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f12f1-120">Tipo: **cadeia \[ \] de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f12f1-120">Type: **string\[\]**</span></span>

<span data-ttu-id="f12f1-121">A lista de nomes de conexão de rede que estão associados aos endereços que estão disponíveis para redirecionamento.</span><span class="sxs-lookup"><span data-stu-id="f12f1-121">The list of network connection names that are associated with the addresses that are available for redirection.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f12f1-122">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f12f1-122">Return value</span></span>

<span data-ttu-id="f12f1-123">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f12f1-123">Type: **uint32**</span></span>

<span data-ttu-id="f12f1-124">Retorna 0 em caso de êxito; caso contrário, retorna um código de erro WMI.</span><span class="sxs-lookup"><span data-stu-id="f12f1-124">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="f12f1-125">Consulte [serviços de área de trabalho remota códigos de erro do provedor WMI](terminal-services-wmi-provider-error-codes.md) para obter uma lista desses valores.</span><span class="sxs-lookup"><span data-stu-id="f12f1-125">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="remarks"></a><span data-ttu-id="f12f1-126">Comentários</span><span class="sxs-lookup"><span data-stu-id="f12f1-126">Remarks</span></span>

<span data-ttu-id="f12f1-127">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="f12f1-127">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="f12f1-128">Os arquivos MOF não são instalados como parte do SDK (Software Development Kit) do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="f12f1-128">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="f12f1-129">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="f12f1-129">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="f12f1-130">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="f12f1-130">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="f12f1-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f12f1-131">Requirements</span></span>



| <span data-ttu-id="f12f1-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="f12f1-132">Requirement</span></span> | <span data-ttu-id="f12f1-133">Valor</span><span class="sxs-lookup"><span data-stu-id="f12f1-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f12f1-134">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f12f1-134">Minimum supported client</span></span><br/> | <span data-ttu-id="f12f1-135">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="f12f1-135">None supported</span></span><br/>                                                               |
| <span data-ttu-id="f12f1-136">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f12f1-136">Minimum supported server</span></span><br/> | <span data-ttu-id="f12f1-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f12f1-137">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f12f1-138">Namespace</span><span class="sxs-lookup"><span data-stu-id="f12f1-138">Namespace</span></span><br/>                | <span data-ttu-id="f12f1-139">\\TerminalServices da CIMv2 raiz \\</span><span class="sxs-lookup"><span data-stu-id="f12f1-139">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="f12f1-140">MOF</span><span class="sxs-lookup"><span data-stu-id="f12f1-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f12f1-141"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f12f1-141"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="f12f1-142">DLL</span><span class="sxs-lookup"><span data-stu-id="f12f1-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f12f1-143"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f12f1-143"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f12f1-144">Confira também</span><span class="sxs-lookup"><span data-stu-id="f12f1-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f12f1-145">**\_TSSessionDirectory Win32**</span><span class="sxs-lookup"><span data-stu-id="f12f1-145">**Win32\_TSSessionDirectory**</span></span>](win32-tssessiondirectory.md)
</dt> </dl>

 

