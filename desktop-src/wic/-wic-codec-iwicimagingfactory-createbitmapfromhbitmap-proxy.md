---
description: Função de proxy para o método CreateBitmapFromHBITMAP.
ms.assetid: e4e9a6b4-00d9-4f87-aeec-f2c02c3f44ab
title: Função IWICImagingFactory_CreateBitmapFromHBITMAP_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICImagingFactory_CreateBitmapFromHBITMAP_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 6599a9699e6fb83c1678cd0360f906cc8e0668c1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105761894"
---
# <a name="iwicimagingfactory_createbitmapfromhbitmap_proxy-function"></a><span data-ttu-id="ad951-103">\_Função de \_ proxy IWICImagingFactory CreateBitmapFromHBITMAP</span><span class="sxs-lookup"><span data-stu-id="ad951-103">IWICImagingFactory\_CreateBitmapFromHBITMAP\_Proxy function</span></span>

<span data-ttu-id="ad951-104">Função de proxy para o método [**CreateBitmapFromHBITMAP**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createbitmapfromhbitmap) .</span><span class="sxs-lookup"><span data-stu-id="ad951-104">Proxy function for the [**CreateBitmapFromHBITMAP**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createbitmapfromhbitmap) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="ad951-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ad951-105">Syntax</span></span>


```C++
HRESULT IWICImagingFactory_CreateBitmapFromHBITMAP_Proxy(
  _In_  IWICImagingFactory          *pFactory,
  _In_  HBITMAP                     hBitmap,
  _In_  HPALETTE                    hPalette,
  _In_  WICBitmapAlphaChannelOption options,
  _Out_ IWICBitmap                  **ppIBitmap
);
```



## <a name="parameters"></a><span data-ttu-id="ad951-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ad951-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ad951-107">*pFactory* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ad951-107">*pFactory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ad951-108">Tipo: \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) \** _</span><span class="sxs-lookup"><span data-stu-id="ad951-108">Type: \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)\** _</span></span>

</dd> <dt>

<span data-ttu-id="ad951-109">_hBitmap \* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ad951-109">_hBitmap\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ad951-110">Tipo: **HBITMAP**</span><span class="sxs-lookup"><span data-stu-id="ad951-110">Type: **HBITMAP**</span></span>

<span data-ttu-id="ad951-111">Um identificador de bitmap do qual criar o bitmap.</span><span class="sxs-lookup"><span data-stu-id="ad951-111">A bitmap handle to create the bitmap from.</span></span>

</dd> <dt>

<span data-ttu-id="ad951-112">*hPalette* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ad951-112">*hPalette* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ad951-113">Tipo: **HPALETTE**</span><span class="sxs-lookup"><span data-stu-id="ad951-113">Type: **HPALETTE**</span></span>

<span data-ttu-id="ad951-114">Um identificador de paleta usado para criar o bitmap.</span><span class="sxs-lookup"><span data-stu-id="ad951-114">A palette handle used to create the bitmap.</span></span>

</dd> <dt>

<span data-ttu-id="ad951-115">*Opções* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="ad951-115">*options* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ad951-116">Tipo: **[ **WICBitmapAlphaChannelOption**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapalphachanneloption)**</span><span class="sxs-lookup"><span data-stu-id="ad951-116">Type: **[**WICBitmapAlphaChannelOption**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapalphachanneloption)**</span></span>

<span data-ttu-id="ad951-117">As opções de canal alfa para criar o bitmap.</span><span class="sxs-lookup"><span data-stu-id="ad951-117">The alpha channel options to create the bitmap.</span></span>

</dd> <dt>

<span data-ttu-id="ad951-118">*ppIBitmap* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="ad951-118">*ppIBitmap* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ad951-119">Tipo: **[ **IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap)\*\***</span><span class="sxs-lookup"><span data-stu-id="ad951-119">Type: **[**IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap)\*\***</span></span>

<span data-ttu-id="ad951-120">Um ponteiro que recebe um ponteiro para o novo bitmap.</span><span class="sxs-lookup"><span data-stu-id="ad951-120">A pointer that receives a pointer to the new bitmap.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ad951-121">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ad951-121">Return value</span></span>

<span data-ttu-id="ad951-122">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="ad951-122">Type: **HRESULT**</span></span>

<span data-ttu-id="ad951-123">Se essa função for bem sucedido, ela retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="ad951-123">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="ad951-124">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="ad951-124">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="ad951-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="ad951-125">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="ad951-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ad951-126">Requirements</span></span>



| <span data-ttu-id="ad951-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="ad951-127">Requirement</span></span> | <span data-ttu-id="ad951-128">Valor</span><span class="sxs-lookup"><span data-stu-id="ad951-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ad951-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ad951-129">Minimum supported client</span></span><br/> | <span data-ttu-id="ad951-130">Windows XP com SP2, \[ somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ad951-130">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="ad951-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ad951-131">Minimum supported server</span></span><br/> | <span data-ttu-id="ad951-132">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="ad951-132">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="ad951-133">DLL</span><span class="sxs-lookup"><span data-stu-id="ad951-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ad951-134"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ad951-134"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




