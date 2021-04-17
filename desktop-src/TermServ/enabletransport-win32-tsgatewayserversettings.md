---
title: Método EnableTransport da classe Win32_TSGatewayServerSettings
description: Habilita ou desabilita o transporte especificado.
ms.assetid: 95c599d7-56c3-462a-9c7d-2ecf8fc55da1
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método EnableTransport
- Método EnableTransport Serviços de Área de Trabalho Remota, classe Win32_TSGatewayServerSettings
- Classe Win32_TSGatewayServerSettings Serviços de Área de Trabalho Remota, método EnableTransport
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.EnableTransport
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4a14e7ee94eb02e1358d66b9965ecc2323d5b773
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105789832"
---
# <a name="enabletransport-method-of-the-win32_tsgatewayserversettings-class"></a><span data-ttu-id="bcd9e-106">Método EnableTransport da classe Win32 \_ TSGatewayServerSettings</span><span class="sxs-lookup"><span data-stu-id="bcd9e-106">EnableTransport method of the Win32\_TSGatewayServerSettings class</span></span>

<span data-ttu-id="bcd9e-107">Habilita ou desabilita o transporte especificado.</span><span class="sxs-lookup"><span data-stu-id="bcd9e-107">Enables or disables the specified transport.</span></span>

## <a name="syntax"></a><span data-ttu-id="bcd9e-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="bcd9e-108">Syntax</span></span>


```mof
uint32 EnableTransport(
  [in] uint16  TransportType,
  [in] boolean Enable
);
```



## <a name="parameters"></a><span data-ttu-id="bcd9e-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="bcd9e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bcd9e-110">*Transportetype* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="bcd9e-110">*TransportType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bcd9e-111">Especifica o tipo de transporte.</span><span class="sxs-lookup"><span data-stu-id="bcd9e-111">Specifies the transport type.</span></span> <span data-ttu-id="bcd9e-112">Deve ser um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="bcd9e-112">This must be one of the following values.</span></span>

<dt>

<span data-ttu-id="bcd9e-113">0</span><span class="sxs-lookup"><span data-stu-id="bcd9e-113">0</span></span>
</dt> <dd>

<span data-ttu-id="bcd9e-114">RPC sobre transporte HTTP.</span><span class="sxs-lookup"><span data-stu-id="bcd9e-114">RPC over HTTP transport.</span></span>

</dd> <dt>

<span data-ttu-id="bcd9e-115">1</span><span class="sxs-lookup"><span data-stu-id="bcd9e-115">1</span></span>
</dt> <dd>

<span data-ttu-id="bcd9e-116">Transporte HTTP.</span><span class="sxs-lookup"><span data-stu-id="bcd9e-116">HTTP transport.</span></span>

</dd> <dt>

<span data-ttu-id="bcd9e-117">2</span><span class="sxs-lookup"><span data-stu-id="bcd9e-117">2</span></span>
</dt> <dd>

<span data-ttu-id="bcd9e-118">Transporte UDP.</span><span class="sxs-lookup"><span data-stu-id="bcd9e-118">UDP transport.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="bcd9e-119">*Habilitar* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="bcd9e-119">*Enable* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bcd9e-120">Especifica se o transporte está habilitado ou desabilitado.</span><span class="sxs-lookup"><span data-stu-id="bcd9e-120">Specifies if the transport is enabled or disabled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bcd9e-121">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="bcd9e-121">Return value</span></span>

<span data-ttu-id="bcd9e-122">Se o método tiver sucesso, ele retornará zero.</span><span class="sxs-lookup"><span data-stu-id="bcd9e-122">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="bcd9e-123">Se o método não for bem-sucedido, ele retornará um valor diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="bcd9e-123">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="bcd9e-124">Para obter uma lista de códigos de erro, consulte [serviços de área de trabalho remota códigos de erro do provedor WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="bcd9e-124">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="bcd9e-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bcd9e-125">Requirements</span></span>



| <span data-ttu-id="bcd9e-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="bcd9e-126">Requirement</span></span> | <span data-ttu-id="bcd9e-127">Valor</span><span class="sxs-lookup"><span data-stu-id="bcd9e-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="bcd9e-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bcd9e-128">Minimum supported client</span></span><br/> | <span data-ttu-id="bcd9e-129">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="bcd9e-129">None supported</span></span><br/>                                                                |
| <span data-ttu-id="bcd9e-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bcd9e-130">Minimum supported server</span></span><br/> | <span data-ttu-id="bcd9e-131">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="bcd9e-131">Windows Server 2012</span></span><br/>                                                           |
| <span data-ttu-id="bcd9e-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="bcd9e-132">Namespace</span></span><br/>                | <span data-ttu-id="bcd9e-133">\\TerminalServices da CIMv2 raiz \\</span><span class="sxs-lookup"><span data-stu-id="bcd9e-133">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="bcd9e-134">MOF</span><span class="sxs-lookup"><span data-stu-id="bcd9e-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="bcd9e-135"><dt>TS. mof</dt></span><span class="sxs-lookup"><span data-stu-id="bcd9e-135"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="bcd9e-136">DLL</span><span class="sxs-lookup"><span data-stu-id="bcd9e-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bcd9e-137"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bcd9e-137"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="bcd9e-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="bcd9e-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bcd9e-139">**\_TSGatewayServerSettings Win32**</span><span class="sxs-lookup"><span data-stu-id="bcd9e-139">**Win32\_TSGatewayServerSettings**</span></span>](win32-tsgatewayserversettings.md)
</dt> </dl>

 

 





