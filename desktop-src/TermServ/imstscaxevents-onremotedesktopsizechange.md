---
title: Método IMsTscAxEvents OnRemoteDesktopSizeChange
description: Chamado para indicar que o tamanho do controle de cliente na área de trabalho remota foi alterado em resposta a uma operação de controle de cliente.
ms.assetid: 6d27aec0-7249-4aac-8755-186815b50be7
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método OnRemoteDesktopSizeChange
- Método OnRemoteDesktopSizeChange Serviços de Área de Trabalho Remota, interface IMsTscAxEvents
- Serviços de Área de Trabalho Remota de interface IMsTscAxEvents, método OnRemoteDesktopSizeChange
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnRemoteDesktopSizeChange
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6aee74049ea726b4e2686a028359afe01d2d7632
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499466"
---
# <a name="imstscaxeventsonremotedesktopsizechange-method"></a><span data-ttu-id="39c1c-106">Método IMsTscAxEvents:: OnRemoteDesktopSizeChange</span><span class="sxs-lookup"><span data-stu-id="39c1c-106">IMsTscAxEvents::OnRemoteDesktopSizeChange method</span></span>

<span data-ttu-id="39c1c-107">Chamado para indicar que o tamanho do controle de cliente na área de trabalho remota foi alterado em resposta a uma operação de controle de cliente.</span><span class="sxs-lookup"><span data-stu-id="39c1c-107">Called to indicate that the size of the client control on the remote desktop has changed in response to a client control operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="39c1c-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="39c1c-108">Syntax</span></span>


```C++
void OnRemoteDesktopSizeChange(
  [in] long width,
  [in] long height
);
```



## <a name="parameters"></a><span data-ttu-id="39c1c-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="39c1c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="39c1c-110">*largura* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="39c1c-110">*width* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="39c1c-111">Largura, em pixels, da área de trabalho remota redimensionada.</span><span class="sxs-lookup"><span data-stu-id="39c1c-111">Width, in pixels, of the resized remote desktop.</span></span>

</dd> <dt>

<span data-ttu-id="39c1c-112">*altura* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="39c1c-112">*height* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="39c1c-113">Altura, em pixels, da área de trabalho remota redimensionada.</span><span class="sxs-lookup"><span data-stu-id="39c1c-113">Height, in pixels, of the resized remote desktop.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="39c1c-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="39c1c-114">Return value</span></span>

<span data-ttu-id="39c1c-115">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="39c1c-115">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="39c1c-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="39c1c-116">Remarks</span></span>

<span data-ttu-id="39c1c-117">Esse evento permite que o contêiner determine se ele deve ser redimensionado em resposta a uma operação de controle de cliente, o que pode resultar em um tamanho de área de trabalho visível maior.</span><span class="sxs-lookup"><span data-stu-id="39c1c-117">This event allows the container to determine if it must resize itself in response to a client control operation, which could result in a larger viewable desktop size.</span></span> <span data-ttu-id="39c1c-118">Observe que o controle ajustará automaticamente as barras de rolagem para o novo tamanho da sessão.</span><span class="sxs-lookup"><span data-stu-id="39c1c-118">Note that the control will automatically adjust scroll bars for the new session size.</span></span>

<span data-ttu-id="39c1c-119">Para obter mais informações sobre Conexão Web de Área de Trabalho Remota, consulte [Requirements for conexão Web de área de trabalho remota](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="39c1c-119">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="39c1c-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="39c1c-120">Requirements</span></span>



| <span data-ttu-id="39c1c-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="39c1c-121">Requirement</span></span> | <span data-ttu-id="39c1c-122">Valor</span><span class="sxs-lookup"><span data-stu-id="39c1c-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="39c1c-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="39c1c-123">Minimum supported client</span></span><br/> | <span data-ttu-id="39c1c-124">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="39c1c-124">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="39c1c-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="39c1c-125">Minimum supported server</span></span><br/> | <span data-ttu-id="39c1c-126">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="39c1c-126">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="39c1c-127">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="39c1c-127">Type library</span></span><br/>             | <dl> <span data-ttu-id="39c1c-128"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="39c1c-128"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="39c1c-129">DLL</span><span class="sxs-lookup"><span data-stu-id="39c1c-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="39c1c-130"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="39c1c-130"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="39c1c-131">IID</span><span class="sxs-lookup"><span data-stu-id="39c1c-131">IID</span></span><br/>                      | <span data-ttu-id="39c1c-132">IMsTscAxEvents é definido como 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span><span class="sxs-lookup"><span data-stu-id="39c1c-132">IMsTscAxEvents is defined as 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="39c1c-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="39c1c-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="39c1c-134">**IMsTscAxEvents**</span><span class="sxs-lookup"><span data-stu-id="39c1c-134">**IMsTscAxEvents**</span></span>](imstscaxevents-interface.md)
</dt> </dl>

 

 





