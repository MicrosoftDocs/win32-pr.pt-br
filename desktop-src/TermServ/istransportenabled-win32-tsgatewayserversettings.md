---
title: Método IsTransportEnabled da classe Win32_TSGatewayServerSettings
description: Determina se o transporte especificado está habilitado.
ms.assetid: 3f08a206-5800-4088-a113-bb3f0cc826f2
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método IsTransportEnabled
- Método IsTransportEnabled Serviços de Área de Trabalho Remota, classe Win32_TSGatewayServerSettings
- Classe Win32_TSGatewayServerSettings Serviços de Área de Trabalho Remota, método IsTransportEnabled
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.IsTransportEnabled
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: da152499138f6c1aba1ff6477c719aa0e787deee
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085484"
---
# <a name="istransportenabled-method-of-the-win32_tsgatewayserversettings-class"></a><span data-ttu-id="afd92-106">Método IsTransportEnabled da classe Win32 \_ TSGatewayServerSettings</span><span class="sxs-lookup"><span data-stu-id="afd92-106">IsTransportEnabled method of the Win32\_TSGatewayServerSettings class</span></span>

<span data-ttu-id="afd92-107">Determina se o transporte especificado está habilitado.</span><span class="sxs-lookup"><span data-stu-id="afd92-107">Determines whether the specified transport is enabled.</span></span>

## <a name="syntax"></a><span data-ttu-id="afd92-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="afd92-108">Syntax</span></span>


```mof
uint32 IsTransportEnabled(
  [in]  uint16  TransportType,
  [out] boolean Enabled
);
```



## <a name="parameters"></a><span data-ttu-id="afd92-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="afd92-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="afd92-110">*Transportetype* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="afd92-110">*TransportType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="afd92-111">Especifica o tipo de transporte.</span><span class="sxs-lookup"><span data-stu-id="afd92-111">Specifies the transport type.</span></span> <span data-ttu-id="afd92-112">Deve ser um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="afd92-112">This must be one of the following values.</span></span>

<dt>

<span data-ttu-id="afd92-113">0</span><span class="sxs-lookup"><span data-stu-id="afd92-113">0</span></span>
</dt> <dd>

<span data-ttu-id="afd92-114">RPC sobre transporte HTTP.</span><span class="sxs-lookup"><span data-stu-id="afd92-114">RPC over HTTP transport.</span></span>

</dd> <dt>

<span data-ttu-id="afd92-115">1</span><span class="sxs-lookup"><span data-stu-id="afd92-115">1</span></span>
</dt> <dd>

<span data-ttu-id="afd92-116">Transporte HTTP.</span><span class="sxs-lookup"><span data-stu-id="afd92-116">HTTP transport.</span></span>

</dd> <dt>

<span data-ttu-id="afd92-117">2</span><span class="sxs-lookup"><span data-stu-id="afd92-117">2</span></span>
</dt> <dd>

<span data-ttu-id="afd92-118">Transporte UDP.</span><span class="sxs-lookup"><span data-stu-id="afd92-118">UDP transport.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="afd92-119">*Habilitado* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="afd92-119">*Enabled* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="afd92-120">Um valor **booliano** que indica se o transporte está habilitado.</span><span class="sxs-lookup"><span data-stu-id="afd92-120">A **boolean** value that indicates whether the transport is enabled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="afd92-121">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="afd92-121">Return value</span></span>

<span data-ttu-id="afd92-122">Se o método tiver sucesso, ele retornará zero.</span><span class="sxs-lookup"><span data-stu-id="afd92-122">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="afd92-123">Se o método não for bem-sucedido, ele retornará um valor diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="afd92-123">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="afd92-124">Para obter uma lista de códigos de erro, consulte [serviços de área de trabalho remota códigos de erro do provedor WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="afd92-124">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="afd92-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="afd92-125">Requirements</span></span>



| <span data-ttu-id="afd92-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="afd92-126">Requirement</span></span> | <span data-ttu-id="afd92-127">Valor</span><span class="sxs-lookup"><span data-stu-id="afd92-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="afd92-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="afd92-128">Minimum supported client</span></span><br/> | <span data-ttu-id="afd92-129">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="afd92-129">None supported</span></span><br/>                                                                |
| <span data-ttu-id="afd92-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="afd92-130">Minimum supported server</span></span><br/> | <span data-ttu-id="afd92-131">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="afd92-131">Windows Server 2012</span></span><br/>                                                           |
| <span data-ttu-id="afd92-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="afd92-132">Namespace</span></span><br/>                | <span data-ttu-id="afd92-133">\\TerminalServices da CIMv2 raiz \\</span><span class="sxs-lookup"><span data-stu-id="afd92-133">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="afd92-134">MOF</span><span class="sxs-lookup"><span data-stu-id="afd92-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="afd92-135"><dt>TS. mof</dt></span><span class="sxs-lookup"><span data-stu-id="afd92-135"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="afd92-136">DLL</span><span class="sxs-lookup"><span data-stu-id="afd92-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="afd92-137"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="afd92-137"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="afd92-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="afd92-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="afd92-139">**\_TSGatewayServerSettings Win32**</span><span class="sxs-lookup"><span data-stu-id="afd92-139">**Win32\_TSGatewayServerSettings**</span></span>](win32-tsgatewayserversettings.md)
</dt> </dl>

 

 





