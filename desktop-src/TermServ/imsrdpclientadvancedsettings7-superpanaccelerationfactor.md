---
title: Propriedade IMsRdpClientAdvancedSettings7 SuperPanAccelerationFactor
description: Especifica ou recupera um valor que indica o fator de aceleração SuperPan. O fator de aceleração SuperPan determina a velocidade da tela no modo SuperPan.
ms.assetid: ce04f109-8a48-48ee-a553-728f12c09dde
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade SuperPanAccelerationFactor
- Propriedade SuperPanAccelerationFactor Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings7
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings7, Propriedade SuperPanAccelerationFactor
- Propriedade SuperPanAccelerationFactor Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings8
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings8, Propriedade SuperPanAccelerationFactor
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings7.SuperPanAccelerationFactor
- IMsRdpClientAdvancedSettings7.get_SuperPanAccelerationFactor
- IMsRdpClientAdvancedSettings7.put_SuperPanAccelerationFactor
- IMsRdpClientAdvancedSettings8.SuperPanAccelerationFactor
- IMsRdpClientAdvancedSettings8.get_SuperPanAccelerationFactor
- IMsRdpClientAdvancedSettings8.put_SuperPanAccelerationFactor
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0919f3b1920980790203dc265e840e24a9315ae0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103919208"
---
# <a name="imsrdpclientadvancedsettings7superpanaccelerationfactor-property"></a><span data-ttu-id="0b2a1-109">Propriedade IMsRdpClientAdvancedSettings7:: SuperPanAccelerationFactor</span><span class="sxs-lookup"><span data-stu-id="0b2a1-109">IMsRdpClientAdvancedSettings7::SuperPanAccelerationFactor property</span></span>

<span data-ttu-id="0b2a1-110">Especifica ou recupera um valor que indica o fator de aceleração SuperPan.</span><span class="sxs-lookup"><span data-stu-id="0b2a1-110">Specifies or retrieves a value that indicates the SuperPan acceleration factor.</span></span> <span data-ttu-id="0b2a1-111">O fator de aceleração SuperPan determina a velocidade da tela no modo SuperPan.</span><span class="sxs-lookup"><span data-stu-id="0b2a1-111">The SuperPan acceleration factor determines how quickly the screen pans when in SuperPan mode.</span></span> <span data-ttu-id="0b2a1-112">O fator de aceleração é o número de pixels que a exibição de tela rola em uma determinada direção para cada pixel de movimento do mouse pelo cliente.</span><span class="sxs-lookup"><span data-stu-id="0b2a1-112">The acceleration factor is the number of pixels that the screen view scrolls in a given direction for every pixel of mouse movement by the client.</span></span>

<span data-ttu-id="0b2a1-113">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="0b2a1-113">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="0b2a1-114">Syntax</span><span class="sxs-lookup"><span data-stu-id="0b2a1-114">Syntax</span></span>


```C++
HRESULT put_SuperPanAccelerationFactor(
  [in]          ULONG uAccelFactor
);

HRESULT get_SuperPanAccelerationFactor(
  [out, retval] ULONG *puAccelFactor
);
```



## <a name="property-value"></a><span data-ttu-id="0b2a1-115">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="0b2a1-115">Property value</span></span>

<span data-ttu-id="0b2a1-116">O fator de aceleração SuperPan a ser definido.</span><span class="sxs-lookup"><span data-stu-id="0b2a1-116">The SuperPan acceleration factor to set.</span></span> <span data-ttu-id="0b2a1-117">O fator de aceleração SuperPan é o número de pixels que a exibição de tela rola em uma determinada direção para cada pixel de movimento do mouse.</span><span class="sxs-lookup"><span data-stu-id="0b2a1-117">The SuperPan acceleration factor is the number of pixels that the screen view scrolls in a given direction for every pixel of mouse movement.</span></span>

## <a name="remarks"></a><span data-ttu-id="0b2a1-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="0b2a1-118">Remarks</span></span>

<span data-ttu-id="0b2a1-119">Para obter mais informações sobre SuperPan, consulte [**EnableSuperPan**](imsrdpclientadvancedsettings7-enablesuperpan.md).</span><span class="sxs-lookup"><span data-stu-id="0b2a1-119">For more information about SuperPan, see [**EnableSuperPan**](imsrdpclientadvancedsettings7-enablesuperpan.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="0b2a1-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0b2a1-120">Requirements</span></span>



| <span data-ttu-id="0b2a1-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="0b2a1-121">Requirement</span></span> | <span data-ttu-id="0b2a1-122">Valor</span><span class="sxs-lookup"><span data-stu-id="0b2a1-122">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0b2a1-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0b2a1-123">Minimum supported client</span></span><br/> | <span data-ttu-id="0b2a1-124">Windows 7</span><span class="sxs-lookup"><span data-stu-id="0b2a1-124">Windows 7</span></span><br/>                                                                             |
| <span data-ttu-id="0b2a1-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0b2a1-125">Minimum supported server</span></span><br/> | <span data-ttu-id="0b2a1-126">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="0b2a1-126">Windows Server 2008 R2</span></span><br/>                                                                |
| <span data-ttu-id="0b2a1-127">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="0b2a1-127">Type library</span></span><br/>             | <dl> <span data-ttu-id="0b2a1-128"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0b2a1-128"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="0b2a1-129">DLL</span><span class="sxs-lookup"><span data-stu-id="0b2a1-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0b2a1-130"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0b2a1-130"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="0b2a1-131">IID</span><span class="sxs-lookup"><span data-stu-id="0b2a1-131">IID</span></span><br/>                      | <span data-ttu-id="0b2a1-132">IID \_ IMsRdpClientAdvancedSettings7 é definido como 26036036-4010-4578-8091-0db9a1edf9c3</span><span class="sxs-lookup"><span data-stu-id="0b2a1-132">IID\_IMsRdpClientAdvancedSettings7 is defined as 26036036-4010-4578-8091-0db9a1edf9c3</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="0b2a1-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="0b2a1-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0b2a1-134">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="0b2a1-134">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="0b2a1-135">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="0b2a1-135">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="0b2a1-136">**EnableSuperPan**</span><span class="sxs-lookup"><span data-stu-id="0b2a1-136">**EnableSuperPan**</span></span>](imsrdpclientadvancedsettings7-enablesuperpan.md)
</dt> </dl>

 

 





