---
title: Propriedade IMsRdpClientTransportSettings2 GatewayUserName
description: Especifica ou recupera o nome de usuário fornecido para o servidor de gateway de Área de Trabalho Remota (gateway de área de trabalho remota).
ms.assetid: eb5ed12f-e650-4abb-be20-bd5fae44e604
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade GatewayUserName
- Propriedade GatewayUserName Serviços de Área de Trabalho Remota, interface IMsRdpClientTransportSettings2
- Serviços de Área de Trabalho Remota de interface IMsRdpClientTransportSettings2, Propriedade GatewayUserName
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings2.GatewayUserName
- IMsRdpClientTransportSettings2.get_GatewayUserName
- IMsRdpClientTransportSettings2.put_GatewayUserName
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 48244c49c942c917c58bfc2790b423981f17fe98
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105787587"
---
# <a name="imsrdpclienttransportsettings2gatewayusername-property"></a><span data-ttu-id="806f4-106">Propriedade IMsRdpClientTransportSettings2:: GatewayUserName</span><span class="sxs-lookup"><span data-stu-id="806f4-106">IMsRdpClientTransportSettings2::GatewayUserName property</span></span>

<span data-ttu-id="806f4-107">Especifica ou recupera o nome de usuário fornecido para o servidor de gateway de Área de Trabalho Remota (gateway de área de trabalho remota).</span><span class="sxs-lookup"><span data-stu-id="806f4-107">Specifies or retrieves the user name that is provided to the Remote Desktop Gateway (RD Gateway) server.</span></span>

<span data-ttu-id="806f4-108">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="806f4-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="806f4-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="806f4-109">Syntax</span></span>


```C++
HRESULT put_GatewayUserName(
  [in]  BSTR proxyUserName
);

HRESULT get_GatewayUserName(
  [out] BSTR *pProxyUserName
);
```



## <a name="property-value"></a><span data-ttu-id="806f4-110">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="806f4-110">Property value</span></span>

<span data-ttu-id="806f4-111">O nome de usuário que é fornecido para se conectar ao servidor de gateway de área de trabalho remota.</span><span class="sxs-lookup"><span data-stu-id="806f4-111">The user name that is provided to connect to the RD Gateway server.</span></span>

## <a name="error-codes"></a><span data-ttu-id="806f4-112">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="806f4-112">Error codes</span></span>

<span data-ttu-id="806f4-113">Retornará **S \_ OK** se for bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="806f4-113">Returns **S\_OK** if successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="806f4-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="806f4-114">Requirements</span></span>



| <span data-ttu-id="806f4-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="806f4-115">Requirement</span></span> | <span data-ttu-id="806f4-116">Valor</span><span class="sxs-lookup"><span data-stu-id="806f4-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="806f4-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="806f4-117">Minimum supported client</span></span><br/> | <span data-ttu-id="806f4-118">Windows Vista com SP1</span><span class="sxs-lookup"><span data-stu-id="806f4-118">Windows Vista with SP1</span></span><br/>                                                                 |
| <span data-ttu-id="806f4-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="806f4-119">Minimum supported server</span></span><br/> | <span data-ttu-id="806f4-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="806f4-120">Windows Server 2008</span></span><br/>                                                                    |
| <span data-ttu-id="806f4-121">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="806f4-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="806f4-122"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="806f4-122"><dt>MsTscAx.dll</dt></span></span> </dl>            |
| <span data-ttu-id="806f4-123">DLL</span><span class="sxs-lookup"><span data-stu-id="806f4-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="806f4-124"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="806f4-124"><dt>MsTscAx.dll</dt></span></span> </dl>            |
| <span data-ttu-id="806f4-125">IID</span><span class="sxs-lookup"><span data-stu-id="806f4-125">IID</span></span><br/>                      | <span data-ttu-id="806f4-126">IID \_ IMsRdpClientTransportSettings2 é definido como 67341688-D606-4C73-A5D2-2E0489009319</span><span class="sxs-lookup"><span data-stu-id="806f4-126">IID\_IMsRdpClientTransportSettings2 is defined as 67341688-D606-4c73-A5D2-2E0489009319</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="806f4-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="806f4-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="806f4-128">**IMsRdpClientTransportSettings**</span><span class="sxs-lookup"><span data-stu-id="806f4-128">**IMsRdpClientTransportSettings**</span></span>](imsrdpclienttransportsettings.md)
</dt> <dt>

[<span data-ttu-id="806f4-129">**IMsRdpClientTransportSettings2**</span><span class="sxs-lookup"><span data-stu-id="806f4-129">**IMsRdpClientTransportSettings2**</span></span>](imsrdpclienttransportsettings2.md)
</dt> </dl>

 

 





