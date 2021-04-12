---
description: Função de proxy para o método GetChannelMask.
ms.assetid: c96e6078-4648-4333-8a25-bcb03a2cd50b
title: Função IWICPixelFormatInfo_GetChannelMask_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICPixelFormatInfo_GetChannelMask_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 0db2c14e89aba2b13cb95209b81f6d0da5d9d949
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171527"
---
# <a name="iwicpixelformatinfo_getchannelmask_proxy-function"></a><span data-ttu-id="1f145-103">\_Função de \_ proxy IWICPixelFormatInfo GetChannelMask</span><span class="sxs-lookup"><span data-stu-id="1f145-103">IWICPixelFormatInfo\_GetChannelMask\_Proxy function</span></span>

<span data-ttu-id="1f145-104">Função de proxy para o método [**GetChannelMask**](/windows/desktop/api/Wincodec/nf-wincodec-iwicpixelformatinfo-getchannelmask) .</span><span class="sxs-lookup"><span data-stu-id="1f145-104">Proxy function for the [**GetChannelMask**](/windows/desktop/api/Wincodec/nf-wincodec-iwicpixelformatinfo-getchannelmask) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="1f145-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1f145-105">Syntax</span></span>


```C++
HRESULT IWICPixelFormatInfo_GetChannelMask_Proxy(
  _In_    IWICPixelFormatInfo *THIS_PTR,
  _In_    UINT                uiChannelIndex,
  _In_    UINT                cbMaskBuffer,
  _Inout_ BYTE                *pbMaskBuffer,
  _Out_   UINT                *pcbActual
);
```



## <a name="parameters"></a><span data-ttu-id="1f145-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1f145-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1f145-107">*Isso \_ PTR* \[\]</span><span class="sxs-lookup"><span data-stu-id="1f145-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1f145-108">Tipo: \**[**IWICPixelFormatInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpixelformatinfo) \** _</span><span class="sxs-lookup"><span data-stu-id="1f145-108">Type: \**[**IWICPixelFormatInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpixelformatinfo)\** _</span></span>

<span data-ttu-id="1f145-109">Ponteiro para este objeto [_ *IWICPixelFormatInfo* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicpixelformatinfo) .</span><span class="sxs-lookup"><span data-stu-id="1f145-109">Pointer to this [_ *IWICPixelFormatInfo*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicpixelformatinfo) object.</span></span>

</dd> <dt>

<span data-ttu-id="1f145-110">*uiChannelIndex* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="1f145-110">*uiChannelIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1f145-111">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="1f145-111">Type: **UINT**</span></span>

<span data-ttu-id="1f145-112">O índice para a máscara de canal a ser recuperada.</span><span class="sxs-lookup"><span data-stu-id="1f145-112">The index to the channel mask to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="1f145-113">*cbMaskBuffer* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="1f145-113">*cbMaskBuffer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1f145-114">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="1f145-114">Type: **UINT**</span></span>

<span data-ttu-id="1f145-115">O tamanho do buffer *pbMaskBuffer* .</span><span class="sxs-lookup"><span data-stu-id="1f145-115">The size of the *pbMaskBuffer* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="1f145-116">*pbMaskBuffer* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="1f145-116">*pbMaskBuffer* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="1f145-117">Tipo: \**byte \** _</span><span class="sxs-lookup"><span data-stu-id="1f145-117">Type: \**BYTE\** _</span></span>

<span data-ttu-id="1f145-118">Ponteiro para o buffer de máscara.</span><span class="sxs-lookup"><span data-stu-id="1f145-118">Pointer to the mask buffer.</span></span>

</dd> <dt>

<span data-ttu-id="1f145-119">_pcbActual \* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="1f145-119">_pcbActual\* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1f145-120">Tipo: \**uint \** _</span><span class="sxs-lookup"><span data-stu-id="1f145-120">Type: \**UINT\** _</span></span>

<span data-ttu-id="1f145-121">O tamanho real do buffer necessário para obter a máscara do canal.</span><span class="sxs-lookup"><span data-stu-id="1f145-121">The actual buffer size needed to obtain the channel mask.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1f145-122">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="1f145-122">Return value</span></span>

<span data-ttu-id="1f145-123">Tipo: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="1f145-123">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="1f145-124">Se essa função for bem sucedido, ela retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="1f145-124">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="1f145-125">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="1f145-125">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="1f145-126">Comentários</span><span class="sxs-lookup"><span data-stu-id="1f145-126">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="1f145-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1f145-127">Requirements</span></span>



| <span data-ttu-id="1f145-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="1f145-128">Requirement</span></span> | <span data-ttu-id="1f145-129">Valor</span><span class="sxs-lookup"><span data-stu-id="1f145-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1f145-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1f145-130">Minimum supported client</span></span><br/> | <span data-ttu-id="1f145-131">Windows XP com SP2, \[ somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="1f145-131">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="1f145-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1f145-132">Minimum supported server</span></span><br/> | <span data-ttu-id="1f145-133">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="1f145-133">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="1f145-134">DLL</span><span class="sxs-lookup"><span data-stu-id="1f145-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1f145-135"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1f145-135"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




