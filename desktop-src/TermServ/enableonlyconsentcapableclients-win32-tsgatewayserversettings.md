---
title: Método EnableOnlyConsentCapableClients da classe Win32_TSGatewayServerSettings
description: Define a propriedade OnlyConsentCapableClients.
ms.assetid: abc91ea8-0f3c-4b7c-9091-3c8193e610da
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método EnableOnlyConsentCapableClients
- Método EnableOnlyConsentCapableClients Serviços de Área de Trabalho Remota, classe Win32_TSGatewayServerSettings
- Classe Win32_TSGatewayServerSettings Serviços de Área de Trabalho Remota, método EnableOnlyConsentCapableClients
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.EnableOnlyConsentCapableClients
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb671ccefe98cdc1b569bcde155071ef7cc0d9ad
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009094"
---
# <a name="enableonlyconsentcapableclients-method-of-the-win32_tsgatewayserversettings-class"></a><span data-ttu-id="0577d-106">Método EnableOnlyConsentCapableClients da classe Win32 \_ TSGatewayServerSettings</span><span class="sxs-lookup"><span data-stu-id="0577d-106">EnableOnlyConsentCapableClients method of the Win32\_TSGatewayServerSettings class</span></span>

<span data-ttu-id="0577d-107">Define a propriedade **OnlyConsentCapableClients** .</span><span class="sxs-lookup"><span data-stu-id="0577d-107">Sets the **OnlyConsentCapableClients** property.</span></span>

## <a name="syntax"></a><span data-ttu-id="0577d-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0577d-108">Syntax</span></span>


```mof
uint32 EnableOnlyConsentCapableClients(
  [in] boolean OnlyConsentCapableClients
);
```



## <a name="parameters"></a><span data-ttu-id="0577d-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0577d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0577d-110">*OnlyConsentCapableClients* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="0577d-110">*OnlyConsentCapableClients* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0577d-111">Tipo: **booliano**</span><span class="sxs-lookup"><span data-stu-id="0577d-111">Type: **boolean**</span></span>

<span data-ttu-id="0577d-112">Especifica o novo valor para a propriedade **OnlyConsentCapableClients** .</span><span class="sxs-lookup"><span data-stu-id="0577d-112">Specifies the new value for the **OnlyConsentCapableClients** property.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0577d-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="0577d-113">Return value</span></span>

<span data-ttu-id="0577d-114">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0577d-114">Type: **uint32**</span></span>

<span data-ttu-id="0577d-115">Se o método tiver sucesso, ele retornará zero.</span><span class="sxs-lookup"><span data-stu-id="0577d-115">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="0577d-116">Se o método não for bem-sucedido, ele retornará um valor diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="0577d-116">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="0577d-117">Para obter uma lista de códigos de erro, consulte [serviços de área de trabalho remota códigos de erro do provedor WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="0577d-117">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="0577d-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="0577d-118">Remarks</span></span>

<span data-ttu-id="0577d-119">Você deve ser um membro do grupo Administradores para chamar esse método.</span><span class="sxs-lookup"><span data-stu-id="0577d-119">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="0577d-120">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="0577d-120">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="0577d-121">Os arquivos MOF não são instalados como parte do SDK (Software Development Kit) do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="0577d-121">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="0577d-122">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="0577d-122">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="0577d-123">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="0577d-123">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="0577d-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0577d-124">Requirements</span></span>



| <span data-ttu-id="0577d-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="0577d-125">Requirement</span></span> | <span data-ttu-id="0577d-126">Valor</span><span class="sxs-lookup"><span data-stu-id="0577d-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="0577d-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0577d-127">Minimum supported client</span></span><br/> | <span data-ttu-id="0577d-128">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="0577d-128">None supported</span></span><br/>                                                                |
| <span data-ttu-id="0577d-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0577d-129">Minimum supported server</span></span><br/> | <span data-ttu-id="0577d-130">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="0577d-130">Windows Server 2008 R2</span></span><br/>                                                        |
| <span data-ttu-id="0577d-131">Namespace</span><span class="sxs-lookup"><span data-stu-id="0577d-131">Namespace</span></span><br/>                | <span data-ttu-id="0577d-132">\\TerminalServices da CIMv2 raiz \\</span><span class="sxs-lookup"><span data-stu-id="0577d-132">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="0577d-133">MOF</span><span class="sxs-lookup"><span data-stu-id="0577d-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0577d-134"><dt>TS. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0577d-134"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="0577d-135">DLL</span><span class="sxs-lookup"><span data-stu-id="0577d-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0577d-136"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0577d-136"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="0577d-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="0577d-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0577d-138">**\_TSGatewayServerSettings Win32**</span><span class="sxs-lookup"><span data-stu-id="0577d-138">**Win32\_TSGatewayServerSettings**</span></span>](win32-tsgatewayserversettings.md)
</dt> </dl>

 

