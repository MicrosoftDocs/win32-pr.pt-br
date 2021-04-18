---
title: Propriedade IMsRdpClientTransportSettings GatewayDefaultUsageMethod
description: O método de uso padrão para gateway de Área de Trabalho Remota (gateway de área de trabalho remota).
ms.assetid: 7014538d-550a-4246-ad32-406ef67fb112
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade GatewayDefaultUsageMethod
- Propriedade GatewayDefaultUsageMethod Serviços de Área de Trabalho Remota, interface IMsRdpClientTransportSettings
- Serviços de Área de Trabalho Remota de interface IMsRdpClientTransportSettings, Propriedade GatewayDefaultUsageMethod
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings.GatewayDefaultUsageMethod
- IMsRdpClientTransportSettings.get_GatewayDefaultUsageMethod
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0b8417da30f9a692e6e233174a33f4b03682a5bd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105788035"
---
# <a name="imsrdpclienttransportsettingsgatewaydefaultusagemethod-property"></a><span data-ttu-id="8200f-106">Propriedade IMsRdpClientTransportSettings:: GatewayDefaultUsageMethod</span><span class="sxs-lookup"><span data-stu-id="8200f-106">IMsRdpClientTransportSettings::GatewayDefaultUsageMethod property</span></span>

<span data-ttu-id="8200f-107">O método de uso padrão para gateway de Área de Trabalho Remota (gateway de área de trabalho remota).</span><span class="sxs-lookup"><span data-stu-id="8200f-107">The default usage method for Remote Desktop Gateway (RD Gateway).</span></span>

<span data-ttu-id="8200f-108">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="8200f-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="8200f-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8200f-109">Syntax</span></span>


```C++
HRESULT get_GatewayDefaultUsageMethod(
  [out] ULONG *pulProxyDefaultUsageMethod
);
```



## <a name="property-value"></a><span data-ttu-id="8200f-110">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="8200f-110">Property value</span></span>

<span data-ttu-id="8200f-111">Um ponteiro para o método de uso padrão para o Gateway RD.</span><span class="sxs-lookup"><span data-stu-id="8200f-111">A pointer to the default usage method for RD Gateway.</span></span> <span data-ttu-id="8200f-112">Retorna uma União das configurações de usuário definidas por [**Put \_ GatewayUsageMethod ()**](imsrdpclienttransportsettings-gatewayusagemethod.md)e configurações de política de grupo.</span><span class="sxs-lookup"><span data-stu-id="8200f-112">Returns a union of the user settings that are set by [**put\_GatewayUsageMethod()**](imsrdpclienttransportsettings-gatewayusagemethod.md), and group policy settings.</span></span> <span data-ttu-id="8200f-113">Se nenhuma configuração de usuário tiver sido definida por **Put \_ GatewayUsageMethod ()**, o **Get \_ GatewayDefaultUsageMethod ()** retornará o valor padrão da **\_ \_ \_ detecção do modo proxy de TSC**.</span><span class="sxs-lookup"><span data-stu-id="8200f-113">If no user settings were set by **put\_GatewayUsageMethod()**, **get\_GatewayDefaultUsageMethod()** will return the default value of **TSC\_PROXY\_MODE\_DETECT**.</span></span>

## <a name="error-codes"></a><span data-ttu-id="8200f-114">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="8200f-114">Error codes</span></span>

<span data-ttu-id="8200f-115">Retornará **S \_ OK** se for bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="8200f-115">Returns **S\_OK** if successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="8200f-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8200f-116">Requirements</span></span>



| <span data-ttu-id="8200f-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="8200f-117">Requirement</span></span> | <span data-ttu-id="8200f-118">Valor</span><span class="sxs-lookup"><span data-stu-id="8200f-118">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8200f-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8200f-119">Minimum supported client</span></span><br/> | <span data-ttu-id="8200f-120">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8200f-120">Windows Vista</span></span><br/>                                                                         |
| <span data-ttu-id="8200f-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8200f-121">Minimum supported server</span></span><br/> | <span data-ttu-id="8200f-122">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8200f-122">Windows Server 2008</span></span><br/>                                                                   |
| <span data-ttu-id="8200f-123">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="8200f-123">Type library</span></span><br/>             | <dl> <span data-ttu-id="8200f-124"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8200f-124"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="8200f-125">DLL</span><span class="sxs-lookup"><span data-stu-id="8200f-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8200f-126"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8200f-126"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="8200f-127">IID</span><span class="sxs-lookup"><span data-stu-id="8200f-127">IID</span></span><br/>                      | <span data-ttu-id="8200f-128">IID \_ IMsRdpClientTransportSettings é definido como 720298C0-A099-46f5-9F82-96921BAE4701</span><span class="sxs-lookup"><span data-stu-id="8200f-128">IID\_IMsRdpClientTransportSettings is defined as 720298C0-A099-46f5-9F82-96921BAE4701</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="8200f-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="8200f-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8200f-130">**IMsRdpClientTransportSettings**</span><span class="sxs-lookup"><span data-stu-id="8200f-130">**IMsRdpClientTransportSettings**</span></span>](imsrdpclienttransportsettings.md)
</dt> </dl>

 

 





