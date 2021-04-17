---
description: Representa um acelerador de hardware para o DXVA (DirectX Video Acceleration) 1,0.
ms.assetid: 63f77cf9-4c04-4ddb-9582-cfcf86f66a2a
title: Interface IDirect3DDXVADevice9 (DXVA. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirect3DDXVADevice9
api_type:
- COM
api_location:
- dxva.h
ms.openlocfilehash: 192f47b8161893f9517bc976452eb8836da4bb53
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105766437"
---
# <a name="idirect3ddxvadevice9-interface"></a><span data-ttu-id="49f30-103">Interface IDirect3DDXVADevice9</span><span class="sxs-lookup"><span data-stu-id="49f30-103">IDirect3DDXVADevice9 interface</span></span>

<span data-ttu-id="49f30-104">Representa um acelerador de hardware para o DXVA (DirectX Video Acceleration) 1,0.</span><span class="sxs-lookup"><span data-stu-id="49f30-104">Represents a hardware accelerator for DirectX Video Acceleration (DXVA) 1.0.</span></span>

## <a name="members"></a><span data-ttu-id="49f30-105">Membros</span><span class="sxs-lookup"><span data-stu-id="49f30-105">Members</span></span>

<span data-ttu-id="49f30-106">A interface **IDirect3DDXVADevice9** herda da interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="49f30-106">The **IDirect3DDXVADevice9** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="49f30-107">**IDirect3DDXVADevice9** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="49f30-107">**IDirect3DDXVADevice9** also has these types of members:</span></span>

-   [<span data-ttu-id="49f30-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="49f30-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="49f30-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="49f30-109">Methods</span></span>

<span data-ttu-id="49f30-110">A interface **IDirect3DDXVADevice9** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="49f30-110">The **IDirect3DDXVADevice9** interface has these methods.</span></span>



| <span data-ttu-id="49f30-111">Método</span><span class="sxs-lookup"><span data-stu-id="49f30-111">Method</span></span>                                                  | <span data-ttu-id="49f30-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="49f30-112">Description</span></span>                                                           |
|:--------------------------------------------------------|:----------------------------------------------------------------------|
| [<span data-ttu-id="49f30-113">**BeginFrame**</span><span class="sxs-lookup"><span data-stu-id="49f30-113">**BeginFrame**</span></span>](idirect3ddxvadevice9-beginframe.md)   | <span data-ttu-id="49f30-114">Inicia o processamento para criar uma imagem decodificada.</span><span class="sxs-lookup"><span data-stu-id="49f30-114">Begins the processing to create a decoded picture.</span></span><br/>         |
| [<span data-ttu-id="49f30-115">**Quadro de fim**</span><span class="sxs-lookup"><span data-stu-id="49f30-115">**EndFrame**</span></span>](idirect3ddxvadevice9-endframe.md)       | <span data-ttu-id="49f30-116">Encerra o processamento para criar uma imagem decodificada.</span><span class="sxs-lookup"><span data-stu-id="49f30-116">Ends the processing to create a decoded picture.</span></span><br/>           |
| [<span data-ttu-id="49f30-117">**Execute (executar)**</span><span class="sxs-lookup"><span data-stu-id="49f30-117">**Execute**</span></span>](idirect3ddxvadevice9-execute.md)         | <span data-ttu-id="49f30-118">Executa uma operação de decodificação de DXVA.</span><span class="sxs-lookup"><span data-stu-id="49f30-118">Performs a DXVA decoding operation.</span></span> <br/>                       |
| [<span data-ttu-id="49f30-119">**QueryStatus**</span><span class="sxs-lookup"><span data-stu-id="49f30-119">**QueryStatus**</span></span>](idirect3ddxvadevice9-querystatus.md) | <span data-ttu-id="49f30-120">Consulta o status de leitura/gravação de uma superfície de decodificação de DXVA.</span><span class="sxs-lookup"><span data-stu-id="49f30-120">Queries the read/write status of a DXVA decoding surface.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="49f30-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="49f30-121">Remarks</span></span>

<span data-ttu-id="49f30-122">Para obter um ponteiro para essa interface, chame [**IDirect3DVideoDevice9:: CreateDXVADevice**](idirect3dvideodevice9-createdxvadevice.md).</span><span class="sxs-lookup"><span data-stu-id="49f30-122">To get a pointer to this interface, call [**IDirect3DVideoDevice9::CreateDXVADevice**](idirect3dvideodevice9-createdxvadevice.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="49f30-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="49f30-123">Requirements</span></span>



| <span data-ttu-id="49f30-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="49f30-124">Requirement</span></span> | <span data-ttu-id="49f30-125">Valor</span><span class="sxs-lookup"><span data-stu-id="49f30-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="49f30-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="49f30-126">Minimum supported client</span></span><br/> | <span data-ttu-id="49f30-127">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="49f30-127">Windows Vista \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="49f30-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="49f30-128">Minimum supported server</span></span><br/> | <span data-ttu-id="49f30-129">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="49f30-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="49f30-130">parâmetro</span><span class="sxs-lookup"><span data-stu-id="49f30-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="49f30-131"><dt>DXVA. h</dt></span><span class="sxs-lookup"><span data-stu-id="49f30-131"><dt>Dxva.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="49f30-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="49f30-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="49f30-133">Interfaces de vídeo Direct3D</span><span class="sxs-lookup"><span data-stu-id="49f30-133">Direct3D Video Interfaces</span></span>](direct3d-video-interfaces.md)
</dt> </dl>

 

 
