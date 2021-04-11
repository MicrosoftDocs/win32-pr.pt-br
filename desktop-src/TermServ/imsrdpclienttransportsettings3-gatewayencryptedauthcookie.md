---
title: Propriedade IMsRdpClientTransportSettings3 GatewayEncryptedAuthCookie
description: O cookie de autenticação criptografado.
ms.assetid: c9ab6667-327c-44f8-a10e-b048ea91980c
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade GatewayEncryptedAuthCookie
- Propriedade GatewayEncryptedAuthCookie Serviços de Área de Trabalho Remota, interface IMsRdpClientTransportSettings3
- Serviços de Área de Trabalho Remota de interface IMsRdpClientTransportSettings3, Propriedade GatewayEncryptedAuthCookie
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings3.GatewayEncryptedAuthCookie
- IMsRdpClientTransportSettings3.get_GatewayEncryptedAuthCookie
- IMsRdpClientTransportSettings3.put_GatewayEncryptedAuthCookie
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f3949d36f25f2029d7b134943b4e57d8a13db798
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104295785"
---
# <a name="imsrdpclienttransportsettings3gatewayencryptedauthcookie-property"></a><span data-ttu-id="17c47-106">Propriedade IMsRdpClientTransportSettings3:: GatewayEncryptedAuthCookie</span><span class="sxs-lookup"><span data-stu-id="17c47-106">IMsRdpClientTransportSettings3::GatewayEncryptedAuthCookie property</span></span>

<span data-ttu-id="17c47-107">O cookie de autenticação criptografado.</span><span class="sxs-lookup"><span data-stu-id="17c47-107">The encrypted authentication cookie.</span></span> <span data-ttu-id="17c47-108">O tamanho da propriedade é especificado pela propriedade [**GatewayEncryptedAuthCookieSize**](imsrdpclienttransportsettings3-gatewayencryptedauthcookiesize.md) .</span><span class="sxs-lookup"><span data-stu-id="17c47-108">The size of the property is specified by the [**GatewayEncryptedAuthCookieSize**](imsrdpclienttransportsettings3-gatewayencryptedauthcookiesize.md) property.</span></span>

<span data-ttu-id="17c47-109">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="17c47-109">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="17c47-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="17c47-110">Syntax</span></span>


```C++
HRESULT put_GatewayEncryptedAuthCookie(
  [in]          BSTR bstrEncryptedAuthCookie
);

HRESULT get_GatewayEncryptedAuthCookie(
  [out, retval] BSTR *pbstrEncryptedAuthCookie
);
```



## <a name="property-value"></a><span data-ttu-id="17c47-111">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="17c47-111">Property value</span></span>

<span data-ttu-id="17c47-112">O novo cookie de autenticação criptografado.</span><span class="sxs-lookup"><span data-stu-id="17c47-112">The new encrypted authentication cookie.</span></span>

## <a name="requirements"></a><span data-ttu-id="17c47-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="17c47-113">Requirements</span></span>



| <span data-ttu-id="17c47-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="17c47-114">Requirement</span></span> | <span data-ttu-id="17c47-115">Valor</span><span class="sxs-lookup"><span data-stu-id="17c47-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="17c47-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="17c47-116">Minimum supported client</span></span><br/> | <span data-ttu-id="17c47-117">Windows 7</span><span class="sxs-lookup"><span data-stu-id="17c47-117">Windows 7</span></span><br/>                                                                   |
| <span data-ttu-id="17c47-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="17c47-118">Minimum supported server</span></span><br/> | <span data-ttu-id="17c47-119">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="17c47-119">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="17c47-120">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="17c47-120">Type library</span></span><br/>             | <dl> <span data-ttu-id="17c47-121"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="17c47-121"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="17c47-122">DLL</span><span class="sxs-lookup"><span data-stu-id="17c47-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="17c47-123"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="17c47-123"><dt>MsTscAx.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="17c47-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="17c47-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="17c47-125">**GatewayEncryptedAuthCookieSize**</span><span class="sxs-lookup"><span data-stu-id="17c47-125">**GatewayEncryptedAuthCookieSize**</span></span>](imsrdpclienttransportsettings3-gatewayencryptedauthcookiesize.md)
</dt> <dt>

[<span data-ttu-id="17c47-126">**IMsRdpClientTransportSettings3**</span><span class="sxs-lookup"><span data-stu-id="17c47-126">**IMsRdpClientTransportSettings3**</span></span>](imsrdpclienttransportsettings3.md)
</dt> </dl>

 

 





