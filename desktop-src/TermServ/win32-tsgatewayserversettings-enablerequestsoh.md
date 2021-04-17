---
title: Método EnableRequestSOH da classe Win32_TSGatewayServerSettings
description: O EnableRequestSOH não está mais disponível.
ms.assetid: 4feb7530-cced-4ead-a1fb-679b81442bb3
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método EnableRequestSOH
- Método EnableRequestSOH Serviços de Área de Trabalho Remota, classe Win32_TSGatewayServerSettings
- Classe Win32_TSGatewayServerSettings Serviços de Área de Trabalho Remota, método EnableRequestSOH
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.EnableRequestSOH
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a90ed6a3929b50d13a27ec559aab534f9e06f738
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105755151"
---
# <a name="enablerequestsoh-method-of-the-win32_tsgatewayserversettings-class"></a><span data-ttu-id="a5a7a-106">Método EnableRequestSOH da classe Win32 \_ TSGatewayServerSettings</span><span class="sxs-lookup"><span data-stu-id="a5a7a-106">EnableRequestSOH method of the Win32\_TSGatewayServerSettings class</span></span>

<span data-ttu-id="a5a7a-107">\[O método **EnableRequestSOH** não está mais disponível a partir do Windows Server 2016.\]</span><span class="sxs-lookup"><span data-stu-id="a5a7a-107">\[The **EnableRequestSOH** method is no longer available as of Windows Server 2016.\]</span></span>

<span data-ttu-id="a5a7a-108">Habilita ou desabilita solicitações para uma SoH (declaração de integridade).</span><span class="sxs-lookup"><span data-stu-id="a5a7a-108">Enables or disables requests for a Statement of Health (SoH).</span></span>

## <a name="syntax"></a><span data-ttu-id="a5a7a-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a5a7a-109">Syntax</span></span>


```mof
uint32 EnableRequestSOH(
  [in] boolean RequestSOH
);
```



## <a name="parameters"></a><span data-ttu-id="a5a7a-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a5a7a-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a5a7a-111">*RequestSOH* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a5a7a-111">*RequestSOH* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a5a7a-112">Especifique **true** para habilitar o recurso ou **false** para desabilitar o recurso.</span><span class="sxs-lookup"><span data-stu-id="a5a7a-112">Specify **TRUE** to enable the feature or **FALSE** to disable the feature.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a5a7a-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a5a7a-113">Return value</span></span>

<span data-ttu-id="a5a7a-114">Se o método tiver sucesso, ele retornará zero.</span><span class="sxs-lookup"><span data-stu-id="a5a7a-114">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="a5a7a-115">Se o método não for bem-sucedido, ele retornará um valor diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="a5a7a-115">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="a5a7a-116">Para obter uma lista de códigos de erro, consulte [serviços de área de trabalho remota códigos de erro do provedor WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="a5a7a-116">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="a5a7a-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="a5a7a-117">Remarks</span></span>

<span data-ttu-id="a5a7a-118">Você deve ser um membro do grupo Administradores para chamar esse método.</span><span class="sxs-lookup"><span data-stu-id="a5a7a-118">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="a5a7a-119">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="a5a7a-119">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="a5a7a-120">Os arquivos MOF não são instalados como parte do SDK (Software Development Kit) do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="a5a7a-120">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="a5a7a-121">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="a5a7a-121">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="a5a7a-122">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="a5a7a-122">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="a5a7a-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a5a7a-123">Requirements</span></span>



| <span data-ttu-id="a5a7a-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="a5a7a-124">Requirement</span></span> | <span data-ttu-id="a5a7a-125">Valor</span><span class="sxs-lookup"><span data-stu-id="a5a7a-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="a5a7a-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a5a7a-126">Minimum supported client</span></span><br/> | <span data-ttu-id="a5a7a-127">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="a5a7a-127">None supported</span></span><br/>                                                                |
| <span data-ttu-id="a5a7a-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a5a7a-128">Minimum supported server</span></span><br/> | <span data-ttu-id="a5a7a-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a5a7a-129">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="a5a7a-130">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="a5a7a-130">End of server support</span></span><br/>    | <span data-ttu-id="a5a7a-131">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="a5a7a-131">Windows Server 2012 R2</span></span><br/>                                                        |
| <span data-ttu-id="a5a7a-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="a5a7a-132">Namespace</span></span><br/>                | <span data-ttu-id="a5a7a-133">\\TerminalServices da CIMv2 raiz \\</span><span class="sxs-lookup"><span data-stu-id="a5a7a-133">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="a5a7a-134">MOF</span><span class="sxs-lookup"><span data-stu-id="a5a7a-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a5a7a-135"><dt>TS. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a5a7a-135"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="a5a7a-136">DLL</span><span class="sxs-lookup"><span data-stu-id="a5a7a-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a5a7a-137"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a5a7a-137"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="a5a7a-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="a5a7a-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a5a7a-139">**\_TSGatewayServerSettings Win32**</span><span class="sxs-lookup"><span data-stu-id="a5a7a-139">**Win32\_TSGatewayServerSettings**</span></span>](win32-tsgatewayserversettings.md)
</dt> </dl>

 

