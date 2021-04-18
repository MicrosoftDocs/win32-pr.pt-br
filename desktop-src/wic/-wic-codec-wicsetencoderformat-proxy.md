---
description: Função de proxy para negociar o formato de pixel e a paleta para o codificador.
ms.assetid: 01179598-ba40-4aed-a7c4-888cb4e851f4
title: Função WICSetEncoderFormat_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WICSetEncoderFormat_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 7ea0988d29d1d9ed04668dfbe8ce86b97af6534a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105760585"
---
# <a name="wicsetencoderformat_proxy-function"></a><span data-ttu-id="c4003-103">\_Função de proxy WICSetEncoderFormat</span><span class="sxs-lookup"><span data-stu-id="c4003-103">WICSetEncoderFormat\_Proxy function</span></span>

<span data-ttu-id="c4003-104">Função de proxy para negociar o formato de pixel e a paleta para o codificador.</span><span class="sxs-lookup"><span data-stu-id="c4003-104">Proxy function for negotiating the pixel format and the palette for the encoder.</span></span>

## <a name="syntax"></a><span data-ttu-id="c4003-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c4003-105">Syntax</span></span>


```C++
HRESULT WICSetEncoderFormat_Proxy(
  _In_  IWICBitmapSource      *pSourceIn,
  _In_  IWICPalette           *pIPalette,
  _In_  IWICBitmapFrameEncode *pIFrameEncode,
  _Out_ IWICBitmapSource      **ppSourceOut
);
```



## <a name="parameters"></a><span data-ttu-id="c4003-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c4003-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c4003-107">*pSourceIn* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c4003-107">*pSourceIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c4003-108">Tipo: \**[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) \** _</span><span class="sxs-lookup"><span data-stu-id="c4003-108">Type: \**[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\** _</span></span>

<span data-ttu-id="c4003-109">Ponteiro para o bitmap de origem.</span><span class="sxs-lookup"><span data-stu-id="c4003-109">Pointer to the source bitmap.</span></span>

</dd> <dt>

<span data-ttu-id="c4003-110">_pIPalette \* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c4003-110">_pIPalette\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c4003-111">Tipo: \**[**IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) \** _</span><span class="sxs-lookup"><span data-stu-id="c4003-111">Type: \**[**IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette)\** _</span></span>

<span data-ttu-id="c4003-112">Ponteiro para a paleta a ser usada para codificação.</span><span class="sxs-lookup"><span data-stu-id="c4003-112">Pointer to the palette to use for encoding.</span></span>

</dd> <dt>

<span data-ttu-id="c4003-113">_pIFrameEncode \* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c4003-113">_pIFrameEncode\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c4003-114">Tipo: \**[**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) \** _</span><span class="sxs-lookup"><span data-stu-id="c4003-114">Type: \**[**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)\** _</span></span>

<span data-ttu-id="c4003-115">Ponteiro para o objeto de codificação do quadro.</span><span class="sxs-lookup"><span data-stu-id="c4003-115">Pointer to the frame encode object.</span></span>

</dd> <dt>

<span data-ttu-id="c4003-116">_ppSourceOut \* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="c4003-116">_ppSourceOut\* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c4003-117">Tipo: **[ **IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\*\***</span><span class="sxs-lookup"><span data-stu-id="c4003-117">Type: **[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\*\***</span></span>

<span data-ttu-id="c4003-118">Ponteiro que recebe um ponteiro para a fonte de saída.</span><span class="sxs-lookup"><span data-stu-id="c4003-118">Pointer that receives a pointer to the output source.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c4003-119">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c4003-119">Return value</span></span>

<span data-ttu-id="c4003-120">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="c4003-120">Type: **HRESULT**</span></span>

<span data-ttu-id="c4003-121">Se essa função for bem sucedido, ela retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="c4003-121">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="c4003-122">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="c4003-122">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="c4003-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="c4003-123">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="c4003-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c4003-124">Requirements</span></span>



| <span data-ttu-id="c4003-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="c4003-125">Requirement</span></span> | <span data-ttu-id="c4003-126">Valor</span><span class="sxs-lookup"><span data-stu-id="c4003-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c4003-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c4003-127">Minimum supported client</span></span><br/> | <span data-ttu-id="c4003-128">Windows XP com SP2, \[ somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c4003-128">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="c4003-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c4003-129">Minimum supported server</span></span><br/> | <span data-ttu-id="c4003-130">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="c4003-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="c4003-131">DLL</span><span class="sxs-lookup"><span data-stu-id="c4003-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c4003-132"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c4003-132"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




