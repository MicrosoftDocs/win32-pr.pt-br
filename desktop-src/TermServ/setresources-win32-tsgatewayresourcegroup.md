---
title: Método Resources da classe Win32_TSGatewayResourceGroup
description: Define a propriedade Resources para esse grupo de recursos.
ms.assetid: 0043ee04-26d1-4907-87cc-a15f72cb0b93
ms.tgt_platform: multiple
keywords:
- Método Resources serviços de área de trabalho remota
- Método Resources serviços de área de trabalho remota, classe Win32_TSGatewayResourceGroup
- Classe Win32_TSGatewayResourceGroup serviços de área de trabalho remota, método Resources
topic_type:
- apiref
api_name:
- Win32_TSGatewayResourceGroup.SetResources
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b23f2ca14597fc7d6ce3660e6e180bf93dfd86cb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369424"
---
# <a name="setresources-method-of-the-win32_tsgatewayresourcegroup-class"></a><span data-ttu-id="d80c6-106">Método Resources da \_ classe Win32 TSGatewayResourceGroup</span><span class="sxs-lookup"><span data-stu-id="d80c6-106">SetResources method of the Win32\_TSGatewayResourceGroup class</span></span>

<span data-ttu-id="d80c6-107">Define a propriedade **Resources** para esse grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="d80c6-107">Sets the **Resources** property for this resource group.</span></span>

## <a name="syntax"></a><span data-ttu-id="d80c6-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d80c6-108">Syntax</span></span>


```mof
uint32 SetResources(
  [in] string Resources
);
```



## <a name="parameters"></a><span data-ttu-id="d80c6-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d80c6-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d80c6-110">*Recursos* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="d80c6-110">*Resources* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d80c6-111">Lista de recursos separados por ponto e vírgula neste grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="d80c6-111">Semicolon-separated list of resources in this resource group.</span></span> <span data-ttu-id="d80c6-112">Um " \* " significa todos os recursos.</span><span class="sxs-lookup"><span data-stu-id="d80c6-112">An "\*" means all resources.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d80c6-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d80c6-113">Return value</span></span>

<span data-ttu-id="d80c6-114">Se o método tiver sucesso, ele retornará zero.</span><span class="sxs-lookup"><span data-stu-id="d80c6-114">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="d80c6-115">Se o método não for bem-sucedido, ele retornará um valor diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="d80c6-115">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="d80c6-116">Para obter uma lista de códigos de erro, consulte [serviços de área de trabalho remota códigos de erro do provedor WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="d80c6-116">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="d80c6-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="d80c6-117">Remarks</span></span>

<span data-ttu-id="d80c6-118">Se vários recursos estiverem no parâmetro de *recursos* e um dos recursos não puder ser processado, nenhum dos recursos será processado.</span><span class="sxs-lookup"><span data-stu-id="d80c6-118">If multiple resources are in the *Resources* parameter and one of the resources cannot be processed, none of the resources will be processed.</span></span>

<span data-ttu-id="d80c6-119">Você deve ser um membro do grupo Administradores para chamar esse método.</span><span class="sxs-lookup"><span data-stu-id="d80c6-119">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="d80c6-120">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="d80c6-120">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="d80c6-121">Os arquivos MOF não são instalados como parte do SDK (Software Development Kit) do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="d80c6-121">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="d80c6-122">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="d80c6-122">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="d80c6-123">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="d80c6-123">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="d80c6-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d80c6-124">Requirements</span></span>



| <span data-ttu-id="d80c6-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="d80c6-125">Requirement</span></span> | <span data-ttu-id="d80c6-126">Valor</span><span class="sxs-lookup"><span data-stu-id="d80c6-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="d80c6-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d80c6-127">Minimum supported client</span></span><br/> | <span data-ttu-id="d80c6-128">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="d80c6-128">None supported</span></span><br/>                                                                |
| <span data-ttu-id="d80c6-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d80c6-129">Minimum supported server</span></span><br/> | <span data-ttu-id="d80c6-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d80c6-130">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="d80c6-131">Namespace</span><span class="sxs-lookup"><span data-stu-id="d80c6-131">Namespace</span></span><br/>                | <span data-ttu-id="d80c6-132">\\TerminalServices da CIMv2 raiz \\</span><span class="sxs-lookup"><span data-stu-id="d80c6-132">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="d80c6-133">MOF</span><span class="sxs-lookup"><span data-stu-id="d80c6-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d80c6-134"><dt>TS. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d80c6-134"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="d80c6-135">DLL</span><span class="sxs-lookup"><span data-stu-id="d80c6-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d80c6-136"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d80c6-136"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="d80c6-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="d80c6-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d80c6-138">**\_TSGatewayResourceGroup Win32**</span><span class="sxs-lookup"><span data-stu-id="d80c6-138">**Win32\_TSGatewayResourceGroup**</span></span>](win32-tsgatewayresourcegroup.md)
</dt> </dl>

 

