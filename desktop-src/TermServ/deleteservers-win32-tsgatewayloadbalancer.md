---
title: Método DeleteServers da classe Win32_TSGatewayLoadBalancer
description: Exclui servidores da propriedade servidores.
ms.assetid: 5ef44725-82b6-464a-abab-a68cc8799669
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método DeleteServers
- Método DeleteServers Serviços de Área de Trabalho Remota, classe Win32_TSGatewayLoadBalancer
- Classe Win32_TSGatewayLoadBalancer Serviços de Área de Trabalho Remota, método DeleteServers
topic_type:
- apiref
api_name:
- Win32_TSGatewayLoadBalancer.DeleteServers
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b889f37b783853fbca0b9cb399a83959e2522d0e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369320"
---
# <a name="deleteservers-method-of-the-win32_tsgatewayloadbalancer-class"></a><span data-ttu-id="5f849-106">Método DeleteServers da classe Win32 \_ TSGatewayLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="5f849-106">DeleteServers method of the Win32\_TSGatewayLoadBalancer class</span></span>

<span data-ttu-id="5f849-107">Exclui servidores da propriedade **servidores** .</span><span class="sxs-lookup"><span data-stu-id="5f849-107">Deletes servers from the **Servers** property.</span></span>

## <a name="syntax"></a><span data-ttu-id="5f849-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5f849-108">Syntax</span></span>


```mof
uint32 DeleteServers(
  [in] string Servers
);
```



## <a name="parameters"></a><span data-ttu-id="5f849-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5f849-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5f849-110">*Servidores* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="5f849-110">*Servers* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5f849-111">Lista separada por ponto-e-vírgula dos servidores de balanceamento de carga do gateway RD para excluir da propriedade **servidores** .</span><span class="sxs-lookup"><span data-stu-id="5f849-111">Semicolon-separated list of RD Gateway load-balancing servers to delete from the **Servers** property.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5f849-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="5f849-112">Return value</span></span>

<span data-ttu-id="5f849-113">Se o método tiver sucesso, ele retornará zero.</span><span class="sxs-lookup"><span data-stu-id="5f849-113">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="5f849-114">Se o método não for bem-sucedido, ele retornará um valor diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="5f849-114">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="5f849-115">Para obter uma lista de códigos de erro, consulte [serviços de área de trabalho remota códigos de erro do provedor WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="5f849-115">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="5f849-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="5f849-116">Remarks</span></span>

<span data-ttu-id="5f849-117">Se vários servidores estiverem no parâmetro *servidores* e um dos servidores não puder ser processado, nenhum dos servidores será processado.</span><span class="sxs-lookup"><span data-stu-id="5f849-117">If multiple servers are in the *Servers* parameter and one of the servers cannot be processed, none of the servers will be processed.</span></span>

<span data-ttu-id="5f849-118">Você deve ser um membro do grupo Administradores para chamar esse método.</span><span class="sxs-lookup"><span data-stu-id="5f849-118">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="5f849-119">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="5f849-119">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="5f849-120">Os arquivos MOF não são instalados como parte do SDK (Software Development Kit) do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="5f849-120">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="5f849-121">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="5f849-121">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="5f849-122">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="5f849-122">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="5f849-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5f849-123">Requirements</span></span>



| <span data-ttu-id="5f849-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="5f849-124">Requirement</span></span> | <span data-ttu-id="5f849-125">Valor</span><span class="sxs-lookup"><span data-stu-id="5f849-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="5f849-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5f849-126">Minimum supported client</span></span><br/> | <span data-ttu-id="5f849-127">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="5f849-127">None supported</span></span><br/>                                                                |
| <span data-ttu-id="5f849-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5f849-128">Minimum supported server</span></span><br/> | <span data-ttu-id="5f849-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5f849-129">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="5f849-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="5f849-130">Namespace</span></span><br/>                | <span data-ttu-id="5f849-131">\\TerminalServices da CIMv2 raiz \\</span><span class="sxs-lookup"><span data-stu-id="5f849-131">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="5f849-132">MOF</span><span class="sxs-lookup"><span data-stu-id="5f849-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5f849-133"><dt>TS. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5f849-133"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="5f849-134">DLL</span><span class="sxs-lookup"><span data-stu-id="5f849-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5f849-135"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5f849-135"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="5f849-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="5f849-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5f849-137">**\_TSGatewayLoadBalancer Win32**</span><span class="sxs-lookup"><span data-stu-id="5f849-137">**Win32\_TSGatewayLoadBalancer**</span></span>](win32-tsgatewayloadbalancer.md)
</dt> </dl>

 

