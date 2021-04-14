---
title: Método EnableCentralCAP da classe Win32_TSGatewayServerSettings
description: Controla a propriedade CentralCAPEnabled, que controla as políticas de autorização de conexão do Serviços de Área de Trabalho Remota (RD \ 160; CAPs) para o servidor do gateway de Área de Trabalho Remota (Gateway RD).
ms.assetid: 43e476df-714d-43bd-b40f-33511b7757a4
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método EnableCentralCAP
- Método EnableCentralCAP Serviços de Área de Trabalho Remota, classe Win32_TSGatewayServerSettings
- Classe Win32_TSGatewayServerSettings Serviços de Área de Trabalho Remota, método EnableCentralCAP
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.EnableCentralCAP
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 933e91a89f9a5afdcd2ae85fa6cb097ef0c29cd2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369933"
---
# <a name="enablecentralcap-method-of-the-win32_tsgatewayserversettings-class"></a><span data-ttu-id="8e72d-106">Método EnableCentralCAP da classe Win32 \_ TSGatewayServerSettings</span><span class="sxs-lookup"><span data-stu-id="8e72d-106">EnableCentralCAP method of the Win32\_TSGatewayServerSettings class</span></span>

<span data-ttu-id="8e72d-107">Controla a propriedade **CentralCAPEnabled** , que controla a serviços de área de trabalho remota RD CAPs (políticas de autorização de conexão) para o servidor de gateway de área de trabalho remota (gateway de área de trabalho remota).</span><span class="sxs-lookup"><span data-stu-id="8e72d-107">Controls the **CentralCAPEnabled** property, which controls the Remote Desktop Services connection authorization policies (RD CAPs) for the Remote Desktop Gateway (RD Gateway) server.</span></span>

## <a name="syntax"></a><span data-ttu-id="8e72d-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8e72d-108">Syntax</span></span>


```mof
uint32 EnableCentralCAP(
  [in] boolean CentralCAPEnabled
);
```



## <a name="parameters"></a><span data-ttu-id="8e72d-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8e72d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8e72d-110">*CentralCAPEnabled* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="8e72d-110">*CentralCAPEnabled* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8e72d-111">Se definido como **true**, as RD CAPs dos servidores de RD CAP central serão usadas.</span><span class="sxs-lookup"><span data-stu-id="8e72d-111">If set to **True**, RD CAPs from central RD CAP servers will be used.</span></span> <span data-ttu-id="8e72d-112">Se definido como **false**, somente as políticas do servidor local serão usadas.</span><span class="sxs-lookup"><span data-stu-id="8e72d-112">If set to **False**, only policies from the local server will be used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8e72d-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="8e72d-113">Return value</span></span>

<span data-ttu-id="8e72d-114">Se o método tiver sucesso, ele retornará zero.</span><span class="sxs-lookup"><span data-stu-id="8e72d-114">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="8e72d-115">Se o método não for bem-sucedido, ele retornará um valor diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="8e72d-115">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="8e72d-116">Para obter uma lista de códigos de erro, consulte [serviços de área de trabalho remota códigos de erro do provedor WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="8e72d-116">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="8e72d-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="8e72d-117">Remarks</span></span>

<span data-ttu-id="8e72d-118">Você deve ser um membro do grupo Administradores para chamar esse método.</span><span class="sxs-lookup"><span data-stu-id="8e72d-118">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="8e72d-119">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="8e72d-119">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="8e72d-120">Os arquivos MOF não são instalados como parte do SDK (Software Development Kit) do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="8e72d-120">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="8e72d-121">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="8e72d-121">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="8e72d-122">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="8e72d-122">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="8e72d-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8e72d-123">Requirements</span></span>



| <span data-ttu-id="8e72d-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="8e72d-124">Requirement</span></span> | <span data-ttu-id="8e72d-125">Valor</span><span class="sxs-lookup"><span data-stu-id="8e72d-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="8e72d-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8e72d-126">Minimum supported client</span></span><br/> | <span data-ttu-id="8e72d-127">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="8e72d-127">None supported</span></span><br/>                                                                |
| <span data-ttu-id="8e72d-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8e72d-128">Minimum supported server</span></span><br/> | <span data-ttu-id="8e72d-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8e72d-129">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="8e72d-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="8e72d-130">Namespace</span></span><br/>                | <span data-ttu-id="8e72d-131">\\TerminalServices da CIMv2 raiz \\</span><span class="sxs-lookup"><span data-stu-id="8e72d-131">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="8e72d-132">MOF</span><span class="sxs-lookup"><span data-stu-id="8e72d-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8e72d-133"><dt>TS. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8e72d-133"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="8e72d-134">DLL</span><span class="sxs-lookup"><span data-stu-id="8e72d-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8e72d-135"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8e72d-135"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="8e72d-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="8e72d-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8e72d-137">**\_TSGatewayServerSettings Win32**</span><span class="sxs-lookup"><span data-stu-id="8e72d-137">**Win32\_TSGatewayServerSettings**</span></span>](win32-tsgatewayserversettings.md)
</dt> </dl>

 

