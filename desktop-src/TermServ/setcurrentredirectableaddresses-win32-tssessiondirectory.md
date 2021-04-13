---
title: Método SetCurrentRedirectableAddresses da classe Win32_TSSessionDirectory
description: Define a lista configurada de endereços DNS qualificados que podem ser usados para redirecionamento.
ms.assetid: cad6a8a8-fdf1-406e-abeb-37acb396ac16
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método SetCurrentRedirectableAddresses
- Método SetCurrentRedirectableAddresses Serviços de Área de Trabalho Remota, classe Win32_TSSessionDirectory
- Classe Win32_TSSessionDirectory Serviços de Área de Trabalho Remota, método SetCurrentRedirectableAddresses
topic_type:
- apiref
api_name:
- Win32_TSSessionDirectory.SetCurrentRedirectableAddresses
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f43e70f8d108e908155b5db3e6800f4be26811c5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369771"
---
# <a name="setcurrentredirectableaddresses-method-of-the-win32_tssessiondirectory-class"></a><span data-ttu-id="636d2-106">Método SetCurrentRedirectableAddresses da classe Win32 \_ TSSessionDirectory</span><span class="sxs-lookup"><span data-stu-id="636d2-106">SetCurrentRedirectableAddresses method of the Win32\_TSSessionDirectory class</span></span>

<span data-ttu-id="636d2-107">O método **SetCurrentRedirectableAddresses** define a lista configurada de endereços DNS qualificados que podem ser usados para redirecionamento.</span><span class="sxs-lookup"><span data-stu-id="636d2-107">The **SetCurrentRedirectableAddresses** method sets the configured list of DNS eligible addresses that can be used for redirection.</span></span>

## <a name="syntax"></a><span data-ttu-id="636d2-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="636d2-108">Syntax</span></span>


```mof
uint32 SetCurrentRedirectableAddresses(
  [in] uint32 fTokenRedirection,
  [in] string IPAddresses[]
);
```



## <a name="parameters"></a><span data-ttu-id="636d2-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="636d2-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="636d2-110">*fTokenRedirection* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="636d2-110">*fTokenRedirection* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="636d2-111">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="636d2-111">Type: **uint32**</span></span>

<span data-ttu-id="636d2-112">Um sinalizador que indica se o redirecionamento de token deve ser usado.</span><span class="sxs-lookup"><span data-stu-id="636d2-112">A flag that indicates whether token redirection should be used.</span></span>

</dd> <dt>

<span data-ttu-id="636d2-113">*IPAddresses* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="636d2-113">*IPAddresses* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="636d2-114">Tipo: **cadeia \[ \] de caracteres**</span><span class="sxs-lookup"><span data-stu-id="636d2-114">Type: **string\[\]**</span></span>

<span data-ttu-id="636d2-115">Uma matriz de cadeias de caracteres que representa a lista de endereços IP qualificados do DNS que podem ser usados para redirecionamento.</span><span class="sxs-lookup"><span data-stu-id="636d2-115">An array of strings that represents the list of DNS eligible IP addresses that can be used for redirection.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="636d2-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="636d2-116">Return value</span></span>

<span data-ttu-id="636d2-117">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="636d2-117">Type: **uint32**</span></span>

<span data-ttu-id="636d2-118">Retorna 0 em caso de êxito; caso contrário, retorna um código de erro WMI.</span><span class="sxs-lookup"><span data-stu-id="636d2-118">Returns 0 on success; otherwise, returns a WMI error code.</span></span> <span data-ttu-id="636d2-119">Consulte [serviços de área de trabalho remota códigos de erro do provedor WMI](terminal-services-wmi-provider-error-codes.md) para obter uma lista desses valores.</span><span class="sxs-lookup"><span data-stu-id="636d2-119">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="remarks"></a><span data-ttu-id="636d2-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="636d2-120">Remarks</span></span>

<span data-ttu-id="636d2-121">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="636d2-121">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="636d2-122">Os arquivos MOF não são instalados como parte do SDK (Software Development Kit) do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="636d2-122">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="636d2-123">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="636d2-123">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="636d2-124">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="636d2-124">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="636d2-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="636d2-125">Requirements</span></span>



| <span data-ttu-id="636d2-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="636d2-126">Requirement</span></span> | <span data-ttu-id="636d2-127">Valor</span><span class="sxs-lookup"><span data-stu-id="636d2-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="636d2-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="636d2-128">Minimum supported client</span></span><br/> | <span data-ttu-id="636d2-129">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="636d2-129">None supported</span></span><br/>                                                               |
| <span data-ttu-id="636d2-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="636d2-130">Minimum supported server</span></span><br/> | <span data-ttu-id="636d2-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="636d2-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="636d2-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="636d2-132">Namespace</span></span><br/>                | <span data-ttu-id="636d2-133">\\TerminalServices da CIMv2 raiz \\</span><span class="sxs-lookup"><span data-stu-id="636d2-133">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="636d2-134">MOF</span><span class="sxs-lookup"><span data-stu-id="636d2-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="636d2-135"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="636d2-135"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="636d2-136">DLL</span><span class="sxs-lookup"><span data-stu-id="636d2-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="636d2-137"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="636d2-137"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="636d2-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="636d2-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="636d2-139">**\_TSSessionDirectory Win32**</span><span class="sxs-lookup"><span data-stu-id="636d2-139">**Win32\_TSSessionDirectory**</span></span>](win32-tssessiondirectory.md)
</dt> </dl>

 

