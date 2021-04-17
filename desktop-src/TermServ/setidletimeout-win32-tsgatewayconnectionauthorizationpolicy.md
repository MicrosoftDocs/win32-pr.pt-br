---
title: Método SetIdleTimeout da classe Win32_TSGatewayConnectionAuthorizationPolicy
description: Define a propriedade IdleTimeout.
ms.assetid: 162224dd-e4d4-483f-9ec4-b87731bc5014
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método SetIdleTimeout
- Método SetIdleTimeout Serviços de Área de Trabalho Remota, classe Win32_TSGatewayConnectionAuthorizationPolicy
- Classe Win32_TSGatewayConnectionAuthorizationPolicy Serviços de Área de Trabalho Remota, método SetIdleTimeout
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnectionAuthorizationPolicy.SetIdleTimeout
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2c166311477dc9de94ca6c9614e14ac98907b406
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105754707"
---
# <a name="setidletimeout-method-of-the-win32_tsgatewayconnectionauthorizationpolicy-class"></a><span data-ttu-id="38273-106">Método SetIdleTimeout da classe Win32 \_ TSGatewayConnectionAuthorizationPolicy</span><span class="sxs-lookup"><span data-stu-id="38273-106">SetIdleTimeout method of the Win32\_TSGatewayConnectionAuthorizationPolicy class</span></span>

<span data-ttu-id="38273-107">Define a propriedade **IdleTimeout** .</span><span class="sxs-lookup"><span data-stu-id="38273-107">Sets the **IdleTimeout** property.</span></span>

## <a name="syntax"></a><span data-ttu-id="38273-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="38273-108">Syntax</span></span>


```mof
uint32 SetIdleTimeout(
  [in] uint32 IdleTimeout
);
```



## <a name="parameters"></a><span data-ttu-id="38273-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="38273-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="38273-110">*IdleTimeout* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="38273-110">*IdleTimeout* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="38273-111">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="38273-111">Type: **uint32**</span></span>

<span data-ttu-id="38273-112">O novo valor de tempo limite, em minutos.</span><span class="sxs-lookup"><span data-stu-id="38273-112">The new timeout value, in minutes.</span></span> <span data-ttu-id="38273-113">Um valor de 0 significa que não há nenhum tempo limite.</span><span class="sxs-lookup"><span data-stu-id="38273-113">A value of 0 means there is no timeout.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="38273-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="38273-114">Return value</span></span>

<span data-ttu-id="38273-115">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="38273-115">Type: **uint32**</span></span>

<span data-ttu-id="38273-116">Se o método tiver sucesso, ele retornará zero.</span><span class="sxs-lookup"><span data-stu-id="38273-116">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="38273-117">Se o método não for bem-sucedido, ele retornará um valor diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="38273-117">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="38273-118">Para obter uma lista de códigos de erro, consulte [serviços de área de trabalho remota códigos de erro do provedor WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="38273-118">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="38273-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="38273-119">Remarks</span></span>

<span data-ttu-id="38273-120">Você deve ser um membro do grupo Administradores para chamar esse método.</span><span class="sxs-lookup"><span data-stu-id="38273-120">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="38273-121">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="38273-121">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="38273-122">Os arquivos MOF não são instalados como parte do SDK (Software Development Kit) do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="38273-122">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="38273-123">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="38273-123">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="38273-124">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="38273-124">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="38273-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="38273-125">Requirements</span></span>



| <span data-ttu-id="38273-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="38273-126">Requirement</span></span> | <span data-ttu-id="38273-127">Valor</span><span class="sxs-lookup"><span data-stu-id="38273-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="38273-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="38273-128">Minimum supported client</span></span><br/> | <span data-ttu-id="38273-129">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="38273-129">None supported</span></span><br/>                                                                |
| <span data-ttu-id="38273-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="38273-130">Minimum supported server</span></span><br/> | <span data-ttu-id="38273-131">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="38273-131">Windows Server 2008 R2</span></span><br/>                                                        |
| <span data-ttu-id="38273-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="38273-132">Namespace</span></span><br/>                | <span data-ttu-id="38273-133">\\TerminalServices da CIMv2 raiz \\</span><span class="sxs-lookup"><span data-stu-id="38273-133">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="38273-134">MOF</span><span class="sxs-lookup"><span data-stu-id="38273-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="38273-135"><dt>TS. mof</dt></span><span class="sxs-lookup"><span data-stu-id="38273-135"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="38273-136">DLL</span><span class="sxs-lookup"><span data-stu-id="38273-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="38273-137"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="38273-137"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="38273-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="38273-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="38273-139">**\_TSGatewayConnectionAuthorizationPolicy Win32**</span><span class="sxs-lookup"><span data-stu-id="38273-139">**Win32\_TSGatewayConnectionAuthorizationPolicy**</span></span>](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> </dl>

 

