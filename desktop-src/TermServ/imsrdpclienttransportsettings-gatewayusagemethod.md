---
title: Propriedade IMsRdpClientTransportSettings GatewayUsageMethod
description: Especifica quando usar um servidor de gateway de Área de Trabalho Remota (gateway de área de trabalho remota).
ms.assetid: 0644c413-9ff7-42c1-a38e-e1ce546972ff
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade GatewayUsageMethod
- Propriedade GatewayUsageMethod Serviços de Área de Trabalho Remota, interface IMsRdpClientTransportSettings
- Serviços de Área de Trabalho Remota de interface IMsRdpClientTransportSettings, Propriedade GatewayUsageMethod
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings.GatewayUsageMethod
- IMsRdpClientTransportSettings.get_GatewayUsageMethod
- IMsRdpClientTransportSettings.put_GatewayUsageMethod
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f07bc10c67d01f957e588d1b50085e57b0fa10b1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105768549"
---
# <a name="imsrdpclienttransportsettingsgatewayusagemethod-property"></a><span data-ttu-id="152ee-106">Propriedade IMsRdpClientTransportSettings:: GatewayUsageMethod</span><span class="sxs-lookup"><span data-stu-id="152ee-106">IMsRdpClientTransportSettings::GatewayUsageMethod property</span></span>

<span data-ttu-id="152ee-107">Especifica quando usar um servidor de gateway de Área de Trabalho Remota (gateway de área de trabalho remota).</span><span class="sxs-lookup"><span data-stu-id="152ee-107">Specifies when to use a Remote Desktop Gateway (RD Gateway) server.</span></span>

<span data-ttu-id="152ee-108">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="152ee-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="152ee-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="152ee-109">Syntax</span></span>


```C++
HRESULT put_GatewayUsageMethod(
  [in]  ULONG ulProxyMethod
);

HRESULT get_GatewayUsageMethod(
  [out] ULONG *pulProxyUsageMethod
);
```



## <a name="property-value"></a><span data-ttu-id="152ee-110">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="152ee-110">Property value</span></span>

<span data-ttu-id="152ee-111">Uma variável **ULONG** que especifica o método de uso do servidor de gateway de área de trabalho remota.</span><span class="sxs-lookup"><span data-stu-id="152ee-111">A **ULONG** variable that specifies the RD Gateway server usage method.</span></span> <span data-ttu-id="152ee-112">Esse parâmetro pode usar um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="152ee-112">This parameter can be one of the following values.</span></span>

<dt>

<span id="TSC_PROXY_MODE_NONE_DIRECT"></span><span id="tsc_proxy_mode_none_direct"></span>

<span data-ttu-id="152ee-113"><span id="TSC_PROXY_MODE_NONE_DIRECT"></span><span id="tsc_proxy_mode_none_direct"></span>**TSC \_ \_Modo proxy \_ nenhum \_ direto** (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="152ee-113"><span id="TSC_PROXY_MODE_NONE_DIRECT"></span><span id="tsc_proxy_mode_none_direct"></span>**TSC\_PROXY\_MODE\_NONE\_DIRECT** (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="152ee-114">Não use um servidor de gateway de área de trabalho remota.</span><span class="sxs-lookup"><span data-stu-id="152ee-114">Do not use an RD Gateway server.</span></span> <span data-ttu-id="152ee-115">Na interface do usuário do cliente do Conexão de Área de Trabalho Remota (RDC), a caixa de seleção **ignorar servidor Gateway RD para endereços locais** está desmarcada.</span><span class="sxs-lookup"><span data-stu-id="152ee-115">In the Remote Desktop Connection (RDC) client UI, the **Bypass RD Gateway server for local addresses** check box is cleared.</span></span>

</dd> <dt>

<span id="TSC_PROXY_MODE_DIRECT"></span><span id="tsc_proxy_mode_direct"></span>

<span data-ttu-id="152ee-116"><span id="TSC_PROXY_MODE_DIRECT"></span><span id="tsc_proxy_mode_direct"></span>**TSC \_ \_Modo proxy \_ direto** (1 (0x1))</span><span class="sxs-lookup"><span data-stu-id="152ee-116"><span id="TSC_PROXY_MODE_DIRECT"></span><span id="tsc_proxy_mode_direct"></span>**TSC\_PROXY\_MODE\_DIRECT** (1 (0x1))</span></span>


</dt> <dd>

<span data-ttu-id="152ee-117">Sempre use um servidor de gateway de área de trabalho remota.</span><span class="sxs-lookup"><span data-stu-id="152ee-117">Always use an RD Gateway server.</span></span> <span data-ttu-id="152ee-118">Na interface do usuário do cliente RDC, a caixa de seleção **ignorar servidor Gateway RD para endereços locais** está desmarcada.</span><span class="sxs-lookup"><span data-stu-id="152ee-118">In the RDC client UI, the **Bypass RD Gateway server for local addresses** check box is cleared.</span></span>

</dd> <dt>

<span id="TSC_PROXY_MODE_DETECT"></span><span id="tsc_proxy_mode_detect"></span>

<span data-ttu-id="152ee-119"><span id="TSC_PROXY_MODE_DETECT"></span><span id="tsc_proxy_mode_detect"></span>**TSC \_ \_ \_ Detecção de modo proxy** (2 (0x2))</span><span class="sxs-lookup"><span data-stu-id="152ee-119"><span id="TSC_PROXY_MODE_DETECT"></span><span id="tsc_proxy_mode_detect"></span>**TSC\_PROXY\_MODE\_DETECT** (2 (0x2))</span></span>


</dt> <dd>

<span data-ttu-id="152ee-120">Use um servidor de gateway de área de trabalho remota se não for possível estabelecer uma conexão direta com o servidor de Host da Sessão RD.</span><span class="sxs-lookup"><span data-stu-id="152ee-120">Use an RD Gateway server if a direct connection cannot be made to the RD Session Host server.</span></span> <span data-ttu-id="152ee-121">Na interface do usuário do cliente RDC, a caixa de seleção **ignorar servidor Gateway RD para endereços locais** está marcada.</span><span class="sxs-lookup"><span data-stu-id="152ee-121">In the RDC client UI, the **Bypass RD Gateway server for local addresses** check box is selected.</span></span>

</dd> <dt>

<span id="TSC_PROXY_MODE_DEFAULT"></span><span id="tsc_proxy_mode_default"></span>

<span data-ttu-id="152ee-122"><span id="TSC_PROXY_MODE_DEFAULT"></span><span id="tsc_proxy_mode_default"></span>**TSC \_ \_ \_ Padrão de modo proxy** (3 (0x3))</span><span class="sxs-lookup"><span data-stu-id="152ee-122"><span id="TSC_PROXY_MODE_DEFAULT"></span><span id="tsc_proxy_mode_default"></span>**TSC\_PROXY\_MODE\_DEFAULT** (3 (0x3))</span></span>


</dt> <dd>

<span data-ttu-id="152ee-123">Use as configurações padrão do servidor Gateway RD.</span><span class="sxs-lookup"><span data-stu-id="152ee-123">Use the default RD Gateway server settings.</span></span>

</dd> <dt>

<span id="TSC_PROXY_MODE_NONE_DETECT"></span><span id="tsc_proxy_mode_none_detect"></span>

<span data-ttu-id="152ee-124"><span id="TSC_PROXY_MODE_NONE_DETECT"></span><span id="tsc_proxy_mode_none_detect"></span>**TSC \_ \_Modo proxy \_ None \_ detectar** (4 (0x4))</span><span class="sxs-lookup"><span data-stu-id="152ee-124"><span id="TSC_PROXY_MODE_NONE_DETECT"></span><span id="tsc_proxy_mode_none_detect"></span>**TSC\_PROXY\_MODE\_NONE\_DETECT** (4 (0x4))</span></span>


</dt> <dd>

<span data-ttu-id="152ee-125">Não use um servidor de gateway de área de trabalho remota.</span><span class="sxs-lookup"><span data-stu-id="152ee-125">Do not use an RD Gateway server.</span></span> <span data-ttu-id="152ee-126">Na interface do usuário do cliente RDC, a caixa de seleção **ignorar servidor Gateway RD para endereços locais** está marcada.</span><span class="sxs-lookup"><span data-stu-id="152ee-126">In the RDC client UI, the **Bypass RD Gateway server for local addresses** check box is selected.</span></span>

</dd> </dl>

## <a name="error-codes"></a><span data-ttu-id="152ee-127">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="152ee-127">Error codes</span></span>

<span data-ttu-id="152ee-128">Retornará **S \_ OK** se for bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="152ee-128">Returns **S\_OK** if successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="152ee-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="152ee-129">Requirements</span></span>



| <span data-ttu-id="152ee-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="152ee-130">Requirement</span></span> | <span data-ttu-id="152ee-131">Valor</span><span class="sxs-lookup"><span data-stu-id="152ee-131">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="152ee-132">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="152ee-132">Minimum supported client</span></span><br/> | <span data-ttu-id="152ee-133">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="152ee-133">Windows Vista</span></span><br/>                                                                         |
| <span data-ttu-id="152ee-134">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="152ee-134">Minimum supported server</span></span><br/> | <span data-ttu-id="152ee-135">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="152ee-135">Windows Server 2008</span></span><br/>                                                                   |
| <span data-ttu-id="152ee-136">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="152ee-136">Type library</span></span><br/>             | <dl> <span data-ttu-id="152ee-137"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="152ee-137"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="152ee-138">DLL</span><span class="sxs-lookup"><span data-stu-id="152ee-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="152ee-139"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="152ee-139"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="152ee-140">IID</span><span class="sxs-lookup"><span data-stu-id="152ee-140">IID</span></span><br/>                      | <span data-ttu-id="152ee-141">IID \_ IMsRdpClientTransportSettings é definido como 720298C0-A099-46f5-9F82-96921BAE4701</span><span class="sxs-lookup"><span data-stu-id="152ee-141">IID\_IMsRdpClientTransportSettings is defined as 720298C0-A099-46f5-9F82-96921BAE4701</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="152ee-142">Confira também</span><span class="sxs-lookup"><span data-stu-id="152ee-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="152ee-143">**IMsRdpClientTransportSettings**</span><span class="sxs-lookup"><span data-stu-id="152ee-143">**IMsRdpClientTransportSettings**</span></span>](imsrdpclienttransportsettings.md)
</dt> </dl>

 

 





