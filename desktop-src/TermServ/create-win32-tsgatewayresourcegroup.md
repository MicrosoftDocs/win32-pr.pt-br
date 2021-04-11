---
title: Método Create da classe Win32_TSGatewayResourceGroup
description: Cria um grupo de recursos.
ms.assetid: 715e6086-1c7d-4b20-983a-3ab98e875ca5
ms.tgt_platform: multiple
keywords:
- Criar Serviços de Área de Trabalho Remota do método
- Criar método Serviços de Área de Trabalho Remota, classe Win32_TSGatewayResourceGroup
- Classe Win32_TSGatewayResourceGroup Serviços de Área de Trabalho Remota, método Create
topic_type:
- apiref
api_name:
- Win32_TSGatewayResourceGroup.Create
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d9c5179967c143faa36763b7a2aabb8849d2f13
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009032"
---
# <a name="create-method-of-the-win32_tsgatewayresourcegroup-class"></a><span data-ttu-id="7cf67-106">Método Create da classe Win32 \_ TSGatewayResourceGroup</span><span class="sxs-lookup"><span data-stu-id="7cf67-106">Create method of the Win32\_TSGatewayResourceGroup class</span></span>

<span data-ttu-id="7cf67-107">Cria um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="7cf67-107">Creates a resource group.</span></span>

## <a name="syntax"></a><span data-ttu-id="7cf67-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7cf67-108">Syntax</span></span>


```mof
uint32 Create(
  [in] string Name,
  [in] string Description,
  [in] string Resources
);
```



## <a name="parameters"></a><span data-ttu-id="7cf67-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7cf67-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7cf67-110">*Nome* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="7cf67-110">*Name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7cf67-111">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="7cf67-111">Name of the resource group.</span></span>

</dd> <dt>

<span data-ttu-id="7cf67-112">*Descrição* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="7cf67-112">*Description* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7cf67-113">Descrição do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="7cf67-113">Description of the resource group.</span></span>

</dd> <dt>

<span data-ttu-id="7cf67-114">*Recursos* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="7cf67-114">*Resources* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7cf67-115">Lista de recursos separados por ponto e vírgula neste grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="7cf67-115">Semicolon-separated list of resources in this resource group.</span></span> <span data-ttu-id="7cf67-116">Um " \* " significa todos os recursos.</span><span class="sxs-lookup"><span data-stu-id="7cf67-116">An "\*" means all resources.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7cf67-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="7cf67-117">Return value</span></span>

<span data-ttu-id="7cf67-118">Se o método tiver sucesso, ele retornará zero.</span><span class="sxs-lookup"><span data-stu-id="7cf67-118">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="7cf67-119">Se o método não for bem-sucedido, ele retornará um valor diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="7cf67-119">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="7cf67-120">Para obter uma lista de códigos de erro, consulte [serviços de área de trabalho remota códigos de erro do provedor WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="7cf67-120">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="7cf67-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="7cf67-121">Remarks</span></span>

<span data-ttu-id="7cf67-122">Você deve ser um membro do grupo Administradores para chamar esse método.</span><span class="sxs-lookup"><span data-stu-id="7cf67-122">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="7cf67-123">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="7cf67-123">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="7cf67-124">Os arquivos MOF não são instalados como parte do SDK (Software Development Kit) do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="7cf67-124">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="7cf67-125">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="7cf67-125">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="7cf67-126">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="7cf67-126">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="7cf67-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7cf67-127">Requirements</span></span>



| <span data-ttu-id="7cf67-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="7cf67-128">Requirement</span></span> | <span data-ttu-id="7cf67-129">Valor</span><span class="sxs-lookup"><span data-stu-id="7cf67-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="7cf67-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7cf67-130">Minimum supported client</span></span><br/> | <span data-ttu-id="7cf67-131">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="7cf67-131">None supported</span></span><br/>                                                                |
| <span data-ttu-id="7cf67-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7cf67-132">Minimum supported server</span></span><br/> | <span data-ttu-id="7cf67-133">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7cf67-133">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="7cf67-134">Namespace</span><span class="sxs-lookup"><span data-stu-id="7cf67-134">Namespace</span></span><br/>                | <span data-ttu-id="7cf67-135">\\TerminalServices da CIMv2 raiz \\</span><span class="sxs-lookup"><span data-stu-id="7cf67-135">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="7cf67-136">MOF</span><span class="sxs-lookup"><span data-stu-id="7cf67-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7cf67-137"><dt>TS. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7cf67-137"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="7cf67-138">DLL</span><span class="sxs-lookup"><span data-stu-id="7cf67-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7cf67-139"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7cf67-139"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="7cf67-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="7cf67-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7cf67-141">**\_TSGatewayResourceGroup Win32**</span><span class="sxs-lookup"><span data-stu-id="7cf67-141">**Win32\_TSGatewayResourceGroup**</span></span>](win32-tsgatewayresourcegroup.md)
</dt> </dl>

 

