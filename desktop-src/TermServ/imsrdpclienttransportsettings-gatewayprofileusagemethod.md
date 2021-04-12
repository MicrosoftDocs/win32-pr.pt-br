---
title: Propriedade IMsRdpClientTransportSettings GatewayProfileUsageMethod
description: Especifica se as configurações padrão de gateway de Área de Trabalho Remota (Gateway RD) devem ser usadas.
ms.assetid: ce774790-31ad-40ba-ba8f-e81b0dbda175
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade GatewayProfileUsageMethod
- Propriedade GatewayProfileUsageMethod Serviços de Área de Trabalho Remota, interface IMsRdpClientTransportSettings
- Serviços de Área de Trabalho Remota de interface IMsRdpClientTransportSettings, Propriedade GatewayProfileUsageMethod
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings.GatewayProfileUsageMethod
- IMsRdpClientTransportSettings.get_GatewayProfileUsageMethod
- IMsRdpClientTransportSettings.put_GatewayProfileUsageMethod
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 05a12a9836e89348d1eb7ccdf680b23e2695c938
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369579"
---
# <a name="imsrdpclienttransportsettingsgatewayprofileusagemethod-property"></a><span data-ttu-id="197bb-106">Propriedade IMsRdpClientTransportSettings:: GatewayProfileUsageMethod</span><span class="sxs-lookup"><span data-stu-id="197bb-106">IMsRdpClientTransportSettings::GatewayProfileUsageMethod property</span></span>

<span data-ttu-id="197bb-107">Especifica se as configurações padrão de gateway de Área de Trabalho Remota (Gateway RD) devem ser usadas.</span><span class="sxs-lookup"><span data-stu-id="197bb-107">Specifies whether to use default Remote Desktop Gateway (RD Gateway) settings.</span></span>

<span data-ttu-id="197bb-108">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="197bb-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="197bb-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="197bb-109">Syntax</span></span>


```C++
HRESULT put_GatewayProfileUsageMethod(
  [in]  ULONG ulProxyProfileMethod
);

HRESULT get_GatewayProfileUsageMethod(
  [out] ULONG *pulProxyProfileUsageMethod
);
```



## <a name="property-value"></a><span data-ttu-id="197bb-110">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="197bb-110">Property value</span></span>

<span data-ttu-id="197bb-111">O método de uso de perfil de gateway de área de trabalho remota.</span><span class="sxs-lookup"><span data-stu-id="197bb-111">The RD Gateway profile usage method.</span></span> <span data-ttu-id="197bb-112">Esse parâmetro pode usar um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="197bb-112">This parameter can be one of the following values.</span></span>

<dt>

<span id="TSC_PROXY_PROFILE_MODE_DEFAULT"></span><span id="tsc_proxy_profile_mode_default"></span>

<span data-ttu-id="197bb-113"><span id="TSC_PROXY_PROFILE_MODE_DEFAULT"></span><span id="tsc_proxy_profile_mode_default"></span>**TSC \_ Modo de perfil de PROXY \_ \_ \_ padrão** (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="197bb-113"><span id="TSC_PROXY_PROFILE_MODE_DEFAULT"></span><span id="tsc_proxy_profile_mode_default"></span>**TSC\_PROXY\_PROFILE\_MODE\_DEFAULT** (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="197bb-114">Use o modo de perfil padrão, conforme especificado pelo administrador.</span><span class="sxs-lookup"><span data-stu-id="197bb-114">Use the default profile mode, as specified by the administrator.</span></span>

</dd> <dt>

<span id="TSC_PROXY_PROFILE_MODE_EXPLICIT"></span><span id="tsc_proxy_profile_mode_explicit"></span>

<span data-ttu-id="197bb-115"><span id="TSC_PROXY_PROFILE_MODE_EXPLICIT"></span><span id="tsc_proxy_profile_mode_explicit"></span>**TSC \_ Modo de perfil de PROXY \_ \_ \_ explícito** (1 (0x1))</span><span class="sxs-lookup"><span data-stu-id="197bb-115"><span id="TSC_PROXY_PROFILE_MODE_EXPLICIT"></span><span id="tsc_proxy_profile_mode_explicit"></span>**TSC\_PROXY\_PROFILE\_MODE\_EXPLICIT** (1 (0x1))</span></span>


</dt> <dd>

<span data-ttu-id="197bb-116">Use configurações explícitas, conforme especificado pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="197bb-116">Use explicit settings, as specified by the user.</span></span>

</dd> </dl>

## <a name="error-codes"></a><span data-ttu-id="197bb-117">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="197bb-117">Error codes</span></span>

<span data-ttu-id="197bb-118">Retornará **S \_ OK** se for bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="197bb-118">Returns **S\_OK** if successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="197bb-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="197bb-119">Requirements</span></span>



| <span data-ttu-id="197bb-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="197bb-120">Requirement</span></span> | <span data-ttu-id="197bb-121">Valor</span><span class="sxs-lookup"><span data-stu-id="197bb-121">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="197bb-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="197bb-122">Minimum supported client</span></span><br/> | <span data-ttu-id="197bb-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="197bb-123">Windows Vista</span></span><br/>                                                                         |
| <span data-ttu-id="197bb-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="197bb-124">Minimum supported server</span></span><br/> | <span data-ttu-id="197bb-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="197bb-125">Windows Server 2008</span></span><br/>                                                                   |
| <span data-ttu-id="197bb-126">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="197bb-126">Type library</span></span><br/>             | <dl> <span data-ttu-id="197bb-127"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="197bb-127"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="197bb-128">DLL</span><span class="sxs-lookup"><span data-stu-id="197bb-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="197bb-129"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="197bb-129"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="197bb-130">IID</span><span class="sxs-lookup"><span data-stu-id="197bb-130">IID</span></span><br/>                      | <span data-ttu-id="197bb-131">IID \_ IMsRdpClientTransportSettings é definido como 720298C0-A099-46f5-9F82-96921BAE4701</span><span class="sxs-lookup"><span data-stu-id="197bb-131">IID\_IMsRdpClientTransportSettings is defined as 720298C0-A099-46f5-9F82-96921BAE4701</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="197bb-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="197bb-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="197bb-133">**IMsRdpClientTransportSettings**</span><span class="sxs-lookup"><span data-stu-id="197bb-133">**IMsRdpClientTransportSettings**</span></span>](imsrdpclienttransportsettings.md)
</dt> </dl>

 

 





