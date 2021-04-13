---
title: Método Update da classe Win32_TSGatewayResourceGroup
description: Atualiza o grupo de recursos.
ms.assetid: b5927046-f461-41cd-861b-0fd77f2008e5
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método de atualização
- Método Update Serviços de Área de Trabalho Remota, classe Win32_TSGatewayResourceGroup
- Serviços de Área de Trabalho Remota de classe Win32_TSGatewayResourceGroup, método Update
topic_type:
- apiref
api_name:
- Win32_TSGatewayResourceGroup.Update
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1a7b1610fc14aa522fa4d8b7caf03fccd7b37375
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369666"
---
# <a name="update-method-of-the-win32_tsgatewayresourcegroup-class"></a><span data-ttu-id="de61b-106">Método Update da classe Win32 \_ TSGatewayResourceGroup</span><span class="sxs-lookup"><span data-stu-id="de61b-106">Update method of the Win32\_TSGatewayResourceGroup class</span></span>

<span data-ttu-id="de61b-107">Atualiza o grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="de61b-107">Updates the resource group.</span></span>

## <a name="syntax"></a><span data-ttu-id="de61b-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="de61b-108">Syntax</span></span>


```mof
uint32 Update(
  [in] string Name,
  [in] string Description,
  [in] string Resources
);
```



## <a name="parameters"></a><span data-ttu-id="de61b-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="de61b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="de61b-110">*Nome* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="de61b-110">*Name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="de61b-111">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="de61b-111">Name of the resource group.</span></span>

</dd> <dt>

<span data-ttu-id="de61b-112">*Descrição* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="de61b-112">*Description* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="de61b-113">Descrição do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="de61b-113">Description of the resource group.</span></span>

</dd> <dt>

<span data-ttu-id="de61b-114">*Recursos* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="de61b-114">*Resources* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="de61b-115">Lista de recursos separados por ponto e vírgula neste grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="de61b-115">Semicolon-separated list of resources in this resource group.</span></span> <span data-ttu-id="de61b-116">Um " \* " significa todos os recursos.</span><span class="sxs-lookup"><span data-stu-id="de61b-116">An "\*" means all resources.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="de61b-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="de61b-117">Return value</span></span>

<span data-ttu-id="de61b-118">Se o método tiver sucesso, ele retornará zero.</span><span class="sxs-lookup"><span data-stu-id="de61b-118">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="de61b-119">Se o método não for bem-sucedido, ele retornará um valor diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="de61b-119">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="de61b-120">Para obter uma lista de códigos de erro, consulte [serviços de área de trabalho remota códigos de erro do provedor WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="de61b-120">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="de61b-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="de61b-121">Remarks</span></span>

<span data-ttu-id="de61b-122">Se vários recursos estiverem no parâmetro de *recursos* e um dos recursos não puder ser processado, nenhum dos recursos será processado.</span><span class="sxs-lookup"><span data-stu-id="de61b-122">If multiple resources are in the *Resources* parameter and one of the resources cannot be processed, none of the resources will be processed.</span></span>

<span data-ttu-id="de61b-123">Você deve ser um membro do grupo Administradores para chamar esse método.</span><span class="sxs-lookup"><span data-stu-id="de61b-123">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="de61b-124">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="de61b-124">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="de61b-125">Os arquivos MOF não são instalados como parte do SDK (Software Development Kit) do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="de61b-125">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="de61b-126">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="de61b-126">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="de61b-127">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="de61b-127">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="de61b-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="de61b-128">Requirements</span></span>



| <span data-ttu-id="de61b-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="de61b-129">Requirement</span></span> | <span data-ttu-id="de61b-130">Valor</span><span class="sxs-lookup"><span data-stu-id="de61b-130">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="de61b-131">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="de61b-131">Minimum supported client</span></span><br/> | <span data-ttu-id="de61b-132">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="de61b-132">None supported</span></span><br/>                                                                |
| <span data-ttu-id="de61b-133">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="de61b-133">Minimum supported server</span></span><br/> | <span data-ttu-id="de61b-134">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="de61b-134">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="de61b-135">Namespace</span><span class="sxs-lookup"><span data-stu-id="de61b-135">Namespace</span></span><br/>                | <span data-ttu-id="de61b-136">\\TerminalServices da CIMv2 raiz \\</span><span class="sxs-lookup"><span data-stu-id="de61b-136">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="de61b-137">MOF</span><span class="sxs-lookup"><span data-stu-id="de61b-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="de61b-138"><dt>TS. mof</dt></span><span class="sxs-lookup"><span data-stu-id="de61b-138"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="de61b-139">DLL</span><span class="sxs-lookup"><span data-stu-id="de61b-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="de61b-140"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="de61b-140"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="de61b-141">Confira também</span><span class="sxs-lookup"><span data-stu-id="de61b-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="de61b-142">**\_TSGatewayResourceGroup Win32**</span><span class="sxs-lookup"><span data-stu-id="de61b-142">**Win32\_TSGatewayResourceGroup**</span></span>](win32-tsgatewayresourcegroup.md)
</dt> </dl>

 

