---
title: Método CheckStatus da classe Win32_TSGatewayConnection
description: Verifica o status de uma conexão de servidor de gateway de Área de Trabalho Remota (gateway de área de trabalho remota) com outro computador e determina se o computador de destino está configurado para balanceamento de carga.
ms.assetid: e8ee3d40-76eb-401f-b255-bccd7ba8c058
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método CheckStatus
- Método CheckStatus Serviços de Área de Trabalho Remota, classe Win32_TSGatewayConnection
- Classe Win32_TSGatewayConnection Serviços de Área de Trabalho Remota, método CheckStatus
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnection.CheckStatus
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: babb083af5c0581abe27d442a466c3d6114b957a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105761334"
---
# <a name="checkstatus-method-of-the-win32_tsgatewayconnection-class"></a><span data-ttu-id="a09a0-106">Método CheckStatus da classe Win32 \_ TSGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="a09a0-106">CheckStatus method of the Win32\_TSGatewayConnection class</span></span>

<span data-ttu-id="a09a0-107">Verifica o status de uma conexão de servidor de gateway de Área de Trabalho Remota (gateway de área de trabalho remota) com outro computador e determina se o computador de destino está configurado para balanceamento de carga.</span><span class="sxs-lookup"><span data-stu-id="a09a0-107">Checks the status of a Remote Desktop Gateway (RD Gateway) server connection to another computer, and determines whether the target computer is configured for load balancing.</span></span>

## <a name="syntax"></a><span data-ttu-id="a09a0-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a09a0-108">Syntax</span></span>


```mof
uint32 CheckStatus(
  [in] string ServerName,
  [in] string EndPointName
);
```



## <a name="parameters"></a><span data-ttu-id="a09a0-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a09a0-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a09a0-110">*Nome do Server* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a09a0-110">*ServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a09a0-111">O nome do servidor de gateway RD de origem do qual a conexão é verificada.</span><span class="sxs-lookup"><span data-stu-id="a09a0-111">The name of the source RD Gateway server from which the connection is checked.</span></span>

</dd> <dt>

<span data-ttu-id="a09a0-112">*Ponto de extremidade* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a09a0-112">*EndPointName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a09a0-113">O nome do servidor de destino (o ponto de extremidade) ao qual o acesso é verificado no servidor de origem.</span><span class="sxs-lookup"><span data-stu-id="a09a0-113">The name of the target server (the endpoint) to which access is checked from the source server.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a09a0-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a09a0-114">Return value</span></span>

<span data-ttu-id="a09a0-115">Esse método retorna os seguintes valores de retorno possíveis.</span><span class="sxs-lookup"><span data-stu-id="a09a0-115">This method returns the following possible return values.</span></span>

<dl> <dt>


</dt> <dd>

<span data-ttu-id="a09a0-116">0</span><span class="sxs-lookup"><span data-stu-id="a09a0-116">0</span></span>

<span data-ttu-id="a09a0-117">O status da conexão é OK.</span><span class="sxs-lookup"><span data-stu-id="a09a0-117">The connection status is OK.</span></span> <span data-ttu-id="a09a0-118">O ponto de extremidade está acessível e está configurado para balanceamento de carga.</span><span class="sxs-lookup"><span data-stu-id="a09a0-118">The endpoint is reachable and is configured for load balancing.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="a09a0-119">1</span><span class="sxs-lookup"><span data-stu-id="a09a0-119">1</span></span>

<span data-ttu-id="a09a0-120">O status da conexão é desconhecido.</span><span class="sxs-lookup"><span data-stu-id="a09a0-120">The connection status is unknown.</span></span> <span data-ttu-id="a09a0-121">Provavelmente, ocorreu uma exceção.</span><span class="sxs-lookup"><span data-stu-id="a09a0-121">Most likely, an exception occurred.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="a09a0-122">0x80075c34</span><span class="sxs-lookup"><span data-stu-id="a09a0-122">0x80075c34</span></span>

<span data-ttu-id="a09a0-123">O ponto de extremidade não pode ser acessado ou não está configurado para balanceamento de carga.</span><span class="sxs-lookup"><span data-stu-id="a09a0-123">The endpoint is either not reachable, or it is not configured for load balancing.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="a09a0-124">0x80075c32</span><span class="sxs-lookup"><span data-stu-id="a09a0-124">0x80075c32</span></span>

<span data-ttu-id="a09a0-125">Ocorreu um erro de status.</span><span class="sxs-lookup"><span data-stu-id="a09a0-125">A status error occurred.</span></span> <span data-ttu-id="a09a0-126">O ponto de extremidade está acessível, mas o serviço de balanceamento de carga RPC/HTTP (RPCHTTPLBS) não foi iniciado no computador de destino.</span><span class="sxs-lookup"><span data-stu-id="a09a0-126">The endpoint is reachable, but the RPC/HTTP Load Balancing Service (RPCHTTPLBS) service is not started on the target computer.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a09a0-127">Comentários</span><span class="sxs-lookup"><span data-stu-id="a09a0-127">Remarks</span></span>

<span data-ttu-id="a09a0-128">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="a09a0-128">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="a09a0-129">Os arquivos MOF não são instalados como parte do SDK (Software Development Kit) do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="a09a0-129">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="a09a0-130">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="a09a0-130">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="a09a0-131">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="a09a0-131">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="a09a0-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a09a0-132">Requirements</span></span>



| <span data-ttu-id="a09a0-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="a09a0-133">Requirement</span></span> | <span data-ttu-id="a09a0-134">Valor</span><span class="sxs-lookup"><span data-stu-id="a09a0-134">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="a09a0-135">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a09a0-135">Minimum supported client</span></span><br/> | <span data-ttu-id="a09a0-136">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="a09a0-136">None supported</span></span><br/>                                                                |
| <span data-ttu-id="a09a0-137">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a09a0-137">Minimum supported server</span></span><br/> | <span data-ttu-id="a09a0-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a09a0-138">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="a09a0-139">Namespace</span><span class="sxs-lookup"><span data-stu-id="a09a0-139">Namespace</span></span><br/>                | <span data-ttu-id="a09a0-140">\\TerminalServices da CIMv2 raiz \\</span><span class="sxs-lookup"><span data-stu-id="a09a0-140">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="a09a0-141">MOF</span><span class="sxs-lookup"><span data-stu-id="a09a0-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a09a0-142"><dt>TS. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a09a0-142"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="a09a0-143">DLL</span><span class="sxs-lookup"><span data-stu-id="a09a0-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a09a0-144"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a09a0-144"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="a09a0-145">Confira também</span><span class="sxs-lookup"><span data-stu-id="a09a0-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a09a0-146">**\_TSGatewayConnection Win32**</span><span class="sxs-lookup"><span data-stu-id="a09a0-146">**Win32\_TSGatewayConnection**</span></span>](win32-tsgatewayconnection.md)
</dt> </dl>

 

