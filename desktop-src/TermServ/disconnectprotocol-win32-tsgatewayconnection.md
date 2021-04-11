---
title: Método DisconnectProtocol da classe Win32_TSGatewayConnection
description: Desconecta todas as conexões do protocolo especificado do servidor gateway de Área de Trabalho Remota (gateway de área de trabalho remota).
ms.assetid: 0ca3f478-dfdc-404e-ac17-43b6873b7256
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método DisconnectProtocol
- Método DisconnectProtocol Serviços de Área de Trabalho Remota, classe Win32_TSGatewayConnection
- Classe Win32_TSGatewayConnection Serviços de Área de Trabalho Remota, método DisconnectProtocol
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnection.DisconnectProtocol
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 53a37050cbd622c6fea14b8b4e5dc6a414eaad85
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104295813"
---
# <a name="disconnectprotocol-method-of-the-win32_tsgatewayconnection-class"></a><span data-ttu-id="e3a17-106">Método DisconnectProtocol da classe Win32 \_ TSGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="e3a17-106">DisconnectProtocol method of the Win32\_TSGatewayConnection class</span></span>

<span data-ttu-id="e3a17-107">Desconecta todas as conexões do protocolo especificado do servidor gateway de Área de Trabalho Remota (gateway de área de trabalho remota).</span><span class="sxs-lookup"><span data-stu-id="e3a17-107">Disconnects all connections of the specified protocol from the Remote Desktop Gateway (RD Gateway) server.</span></span>

## <a name="syntax"></a><span data-ttu-id="e3a17-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e3a17-108">Syntax</span></span>


```mof
uint32 DisconnectProtocol(
  [in] string ProtocolName
);
```



## <a name="parameters"></a><span data-ttu-id="e3a17-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e3a17-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e3a17-110">*ProtocolName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e3a17-110">*ProtocolName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e3a17-111">O nome do protocolo para uma conexão específica.</span><span class="sxs-lookup"><span data-stu-id="e3a17-111">The protocol name for a specific connection.</span></span> <span data-ttu-id="e3a17-112">Isso pode ser recuperado da propriedade **ProtocolName** da classe **Win32 \_ TSGatewayConnection** .</span><span class="sxs-lookup"><span data-stu-id="e3a17-112">This can be retrieved from the **ProtocolName** property of the **Win32\_TSGatewayConnection** class.</span></span>

<dt>

<span data-ttu-id="e3a17-113">CALs</span><span class="sxs-lookup"><span data-stu-id="e3a17-113">"TS"</span></span>
</dt> <dd>

<span data-ttu-id="e3a17-114">O protocolo para o servidor de gateway de área de trabalho remota.</span><span class="sxs-lookup"><span data-stu-id="e3a17-114">The protocol for the RD Gateway server.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e3a17-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e3a17-115">Return value</span></span>

<span data-ttu-id="e3a17-116">Se o método tiver sucesso, ele retornará zero.</span><span class="sxs-lookup"><span data-stu-id="e3a17-116">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="e3a17-117">Se o método não for bem-sucedido, ele retornará um valor diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="e3a17-117">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="e3a17-118">Para obter uma lista de códigos de erro, consulte [serviços de área de trabalho remota códigos de erro do provedor WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="e3a17-118">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="e3a17-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="e3a17-119">Remarks</span></span>

<span data-ttu-id="e3a17-120">Você deve ser um membro do grupo Administradores para chamar esse método.</span><span class="sxs-lookup"><span data-stu-id="e3a17-120">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="e3a17-121">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="e3a17-121">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="e3a17-122">Os arquivos MOF não são instalados como parte do SDK (Software Development Kit) do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="e3a17-122">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="e3a17-123">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="e3a17-123">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="e3a17-124">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="e3a17-124">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="e3a17-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e3a17-125">Requirements</span></span>



| <span data-ttu-id="e3a17-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="e3a17-126">Requirement</span></span> | <span data-ttu-id="e3a17-127">Valor</span><span class="sxs-lookup"><span data-stu-id="e3a17-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="e3a17-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e3a17-128">Minimum supported client</span></span><br/> | <span data-ttu-id="e3a17-129">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="e3a17-129">None supported</span></span><br/>                                                                |
| <span data-ttu-id="e3a17-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e3a17-130">Minimum supported server</span></span><br/> | <span data-ttu-id="e3a17-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e3a17-131">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="e3a17-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="e3a17-132">Namespace</span></span><br/>                | <span data-ttu-id="e3a17-133">\\TerminalServices da CIMv2 raiz \\</span><span class="sxs-lookup"><span data-stu-id="e3a17-133">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="e3a17-134">MOF</span><span class="sxs-lookup"><span data-stu-id="e3a17-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e3a17-135"><dt>TS. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e3a17-135"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="e3a17-136">DLL</span><span class="sxs-lookup"><span data-stu-id="e3a17-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e3a17-137"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e3a17-137"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="e3a17-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="e3a17-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e3a17-139">**\_TSGatewayConnection Win32**</span><span class="sxs-lookup"><span data-stu-id="e3a17-139">**Win32\_TSGatewayConnection**</span></span>](win32-tsgatewayconnection.md)
</dt> </dl>

 

