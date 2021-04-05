---
title: Método AddComputerGroupNames da classe Win32_TSGatewayConnectionAuthorizationPolicy
description: Adiciona os nomes de grupo de computadores especificados à propriedade ComputerGroupNames.
ms.assetid: f0c440d6-0cc2-48b4-b656-65f12e652151
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método AddComputerGroupNames
- Método AddComputerGroupNames Serviços de Área de Trabalho Remota, classe Win32_TSGatewayConnectionAuthorizationPolicy
- Classe Win32_TSGatewayConnectionAuthorizationPolicy Serviços de Área de Trabalho Remota, método AddComputerGroupNames
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnectionAuthorizationPolicy.AddComputerGroupNames
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72647ef66b9e2eeaed824b3e77c404214786b615
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085776"
---
# <a name="addcomputergroupnames-method-of-the-win32_tsgatewayconnectionauthorizationpolicy-class"></a><span data-ttu-id="6b89b-106">Método AddComputerGroupNames da classe Win32 \_ TSGatewayConnectionAuthorizationPolicy</span><span class="sxs-lookup"><span data-stu-id="6b89b-106">AddComputerGroupNames method of the Win32\_TSGatewayConnectionAuthorizationPolicy class</span></span>

<span data-ttu-id="6b89b-107">Adiciona os nomes de grupo de computadores especificados à propriedade **ComputerGroupNames** .</span><span class="sxs-lookup"><span data-stu-id="6b89b-107">Adds the specified computer group names to the **ComputerGroupNames** property.</span></span>

## <a name="syntax"></a><span data-ttu-id="6b89b-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6b89b-108">Syntax</span></span>


```mof
uint32 AddComputerGroupNames(
  [in] string ComputerGroupNames
);
```



## <a name="parameters"></a><span data-ttu-id="6b89b-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6b89b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6b89b-110">*ComputerGroupNames* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6b89b-110">*ComputerGroupNames* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6b89b-111">Lista separada por ponto e vírgula de nomes de grupos de computadores para adicionar à propriedade **ComputerGroupNames** .</span><span class="sxs-lookup"><span data-stu-id="6b89b-111">Semicolon-separated list of computer group names to add to the **ComputerGroupNames** property.</span></span> <span data-ttu-id="6b89b-112">Os nomes de grupos de computadores devem ter o formato *Domain \\ ComputerGroupName*.</span><span class="sxs-lookup"><span data-stu-id="6b89b-112">Computer group names should be of the format *Domain\\ComputerGroupName*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6b89b-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6b89b-113">Return value</span></span>

<span data-ttu-id="6b89b-114">Se o método tiver sucesso, ele retornará zero.</span><span class="sxs-lookup"><span data-stu-id="6b89b-114">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="6b89b-115">Se o método não for bem-sucedido, ele retornará um valor diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="6b89b-115">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="6b89b-116">Para obter uma lista de códigos de erro, consulte [serviços de área de trabalho remota códigos de erro do provedor WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="6b89b-116">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="6b89b-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="6b89b-117">Remarks</span></span>

<span data-ttu-id="6b89b-118">Se vários nomes de grupos de computadores estiverem no parâmetro *ComputerGroupNames* e um dos nomes não puder ser processado, nenhum dos nomes será processado.</span><span class="sxs-lookup"><span data-stu-id="6b89b-118">If multiple computer group names are in the *ComputerGroupNames* parameter and one of the names cannot be processed, none of the names will be processed.</span></span>

<span data-ttu-id="6b89b-119">Você deve ser um membro do grupo Administradores para chamar esse método.</span><span class="sxs-lookup"><span data-stu-id="6b89b-119">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="6b89b-120">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="6b89b-120">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="6b89b-121">Os arquivos MOF não são instalados como parte do SDK (Software Development Kit) do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="6b89b-121">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="6b89b-122">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="6b89b-122">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="6b89b-123">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="6b89b-123">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="6b89b-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6b89b-124">Requirements</span></span>



| <span data-ttu-id="6b89b-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="6b89b-125">Requirement</span></span> | <span data-ttu-id="6b89b-126">Valor</span><span class="sxs-lookup"><span data-stu-id="6b89b-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="6b89b-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6b89b-127">Minimum supported client</span></span><br/> | <span data-ttu-id="6b89b-128">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="6b89b-128">None supported</span></span><br/>                                                                |
| <span data-ttu-id="6b89b-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6b89b-129">Minimum supported server</span></span><br/> | <span data-ttu-id="6b89b-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6b89b-130">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="6b89b-131">Namespace</span><span class="sxs-lookup"><span data-stu-id="6b89b-131">Namespace</span></span><br/>                | <span data-ttu-id="6b89b-132">\\TerminalServices da CIMv2 raiz \\</span><span class="sxs-lookup"><span data-stu-id="6b89b-132">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="6b89b-133">MOF</span><span class="sxs-lookup"><span data-stu-id="6b89b-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6b89b-134"><dt>TS. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6b89b-134"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="6b89b-135">DLL</span><span class="sxs-lookup"><span data-stu-id="6b89b-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6b89b-136"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6b89b-136"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="6b89b-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="6b89b-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6b89b-138">**\_TSGatewayConnectionAuthorizationPolicy Win32**</span><span class="sxs-lookup"><span data-stu-id="6b89b-138">**Win32\_TSGatewayConnectionAuthorizationPolicy**</span></span>](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> </dl>

 

