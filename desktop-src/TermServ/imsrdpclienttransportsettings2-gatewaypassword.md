---
title: Propriedade IMsRdpClientTransportSettings2 GatewayPassword
description: Especifica a senha que um usuário fornece para se conectar ao servidor de gateway de Área de Trabalho Remota (gateway de área de trabalho remota).
ms.assetid: f29078e5-49ab-45a0-8d79-4b57d7c35e3a
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade GatewayPassword
- Propriedade GatewayPassword Serviços de Área de Trabalho Remota, interface IMsRdpClientTransportSettings2
- Serviços de Área de Trabalho Remota de interface IMsRdpClientTransportSettings2, Propriedade GatewayPassword
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings2.GatewayPassword
- IMsRdpClientTransportSettings2.put_GatewayPassword
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d532f28023b7ff0eb3b8571e3875d0b63606535
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499277"
---
# <a name="imsrdpclienttransportsettings2gatewaypassword-property"></a><span data-ttu-id="945b8-106">Propriedade IMsRdpClientTransportSettings2:: GatewayPassword</span><span class="sxs-lookup"><span data-stu-id="945b8-106">IMsRdpClientTransportSettings2::GatewayPassword property</span></span>

<span data-ttu-id="945b8-107">Especifica a senha que um usuário fornece para se conectar ao servidor de gateway de Área de Trabalho Remota (gateway de área de trabalho remota).</span><span class="sxs-lookup"><span data-stu-id="945b8-107">Specifies the password that a user provides to connect to the Remote Desktop Gateway (RD Gateway) server.</span></span>

<span data-ttu-id="945b8-108">Essa propriedade é somente gravação.</span><span class="sxs-lookup"><span data-stu-id="945b8-108">This property is write-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="945b8-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="945b8-109">Syntax</span></span>


```C++
HRESULT put_GatewayPassword(
  [in] BSTR proxyPassword
);
```



## <a name="property-value"></a><span data-ttu-id="945b8-110">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="945b8-110">Property value</span></span>

<span data-ttu-id="945b8-111">A senha que um usuário fornece para se conectar ao servidor de gateway de área de trabalho remota.</span><span class="sxs-lookup"><span data-stu-id="945b8-111">The password that a user provides to connect to the RD Gateway server.</span></span>

## <a name="error-codes"></a><span data-ttu-id="945b8-112">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="945b8-112">Error codes</span></span>

<span data-ttu-id="945b8-113">Retornará **S \_ OK** se for bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="945b8-113">Returns **S\_OK** if successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="945b8-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="945b8-114">Requirements</span></span>



| <span data-ttu-id="945b8-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="945b8-115">Requirement</span></span> | <span data-ttu-id="945b8-116">Valor</span><span class="sxs-lookup"><span data-stu-id="945b8-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="945b8-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="945b8-117">Minimum supported client</span></span><br/> | <span data-ttu-id="945b8-118">Windows Vista com SP1</span><span class="sxs-lookup"><span data-stu-id="945b8-118">Windows Vista with SP1</span></span><br/>                                                                 |
| <span data-ttu-id="945b8-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="945b8-119">Minimum supported server</span></span><br/> | <span data-ttu-id="945b8-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="945b8-120">Windows Server 2008</span></span><br/>                                                                    |
| <span data-ttu-id="945b8-121">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="945b8-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="945b8-122"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="945b8-122"><dt>MsTscAx.dll</dt></span></span> </dl>            |
| <span data-ttu-id="945b8-123">DLL</span><span class="sxs-lookup"><span data-stu-id="945b8-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="945b8-124"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="945b8-124"><dt>MsTscAx.dll</dt></span></span> </dl>            |
| <span data-ttu-id="945b8-125">IID</span><span class="sxs-lookup"><span data-stu-id="945b8-125">IID</span></span><br/>                      | <span data-ttu-id="945b8-126">IID \_ IMsRdpClientTransportSettings2 é definido como 67341688-D606-4C73-A5D2-2E0489009319</span><span class="sxs-lookup"><span data-stu-id="945b8-126">IID\_IMsRdpClientTransportSettings2 is defined as 67341688-D606-4c73-A5D2-2E0489009319</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="945b8-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="945b8-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="945b8-128">**IMsRdpClientTransportSettings**</span><span class="sxs-lookup"><span data-stu-id="945b8-128">**IMsRdpClientTransportSettings**</span></span>](imsrdpclienttransportsettings.md)
</dt> <dt>

[<span data-ttu-id="945b8-129">**IMsRdpClientTransportSettings2**</span><span class="sxs-lookup"><span data-stu-id="945b8-129">**IMsRdpClientTransportSettings2**</span></span>](imsrdpclienttransportsettings2.md)
</dt> </dl>

 

 





