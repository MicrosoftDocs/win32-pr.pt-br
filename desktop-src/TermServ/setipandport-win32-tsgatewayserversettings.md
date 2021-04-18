---
title: Método SetIPAndPort da classe Win32_TSGatewayServerSettings
description: Define o endereço IP de escuta e o número da porta para o transporte especificado.
ms.assetid: f46f4660-31ce-4513-b93d-acd50b42ae0a
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método SetIPAndPort
- Método SetIPAndPort Serviços de Área de Trabalho Remota, classe Win32_TSGatewayServerSettings
- Classe Win32_TSGatewayServerSettings Serviços de Área de Trabalho Remota, método SetIPAndPort
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.SetIPAndPort
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 88870cce628a94ca34b38ccf315edc87a1a734b3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499344"
---
# <a name="setipandport-method-of-the-win32_tsgatewayserversettings-class"></a><span data-ttu-id="8f3d8-106">Método SetIPAndPort da classe Win32 \_ TSGatewayServerSettings</span><span class="sxs-lookup"><span data-stu-id="8f3d8-106">SetIPAndPort method of the Win32\_TSGatewayServerSettings class</span></span>

<span data-ttu-id="8f3d8-107">Define o endereço IP de escuta e o número da porta para o transporte especificado.</span><span class="sxs-lookup"><span data-stu-id="8f3d8-107">Sets the listening IP address and port number for the specified transport.</span></span>

## <a name="syntax"></a><span data-ttu-id="8f3d8-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8f3d8-108">Syntax</span></span>


```mof
uint32 SetIPAndPort(
  [in] uint16  TransportType,
  [in] string  IPAddress,
  [in] uint16  Port,
  [in] boolean OverrideExisting
);
```



## <a name="parameters"></a><span data-ttu-id="8f3d8-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8f3d8-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8f3d8-110">*Transportetype* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="8f3d8-110">*TransportType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8f3d8-111">Especifica o tipo de transporte.</span><span class="sxs-lookup"><span data-stu-id="8f3d8-111">Specifies the transport type.</span></span> <span data-ttu-id="8f3d8-112">Deve ser um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="8f3d8-112">This must be one of the following values.</span></span>

<dt>

<span data-ttu-id="8f3d8-113">0</span><span class="sxs-lookup"><span data-stu-id="8f3d8-113">0</span></span>
</dt> <dd>

<span data-ttu-id="8f3d8-114">RPC sobre transporte HTTP.</span><span class="sxs-lookup"><span data-stu-id="8f3d8-114">RPC over HTTP transport.</span></span>

</dd> <dt>

<span data-ttu-id="8f3d8-115">1</span><span class="sxs-lookup"><span data-stu-id="8f3d8-115">1</span></span>
</dt> <dd>

<span data-ttu-id="8f3d8-116">Transporte HTTP.</span><span class="sxs-lookup"><span data-stu-id="8f3d8-116">HTTP transport.</span></span>

</dd> <dt>

<span data-ttu-id="8f3d8-117">2</span><span class="sxs-lookup"><span data-stu-id="8f3d8-117">2</span></span>
</dt> <dd>

<span data-ttu-id="8f3d8-118">Transporte UDP.</span><span class="sxs-lookup"><span data-stu-id="8f3d8-118">UDP transport.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="8f3d8-119">*IPAddress* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="8f3d8-119">*IPAddress* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8f3d8-120">Especifica o endereço IP de escuta, em formato de octeto (por exemplo, "192.168.1.1").</span><span class="sxs-lookup"><span data-stu-id="8f3d8-120">Specifies the listening IP address, in octet form (for example, "192.168.1.1").</span></span>

</dd> <dt>

<span data-ttu-id="8f3d8-121">*Porta* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="8f3d8-121">*Port* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8f3d8-122">Especifica o número da porta de escuta.</span><span class="sxs-lookup"><span data-stu-id="8f3d8-122">Specifies the listening port number.</span></span>

</dd> <dt>

<span data-ttu-id="8f3d8-123">*OverrideExisting* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="8f3d8-123">*OverrideExisting* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8f3d8-124">Indica se a associação de IP/porta existente deve ser substituída para HTTP.</span><span class="sxs-lookup"><span data-stu-id="8f3d8-124">Indicates whether to override the existing IP/Port binding for HTTP.</span></span> <span data-ttu-id="8f3d8-125">Esse parâmetro só será usado se o parâmetro *TransportType* contiver 0 (RPC sobre http) ou 1 (http).</span><span class="sxs-lookup"><span data-stu-id="8f3d8-125">This parameter is only used if the *TransportType* parameter contains 0 (RPC over HTTP) or 1 (HTTP).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8f3d8-126">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="8f3d8-126">Return value</span></span>

<span data-ttu-id="8f3d8-127">Se o método tiver sucesso, ele retornará zero.</span><span class="sxs-lookup"><span data-stu-id="8f3d8-127">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="8f3d8-128">Se o método não for bem-sucedido, ele retornará um valor diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="8f3d8-128">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="8f3d8-129">Para obter uma lista de códigos de erro, consulte [serviços de área de trabalho remota códigos de erro do provedor WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="8f3d8-129">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="8f3d8-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8f3d8-130">Requirements</span></span>



| <span data-ttu-id="8f3d8-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="8f3d8-131">Requirement</span></span> | <span data-ttu-id="8f3d8-132">Valor</span><span class="sxs-lookup"><span data-stu-id="8f3d8-132">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="8f3d8-133">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8f3d8-133">Minimum supported client</span></span><br/> | <span data-ttu-id="8f3d8-134">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="8f3d8-134">None supported</span></span><br/>                                                                |
| <span data-ttu-id="8f3d8-135">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8f3d8-135">Minimum supported server</span></span><br/> | <span data-ttu-id="8f3d8-136">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="8f3d8-136">Windows Server 2012</span></span><br/>                                                           |
| <span data-ttu-id="8f3d8-137">Namespace</span><span class="sxs-lookup"><span data-stu-id="8f3d8-137">Namespace</span></span><br/>                | <span data-ttu-id="8f3d8-138">\\TerminalServices da CIMv2 raiz \\</span><span class="sxs-lookup"><span data-stu-id="8f3d8-138">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="8f3d8-139">MOF</span><span class="sxs-lookup"><span data-stu-id="8f3d8-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8f3d8-140"><dt>TS. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8f3d8-140"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="8f3d8-141">DLL</span><span class="sxs-lookup"><span data-stu-id="8f3d8-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8f3d8-142"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8f3d8-142"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="8f3d8-143">Confira também</span><span class="sxs-lookup"><span data-stu-id="8f3d8-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8f3d8-144">**\_TSGatewayServerSettings Win32**</span><span class="sxs-lookup"><span data-stu-id="8f3d8-144">**Win32\_TSGatewayServerSettings**</span></span>](win32-tsgatewayserversettings.md)
</dt> </dl>

 

 





