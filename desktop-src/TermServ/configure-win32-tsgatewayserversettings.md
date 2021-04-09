---
title: Configurar o método da classe Win32_TSGatewayServerSettings
description: Define as configurações de IIS e RPC exigidas pelo serviço gateway de Área de Trabalho Remota (gateway de área de trabalho remota).
ms.assetid: 12d7264e-46aa-457f-b89d-547231573db8
ms.tgt_platform: multiple
keywords:
- Configurar o método Serviços de Área de Trabalho Remota
- Configurar o método Serviços de Área de Trabalho Remota, Win32_TSGatewayServerSettings classe
- Classe Win32_TSGatewayServerSettings Serviços de Área de Trabalho Remota, método de configuração
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.Configure
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1880e1a9811c8aab2660993c6c8ab05061163e1a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009035"
---
# <a name="configure-method-of-the-win32_tsgatewayserversettings-class"></a><span data-ttu-id="62535-106">Configurar o método da \_ classe Win32 TSGatewayServerSettings</span><span class="sxs-lookup"><span data-stu-id="62535-106">Configure method of the Win32\_TSGatewayServerSettings class</span></span>

<span data-ttu-id="62535-107">Define as configurações de IIS e RPC exigidas pelo serviço gateway de Área de Trabalho Remota (gateway de área de trabalho remota).</span><span class="sxs-lookup"><span data-stu-id="62535-107">Configures the IIS and RPC settings required by the Remote Desktop Gateway (RD Gateway) service.</span></span>

## <a name="syntax"></a><span data-ttu-id="62535-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="62535-108">Syntax</span></span>


```mof
uint32 Configure();
```



## <a name="parameters"></a><span data-ttu-id="62535-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="62535-109">Parameters</span></span>

<span data-ttu-id="62535-110">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="62535-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="62535-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="62535-111">Return value</span></span>

<span data-ttu-id="62535-112">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="62535-112">Type: **uint32**</span></span>

<span data-ttu-id="62535-113">Se o método tiver sucesso, ele retornará zero.</span><span class="sxs-lookup"><span data-stu-id="62535-113">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="62535-114">Se o método não for bem-sucedido, ele retornará um valor diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="62535-114">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="62535-115">Para obter uma lista de códigos de erro, consulte [serviços de área de trabalho remota códigos de erro do provedor WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="62535-115">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="62535-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="62535-116">Remarks</span></span>

<span data-ttu-id="62535-117">Você deve ser um membro do grupo Administradores para chamar esse método.</span><span class="sxs-lookup"><span data-stu-id="62535-117">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="62535-118">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="62535-118">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="62535-119">Os arquivos MOF não são instalados como parte do SDK (Software Development Kit) do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="62535-119">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="62535-120">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="62535-120">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="62535-121">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="62535-121">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="62535-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="62535-122">Requirements</span></span>



| <span data-ttu-id="62535-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="62535-123">Requirement</span></span> | <span data-ttu-id="62535-124">Valor</span><span class="sxs-lookup"><span data-stu-id="62535-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="62535-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="62535-125">Minimum supported client</span></span><br/> | <span data-ttu-id="62535-126">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="62535-126">None supported</span></span><br/>                                                                |
| <span data-ttu-id="62535-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="62535-127">Minimum supported server</span></span><br/> | <span data-ttu-id="62535-128">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="62535-128">Windows Server 2008 R2</span></span><br/>                                                        |
| <span data-ttu-id="62535-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="62535-129">Namespace</span></span><br/>                | <span data-ttu-id="62535-130">\\TerminalServices da CIMv2 raiz \\</span><span class="sxs-lookup"><span data-stu-id="62535-130">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="62535-131">MOF</span><span class="sxs-lookup"><span data-stu-id="62535-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="62535-132"><dt>TS. mof</dt></span><span class="sxs-lookup"><span data-stu-id="62535-132"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="62535-133">DLL</span><span class="sxs-lookup"><span data-stu-id="62535-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="62535-134"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="62535-134"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="62535-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="62535-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="62535-136">**\_TSGatewayServerSettings Win32**</span><span class="sxs-lookup"><span data-stu-id="62535-136">**Win32\_TSGatewayServerSettings**</span></span>](win32-tsgatewayserversettings.md)
</dt> </dl>

 

