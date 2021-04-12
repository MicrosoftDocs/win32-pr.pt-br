---
title: Método Resources da classe Win32_TSGatewayResourceGroup
description: Adiciona recursos ao grupo de recursos.
ms.assetid: 3210b468-6b82-4edb-ac8b-95f66a7b9328
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método addresources
- Método addresources Serviços de Área de Trabalho Remota, classe Win32_TSGatewayResourceGroup
- Classe Win32_TSGatewayResourceGroup Serviços de Área de Trabalho Remota, método addresources
topic_type:
- apiref
api_name:
- Win32_TSGatewayResourceGroup.AddResources
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a37498accf76b28f16e0de45565916c18ab8d9dc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499269"
---
# <a name="addresources-method-of-the-win32_tsgatewayresourcegroup-class"></a><span data-ttu-id="776b9-106">Método Resources da \_ classe Win32 TSGatewayResourceGroup</span><span class="sxs-lookup"><span data-stu-id="776b9-106">AddResources method of the Win32\_TSGatewayResourceGroup class</span></span>

<span data-ttu-id="776b9-107">Adiciona recursos ao grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="776b9-107">Adds resources to the resource group.</span></span>

## <a name="syntax"></a><span data-ttu-id="776b9-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="776b9-108">Syntax</span></span>


```mof
uint32 AddResources(
  [in] string Resources
);
```



## <a name="parameters"></a><span data-ttu-id="776b9-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="776b9-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="776b9-110">*Recursos* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="776b9-110">*Resources* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="776b9-111">Lista separada por ponto e vírgula de recursos a serem adicionados ao grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="776b9-111">Semicolon-separated list of resources to be added to the resource group.</span></span> <span data-ttu-id="776b9-112">Um " \* " significa todos os recursos.</span><span class="sxs-lookup"><span data-stu-id="776b9-112">An "\*" means all resources.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="776b9-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="776b9-113">Return value</span></span>

<span data-ttu-id="776b9-114">Se o método tiver sucesso, ele retornará zero.</span><span class="sxs-lookup"><span data-stu-id="776b9-114">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="776b9-115">Se o método não for bem-sucedido, ele retornará um valor diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="776b9-115">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="776b9-116">Para obter uma lista de códigos de erro, consulte [serviços de área de trabalho remota códigos de erro do provedor WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="776b9-116">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="776b9-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="776b9-117">Remarks</span></span>

<span data-ttu-id="776b9-118">Se vários recursos estiverem no parâmetro de *recursos* e um dos recursos não puder ser processado, nenhum dos recursos será processado.</span><span class="sxs-lookup"><span data-stu-id="776b9-118">If multiple resources are in the *Resources* parameter and one of the resources cannot be processed, none of the resources will be processed.</span></span>

<span data-ttu-id="776b9-119">Você deve ser um membro do grupo Administradores para chamar esse método.</span><span class="sxs-lookup"><span data-stu-id="776b9-119">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="776b9-120">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="776b9-120">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="776b9-121">Os arquivos MOF não são instalados como parte do SDK (Software Development Kit) do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="776b9-121">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="776b9-122">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="776b9-122">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="776b9-123">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="776b9-123">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="776b9-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="776b9-124">Requirements</span></span>



| <span data-ttu-id="776b9-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="776b9-125">Requirement</span></span> | <span data-ttu-id="776b9-126">Valor</span><span class="sxs-lookup"><span data-stu-id="776b9-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="776b9-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="776b9-127">Minimum supported client</span></span><br/> | <span data-ttu-id="776b9-128">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="776b9-128">None supported</span></span><br/>                                                                |
| <span data-ttu-id="776b9-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="776b9-129">Minimum supported server</span></span><br/> | <span data-ttu-id="776b9-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="776b9-130">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="776b9-131">Namespace</span><span class="sxs-lookup"><span data-stu-id="776b9-131">Namespace</span></span><br/>                | <span data-ttu-id="776b9-132">\\TerminalServices da CIMv2 raiz \\</span><span class="sxs-lookup"><span data-stu-id="776b9-132">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="776b9-133">MOF</span><span class="sxs-lookup"><span data-stu-id="776b9-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="776b9-134"><dt>TS. mof</dt></span><span class="sxs-lookup"><span data-stu-id="776b9-134"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="776b9-135">DLL</span><span class="sxs-lookup"><span data-stu-id="776b9-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="776b9-136"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="776b9-136"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="776b9-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="776b9-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="776b9-138">**\_TSGatewayResourceGroup Win32**</span><span class="sxs-lookup"><span data-stu-id="776b9-138">**Win32\_TSGatewayResourceGroup**</span></span>](win32-tsgatewayresourcegroup.md)
</dt> </dl>

 

