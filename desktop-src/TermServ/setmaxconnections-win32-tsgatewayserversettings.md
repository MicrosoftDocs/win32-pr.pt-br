---
title: Método SetMaxConnections da classe Win32_TSGatewayServerSettings
description: Define as propriedades MaxConnections e UnlimitedConnections, que controlam o número máximo de conexões permitidas para o servidor gateway de Área de Trabalho Remota (Gateway RD).
ms.assetid: cfdbacb7-4969-4ec5-8301-e8020f3af0cd
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método SetMaxConnections
- Método SetMaxConnections Serviços de Área de Trabalho Remota, classe Win32_TSGatewayServerSettings
- Classe Win32_TSGatewayServerSettings Serviços de Área de Trabalho Remota, método SetMaxConnections
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.SetMaxConnections
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c7e8a2fa18491232a058913fd338bb871b0a98aa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105753517"
---
# <a name="setmaxconnections-method-of-the-win32_tsgatewayserversettings-class"></a><span data-ttu-id="9ca10-106">Método SetMaxConnections da classe Win32 \_ TSGatewayServerSettings</span><span class="sxs-lookup"><span data-stu-id="9ca10-106">SetMaxConnections method of the Win32\_TSGatewayServerSettings class</span></span>

<span data-ttu-id="9ca10-107">Define as propriedades **MaxConnections** e **UnlimitedConnections** , que controlam o número máximo de conexões permitidas para o servidor gateway de área de trabalho remota (Gateway RD).</span><span class="sxs-lookup"><span data-stu-id="9ca10-107">Sets the **MaxConnections** and **UnlimitedConnections** properties, which control the maximum number of allowed connections to the Remote Desktop Gateway (RD Gateway) server.</span></span>

## <a name="syntax"></a><span data-ttu-id="9ca10-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9ca10-108">Syntax</span></span>


```mof
uint32 SetMaxConnections(
  [in] uint32  Connections,
  [in] boolean IsUnlimited
);
```



## <a name="parameters"></a><span data-ttu-id="9ca10-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9ca10-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9ca10-110">*Conexões* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="9ca10-110">*Connections* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9ca10-111">Número de conexões que este servidor deve aceitar.</span><span class="sxs-lookup"><span data-stu-id="9ca10-111">Number of connections that this server should accept.</span></span> <span data-ttu-id="9ca10-112">Para um número ilimitado de conexões, defina o parâmetro *Unlimited* como **true**.</span><span class="sxs-lookup"><span data-stu-id="9ca10-112">For an unlimited number of connections, set the *IsUnlimited* parameter to **True**.</span></span>

</dd> <dt>

<span data-ttu-id="9ca10-113">*Islimite* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="9ca10-113">*IsUnlimited* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9ca10-114">Se **for true**, as conexões com o serviço não serão limitadas a um número específico.</span><span class="sxs-lookup"><span data-stu-id="9ca10-114">If **True**, connections to the service are not limited to a specific number.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9ca10-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="9ca10-115">Return value</span></span>

<span data-ttu-id="9ca10-116">Se o método tiver sucesso, ele retornará zero.</span><span class="sxs-lookup"><span data-stu-id="9ca10-116">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="9ca10-117">Se o método não for bem-sucedido, ele retornará um valor diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="9ca10-117">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="9ca10-118">Para obter uma lista de códigos de erro, consulte [serviços de área de trabalho remota códigos de erro do provedor WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="9ca10-118">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="9ca10-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="9ca10-119">Remarks</span></span>

<span data-ttu-id="9ca10-120">Você deve ser um membro do grupo Administradores para chamar esse método.</span><span class="sxs-lookup"><span data-stu-id="9ca10-120">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="9ca10-121">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="9ca10-121">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="9ca10-122">Os arquivos MOF não são instalados como parte do SDK (Software Development Kit) do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="9ca10-122">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="9ca10-123">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="9ca10-123">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="9ca10-124">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="9ca10-124">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="9ca10-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9ca10-125">Requirements</span></span>



| <span data-ttu-id="9ca10-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="9ca10-126">Requirement</span></span> | <span data-ttu-id="9ca10-127">Valor</span><span class="sxs-lookup"><span data-stu-id="9ca10-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="9ca10-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9ca10-128">Minimum supported client</span></span><br/> | <span data-ttu-id="9ca10-129">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="9ca10-129">None supported</span></span><br/>                                                                |
| <span data-ttu-id="9ca10-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9ca10-130">Minimum supported server</span></span><br/> | <span data-ttu-id="9ca10-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9ca10-131">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="9ca10-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="9ca10-132">Namespace</span></span><br/>                | <span data-ttu-id="9ca10-133">\\TerminalServices da CIMv2 raiz \\</span><span class="sxs-lookup"><span data-stu-id="9ca10-133">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="9ca10-134">MOF</span><span class="sxs-lookup"><span data-stu-id="9ca10-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9ca10-135"><dt>TS. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9ca10-135"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="9ca10-136">DLL</span><span class="sxs-lookup"><span data-stu-id="9ca10-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9ca10-137"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9ca10-137"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="9ca10-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="9ca10-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9ca10-139">**\_TSGatewayServerSettings Win32**</span><span class="sxs-lookup"><span data-stu-id="9ca10-139">**Win32\_TSGatewayServerSettings**</span></span>](win32-tsgatewayserversettings.md)
</dt> </dl>

 

