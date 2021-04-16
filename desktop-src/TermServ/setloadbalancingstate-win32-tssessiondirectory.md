---
title: Método SetLoadBalancingState da classe Win32_TSSessionDirectory
description: Define o valor para indicar se o servidor participará do balanceamento de carga do agente de Conexão de Área de Trabalho Remota (agente de conexão RD).
ms.assetid: 6368043c-1808-4757-9756-10b3800190b0
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método SetLoadBalancingState
- Método SetLoadBalancingState Serviços de Área de Trabalho Remota, classe Win32_TSSessionDirectory
- Classe Win32_TSSessionDirectory Serviços de Área de Trabalho Remota, método SetLoadBalancingState
topic_type:
- apiref
api_name:
- Win32_TSSessionDirectory.SetLoadBalancingState
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 88142f5a9c87b4af2688e06d2766ac38d7e234c0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105758092"
---
# <a name="setloadbalancingstate-method-of-the-win32_tssessiondirectory-class"></a><span data-ttu-id="e0e0c-106">Método SetLoadBalancingState da classe Win32 \_ TSSessionDirectory</span><span class="sxs-lookup"><span data-stu-id="e0e0c-106">SetLoadBalancingState method of the Win32\_TSSessionDirectory class</span></span>

<span data-ttu-id="e0e0c-107">Define o valor para indicar se o servidor participará do balanceamento de carga do agente de Conexão de Área de Trabalho Remota (agente de conexão RD).</span><span class="sxs-lookup"><span data-stu-id="e0e0c-107">Sets the value to indicate whether the server will participate in Remote Desktop Connection Broker (RD Connection Broker) load balancing.</span></span>

## <a name="syntax"></a><span data-ttu-id="e0e0c-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e0e0c-108">Syntax</span></span>


```mof
uint32 SetLoadBalancingState(
  [in] uint32 StateValue
);
```



## <a name="parameters"></a><span data-ttu-id="e0e0c-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e0e0c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e0e0c-110">*Estadovalue* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e0e0c-110">*StateValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e0e0c-111">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e0e0c-111">Type: **uint32**</span></span>

<span data-ttu-id="e0e0c-112">Indica se o servidor participará do balanceamento de carga do agente de conexão RD.</span><span class="sxs-lookup"><span data-stu-id="e0e0c-112">Indicates whether the server will participate in RD Connection Broker load balancing.</span></span>

<dt>

<span data-ttu-id="e0e0c-113">0</span><span class="sxs-lookup"><span data-stu-id="e0e0c-113">0</span></span>
</dt> <dd>

<span data-ttu-id="e0e0c-114">O servidor não participará do balanceamento de carga do agente de conexão de área de trabalho remota.</span><span class="sxs-lookup"><span data-stu-id="e0e0c-114">The server will not participate in RD Connection Broker load balancing.</span></span>

</dd> <dt>

<span data-ttu-id="e0e0c-115">1</span><span class="sxs-lookup"><span data-stu-id="e0e0c-115">1</span></span>
</dt> <dd>

<span data-ttu-id="e0e0c-116">O servidor participará do balanceamento de carga do agente de conexão RD.</span><span class="sxs-lookup"><span data-stu-id="e0e0c-116">The server will participate in RD Connection Broker load balancing.</span></span>

</dd> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e0e0c-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="e0e0c-117">Remarks</span></span>

<span data-ttu-id="e0e0c-118">O servidor deve ser Unido a um farm no agente de conexão RD.</span><span class="sxs-lookup"><span data-stu-id="e0e0c-118">The server must be joined to a farm in RD Connection Broker.</span></span>

<span data-ttu-id="e0e0c-119">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="e0e0c-119">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="e0e0c-120">Os arquivos MOF não são instalados como parte do SDK (Software Development Kit) do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="e0e0c-120">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="e0e0c-121">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="e0e0c-121">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="e0e0c-122">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="e0e0c-122">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="e0e0c-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e0e0c-123">Requirements</span></span>



| <span data-ttu-id="e0e0c-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="e0e0c-124">Requirement</span></span> | <span data-ttu-id="e0e0c-125">Valor</span><span class="sxs-lookup"><span data-stu-id="e0e0c-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e0e0c-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e0e0c-126">Minimum supported client</span></span><br/> | <span data-ttu-id="e0e0c-127">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="e0e0c-127">None supported</span></span><br/>                                                               |
| <span data-ttu-id="e0e0c-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e0e0c-128">Minimum supported server</span></span><br/> | <span data-ttu-id="e0e0c-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e0e0c-129">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="e0e0c-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="e0e0c-130">Namespace</span></span><br/>                | <span data-ttu-id="e0e0c-131">\\TerminalServices da CIMv2 raiz \\</span><span class="sxs-lookup"><span data-stu-id="e0e0c-131">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="e0e0c-132">MOF</span><span class="sxs-lookup"><span data-stu-id="e0e0c-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e0e0c-133"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e0e0c-133"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="e0e0c-134">DLL</span><span class="sxs-lookup"><span data-stu-id="e0e0c-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e0e0c-135"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e0e0c-135"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e0e0c-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="e0e0c-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e0e0c-137">**\_TSSessionDirectory Win32**</span><span class="sxs-lookup"><span data-stu-id="e0e0c-137">**Win32\_TSSessionDirectory**</span></span>](win32-tssessiondirectory.md)
</dt> </dl>

 

