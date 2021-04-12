---
title: Propriedade IMsRdpClientTransportSettings GatewayUserSelectedCredsSource
description: Define ou recupera a origem de credencial do gateway de Área de Trabalho Remota especificado pelo usuário (Gateway RD).
ms.assetid: 0c12ddf6-52c2-40a2-af2b-effd4e8bbdb6
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade GatewayUserSelectedCredsSource
- Propriedade GatewayUserSelectedCredsSource Serviços de Área de Trabalho Remota, interface IMsRdpClientTransportSettings
- Serviços de Área de Trabalho Remota de interface IMsRdpClientTransportSettings, Propriedade GatewayUserSelectedCredsSource
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings.GatewayUserSelectedCredsSource
- IMsRdpClientTransportSettings.get_GatewayUserSelectedCredsSource
- IMsRdpClientTransportSettings.put_GatewayUserSelectedCredsSource
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1556088e62221df7ff91b4b0069bb1ec938ebf23
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499278"
---
# <a name="imsrdpclienttransportsettingsgatewayuserselectedcredssource-property"></a><span data-ttu-id="4fd21-106">Propriedade IMsRdpClientTransportSettings:: GatewayUserSelectedCredsSource</span><span class="sxs-lookup"><span data-stu-id="4fd21-106">IMsRdpClientTransportSettings::GatewayUserSelectedCredsSource property</span></span>

<span data-ttu-id="4fd21-107">Define ou recupera a origem de credencial do gateway de Área de Trabalho Remota especificado pelo usuário (Gateway RD).</span><span class="sxs-lookup"><span data-stu-id="4fd21-107">Sets or retrieves the user-specified Remote Desktop Gateway (RD Gateway) credential source.</span></span>

<span data-ttu-id="4fd21-108">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="4fd21-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="4fd21-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="4fd21-109">Syntax</span></span>


```C++
HRESULT put_GatewayUserSelectedCredsSource(
  [in]  ULONG ulProxyCredsSource
);

HRESULT get_GatewayUserSelectedCredsSource(
  [out] ULONG *pulProxyCredsSource
);
```



## <a name="property-value"></a><span data-ttu-id="4fd21-110">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="4fd21-110">Property value</span></span>

<span data-ttu-id="4fd21-111">Uma variável **ULONG** que especifica o método de autenticação de gateway de área de trabalho remota.</span><span class="sxs-lookup"><span data-stu-id="4fd21-111">A **ULONG** variable that specifies the RD Gateway authentication method.</span></span> <span data-ttu-id="4fd21-112">Esse parâmetro pode usar um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="4fd21-112">This parameter can be one of the following values.</span></span>

<dt>

<span id="TSC_PROXY_CREDS_MODE_USERPASS"></span><span id="tsc_proxy_creds_mode_userpass"></span>

<span data-ttu-id="4fd21-113"><span id="TSC_PROXY_CREDS_MODE_USERPASS"></span><span id="tsc_proxy_creds_mode_userpass"></span>**TSC \_ Modo de credenciais de PROXY \_ \_ \_ userpass** (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="4fd21-113"><span id="TSC_PROXY_CREDS_MODE_USERPASS"></span><span id="tsc_proxy_creds_mode_userpass"></span>**TSC\_PROXY\_CREDS\_MODE\_USERPASS** (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="4fd21-114">Use uma senha (NTLM) como o método de autenticação para o gateway de área de trabalho remota.</span><span class="sxs-lookup"><span data-stu-id="4fd21-114">Use a password (NTLM) as the authentication method for RD Gateway.</span></span>

</dd> <dt>

<span id="TSC_PROXY_CREDS_MODE_SMARTCARD"></span><span id="tsc_proxy_creds_mode_smartcard"></span>

<span data-ttu-id="4fd21-115"><span id="TSC_PROXY_CREDS_MODE_SMARTCARD"></span><span id="tsc_proxy_creds_mode_smartcard"></span>**TSC \_ \_ \_ \_ SmartCard do modo de credenciais de proxy** (1 (0x1))</span><span class="sxs-lookup"><span data-stu-id="4fd21-115"><span id="TSC_PROXY_CREDS_MODE_SMARTCARD"></span><span id="tsc_proxy_creds_mode_smartcard"></span>**TSC\_PROXY\_CREDS\_MODE\_SMARTCARD** (1 (0x1))</span></span>


</dt> <dd>

<span data-ttu-id="4fd21-116">Use um cartão inteligente como o método de autenticação para o Gateway RD.</span><span class="sxs-lookup"><span data-stu-id="4fd21-116">Use a smart card as the authentication method for RD Gateway.</span></span>

</dd> <dt>

<span id="TSC_PROXY_CREDS_MODE_ANY"></span><span id="tsc_proxy_creds_mode_any"></span>

<span data-ttu-id="4fd21-117"><span id="TSC_PROXY_CREDS_MODE_ANY"></span><span id="tsc_proxy_creds_mode_any"></span>**TSC \_ Modo de credenciais de PROXY \_ \_ \_ any** (4 (0x4))</span><span class="sxs-lookup"><span data-stu-id="4fd21-117"><span id="TSC_PROXY_CREDS_MODE_ANY"></span><span id="tsc_proxy_creds_mode_any"></span>**TSC\_PROXY\_CREDS\_MODE\_ANY** (4 (0x4))</span></span>


</dt> <dd>

<span data-ttu-id="4fd21-118">Use qualquer método de autenticação para o Gateway RD.</span><span class="sxs-lookup"><span data-stu-id="4fd21-118">Use any authentication method for RD Gateway.</span></span>

</dd> </dl>

## <a name="error-codes"></a><span data-ttu-id="4fd21-119">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="4fd21-119">Error codes</span></span>

<span data-ttu-id="4fd21-120">Retornará **S \_ OK** se for bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="4fd21-120">Returns **S\_OK** if successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="4fd21-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4fd21-121">Requirements</span></span>



| <span data-ttu-id="4fd21-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="4fd21-122">Requirement</span></span> | <span data-ttu-id="4fd21-123">Valor</span><span class="sxs-lookup"><span data-stu-id="4fd21-123">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4fd21-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4fd21-124">Minimum supported client</span></span><br/> | <span data-ttu-id="4fd21-125">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4fd21-125">Windows Vista</span></span><br/>                                                                         |
| <span data-ttu-id="4fd21-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4fd21-126">Minimum supported server</span></span><br/> | <span data-ttu-id="4fd21-127">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4fd21-127">Windows Server 2008</span></span><br/>                                                                   |
| <span data-ttu-id="4fd21-128">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="4fd21-128">Type library</span></span><br/>             | <dl> <span data-ttu-id="4fd21-129"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4fd21-129"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="4fd21-130">DLL</span><span class="sxs-lookup"><span data-stu-id="4fd21-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4fd21-131"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4fd21-131"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="4fd21-132">IID</span><span class="sxs-lookup"><span data-stu-id="4fd21-132">IID</span></span><br/>                      | <span data-ttu-id="4fd21-133">IID \_ IMsRdpClientTransportSettings é definido como 720298C0-A099-46f5-9F82-96921BAE4701</span><span class="sxs-lookup"><span data-stu-id="4fd21-133">IID\_IMsRdpClientTransportSettings is defined as 720298C0-A099-46f5-9F82-96921BAE4701</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="4fd21-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="4fd21-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4fd21-135">**IMsRdpClientTransportSettings**</span><span class="sxs-lookup"><span data-stu-id="4fd21-135">**IMsRdpClientTransportSettings**</span></span>](imsrdpclienttransportsettings.md)
</dt> </dl>

 

 





