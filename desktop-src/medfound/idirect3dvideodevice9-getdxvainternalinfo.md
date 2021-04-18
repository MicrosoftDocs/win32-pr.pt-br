---
description: Consulta a quantidade de memória temporária que a HAL (camada de abstração de hardware) alocará para seu uso particular.
ms.assetid: 20e3dbef-daf5-487a-8d50-e2ebdb712cc0
title: 'Método IDirect3DVideoDevice9:: GetDXVAInternalInfo (DXVA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirect3DVideoDevice9.GetDXVAInternalInfo
api_type:
- COM
api_location:
- dxva.h
ms.openlocfilehash: aa512130b622d192acc37d8c309f462f8ecc87e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105780400"
---
# <a name="idirect3dvideodevice9getdxvainternalinfo-method"></a><span data-ttu-id="0be72-103">Método IDirect3DVideoDevice9:: GetDXVAInternalInfo</span><span class="sxs-lookup"><span data-stu-id="0be72-103">IDirect3DVideoDevice9::GetDXVAInternalInfo method</span></span>

<span data-ttu-id="0be72-104">Consulta a quantidade de memória temporária que a HAL (camada de abstração de hardware) alocará para seu uso particular.</span><span class="sxs-lookup"><span data-stu-id="0be72-104">Queries for the amount of scratch memory that the hardware abstraction layer (HAL) will allocate for its private use.</span></span>

## <a name="syntax"></a><span data-ttu-id="0be72-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0be72-105">Syntax</span></span>


```C++
HRESULT GetDXVAInternalInfo(
   GUID               *pGuid,
   DXVAUncompDataInfo *pUncompData,
   DWORD              *pMemoryUsed
);
```



## <a name="parameters"></a><span data-ttu-id="0be72-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0be72-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0be72-107">*pGuid*</span><span class="sxs-lookup"><span data-stu-id="0be72-107">*pGuid*</span></span> 
</dt> <dd>

<span data-ttu-id="0be72-108">Ponteiro para um GUID que especifica o perfil de DXVA.</span><span class="sxs-lookup"><span data-stu-id="0be72-108">Pointer to a GUID that specifies the DXVA profile.</span></span> <span data-ttu-id="0be72-109">Para obter uma lista de perfis com suporte, chame [**IDirect3DVideoDevice9:: GetDXVAGuids**](idirect3dvideodevice9-getdxvaguids.md).</span><span class="sxs-lookup"><span data-stu-id="0be72-109">To get a list of supported profiles, call [**IDirect3DVideoDevice9::GetDXVAGuids**](idirect3dvideodevice9-getdxvaguids.md).</span></span>

</dd> <dt>

<span data-ttu-id="0be72-110">*pUncompData*</span><span class="sxs-lookup"><span data-stu-id="0be72-110">*pUncompData*</span></span> 
</dt> <dd>

<span data-ttu-id="0be72-111">Ponteiro para uma estrutura [**DXVAUncompDataInfo**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxvauncompdatainfo) que especifica o tamanho e o formato de pixel dos dados descompactados.</span><span class="sxs-lookup"><span data-stu-id="0be72-111">Pointer to a [**DXVAUncompDataInfo**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxvauncompdatainfo) structure that specifies the size and pixel format of the uncompressed data.</span></span>

</dd> <dt>

<span data-ttu-id="0be72-112">*pMemoryUsed*</span><span class="sxs-lookup"><span data-stu-id="0be72-112">*pMemoryUsed*</span></span> 
</dt> <dd>

<span data-ttu-id="0be72-113">Recebe a quantidade de memória temporária que o HAL alocará, em bytes.</span><span class="sxs-lookup"><span data-stu-id="0be72-113">Receives the amount of scratch memory that the HAL will allocate, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0be72-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="0be72-114">Return value</span></span>

<span data-ttu-id="0be72-115">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="0be72-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="0be72-116">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="0be72-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="0be72-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0be72-117">Requirements</span></span>



| <span data-ttu-id="0be72-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="0be72-118">Requirement</span></span> | <span data-ttu-id="0be72-119">Valor</span><span class="sxs-lookup"><span data-stu-id="0be72-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="0be72-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0be72-120">Minimum supported client</span></span><br/> | <span data-ttu-id="0be72-121">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="0be72-121">Windows Vista \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="0be72-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0be72-122">Minimum supported server</span></span><br/> | <span data-ttu-id="0be72-123">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="0be72-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="0be72-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="0be72-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="0be72-125"><dt>DXVA. h</dt></span><span class="sxs-lookup"><span data-stu-id="0be72-125"><dt>Dxva.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0be72-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="0be72-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0be72-127">**IDirect3DVideoDevice9**</span><span class="sxs-lookup"><span data-stu-id="0be72-127">**IDirect3DVideoDevice9**</span></span>](idirect3dvideodevice9.md)
</dt> </dl>

 

 




