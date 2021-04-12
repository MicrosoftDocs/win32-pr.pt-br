---
title: Método GetIPAndPort da classe Win32_TSGatewayServerSettings
description: Obtém o endereço IP de escuta e o número da porta para o transporte especificado.
ms.assetid: e12451c3-2641-49e1-bd35-f7cab37865ae
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método GetIPAndPort
- Método GetIPAndPort Serviços de Área de Trabalho Remota, classe Win32_TSGatewayServerSettings
- Classe Win32_TSGatewayServerSettings Serviços de Área de Trabalho Remota, método GetIPAndPort
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.GetIPAndPort
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 260cc45961720ae8d175d4df3e84edc7a0c15c13
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104294776"
---
# <a name="getipandport-method-of-the-win32_tsgatewayserversettings-class"></a><span data-ttu-id="8fe92-106">Método GetIPAndPort da classe Win32 \_ TSGatewayServerSettings</span><span class="sxs-lookup"><span data-stu-id="8fe92-106">GetIPAndPort method of the Win32\_TSGatewayServerSettings class</span></span>

<span data-ttu-id="8fe92-107">Obtém o endereço IP de escuta e o número da porta para o transporte especificado.</span><span class="sxs-lookup"><span data-stu-id="8fe92-107">Obtains the listening IP address and port number for the specified transport.</span></span>

## <a name="syntax"></a><span data-ttu-id="8fe92-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8fe92-108">Syntax</span></span>


```mof
uint32 GetIPAndPort(
  [in]  uint16 TransportType,
  [out] string IPAddress,
  [out] uint16 Port
);
```



## <a name="parameters"></a><span data-ttu-id="8fe92-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8fe92-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8fe92-110">*Transportetype* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="8fe92-110">*TransportType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8fe92-111">Especifica o tipo de transporte.</span><span class="sxs-lookup"><span data-stu-id="8fe92-111">Specifies the transport type.</span></span> <span data-ttu-id="8fe92-112">Deve ser um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="8fe92-112">This must be one of the following values.</span></span>

<dt>

<span data-ttu-id="8fe92-113">0</span><span class="sxs-lookup"><span data-stu-id="8fe92-113">0</span></span>
</dt> <dd>

<span data-ttu-id="8fe92-114">RPC sobre transporte HTTP.</span><span class="sxs-lookup"><span data-stu-id="8fe92-114">RPC over HTTP transport.</span></span>

</dd> <dt>

<span data-ttu-id="8fe92-115">1</span><span class="sxs-lookup"><span data-stu-id="8fe92-115">1</span></span>
</dt> <dd>

<span data-ttu-id="8fe92-116">Transporte HTTP.</span><span class="sxs-lookup"><span data-stu-id="8fe92-116">HTTP transport.</span></span>

</dd> <dt>

<span data-ttu-id="8fe92-117">2</span><span class="sxs-lookup"><span data-stu-id="8fe92-117">2</span></span>
</dt> <dd>

<span data-ttu-id="8fe92-118">Transporte UDP.</span><span class="sxs-lookup"><span data-stu-id="8fe92-118">UDP transport.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="8fe92-119">*IPAddress* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="8fe92-119">*IPAddress* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8fe92-120">Uma cadeia de caracteres que recebe o endereço IP de escuta, em formato de octeto (por exemplo, "192.168.1.1").</span><span class="sxs-lookup"><span data-stu-id="8fe92-120">A string that receives the listening IP address, in octet form (for example, "192.168.1.1").</span></span>

</dd> <dt>

<span data-ttu-id="8fe92-121">*Porta* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="8fe92-121">*Port* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8fe92-122">Especifica o número da porta de escuta.</span><span class="sxs-lookup"><span data-stu-id="8fe92-122">Specifies the listening port number.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8fe92-123">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="8fe92-123">Return value</span></span>

<span data-ttu-id="8fe92-124">Se o método tiver sucesso, ele retornará zero.</span><span class="sxs-lookup"><span data-stu-id="8fe92-124">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="8fe92-125">Se o método não for bem-sucedido, ele retornará um valor diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="8fe92-125">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="8fe92-126">Para obter uma lista de códigos de erro, consulte [serviços de área de trabalho remota códigos de erro do provedor WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="8fe92-126">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="8fe92-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8fe92-127">Requirements</span></span>



| <span data-ttu-id="8fe92-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="8fe92-128">Requirement</span></span> | <span data-ttu-id="8fe92-129">Valor</span><span class="sxs-lookup"><span data-stu-id="8fe92-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="8fe92-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8fe92-130">Minimum supported client</span></span><br/> | <span data-ttu-id="8fe92-131">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="8fe92-131">None supported</span></span><br/>                                                                |
| <span data-ttu-id="8fe92-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8fe92-132">Minimum supported server</span></span><br/> | <span data-ttu-id="8fe92-133">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="8fe92-133">Windows Server 2012</span></span><br/>                                                           |
| <span data-ttu-id="8fe92-134">Namespace</span><span class="sxs-lookup"><span data-stu-id="8fe92-134">Namespace</span></span><br/>                | <span data-ttu-id="8fe92-135">\\TerminalServices da CIMv2 raiz \\</span><span class="sxs-lookup"><span data-stu-id="8fe92-135">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="8fe92-136">MOF</span><span class="sxs-lookup"><span data-stu-id="8fe92-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8fe92-137"><dt>TS. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8fe92-137"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="8fe92-138">DLL</span><span class="sxs-lookup"><span data-stu-id="8fe92-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8fe92-139"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8fe92-139"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="8fe92-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="8fe92-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8fe92-141">**\_TSGatewayServerSettings Win32**</span><span class="sxs-lookup"><span data-stu-id="8fe92-141">**Win32\_TSGatewayServerSettings**</span></span>](win32-tsgatewayserversettings.md)
</dt> </dl>

 

 





