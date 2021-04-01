---
title: Propriedade IMsRdpClientTransportSettings2 GatewayEncryptedOtpCookieSize
description: Especifica ou recupera o tamanho do cookie de senha de uso único (OTP) criptografado.
ms.assetid: a4fdcd06-59ae-407f-9ac6-dfe4b52fb5d7
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade GatewayEncryptedOtpCookieSize
- Propriedade GatewayEncryptedOtpCookieSize Serviços de Área de Trabalho Remota, interface IMsRdpClientTransportSettings2
- Serviços de Área de Trabalho Remota de interface IMsRdpClientTransportSettings2, Propriedade GatewayEncryptedOtpCookieSize
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings2.GatewayEncryptedOtpCookieSize
- IMsRdpClientTransportSettings2.get_GatewayEncryptedOtpCookieSize
- IMsRdpClientTransportSettings2.put_GatewayEncryptedOtpCookieSize
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e714b7c03e898b29b1ae02e3b19d65fde8dfcb91
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644609"
---
# <a name="imsrdpclienttransportsettings2gatewayencryptedotpcookiesize-property"></a><span data-ttu-id="2b438-106">Propriedade IMsRdpClientTransportSettings2:: GatewayEncryptedOtpCookieSize</span><span class="sxs-lookup"><span data-stu-id="2b438-106">IMsRdpClientTransportSettings2::GatewayEncryptedOtpCookieSize property</span></span>

<span data-ttu-id="2b438-107">Especifica ou recupera o tamanho do cookie de senha de uso único (OTP) criptografado.</span><span class="sxs-lookup"><span data-stu-id="2b438-107">Specifies or retrieves the size of the encrypted one-time password (OTP) cookie.</span></span>

<span data-ttu-id="2b438-108">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="2b438-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="2b438-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="2b438-109">Syntax</span></span>


```C++
HRESULT put_GatewayEncryptedOtpCookieSize(
  [in]  ULONG ulEncryptedOtpCookieSize
);

HRESULT get_GatewayEncryptedOtpCookieSize(
  [out] ULONG *pulEncryptedOtpCookieSize
);
```



## <a name="property-value"></a><span data-ttu-id="2b438-110">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="2b438-110">Property value</span></span>

<span data-ttu-id="2b438-111">Especifica ou recupera o tamanho do cookie de senha de uso único (OTP) criptografado.</span><span class="sxs-lookup"><span data-stu-id="2b438-111">Specifies or retrieves the size of the encrypted one-time password (OTP) cookie.</span></span>

## <a name="requirements"></a><span data-ttu-id="2b438-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2b438-112">Requirements</span></span>



| <span data-ttu-id="2b438-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="2b438-113">Requirement</span></span> | <span data-ttu-id="2b438-114">Valor</span><span class="sxs-lookup"><span data-stu-id="2b438-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2b438-115">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2b438-115">Minimum supported client</span></span><br/> | <span data-ttu-id="2b438-116">Windows Vista com SP1</span><span class="sxs-lookup"><span data-stu-id="2b438-116">Windows Vista with SP1</span></span><br/>                                                                 |
| <span data-ttu-id="2b438-117">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2b438-117">Minimum supported server</span></span><br/> | <span data-ttu-id="2b438-118">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2b438-118">Windows Server 2008</span></span><br/>                                                                    |
| <span data-ttu-id="2b438-119">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="2b438-119">Type library</span></span><br/>             | <dl> <span data-ttu-id="2b438-120"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2b438-120"><dt>MsTscAx.dll</dt></span></span> </dl>            |
| <span data-ttu-id="2b438-121">DLL</span><span class="sxs-lookup"><span data-stu-id="2b438-121">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2b438-122"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2b438-122"><dt>MsTscAx.dll</dt></span></span> </dl>            |
| <span data-ttu-id="2b438-123">IID</span><span class="sxs-lookup"><span data-stu-id="2b438-123">IID</span></span><br/>                      | <span data-ttu-id="2b438-124">IID \_ IMsRdpClientTransportSettings2 é definido como 67341688-D606-4C73-A5D2-2E0489009319</span><span class="sxs-lookup"><span data-stu-id="2b438-124">IID\_IMsRdpClientTransportSettings2 is defined as 67341688-D606-4c73-A5D2-2E0489009319</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="2b438-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="2b438-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2b438-126">**IMsRdpClientTransportSettings**</span><span class="sxs-lookup"><span data-stu-id="2b438-126">**IMsRdpClientTransportSettings**</span></span>](imsrdpclienttransportsettings.md)
</dt> <dt>

[<span data-ttu-id="2b438-127">**IMsRdpClientTransportSettings2**</span><span class="sxs-lookup"><span data-stu-id="2b438-127">**IMsRdpClientTransportSettings2**</span></span>](imsrdpclienttransportsettings2.md)
</dt> </dl>

 

 





