---
description: Executa uma operação de decodificação de aceleração de vídeo DirectX (DXVA).
ms.assetid: cb87a087-ca53-470e-ab46-f4022cfd7869
title: 'Método IDirect3DDXVADevice9:: Execute (DXVA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirect3DDXVADevice9.Execute
api_type:
- COM
api_location:
- dxva.h
ms.openlocfilehash: d624146c32b5f7eaeb4e680cf03878e8d065ee5b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105772569"
---
# <a name="idirect3ddxvadevice9execute-method"></a><span data-ttu-id="abe1c-103">Método IDirect3DDXVADevice9:: execute</span><span class="sxs-lookup"><span data-stu-id="abe1c-103">IDirect3DDXVADevice9::Execute method</span></span>

<span data-ttu-id="abe1c-104">Executa uma operação de decodificação de aceleração de vídeo DirectX (DXVA).</span><span class="sxs-lookup"><span data-stu-id="abe1c-104">Performs a DirectX Video Acceleration (DXVA) decoding operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="abe1c-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="abe1c-105">Syntax</span></span>


```C++
HRESULT Execute(
   DWORD          FunctionNum,
   VOID           *pInputData,
   DWORD          InputSize,
   VOID           *OutputData,
   DWORD          OutputSize,
   DWORD          NumBuffers,
   DXVABufferInfo *pBufferInfo
);
```



## <a name="parameters"></a><span data-ttu-id="abe1c-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="abe1c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="abe1c-107">*FunctionNum*</span><span class="sxs-lookup"><span data-stu-id="abe1c-107">*FunctionNum*</span></span> 
</dt> <dd>

<span data-ttu-id="abe1c-108">Um **DWORD** que contém um ou mais números de função de DXVA.</span><span class="sxs-lookup"><span data-stu-id="abe1c-108">A **DWORD** that contains one or more DXVA function numbers.</span></span> <span data-ttu-id="abe1c-109">Para obter detalhes, consulte a [especificação DXVA 1,0](/windows-hardware/drivers/display/directx-video-acceleration).</span><span class="sxs-lookup"><span data-stu-id="abe1c-109">For details, refer to the [DXVA 1.0 specification](/windows-hardware/drivers/display/directx-video-acceleration).</span></span>

</dd> <dt>

<span data-ttu-id="abe1c-110">*pInputData*</span><span class="sxs-lookup"><span data-stu-id="abe1c-110">*pInputData*</span></span> 
</dt> <dd>

<span data-ttu-id="abe1c-111">Um ponteiro para um buffer que contém dados de entrada para a operação de decodificação.</span><span class="sxs-lookup"><span data-stu-id="abe1c-111">A pointer to a buffer that contains input data for the decoding operation.</span></span> <span data-ttu-id="abe1c-112">O significado desses dados depende do tipo de superfície e do número da função.</span><span class="sxs-lookup"><span data-stu-id="abe1c-112">The meaning of this data depends on the surface type and function number.</span></span>

</dd> <dt>

<span data-ttu-id="abe1c-113">*Incolocar*</span><span class="sxs-lookup"><span data-stu-id="abe1c-113">*InputSize*</span></span> 
</dt> <dd>

<span data-ttu-id="abe1c-114">O tamanho dos dados de entrada, em bytes.</span><span class="sxs-lookup"><span data-stu-id="abe1c-114">The size of the input data, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="abe1c-115">*OutputData*</span><span class="sxs-lookup"><span data-stu-id="abe1c-115">*OutputData*</span></span> 
</dt> <dd>

<span data-ttu-id="abe1c-116">Ponteiro para um buffer no qual o acelerador de vídeo grava dados de saída.</span><span class="sxs-lookup"><span data-stu-id="abe1c-116">Pointer to a buffer where the video accelerator writes output data.</span></span>

</dd> <dt>

<span data-ttu-id="abe1c-117">*Sobrecolocações*</span><span class="sxs-lookup"><span data-stu-id="abe1c-117">*OutputSize*</span></span> 
</dt> <dd>

<span data-ttu-id="abe1c-118">O tamanho do buffer *OutputData* , em bytes.</span><span class="sxs-lookup"><span data-stu-id="abe1c-118">The size of the *OutputData* buffer, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="abe1c-119">*NumBuffers*</span><span class="sxs-lookup"><span data-stu-id="abe1c-119">*NumBuffers*</span></span> 
</dt> <dd>

<span data-ttu-id="abe1c-120">O número de elementos na matriz *pBufferInfo* .</span><span class="sxs-lookup"><span data-stu-id="abe1c-120">The number of elements in the *pBufferInfo* array.</span></span>

</dd> <dt>

<span data-ttu-id="abe1c-121">*pBufferInfo*</span><span class="sxs-lookup"><span data-stu-id="abe1c-121">*pBufferInfo*</span></span> 
</dt> <dd>

<span data-ttu-id="abe1c-122">Um ponteiro para uma matriz de estruturas [**DXVABufferInfo**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxvabufferinfo) .</span><span class="sxs-lookup"><span data-stu-id="abe1c-122">A pointer to an array of [**DXVABufferInfo**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxvabufferinfo) structures.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="abe1c-123">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="abe1c-123">Return value</span></span>

<span data-ttu-id="abe1c-124">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="abe1c-124">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="abe1c-125">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="abe1c-125">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="abe1c-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="abe1c-126">Requirements</span></span>



| <span data-ttu-id="abe1c-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="abe1c-127">Requirement</span></span> | <span data-ttu-id="abe1c-128">Valor</span><span class="sxs-lookup"><span data-stu-id="abe1c-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="abe1c-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="abe1c-129">Minimum supported client</span></span><br/> | <span data-ttu-id="abe1c-130">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="abe1c-130">Windows Vista \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="abe1c-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="abe1c-131">Minimum supported server</span></span><br/> | <span data-ttu-id="abe1c-132">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="abe1c-132">Windows Server 2008 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="abe1c-133">parâmetro</span><span class="sxs-lookup"><span data-stu-id="abe1c-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="abe1c-134"><dt>DXVA. h</dt></span><span class="sxs-lookup"><span data-stu-id="abe1c-134"><dt>Dxva.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="abe1c-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="abe1c-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="abe1c-136">**IDirect3DDXVADevice9**</span><span class="sxs-lookup"><span data-stu-id="abe1c-136">**IDirect3DDXVADevice9**</span></span>](idirect3ddxvadevice9.md)
</dt> </dl>

 

 
