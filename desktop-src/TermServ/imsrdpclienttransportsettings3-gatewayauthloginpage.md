---
title: Propriedade IMsRdpClientTransportSettings3 GatewayAuthLoginPage
description: O endereço da página da Web de logon a ser usada para autenticar um usuário.
ms.assetid: d7a5e0d8-353e-416d-a9e0-11ef5072f9ff
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade GatewayAuthLoginPage
- Propriedade GatewayAuthLoginPage Serviços de Área de Trabalho Remota, interface IMsRdpClientTransportSettings3
- Serviços de Área de Trabalho Remota de interface IMsRdpClientTransportSettings3, Propriedade GatewayAuthLoginPage
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings3.GatewayAuthLoginPage
- IMsRdpClientTransportSettings3.get_GatewayAuthLoginPage
- IMsRdpClientTransportSettings3.put_GatewayAuthLoginPage
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5be535dea0a89f1cf6e7c238029e53f38f58b0c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086359"
---
# <a name="imsrdpclienttransportsettings3gatewayauthloginpage-property"></a><span data-ttu-id="908c8-106">Propriedade IMsRdpClientTransportSettings3:: GatewayAuthLoginPage</span><span class="sxs-lookup"><span data-stu-id="908c8-106">IMsRdpClientTransportSettings3::GatewayAuthLoginPage property</span></span>

<span data-ttu-id="908c8-107">O endereço da página da Web de logon a ser usada para autenticar um usuário.</span><span class="sxs-lookup"><span data-stu-id="908c8-107">The address of the login webpage to use to authenticate a user.</span></span>

<span data-ttu-id="908c8-108">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="908c8-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="908c8-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="908c8-109">Syntax</span></span>


```C++
HRESULT put_GatewayAuthLoginPage(
  [in]          BSTR bstrProxyAuthLoginPage
);

HRESULT get_GatewayAuthLoginPage(
  [out, retval] BSTR *pbstrProxyAuthLoginPage
);
```



## <a name="property-value"></a><span data-ttu-id="908c8-110">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="908c8-110">Property value</span></span>

<span data-ttu-id="908c8-111">O novo endereço da página da Web de logon.</span><span class="sxs-lookup"><span data-stu-id="908c8-111">The new login webpage address.</span></span>

## <a name="requirements"></a><span data-ttu-id="908c8-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="908c8-112">Requirements</span></span>



| <span data-ttu-id="908c8-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="908c8-113">Requirement</span></span> | <span data-ttu-id="908c8-114">Valor</span><span class="sxs-lookup"><span data-stu-id="908c8-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="908c8-115">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="908c8-115">Minimum supported client</span></span><br/> | <span data-ttu-id="908c8-116">Windows 7</span><span class="sxs-lookup"><span data-stu-id="908c8-116">Windows 7</span></span><br/>                                                                   |
| <span data-ttu-id="908c8-117">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="908c8-117">Minimum supported server</span></span><br/> | <span data-ttu-id="908c8-118">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="908c8-118">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="908c8-119">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="908c8-119">Type library</span></span><br/>             | <dl> <span data-ttu-id="908c8-120"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="908c8-120"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="908c8-121">DLL</span><span class="sxs-lookup"><span data-stu-id="908c8-121">DLL</span></span><br/>                      | <dl> <span data-ttu-id="908c8-122"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="908c8-122"><dt>MsTscAx.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="908c8-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="908c8-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="908c8-124">**IMsRdpClientTransportSettings3**</span><span class="sxs-lookup"><span data-stu-id="908c8-124">**IMsRdpClientTransportSettings3**</span></span>](imsrdpclienttransportsettings3.md)
</dt> </dl>

 

 





