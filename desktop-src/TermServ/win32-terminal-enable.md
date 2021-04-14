---
title: Método Enable da classe Win32_Terminal
description: O método Enable desabilita ou habilita o terminal.
ms.assetid: f249563b-6fa0-413c-9fc7-01dd16d5c561
ms.tgt_platform: multiple
keywords:
- Habilitar método Serviços de Área de Trabalho Remota
- Habilitar método Serviços de Área de Trabalho Remota, classe Win32_Terminal
- Classe Win32_Terminal Serviços de Área de Trabalho Remota, método Enable
topic_type:
- apiref
api_name:
- Win32_Terminal.Enable
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: afedef572c65f249c48da850172bb9fc4d222c19
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369360"
---
# <a name="enable-method-of-the-win32_terminal-class"></a><span data-ttu-id="71dfb-106">Habilitar o método da \_ classe terminal do Win32</span><span class="sxs-lookup"><span data-stu-id="71dfb-106">Enable method of the Win32\_Terminal class</span></span>

<span data-ttu-id="71dfb-107">O método **Enable** desabilita ou habilita o terminal.</span><span class="sxs-lookup"><span data-stu-id="71dfb-107">The **Enable** method disables or enables the terminal.</span></span>

## <a name="syntax"></a><span data-ttu-id="71dfb-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="71dfb-108">Syntax</span></span>


```mof
uint32 Enable(
  [in] uint32 fEnableTerminal
);
```



## <a name="parameters"></a><span data-ttu-id="71dfb-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="71dfb-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="71dfb-110">*fEnableTerminal* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="71dfb-110">*fEnableTerminal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="71dfb-111">Sinalizador que desabilita ou habilita o terminal.</span><span class="sxs-lookup"><span data-stu-id="71dfb-111">Flag that disables or enables the terminal.</span></span>

<dt>

<span id="0"></span>

<span data-ttu-id="71dfb-112"><span id="0"></span>**0**</span><span class="sxs-lookup"><span data-stu-id="71dfb-112"><span id="0"></span>**0**</span></span>


</dt> <dd>

<span data-ttu-id="71dfb-113">O terminal está desabilitado.</span><span class="sxs-lookup"><span data-stu-id="71dfb-113">The terminal is disabled.</span></span>

</dd> <dt>

<span id="1"></span>

<span data-ttu-id="71dfb-114"><span id="1"></span>**1**</span><span class="sxs-lookup"><span data-stu-id="71dfb-114"><span id="1"></span>**1**</span></span>


</dt> <dd>

<span data-ttu-id="71dfb-115">O terminal está habilitado.</span><span class="sxs-lookup"><span data-stu-id="71dfb-115">The terminal is enabled.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="71dfb-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="71dfb-116">Return value</span></span>

<span data-ttu-id="71dfb-117">Retorna 0 em caso de êxito; caso contrário, retorna um código de erro WMI.</span><span class="sxs-lookup"><span data-stu-id="71dfb-117">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="71dfb-118">Consulte [serviços de área de trabalho remota códigos de erro do provedor WMI](terminal-services-wmi-provider-error-codes.md) para obter uma lista desses valores.</span><span class="sxs-lookup"><span data-stu-id="71dfb-118">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="remarks"></a><span data-ttu-id="71dfb-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="71dfb-119">Remarks</span></span>

<span data-ttu-id="71dfb-120">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="71dfb-120">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="71dfb-121">Os arquivos MOF não são instalados como parte do SDK (Software Development Kit) do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="71dfb-121">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="71dfb-122">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="71dfb-122">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="71dfb-123">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="71dfb-123">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="71dfb-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="71dfb-124">Requirements</span></span>



| <span data-ttu-id="71dfb-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="71dfb-125">Requirement</span></span> | <span data-ttu-id="71dfb-126">Valor</span><span class="sxs-lookup"><span data-stu-id="71dfb-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="71dfb-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="71dfb-127">Minimum supported client</span></span><br/> | <span data-ttu-id="71dfb-128">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="71dfb-128">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="71dfb-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="71dfb-129">Minimum supported server</span></span><br/> | <span data-ttu-id="71dfb-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="71dfb-130">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="71dfb-131">Namespace</span><span class="sxs-lookup"><span data-stu-id="71dfb-131">Namespace</span></span><br/>                | <span data-ttu-id="71dfb-132">\\TerminalServices da CIMv2 raiz \\</span><span class="sxs-lookup"><span data-stu-id="71dfb-132">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="71dfb-133">MOF</span><span class="sxs-lookup"><span data-stu-id="71dfb-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="71dfb-134"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="71dfb-134"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="71dfb-135">DLL</span><span class="sxs-lookup"><span data-stu-id="71dfb-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="71dfb-136"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="71dfb-136"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="71dfb-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="71dfb-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="71dfb-138">**Terminal do Win32 \_**</span><span class="sxs-lookup"><span data-stu-id="71dfb-138">**Win32\_Terminal**</span></span>](win32-terminal.md)
</dt> </dl>

 

