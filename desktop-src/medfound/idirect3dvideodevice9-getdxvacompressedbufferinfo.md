---
description: Obtém informações sobre os buffers compactados necessários para a decodificação acelerada por hardware.
ms.assetid: 5a9fb077-fd79-4faa-a0f8-b3ac987adf36
title: 'Método IDirect3DVideoDevice9:: GetDXVACompressedBufferInfo (DXVA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirect3DVideoDevice9.GetDXVACompressedBufferInfo
api_type:
- COM
api_location:
- dxva.h
ms.openlocfilehash: 2bd2dcdd931ac8778e4f1c11f1479fe54e23d1b3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105815514"
---
# <a name="idirect3dvideodevice9getdxvacompressedbufferinfo-method"></a><span data-ttu-id="9ae27-103">Método IDirect3DVideoDevice9:: GetDXVACompressedBufferInfo</span><span class="sxs-lookup"><span data-stu-id="9ae27-103">IDirect3DVideoDevice9::GetDXVACompressedBufferInfo method</span></span>

<span data-ttu-id="9ae27-104">Obtém informações sobre os buffers compactados necessários para a decodificação acelerada por hardware.</span><span class="sxs-lookup"><span data-stu-id="9ae27-104">Gets information about the compressed buffers needed for hardware-accelerated decoding.</span></span>

## <a name="syntax"></a><span data-ttu-id="9ae27-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9ae27-105">Syntax</span></span>


```C++
HRESULT GetDXVACompressedBufferInfo(
   GUID               *pGuid,
   DXVAUncompDataInfo *pUncompData,
   DWORD              *pNumBuffers,
   DXVACompBufferInfo *pBufferInfo
);
```



## <a name="parameters"></a><span data-ttu-id="9ae27-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9ae27-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9ae27-107">*pGuid*</span><span class="sxs-lookup"><span data-stu-id="9ae27-107">*pGuid*</span></span> 
</dt> <dd>

<span data-ttu-id="9ae27-108">Ponteiro para um GUID que especifica o perfil de DXVA.</span><span class="sxs-lookup"><span data-stu-id="9ae27-108">Pointer to a GUID that specifies the DXVA profile.</span></span> <span data-ttu-id="9ae27-109">Para obter uma lista de perfis com suporte, chame [**IDirect3DVideoDevice9:: GetDXVAGuids**](idirect3dvideodevice9-getdxvaguids.md).</span><span class="sxs-lookup"><span data-stu-id="9ae27-109">To get a list of supported profiles, call [**IDirect3DVideoDevice9::GetDXVAGuids**](idirect3dvideodevice9-getdxvaguids.md).</span></span>

</dd> <dt>

<span data-ttu-id="9ae27-110">*pUncompData*</span><span class="sxs-lookup"><span data-stu-id="9ae27-110">*pUncompData*</span></span> 
</dt> <dd>

<span data-ttu-id="9ae27-111">Ponteiro para uma estrutura [**DXVAUncompDataInfo**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxvauncompdatainfo) que especifica o tamanho e o formato de pixel dos dados descompactados.</span><span class="sxs-lookup"><span data-stu-id="9ae27-111">Pointer to a [**DXVAUncompDataInfo**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxvauncompdatainfo) structure that specifies the size and pixel format of the uncompressed data.</span></span>

</dd> <dt>

<span data-ttu-id="9ae27-112">*pNumBuffers*</span><span class="sxs-lookup"><span data-stu-id="9ae27-112">*pNumBuffers*</span></span> 
</dt> <dd>

<span data-ttu-id="9ae27-113">Na entrada, especifica o número de elementos na matriz *pBufferInfo* .</span><span class="sxs-lookup"><span data-stu-id="9ae27-113">On input, specifies the number of elements in the *pBufferInfo* array.</span></span> <span data-ttu-id="9ae27-114">Se *pBufferInfo* for **NULL**, o valor de `*pNumBuffers` deverá ser zero.</span><span class="sxs-lookup"><span data-stu-id="9ae27-114">If *pBufferInfo* is **NULL**, the value of `*pNumBuffers` must be zero.</span></span>

<span data-ttu-id="9ae27-115">Na saída, se *pBufferInfo* for **NULL**, *pNumBuffers* receberá o tamanho da matriz a ser alocada.</span><span class="sxs-lookup"><span data-stu-id="9ae27-115">On output, if *pBufferInfo* is **NULL**, *pNumBuffers* receives the size of array to allocate.</span></span> <span data-ttu-id="9ae27-116">Caso contrário, *pNumBuffers* receberá o número real de elementos que são copiados para a matriz *pBufferInfo* .</span><span class="sxs-lookup"><span data-stu-id="9ae27-116">Otherwise, *pNumBuffers* receives the actual number of elements that are copied to the *pBufferInfo* array.</span></span>

</dd> <dt>

<span data-ttu-id="9ae27-117">*pBufferInfo*</span><span class="sxs-lookup"><span data-stu-id="9ae27-117">*pBufferInfo*</span></span> 
</dt> <dd>

<span data-ttu-id="9ae27-118">Endereço de uma matriz de estruturas [**DXVACompBufferInfo**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxvacompbufferinfo) ou **NULL**.</span><span class="sxs-lookup"><span data-stu-id="9ae27-118">Address of an array of [**DXVACompBufferInfo**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxvacompbufferinfo) structures or **NULL**.</span></span> <span data-ttu-id="9ae27-119">Se o valor for não **nulo**, o método copiará uma lista de estruturas **DXVACompBufferInfo** para essa matriz.</span><span class="sxs-lookup"><span data-stu-id="9ae27-119">If the value is non-**NULL**, the method copies a list of **DXVACompBufferInfo** structures to this array.</span></span> <span data-ttu-id="9ae27-120">Cada estrutura corresponde a um tipo de buffer de dados compactado que é usado pelo acelerador de vídeo.</span><span class="sxs-lookup"><span data-stu-id="9ae27-120">Each structure corresponds to one type of compressed data buffer that is used by the video accelerator.</span></span>

<span data-ttu-id="9ae27-121">Defina todos os elementos da matriz como zero antes de chamar esse método.</span><span class="sxs-lookup"><span data-stu-id="9ae27-121">Set all of the array elements to zero before calling this method.</span></span>

<span data-ttu-id="9ae27-122">Cada índice de matriz corresponde a um dos tipos de superfície de DXVA definidos em DXVA. h.</span><span class="sxs-lookup"><span data-stu-id="9ae27-122">Each array index corresponds to one of the DXVA surface types defined in dxva.h.</span></span> <span data-ttu-id="9ae27-123">O acelerador de vídeo retorna uma lista de até as entradas de matriz de **\_ \_ \_ \_ buffers de comp. de tipos de número DXVA** .</span><span class="sxs-lookup"><span data-stu-id="9ae27-123">The video accelerator returns a list of up to **DXVA\_NUM\_TYPES\_COMP\_BUFFERS** array entries.</span></span> <span data-ttu-id="9ae27-124">Para obter detalhes, consulte a [especificação de DXVA 1,0](/windows-hardware/drivers/display/directx-video-acceleration), seção 3,4, "lista de descrição de buffer".</span><span class="sxs-lookup"><span data-stu-id="9ae27-124">For details, refer to the [DXVA 1.0 specification](/windows-hardware/drivers/display/directx-video-acceleration), section 3.4, "Buffer Description List."</span></span> <span data-ttu-id="9ae27-125">Se um determinado tipo de buffer não for usado pelo perfil de DXVA, a entrada nesse índice conterá zeros para todos os valores.</span><span class="sxs-lookup"><span data-stu-id="9ae27-125">If a particular buffer type is not used by the DXVA profile, the entry at that index contains zeros for all values.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9ae27-126">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="9ae27-126">Return value</span></span>

<span data-ttu-id="9ae27-127">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="9ae27-127">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="9ae27-128">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="9ae27-128">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="9ae27-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9ae27-129">Requirements</span></span>



| <span data-ttu-id="9ae27-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="9ae27-130">Requirement</span></span> | <span data-ttu-id="9ae27-131">Valor</span><span class="sxs-lookup"><span data-stu-id="9ae27-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="9ae27-132">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9ae27-132">Minimum supported client</span></span><br/> | <span data-ttu-id="9ae27-133">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="9ae27-133">Windows Vista \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="9ae27-134">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9ae27-134">Minimum supported server</span></span><br/> | <span data-ttu-id="9ae27-135">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="9ae27-135">Windows Server 2008 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="9ae27-136">parâmetro</span><span class="sxs-lookup"><span data-stu-id="9ae27-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="9ae27-137"><dt>DXVA. h</dt></span><span class="sxs-lookup"><span data-stu-id="9ae27-137"><dt>Dxva.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9ae27-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="9ae27-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9ae27-139">**IDirect3DVideoDevice9**</span><span class="sxs-lookup"><span data-stu-id="9ae27-139">**IDirect3DVideoDevice9**</span></span>](idirect3dvideodevice9.md)
</dt> </dl>

 

 
