---
description: Função de proxy para o método CopyPixels.
ms.assetid: 020c11e9-0847-468e-b240-20529f6460cd
title: Função IWICBitmapSource_CopyPixels_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapSource_CopyPixels_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 5c759bd1731e2f3cbc4da9c40cb590e0f39686de
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171155"
---
# <a name="iwicbitmapsource_copypixels_proxy-function"></a><span data-ttu-id="b1514-103">\_Função de \_ proxy IWICBitmapSource CopyPixels</span><span class="sxs-lookup"><span data-stu-id="b1514-103">IWICBitmapSource\_CopyPixels\_Proxy function</span></span>

<span data-ttu-id="b1514-104">Função de proxy para o método [**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-copypixels) .</span><span class="sxs-lookup"><span data-stu-id="b1514-104">Proxy function for the [**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-copypixels) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="b1514-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b1514-105">Syntax</span></span>


```C++
HRESULT IWICBitmapSource_CopyPixels_Proxy(
  _In_        IWICBitmapSource *THIS_PTR,
  _In_  const WICRect          *prc,
  _In_        UINT             cbStride,
  _In_        UINT             cbBufferSize,
  _Out_       BYTE             *pbBuffer
);
```



## <a name="parameters"></a><span data-ttu-id="b1514-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b1514-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b1514-107">*Isso \_ PTR* \[\]</span><span class="sxs-lookup"><span data-stu-id="b1514-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b1514-108">Tipo: \**[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) \** _</span><span class="sxs-lookup"><span data-stu-id="b1514-108">Type: \**[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\** _</span></span>

<span data-ttu-id="b1514-109">Ponteiro para este objeto [_ *IWICBitmapSource* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) .</span><span class="sxs-lookup"><span data-stu-id="b1514-109">Pointer to this [_ *IWICBitmapSource*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) object.</span></span>

</dd> <dt>

<span data-ttu-id="b1514-110">*prc* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b1514-110">*prc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b1514-111">Tipo: \**const [**WICRect**](/windows/desktop/api/Wincodec/ns-wincodec-wicrect) \** _</span><span class="sxs-lookup"><span data-stu-id="b1514-111">Type: \**const [**WICRect**](/windows/desktop/api/Wincodec/ns-wincodec-wicrect)\** _</span></span>

<span data-ttu-id="b1514-112">O retângulo a ser copiado.</span><span class="sxs-lookup"><span data-stu-id="b1514-112">The rectangle to copy.</span></span> <span data-ttu-id="b1514-113">Um valor nulo especifica o bitmap inteiro.</span><span class="sxs-lookup"><span data-stu-id="b1514-113">A NULL value specifies the entire bitmap.</span></span>

</dd> <dt>

<span data-ttu-id="b1514-114">_cbStride \* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b1514-114">_cbStride\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b1514-115">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="b1514-115">Type: **UINT**</span></span>

<span data-ttu-id="b1514-116">O stride do bitmap</span><span class="sxs-lookup"><span data-stu-id="b1514-116">The stride of the bitmap</span></span>

</dd> <dt>

<span data-ttu-id="b1514-117">*cbBufferSize* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b1514-117">*cbBufferSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b1514-118">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="b1514-118">Type: **UINT**</span></span>

<span data-ttu-id="b1514-119">O tamanho do buffer.</span><span class="sxs-lookup"><span data-stu-id="b1514-119">The size of the buffer.</span></span>

</dd> <dt>

<span data-ttu-id="b1514-120">*pbBuffer* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="b1514-120">*pbBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b1514-121">Tipo: \**byte \** _</span><span class="sxs-lookup"><span data-stu-id="b1514-121">Type: \**BYTE\** _</span></span>

<span data-ttu-id="b1514-122">Um ponteiro para o buffer.</span><span class="sxs-lookup"><span data-stu-id="b1514-122">A pointer to the buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b1514-123">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b1514-123">Return value</span></span>

<span data-ttu-id="b1514-124">Tipo: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="b1514-124">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="b1514-125">Se essa função for bem sucedido, ela retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="b1514-125">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="b1514-126">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="b1514-126">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="b1514-127">Comentários</span><span class="sxs-lookup"><span data-stu-id="b1514-127">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="b1514-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b1514-128">Requirements</span></span>



| <span data-ttu-id="b1514-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="b1514-129">Requirement</span></span> | <span data-ttu-id="b1514-130">Valor</span><span class="sxs-lookup"><span data-stu-id="b1514-130">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b1514-131">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b1514-131">Minimum supported client</span></span><br/> | <span data-ttu-id="b1514-132">Windows XP com SP2, \[ somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b1514-132">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="b1514-133">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b1514-133">Minimum supported server</span></span><br/> | <span data-ttu-id="b1514-134">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="b1514-134">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="b1514-135">DLL</span><span class="sxs-lookup"><span data-stu-id="b1514-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b1514-136"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b1514-136"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




