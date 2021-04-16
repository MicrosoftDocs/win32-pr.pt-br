---
title: Método SetDescription da classe Win32_TSGatewayResourceGroup
description: Define a propriedade Description para o grupo de recursos.
ms.assetid: ab1280c7-ce53-4807-9537-953b597dd636
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método SetDescription
- Método SetDescription Serviços de Área de Trabalho Remota, classe Win32_TSGatewayResourceGroup
- Classe Win32_TSGatewayResourceGroup Serviços de Área de Trabalho Remota, método SetDescription
topic_type:
- apiref
api_name:
- Win32_TSGatewayResourceGroup.SetDescription
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d815cc5400a182f2dff3b982643d5e6bfd861002
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105758379"
---
# <a name="setdescription-method-of-the-win32_tsgatewayresourcegroup-class"></a><span data-ttu-id="73e0b-106">Método SetDescription da classe Win32 \_ TSGatewayResourceGroup</span><span class="sxs-lookup"><span data-stu-id="73e0b-106">SetDescription method of the Win32\_TSGatewayResourceGroup class</span></span>

<span data-ttu-id="73e0b-107">Define a propriedade **Description** para o grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="73e0b-107">Sets the **Description** property for the resource group.</span></span>

## <a name="syntax"></a><span data-ttu-id="73e0b-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="73e0b-108">Syntax</span></span>


```mof
uint32 SetDescription(
  [in] string Description
);
```



## <a name="parameters"></a><span data-ttu-id="73e0b-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="73e0b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="73e0b-110">*Descrição* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="73e0b-110">*Description* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="73e0b-111">Descrição do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="73e0b-111">Description of the resource group.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="73e0b-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="73e0b-112">Return value</span></span>

<span data-ttu-id="73e0b-113">Se o método tiver sucesso, ele retornará zero.</span><span class="sxs-lookup"><span data-stu-id="73e0b-113">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="73e0b-114">Se o método não for bem-sucedido, ele retornará um valor diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="73e0b-114">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="73e0b-115">Para obter uma lista de códigos de erro, consulte [serviços de área de trabalho remota códigos de erro do provedor WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="73e0b-115">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="73e0b-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="73e0b-116">Remarks</span></span>

<span data-ttu-id="73e0b-117">Você deve ser um membro do grupo Administradores para chamar esse método.</span><span class="sxs-lookup"><span data-stu-id="73e0b-117">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="73e0b-118">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="73e0b-118">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="73e0b-119">Os arquivos MOF não são instalados como parte do SDK (Software Development Kit) do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="73e0b-119">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="73e0b-120">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="73e0b-120">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="73e0b-121">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="73e0b-121">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="73e0b-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="73e0b-122">Requirements</span></span>



| <span data-ttu-id="73e0b-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="73e0b-123">Requirement</span></span> | <span data-ttu-id="73e0b-124">Valor</span><span class="sxs-lookup"><span data-stu-id="73e0b-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="73e0b-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="73e0b-125">Minimum supported client</span></span><br/> | <span data-ttu-id="73e0b-126">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="73e0b-126">None supported</span></span><br/>                                                                |
| <span data-ttu-id="73e0b-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="73e0b-127">Minimum supported server</span></span><br/> | <span data-ttu-id="73e0b-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="73e0b-128">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="73e0b-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="73e0b-129">Namespace</span></span><br/>                | <span data-ttu-id="73e0b-130">\\TerminalServices da CIMv2 raiz \\</span><span class="sxs-lookup"><span data-stu-id="73e0b-130">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="73e0b-131">MOF</span><span class="sxs-lookup"><span data-stu-id="73e0b-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="73e0b-132"><dt>TS. mof</dt></span><span class="sxs-lookup"><span data-stu-id="73e0b-132"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="73e0b-133">DLL</span><span class="sxs-lookup"><span data-stu-id="73e0b-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="73e0b-134"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="73e0b-134"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="73e0b-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="73e0b-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="73e0b-136">**\_TSGatewayResourceGroup Win32**</span><span class="sxs-lookup"><span data-stu-id="73e0b-136">**Win32\_TSGatewayResourceGroup**</span></span>](win32-tsgatewayresourcegroup.md)
</dt> </dl>

 

