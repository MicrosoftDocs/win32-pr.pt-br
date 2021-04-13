---
title: Propriedade IMsRdpClientTransportSettings2 GatewayEncryptedOtpCookie
description: Especifica ou recupera o cookie de senha de uso único (OTP) criptografado.
ms.assetid: 09b90231-ebe5-4165-b0e5-edba18472391
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade GatewayEncryptedOtpCookie
- Propriedade GatewayEncryptedOtpCookie Serviços de Área de Trabalho Remota, interface IMsRdpClientTransportSettings2
- Serviços de Área de Trabalho Remota de interface IMsRdpClientTransportSettings2, Propriedade GatewayEncryptedOtpCookie
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings2.GatewayEncryptedOtpCookie
- IMsRdpClientTransportSettings2.get_GatewayEncryptedOtpCookie
- IMsRdpClientTransportSettings2.put_GatewayEncryptedOtpCookie
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7df5463d3d576144fc0a58b543904d6d4934b68c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499842"
---
# <a name="imsrdpclienttransportsettings2gatewayencryptedotpcookie-property"></a><span data-ttu-id="66bb0-106">Propriedade IMsRdpClientTransportSettings2:: GatewayEncryptedOtpCookie</span><span class="sxs-lookup"><span data-stu-id="66bb0-106">IMsRdpClientTransportSettings2::GatewayEncryptedOtpCookie property</span></span>

<span data-ttu-id="66bb0-107">Especifica ou recupera o cookie de senha de uso único (OTP) criptografado.</span><span class="sxs-lookup"><span data-stu-id="66bb0-107">Specifies or retrieves the encrypted one-time password (OTP) cookie.</span></span>

<span data-ttu-id="66bb0-108">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="66bb0-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="66bb0-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="66bb0-109">Syntax</span></span>


```C++
HRESULT put_GatewayEncryptedOtpCookie(
  [in]  BSTR bstrEncryptedOtpCookie
);

HRESULT get_GatewayEncryptedOtpCookie(
  [out] BSTR *pbstrEncryptedOtpCookie
);
```



## <a name="property-value"></a><span data-ttu-id="66bb0-110">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="66bb0-110">Property value</span></span>

<span data-ttu-id="66bb0-111">Especifica ou recupera o cookie de OTP criptografado.</span><span class="sxs-lookup"><span data-stu-id="66bb0-111">Specifies or retrieves the encrypted OTP cookie.</span></span>

## <a name="requirements"></a><span data-ttu-id="66bb0-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="66bb0-112">Requirements</span></span>



| <span data-ttu-id="66bb0-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="66bb0-113">Requirement</span></span> | <span data-ttu-id="66bb0-114">Valor</span><span class="sxs-lookup"><span data-stu-id="66bb0-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="66bb0-115">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="66bb0-115">Minimum supported client</span></span><br/> | <span data-ttu-id="66bb0-116">Windows Vista com SP1</span><span class="sxs-lookup"><span data-stu-id="66bb0-116">Windows Vista with SP1</span></span><br/>                                                                 |
| <span data-ttu-id="66bb0-117">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="66bb0-117">Minimum supported server</span></span><br/> | <span data-ttu-id="66bb0-118">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="66bb0-118">Windows Server 2008</span></span><br/>                                                                    |
| <span data-ttu-id="66bb0-119">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="66bb0-119">Type library</span></span><br/>             | <dl> <span data-ttu-id="66bb0-120"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="66bb0-120"><dt>MsTscAx.dll</dt></span></span> </dl>            |
| <span data-ttu-id="66bb0-121">DLL</span><span class="sxs-lookup"><span data-stu-id="66bb0-121">DLL</span></span><br/>                      | <dl> <span data-ttu-id="66bb0-122"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="66bb0-122"><dt>MsTscAx.dll</dt></span></span> </dl>            |
| <span data-ttu-id="66bb0-123">IID</span><span class="sxs-lookup"><span data-stu-id="66bb0-123">IID</span></span><br/>                      | <span data-ttu-id="66bb0-124">IID \_ IMsRdpClientTransportSettings2 é definido como 67341688-D606-4C73-A5D2-2E0489009319</span><span class="sxs-lookup"><span data-stu-id="66bb0-124">IID\_IMsRdpClientTransportSettings2 is defined as 67341688-D606-4c73-A5D2-2E0489009319</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="66bb0-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="66bb0-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="66bb0-126">**IMsRdpClientTransportSettings**</span><span class="sxs-lookup"><span data-stu-id="66bb0-126">**IMsRdpClientTransportSettings**</span></span>](imsrdpclienttransportsettings.md)
</dt> <dt>

[<span data-ttu-id="66bb0-127">**IMsRdpClientTransportSettings2**</span><span class="sxs-lookup"><span data-stu-id="66bb0-127">**IMsRdpClientTransportSettings2**</span></span>](imsrdpclienttransportsettings2.md)
</dt> </dl>

 

 





