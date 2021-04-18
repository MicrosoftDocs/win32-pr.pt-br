---
description: Inicia o processamento para criar uma imagem decodificada.
ms.assetid: 80471cc6-c66d-49d9-8593-780e41ac39b9
title: 'Método IDirect3DDXVADevice9:: BeginFrame (DXVA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirect3DDXVADevice9.BeginFrame
api_type:
- COM
api_location:
- dxva.h
ms.openlocfilehash: 3090d7868316d08fa91f36dffcc938eb31e06a7d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105793610"
---
# <a name="idirect3ddxvadevice9beginframe-method"></a><span data-ttu-id="5fd23-103">Método IDirect3DDXVADevice9:: BeginFrame</span><span class="sxs-lookup"><span data-stu-id="5fd23-103">IDirect3DDXVADevice9::BeginFrame method</span></span>

<span data-ttu-id="5fd23-104">Inicia o processamento para criar uma imagem decodificada.</span><span class="sxs-lookup"><span data-stu-id="5fd23-104">Begins the processing to create a decoded picture.</span></span>

## <a name="syntax"></a><span data-ttu-id="5fd23-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5fd23-105">Syntax</span></span>


```C++
HRESULT BeginFrame(
   IDirect3DSurface9 *pDstSurface,
   DWORD             SizeInputData,
   VOID              *pInputData,
   DWORD             *pSizeOutputData,
   VOID              *pOutputData
);
```



## <a name="parameters"></a><span data-ttu-id="5fd23-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5fd23-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5fd23-107">*pDstSurface*</span><span class="sxs-lookup"><span data-stu-id="5fd23-107">*pDstSurface*</span></span> 
</dt> <dd>

<span data-ttu-id="5fd23-108">Um ponteiro para a interface **IDirect3DSurface9** da superfície de destino descompactada.</span><span class="sxs-lookup"><span data-stu-id="5fd23-108">A pointer to the **IDirect3DSurface9** interface of the uncompressed destination surface.</span></span>

</dd> <dt>

<span data-ttu-id="5fd23-109">*SizeInputData*</span><span class="sxs-lookup"><span data-stu-id="5fd23-109">*SizeInputData*</span></span> 
</dt> <dd>

<span data-ttu-id="5fd23-110">O tamanho do buffer especificado por *pInputData*, em bytes.</span><span class="sxs-lookup"><span data-stu-id="5fd23-110">The size of the buffer specified by *pInputData*, in bytes.</span></span> <span data-ttu-id="5fd23-111">O valor deve ser 2.</span><span class="sxs-lookup"><span data-stu-id="5fd23-111">The value must be 2.</span></span>

</dd> <dt>

<span data-ttu-id="5fd23-112">*pInputData*</span><span class="sxs-lookup"><span data-stu-id="5fd23-112">*pInputData*</span></span> 
</dt> <dd>

<span data-ttu-id="5fd23-113">Ponteiro para um buffer que contém dados para o acelerador de vídeo.</span><span class="sxs-lookup"><span data-stu-id="5fd23-113">Pointer to a buffer that contains data for the video accelerator.</span></span> <span data-ttu-id="5fd23-114">Esse buffer deve conter o índice de quadro baseado em zero, especificado como um valor de **palavra** .</span><span class="sxs-lookup"><span data-stu-id="5fd23-114">This buffer must contain the zero-based frame index, specified as a **WORD** value.</span></span>

</dd> <dt>

<span data-ttu-id="5fd23-115">*pSizeOutputData*</span><span class="sxs-lookup"><span data-stu-id="5fd23-115">*pSizeOutputData*</span></span> 
</dt> <dd>

<span data-ttu-id="5fd23-116">O tamanho do buffer especificado por *pOutputData*, em bytes.</span><span class="sxs-lookup"><span data-stu-id="5fd23-116">The size of the buffer specified by *pOutputData*, in bytes.</span></span> <span data-ttu-id="5fd23-117">O valor deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="5fd23-117">The value must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="5fd23-118">*pOutputData*</span><span class="sxs-lookup"><span data-stu-id="5fd23-118">*pOutputData*</span></span> 
</dt> <dd>

<span data-ttu-id="5fd23-119">Ponteiro para um buffer no qual o acelerador de vídeo pode gravar.</span><span class="sxs-lookup"><span data-stu-id="5fd23-119">Pointer to a buffer that the video accelerator can write to.</span></span> <span data-ttu-id="5fd23-120">Defina esse parâmetro como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="5fd23-120">Set this parameter to **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5fd23-121">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="5fd23-121">Return value</span></span>

<span data-ttu-id="5fd23-122">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="5fd23-122">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="5fd23-123">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="5fd23-123">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="5fd23-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="5fd23-124">Remarks</span></span>

<span data-ttu-id="5fd23-125">Para cada chamada para **BeginFrame**, o decodificador deve fazer uma chamada correspondente para [**IDirect3DDXVADevice9:: endframe**](idirect3ddxvadevice9-endframe.md).</span><span class="sxs-lookup"><span data-stu-id="5fd23-125">For each call to **BeginFrame**, the decoder must make a corresponding call to [**IDirect3DDXVADevice9::EndFrame**](idirect3ddxvadevice9-endframe.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="5fd23-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5fd23-126">Requirements</span></span>



| <span data-ttu-id="5fd23-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="5fd23-127">Requirement</span></span> | <span data-ttu-id="5fd23-128">Valor</span><span class="sxs-lookup"><span data-stu-id="5fd23-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="5fd23-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5fd23-129">Minimum supported client</span></span><br/> | <span data-ttu-id="5fd23-130">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="5fd23-130">Windows Vista \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="5fd23-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5fd23-131">Minimum supported server</span></span><br/> | <span data-ttu-id="5fd23-132">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="5fd23-132">Windows Server 2008 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="5fd23-133">parâmetro</span><span class="sxs-lookup"><span data-stu-id="5fd23-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="5fd23-134"><dt>DXVA. h</dt></span><span class="sxs-lookup"><span data-stu-id="5fd23-134"><dt>Dxva.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5fd23-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="5fd23-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5fd23-136">**IDirect3DDXVADevice9**</span><span class="sxs-lookup"><span data-stu-id="5fd23-136">**IDirect3DDXVADevice9**</span></span>](idirect3ddxvadevice9.md)
</dt> </dl>

 

 




