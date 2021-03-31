---
description: Função de proxy para o método Initialize.
ms.assetid: 26112d52-95e2-4c67-83fc-cf5e28712730
title: Função IWICFormatConverter_Initialize_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICFormatConverter_Initialize_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 6450c1a508507db73e44ef8b88b4f94970ac6004
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171154"
---
# <a name="iwicformatconverter_initialize_proxy-function"></a><span data-ttu-id="5bd4b-103">Função de proxy de \_ inicialização IWICFormatConverter \_</span><span class="sxs-lookup"><span data-stu-id="5bd4b-103">IWICFormatConverter\_Initialize\_Proxy function</span></span>

<span data-ttu-id="5bd4b-104">Função de proxy para o método [**Initialize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicformatconverter-initialize) .</span><span class="sxs-lookup"><span data-stu-id="5bd4b-104">Proxy function for the [**Initialize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicformatconverter-initialize) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="5bd4b-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5bd4b-105">Syntax</span></span>


```C++
HRESULT IWICFormatConverter_Initialize_Proxy(
  _In_ IWICFormatConverter   *THIS_PTR,
  _In_ IWICBitmapSource      *pISource,
  _In_ REFWICPixelFormatGUID dstFormat,
  _In_ WICBitmapDitherType   dither,
  _In_ IWICPalette           *pIPalette,
  _In_ double                alphaThresholdPercent,
  _In_ WICBitmapPaletteType  paletteTranslate
);
```



## <a name="parameters"></a><span data-ttu-id="5bd4b-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5bd4b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5bd4b-107">*Isso \_ PTR* \[\]</span><span class="sxs-lookup"><span data-stu-id="5bd4b-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5bd4b-108">Tipo: \**[**IWICFormatConverter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicformatconverter) \** _</span><span class="sxs-lookup"><span data-stu-id="5bd4b-108">Type: \**[**IWICFormatConverter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicformatconverter)\** _</span></span>

<span data-ttu-id="5bd4b-109">Ponteiro para este objeto [_ *IWICFormatConverter* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicformatconverter) .</span><span class="sxs-lookup"><span data-stu-id="5bd4b-109">Pointer to this [_ *IWICFormatConverter*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicformatconverter) object.</span></span>

</dd> <dt>

<span data-ttu-id="5bd4b-110">*pISource* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="5bd4b-110">*pISource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5bd4b-111">Tipo: \**[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) \** _</span><span class="sxs-lookup"><span data-stu-id="5bd4b-111">Type: \**[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\** _</span></span>

<span data-ttu-id="5bd4b-112">O bitmap de entrada a ser convertido</span><span class="sxs-lookup"><span data-stu-id="5bd4b-112">The input bitmap to convert</span></span>

</dd> <dt>

<span data-ttu-id="5bd4b-113">_dstFormat \* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5bd4b-113">_dstFormat\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5bd4b-114">Tipo: **REFWICPixelFormatGUID**</span><span class="sxs-lookup"><span data-stu-id="5bd4b-114">Type: **REFWICPixelFormatGUID**</span></span>

<span data-ttu-id="5bd4b-115">O GUID de formato de pixel de destino.</span><span class="sxs-lookup"><span data-stu-id="5bd4b-115">The destination pixel format GUID.</span></span>

</dd> <dt>

<span data-ttu-id="5bd4b-116">*pontilhado* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="5bd4b-116">*dither* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5bd4b-117">Tipo: **[ **WICBitmapDitherType**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapdithertype)**</span><span class="sxs-lookup"><span data-stu-id="5bd4b-117">Type: **[**WICBitmapDitherType**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapdithertype)**</span></span>

<span data-ttu-id="5bd4b-118">O [**WICBitmapDitherType**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapdithertype) usado para conversão.</span><span class="sxs-lookup"><span data-stu-id="5bd4b-118">The [**WICBitmapDitherType**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapdithertype) used for conversion.</span></span>

</dd> <dt>

<span data-ttu-id="5bd4b-119">*pIPalette* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="5bd4b-119">*pIPalette* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5bd4b-120">Tipo: \**[**IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) \** _</span><span class="sxs-lookup"><span data-stu-id="5bd4b-120">Type: \**[**IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette)\** _</span></span>

<span data-ttu-id="5bd4b-121">A paleta a ser usada para conversão.</span><span class="sxs-lookup"><span data-stu-id="5bd4b-121">The palette to use for conversion.</span></span>

</dd> <dt>

<span data-ttu-id="5bd4b-122">_alphaThresholdPercent \* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5bd4b-122">_alphaThresholdPercent\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5bd4b-123">Tipo: **duplo**</span><span class="sxs-lookup"><span data-stu-id="5bd4b-123">Type: **double**</span></span>

<span data-ttu-id="5bd4b-124">O limite Alfa a ser usado para conversão.</span><span class="sxs-lookup"><span data-stu-id="5bd4b-124">The alpha threshold to use for conversion.</span></span>

</dd> <dt>

<span data-ttu-id="5bd4b-125">*paletteTranslate* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="5bd4b-125">*paletteTranslate* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5bd4b-126">Tipo: **[ **WICBitmapPaletteType**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmappalettetype)**</span><span class="sxs-lookup"><span data-stu-id="5bd4b-126">Type: **[**WICBitmapPaletteType**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmappalettetype)**</span></span>

<span data-ttu-id="5bd4b-127">O tipo de tradução da paleta a ser usado para conversão.</span><span class="sxs-lookup"><span data-stu-id="5bd4b-127">The palette translation type to use for conversion.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5bd4b-128">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="5bd4b-128">Return value</span></span>

<span data-ttu-id="5bd4b-129">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="5bd4b-129">Type: **HRESULT**</span></span>

<span data-ttu-id="5bd4b-130">Se essa função for bem sucedido, ela retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="5bd4b-130">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="5bd4b-131">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="5bd4b-131">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="5bd4b-132">Comentários</span><span class="sxs-lookup"><span data-stu-id="5bd4b-132">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="5bd4b-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5bd4b-133">Requirements</span></span>



| <span data-ttu-id="5bd4b-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="5bd4b-134">Requirement</span></span> | <span data-ttu-id="5bd4b-135">Valor</span><span class="sxs-lookup"><span data-stu-id="5bd4b-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5bd4b-136">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5bd4b-136">Minimum supported client</span></span><br/> | <span data-ttu-id="5bd4b-137">Windows XP com SP2, \[ somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="5bd4b-137">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="5bd4b-138">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5bd4b-138">Minimum supported server</span></span><br/> | <span data-ttu-id="5bd4b-139">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="5bd4b-139">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="5bd4b-140">DLL</span><span class="sxs-lookup"><span data-stu-id="5bd4b-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5bd4b-141"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5bd4b-141"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




