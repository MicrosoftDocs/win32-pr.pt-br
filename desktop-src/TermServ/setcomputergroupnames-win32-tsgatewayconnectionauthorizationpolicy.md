---
title: Método SetComputerGroupNames da classe Win32_TSGatewayConnectionAuthorizationPolicy
description: Define a propriedade ComputerGroupNames.
ms.assetid: dd6747df-140f-4eeb-857b-d14f8713586c
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método SetComputerGroupNames
- Método SetComputerGroupNames Serviços de Área de Trabalho Remota, classe Win32_TSGatewayConnectionAuthorizationPolicy
- Classe Win32_TSGatewayConnectionAuthorizationPolicy Serviços de Área de Trabalho Remota, método SetComputerGroupNames
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnectionAuthorizationPolicy.SetComputerGroupNames
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a99c29ce37aeb8bfad0ae77197c7364b0135fa99
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369569"
---
# <a name="setcomputergroupnames-method-of-the-win32_tsgatewayconnectionauthorizationpolicy-class"></a><span data-ttu-id="aa8a1-106">Método SetComputerGroupNames da classe Win32 \_ TSGatewayConnectionAuthorizationPolicy</span><span class="sxs-lookup"><span data-stu-id="aa8a1-106">SetComputerGroupNames method of the Win32\_TSGatewayConnectionAuthorizationPolicy class</span></span>

<span data-ttu-id="aa8a1-107">Define a propriedade **ComputerGroupNames** .</span><span class="sxs-lookup"><span data-stu-id="aa8a1-107">Sets the **ComputerGroupNames** property.</span></span>

## <a name="syntax"></a><span data-ttu-id="aa8a1-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="aa8a1-108">Syntax</span></span>


```mof
uint32 SetComputerGroupNames(
  [in] string ComputerGroupNames
);
```



## <a name="parameters"></a><span data-ttu-id="aa8a1-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="aa8a1-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aa8a1-110">*ComputerGroupNames* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="aa8a1-110">*ComputerGroupNames* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aa8a1-111">Lista de nomes de grupos de computadores separados por ponto e vírgula.</span><span class="sxs-lookup"><span data-stu-id="aa8a1-111">List of semicolon-separated computer group names.</span></span> <span data-ttu-id="aa8a1-112">Esse valor pode estar vazio.</span><span class="sxs-lookup"><span data-stu-id="aa8a1-112">This value can be empty.</span></span> <span data-ttu-id="aa8a1-113">Os nomes são do formato *domínio \\ ComputerGroupName*.</span><span class="sxs-lookup"><span data-stu-id="aa8a1-113">The names are of the format *Domain\\ComputerGroupName*.</span></span> <span data-ttu-id="aa8a1-114">Se um valor for especificado, o computador cliente deverá pertencer a um desses grupos de computadores para que o usuário acesse o servidor de gateway de área de trabalho remota.</span><span class="sxs-lookup"><span data-stu-id="aa8a1-114">If a value is specified, the client computer must belong to one of these computer groups for the user to access the RD Gateway server.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aa8a1-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="aa8a1-115">Return value</span></span>

<span data-ttu-id="aa8a1-116">Se o método tiver sucesso, ele retornará zero.</span><span class="sxs-lookup"><span data-stu-id="aa8a1-116">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="aa8a1-117">Se o método não for bem-sucedido, ele retornará um valor diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="aa8a1-117">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="aa8a1-118">Para obter uma lista de códigos de erro, consulte [serviços de área de trabalho remota códigos de erro do provedor WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="aa8a1-118">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="aa8a1-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="aa8a1-119">Remarks</span></span>

<span data-ttu-id="aa8a1-120">Se vários nomes de grupos de computadores estiverem no parâmetro *ComputerGroupNames* e um dos nomes não puder ser processado, nenhum dos nomes será processado.</span><span class="sxs-lookup"><span data-stu-id="aa8a1-120">If multiple computer group names are in the *ComputerGroupNames* parameter and one of the names cannot be processed, none of the names will be processed.</span></span>

<span data-ttu-id="aa8a1-121">Você deve ser um membro do grupo Administradores para chamar esse método.</span><span class="sxs-lookup"><span data-stu-id="aa8a1-121">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="aa8a1-122">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="aa8a1-122">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="aa8a1-123">Os arquivos MOF não são instalados como parte do SDK (Software Development Kit) do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="aa8a1-123">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="aa8a1-124">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="aa8a1-124">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="aa8a1-125">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="aa8a1-125">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="aa8a1-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="aa8a1-126">Requirements</span></span>



| <span data-ttu-id="aa8a1-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="aa8a1-127">Requirement</span></span> | <span data-ttu-id="aa8a1-128">Valor</span><span class="sxs-lookup"><span data-stu-id="aa8a1-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="aa8a1-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="aa8a1-129">Minimum supported client</span></span><br/> | <span data-ttu-id="aa8a1-130">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="aa8a1-130">None supported</span></span><br/>                                                                |
| <span data-ttu-id="aa8a1-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="aa8a1-131">Minimum supported server</span></span><br/> | <span data-ttu-id="aa8a1-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="aa8a1-132">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="aa8a1-133">Namespace</span><span class="sxs-lookup"><span data-stu-id="aa8a1-133">Namespace</span></span><br/>                | <span data-ttu-id="aa8a1-134">\\TerminalServices da CIMv2 raiz \\</span><span class="sxs-lookup"><span data-stu-id="aa8a1-134">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="aa8a1-135">MOF</span><span class="sxs-lookup"><span data-stu-id="aa8a1-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="aa8a1-136"><dt>TS. mof</dt></span><span class="sxs-lookup"><span data-stu-id="aa8a1-136"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="aa8a1-137">DLL</span><span class="sxs-lookup"><span data-stu-id="aa8a1-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="aa8a1-138"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="aa8a1-138"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="aa8a1-139">Consulte também</span><span class="sxs-lookup"><span data-stu-id="aa8a1-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aa8a1-140">**\_TSGatewayConnectionAuthorizationPolicy Win32**</span><span class="sxs-lookup"><span data-stu-id="aa8a1-140">**Win32\_TSGatewayConnectionAuthorizationPolicy**</span></span>](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> </dl>

 

