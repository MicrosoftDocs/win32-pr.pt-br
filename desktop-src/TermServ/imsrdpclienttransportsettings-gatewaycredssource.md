---
title: Propriedade IMsRdpClientTransportSettings GatewayCredsSource
description: Especifica ou recupera o método de autenticação do gateway de Área de Trabalho Remota (Gateway RD).
ms.assetid: 3b05edcb-f678-4d80-99fd-b76d27c80c68
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade GatewayCredsSource
- Propriedade GatewayCredsSource Serviços de Área de Trabalho Remota, interface IMsRdpClientTransportSettings
- Serviços de Área de Trabalho Remota de interface IMsRdpClientTransportSettings, Propriedade GatewayCredsSource
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings.GatewayCredsSource
- IMsRdpClientTransportSettings.get_GatewayCredsSource
- IMsRdpClientTransportSettings.put_GatewayCredsSource
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2771998ddc7c53d05c5d0db452f34a734a7c3e58
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369374"
---
# <a name="imsrdpclienttransportsettingsgatewaycredssource-property"></a><span data-ttu-id="e6fac-106">Propriedade IMsRdpClientTransportSettings:: GatewayCredsSource</span><span class="sxs-lookup"><span data-stu-id="e6fac-106">IMsRdpClientTransportSettings::GatewayCredsSource property</span></span>

<span data-ttu-id="e6fac-107">Especifica ou recupera o método de autenticação do gateway de Área de Trabalho Remota (Gateway RD).</span><span class="sxs-lookup"><span data-stu-id="e6fac-107">Specifies or retrieves the Remote Desktop Gateway (RD Gateway) authentication method.</span></span>

<span data-ttu-id="e6fac-108">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="e6fac-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="e6fac-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="e6fac-109">Syntax</span></span>


```C++
HRESULT put_GatewayCredsSource(
  [in]  ULONG ulProxyCredsSource
);

HRESULT get_GatewayCredsSource(
  [out] ULONG *pulProxyCredsSource
);
```



## <a name="property-value"></a><span data-ttu-id="e6fac-110">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="e6fac-110">Property value</span></span>

<span data-ttu-id="e6fac-111">Uma variável **ULONG** que especifica o método de autenticação de gateway de área de trabalho remota.</span><span class="sxs-lookup"><span data-stu-id="e6fac-111">A **ULONG** variable that specifies the RD Gateway authentication method.</span></span> <span data-ttu-id="e6fac-112">Esse parâmetro pode usar um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="e6fac-112">This parameter can be one of the following values.</span></span>

<dt>

<span data-ttu-id="e6fac-113">\_ \_ Modo de credenciais de proxy de TSC \_ \_ userpass (0)</span><span class="sxs-lookup"><span data-stu-id="e6fac-113">TSC\_PROXY\_CREDS\_MODE\_USERPASS (0)</span></span>
</dt> <dd>

<span data-ttu-id="e6fac-114">Use uma senha (NTLM) como o método de autenticação para o gateway de área de trabalho remota.</span><span class="sxs-lookup"><span data-stu-id="e6fac-114">Use a password (NTLM) as the authentication method for RD Gateway.</span></span>

</dd> <dt>

<span data-ttu-id="e6fac-115">\_ \_ \_ \_ Cartão inteligente de credenciais de proxy de TSC (1)</span><span class="sxs-lookup"><span data-stu-id="e6fac-115">TSC\_PROXY\_CREDS\_MODE\_SMARTCARD (1)</span></span>
</dt> <dd>

<span data-ttu-id="e6fac-116">Use um cartão inteligente como o método de autenticação para o Gateway RD.</span><span class="sxs-lookup"><span data-stu-id="e6fac-116">Use a smart card as the authentication method for RD Gateway.</span></span>

</dd> <dt>

<span data-ttu-id="e6fac-117">\_ \_ \_ Modo de credenciais de proxy \_ de TSC Any (4)</span><span class="sxs-lookup"><span data-stu-id="e6fac-117">TSC\_PROXY\_CREDS\_MODE\_ANY (4)</span></span>
</dt> <dd>

<span data-ttu-id="e6fac-118">Use qualquer método de autenticação para o Gateway RD.</span><span class="sxs-lookup"><span data-stu-id="e6fac-118">Use any authentication method for RD Gateway.</span></span>

</dd> </dl>

## <a name="error-codes"></a><span data-ttu-id="e6fac-119">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="e6fac-119">Error codes</span></span>

<span data-ttu-id="e6fac-120">Retornará **S \_ OK** se for bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="e6fac-120">Returns **S\_OK** if successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="e6fac-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e6fac-121">Requirements</span></span>



| <span data-ttu-id="e6fac-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="e6fac-122">Requirement</span></span> | <span data-ttu-id="e6fac-123">Valor</span><span class="sxs-lookup"><span data-stu-id="e6fac-123">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e6fac-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e6fac-124">Minimum supported client</span></span><br/> | <span data-ttu-id="e6fac-125">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e6fac-125">Windows Vista</span></span><br/>                                                                         |
| <span data-ttu-id="e6fac-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e6fac-126">Minimum supported server</span></span><br/> | <span data-ttu-id="e6fac-127">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e6fac-127">Windows Server 2008</span></span><br/>                                                                   |
| <span data-ttu-id="e6fac-128">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="e6fac-128">Type library</span></span><br/>             | <dl> <span data-ttu-id="e6fac-129"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e6fac-129"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="e6fac-130">DLL</span><span class="sxs-lookup"><span data-stu-id="e6fac-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e6fac-131"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e6fac-131"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="e6fac-132">IID</span><span class="sxs-lookup"><span data-stu-id="e6fac-132">IID</span></span><br/>                      | <span data-ttu-id="e6fac-133">IID \_ IMsRdpClientTransportSettings é definido como 720298C0-A099-46f5-9F82-96921BAE4701</span><span class="sxs-lookup"><span data-stu-id="e6fac-133">IID\_IMsRdpClientTransportSettings is defined as 720298C0-A099-46f5-9F82-96921BAE4701</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e6fac-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="e6fac-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e6fac-135">**IMsRdpClientTransportSettings**</span><span class="sxs-lookup"><span data-stu-id="e6fac-135">**IMsRdpClientTransportSettings**</span></span>](imsrdpclienttransportsettings.md)
</dt> </dl>

 

 





