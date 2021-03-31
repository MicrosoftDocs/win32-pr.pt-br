---
title: Método SetName da classe Win32_TSGatewayResourceGroup
description: Define a propriedade Name para o grupo de recursos.
ms.assetid: 2c2fe1b6-5826-490e-aec2-479a0191e215
ms.tgt_platform: multiple
keywords:
- Método SetName Serviços de Área de Trabalho Remota
- Método SetName Serviços de Área de Trabalho Remota, classe Win32_TSGatewayResourceGroup
- Classe Win32_TSGatewayResourceGroup Serviços de Área de Trabalho Remota, método SetName
topic_type:
- apiref
api_name:
- Win32_TSGatewayResourceGroup.SetName
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac9ea16eb82896bb8fad67fff7ed849308100726
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824412"
---
# <a name="setname-method-of-the-win32_tsgatewayresourcegroup-class"></a><span data-ttu-id="6a5d7-106">Método SetName da classe Win32 \_ TSGatewayResourceGroup</span><span class="sxs-lookup"><span data-stu-id="6a5d7-106">SetName method of the Win32\_TSGatewayResourceGroup class</span></span>

<span data-ttu-id="6a5d7-107">Define a propriedade **Name** para o grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="6a5d7-107">Sets the **Name** property for the resource group.</span></span>

## <a name="syntax"></a><span data-ttu-id="6a5d7-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6a5d7-108">Syntax</span></span>


```mof
uint32 SetName(
  [in] string Name
);
```



## <a name="parameters"></a><span data-ttu-id="6a5d7-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6a5d7-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6a5d7-110">*Nome* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="6a5d7-110">*Name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6a5d7-111">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="6a5d7-111">Name of the resource group.</span></span> <span data-ttu-id="6a5d7-112">O nome deve ter 64 caracteres ou menos, exclusivo (o caso é ignorado) e não pode conter os seguintes caracteres reservados:</span><span class="sxs-lookup"><span data-stu-id="6a5d7-112">The name must be 64 characters or less, unique (case is ignored), and cannot contain the following reserved characters:</span></span>

<span data-ttu-id="6a5d7-113"><> :; " / \\ \| ?</span><span class="sxs-lookup"><span data-stu-id="6a5d7-113"><> : ; " / \\ \| ?</span></span> <span data-ttu-id="6a5d7-114">\*\[Guia\]</span><span class="sxs-lookup"><span data-stu-id="6a5d7-114">\* \[TAB\]</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6a5d7-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6a5d7-115">Return value</span></span>

<span data-ttu-id="6a5d7-116">Se o método tiver sucesso, ele retornará zero.</span><span class="sxs-lookup"><span data-stu-id="6a5d7-116">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="6a5d7-117">Se o método não for bem-sucedido, ele retornará um valor diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="6a5d7-117">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="6a5d7-118">Para obter uma lista de códigos de erro, consulte [serviços de área de trabalho remota códigos de erro do provedor WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="6a5d7-118">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="6a5d7-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="6a5d7-119">Remarks</span></span>

<span data-ttu-id="6a5d7-120">Você deve ser um membro do grupo Administradores para chamar esse método.</span><span class="sxs-lookup"><span data-stu-id="6a5d7-120">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="6a5d7-121">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="6a5d7-121">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="6a5d7-122">Os arquivos MOF não são instalados como parte do SDK (Software Development Kit) do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="6a5d7-122">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="6a5d7-123">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="6a5d7-123">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="6a5d7-124">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="6a5d7-124">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="6a5d7-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6a5d7-125">Requirements</span></span>



| <span data-ttu-id="6a5d7-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="6a5d7-126">Requirement</span></span> | <span data-ttu-id="6a5d7-127">Valor</span><span class="sxs-lookup"><span data-stu-id="6a5d7-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="6a5d7-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6a5d7-128">Minimum supported client</span></span><br/> | <span data-ttu-id="6a5d7-129">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="6a5d7-129">None supported</span></span><br/>                                                                |
| <span data-ttu-id="6a5d7-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6a5d7-130">Minimum supported server</span></span><br/> | <span data-ttu-id="6a5d7-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6a5d7-131">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="6a5d7-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="6a5d7-132">Namespace</span></span><br/>                | <span data-ttu-id="6a5d7-133">\\TerminalServices da CIMv2 raiz \\</span><span class="sxs-lookup"><span data-stu-id="6a5d7-133">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="6a5d7-134">MOF</span><span class="sxs-lookup"><span data-stu-id="6a5d7-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6a5d7-135"><dt>TS. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6a5d7-135"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="6a5d7-136">DLL</span><span class="sxs-lookup"><span data-stu-id="6a5d7-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6a5d7-137"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6a5d7-137"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="6a5d7-138">Consulte também</span><span class="sxs-lookup"><span data-stu-id="6a5d7-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6a5d7-139">**\_TSGatewayResourceGroup Win32**</span><span class="sxs-lookup"><span data-stu-id="6a5d7-139">**Win32\_TSGatewayResourceGroup**</span></span>](win32-tsgatewayresourcegroup.md)
</dt> </dl>

 

