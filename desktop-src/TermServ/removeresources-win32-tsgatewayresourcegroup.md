---
title: Método RemoveResources da classe Win32_TSGatewayResourceGroup
description: Remove os recursos do grupo de recursos.
ms.assetid: 5f339990-8273-4658-843e-b6b7a85808e1
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método RemoveResources
- Método RemoveResources Serviços de Área de Trabalho Remota, classe Win32_TSGatewayResourceGroup
- Classe Win32_TSGatewayResourceGroup Serviços de Área de Trabalho Remota, método RemoveResources
topic_type:
- apiref
api_name:
- Win32_TSGatewayResourceGroup.RemoveResources
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2e3d1cc1e39d8c96833fc6a371741493457a28b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369916"
---
# <a name="removeresources-method-of-the-win32_tsgatewayresourcegroup-class"></a><span data-ttu-id="b0eb2-106">Método RemoveResources da classe Win32 \_ TSGatewayResourceGroup</span><span class="sxs-lookup"><span data-stu-id="b0eb2-106">RemoveResources method of the Win32\_TSGatewayResourceGroup class</span></span>

<span data-ttu-id="b0eb2-107">Remove os recursos do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="b0eb2-107">Removes resources from the resource group.</span></span>

## <a name="syntax"></a><span data-ttu-id="b0eb2-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b0eb2-108">Syntax</span></span>


```mof
uint32 RemoveResources(
  [in] string Resources
);
```



## <a name="parameters"></a><span data-ttu-id="b0eb2-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b0eb2-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b0eb2-110">*Recursos* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="b0eb2-110">*Resources* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b0eb2-111">Lista de recursos separados por ponto-e-vírgula a serem removidos.</span><span class="sxs-lookup"><span data-stu-id="b0eb2-111">Semicolon-separated list of resources to be removed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b0eb2-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b0eb2-112">Return value</span></span>

<span data-ttu-id="b0eb2-113">Se o método tiver sucesso, ele retornará zero.</span><span class="sxs-lookup"><span data-stu-id="b0eb2-113">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="b0eb2-114">Se o método não for bem-sucedido, ele retornará um valor diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="b0eb2-114">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="b0eb2-115">Para obter uma lista de códigos de erro, consulte [serviços de área de trabalho remota códigos de erro do provedor WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="b0eb2-115">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="b0eb2-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="b0eb2-116">Remarks</span></span>

<span data-ttu-id="b0eb2-117">Se vários recursos estiverem no parâmetro de *recursos* e um dos recursos não puder ser processado, nenhum dos recursos será processado.</span><span class="sxs-lookup"><span data-stu-id="b0eb2-117">If multiple resources are in the *Resources* parameter and one of the resources cannot be processed, none of the resources will be processed.</span></span>

<span data-ttu-id="b0eb2-118">Você deve ser um membro do grupo Administradores para chamar esse método.</span><span class="sxs-lookup"><span data-stu-id="b0eb2-118">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="b0eb2-119">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="b0eb2-119">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="b0eb2-120">Os arquivos MOF não são instalados como parte do SDK (Software Development Kit) do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="b0eb2-120">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="b0eb2-121">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="b0eb2-121">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="b0eb2-122">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="b0eb2-122">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="b0eb2-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b0eb2-123">Requirements</span></span>



| <span data-ttu-id="b0eb2-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="b0eb2-124">Requirement</span></span> | <span data-ttu-id="b0eb2-125">Valor</span><span class="sxs-lookup"><span data-stu-id="b0eb2-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="b0eb2-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b0eb2-126">Minimum supported client</span></span><br/> | <span data-ttu-id="b0eb2-127">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="b0eb2-127">None supported</span></span><br/>                                                                |
| <span data-ttu-id="b0eb2-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b0eb2-128">Minimum supported server</span></span><br/> | <span data-ttu-id="b0eb2-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b0eb2-129">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="b0eb2-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="b0eb2-130">Namespace</span></span><br/>                | <span data-ttu-id="b0eb2-131">\\TerminalServices da CIMv2 raiz \\</span><span class="sxs-lookup"><span data-stu-id="b0eb2-131">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="b0eb2-132">MOF</span><span class="sxs-lookup"><span data-stu-id="b0eb2-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b0eb2-133"><dt>TS. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b0eb2-133"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="b0eb2-134">DLL</span><span class="sxs-lookup"><span data-stu-id="b0eb2-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b0eb2-135"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b0eb2-135"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="b0eb2-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="b0eb2-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b0eb2-137">**\_TSGatewayResourceGroup Win32**</span><span class="sxs-lookup"><span data-stu-id="b0eb2-137">**Win32\_TSGatewayResourceGroup**</span></span>](win32-tsgatewayresourcegroup.md)
</dt> </dl>

 

