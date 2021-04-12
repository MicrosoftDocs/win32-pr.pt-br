---
title: Propriedade IMsRdpClientTransportSettings3 GatewayEncryptedAuthCookieSize
description: O tamanho, em caracteres, da propriedade GatewayEncryptedAuthCookie.
ms.assetid: 52e24bef-5afa-4954-b639-08ea8701404a
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade GatewayEncryptedAuthCookieSize
- Propriedade GatewayEncryptedAuthCookieSize Serviços de Área de Trabalho Remota, interface IMsRdpClientTransportSettings3
- Serviços de Área de Trabalho Remota de interface IMsRdpClientTransportSettings3, Propriedade GatewayEncryptedAuthCookieSize
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings3.GatewayEncryptedAuthCookieSize
- IMsRdpClientTransportSettings3.get_GatewayEncryptedAuthCookieSize
- IMsRdpClientTransportSettings3.put_GatewayEncryptedAuthCookieSize
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 238245cdb9c0164b69434cf61f790b8f81fa3da2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455387"
---
# <a name="imsrdpclienttransportsettings3gatewayencryptedauthcookiesize-property"></a><span data-ttu-id="bd273-106">Propriedade IMsRdpClientTransportSettings3:: GatewayEncryptedAuthCookieSize</span><span class="sxs-lookup"><span data-stu-id="bd273-106">IMsRdpClientTransportSettings3::GatewayEncryptedAuthCookieSize property</span></span>

<span data-ttu-id="bd273-107">O tamanho, em caracteres, da propriedade [**GatewayEncryptedAuthCookie**](imsrdpclienttransportsettings3-gatewayencryptedauthcookie.md) .</span><span class="sxs-lookup"><span data-stu-id="bd273-107">The size, in characters, of the [**GatewayEncryptedAuthCookie**](imsrdpclienttransportsettings3-gatewayencryptedauthcookie.md) property.</span></span>

<span data-ttu-id="bd273-108">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="bd273-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="bd273-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="bd273-109">Syntax</span></span>


```C++
HRESULT put_GatewayEncryptedAuthCookieSize(
  [in]          ULONG ulEncryptedAuthCookieSize
);

HRESULT get_GatewayEncryptedAuthCookieSize(
  [out, retval] ULONG *ulEncryptedAuthCookieSize
);
```



## <a name="property-value"></a><span data-ttu-id="bd273-110">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="bd273-110">Property value</span></span>

<span data-ttu-id="bd273-111">Um valor **ULONG** que contém o novo valor de tamanho.</span><span class="sxs-lookup"><span data-stu-id="bd273-111">A **ULONG** value that contains the new size value.</span></span>

## <a name="requirements"></a><span data-ttu-id="bd273-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bd273-112">Requirements</span></span>



| <span data-ttu-id="bd273-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="bd273-113">Requirement</span></span> | <span data-ttu-id="bd273-114">Valor</span><span class="sxs-lookup"><span data-stu-id="bd273-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="bd273-115">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bd273-115">Minimum supported client</span></span><br/> | <span data-ttu-id="bd273-116">Windows 7</span><span class="sxs-lookup"><span data-stu-id="bd273-116">Windows 7</span></span><br/>                                                                   |
| <span data-ttu-id="bd273-117">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bd273-117">Minimum supported server</span></span><br/> | <span data-ttu-id="bd273-118">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bd273-118">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="bd273-119">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="bd273-119">Type library</span></span><br/>             | <dl> <span data-ttu-id="bd273-120"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bd273-120"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="bd273-121">DLL</span><span class="sxs-lookup"><span data-stu-id="bd273-121">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bd273-122"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bd273-122"><dt>MsTscAx.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bd273-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="bd273-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bd273-124">**IMsRdpClientTransportSettings3**</span><span class="sxs-lookup"><span data-stu-id="bd273-124">**IMsRdpClientTransportSettings3**</span></span>](imsrdpclienttransportsettings3.md)
</dt> </dl>

 

 





