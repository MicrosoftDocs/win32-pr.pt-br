---
description: Função de proxy para o método CreateBitmap.
ms.assetid: 5647521b-231d-4819-97ab-4dfb5f796211
title: Função IWICImagingFactory_CreateBitmap_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICImagingFactory_CreateBitmap_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 56684de0280ae27bf2ec1e900bd718faec4733fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105788642"
---
# <a name="iwicimagingfactory_createbitmap_proxy-function"></a><span data-ttu-id="91d68-103">\_Função de proxy CreateBitmap IWICImagingFactory \_</span><span class="sxs-lookup"><span data-stu-id="91d68-103">IWICImagingFactory\_CreateBitmap\_Proxy function</span></span>

<span data-ttu-id="91d68-104">Função de proxy para o método [**CreateBitmap**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createbitmap) .</span><span class="sxs-lookup"><span data-stu-id="91d68-104">Proxy function for the [**CreateBitmap**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createbitmap) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="91d68-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="91d68-105">Syntax</span></span>


```C++
HRESULT IWICImagingFactory_CreateBitmap_Proxy(
  _In_  IWICImagingFactory         *pFactory,
  _In_  UINT                       uiWidth,
  _In_  UINT                       uiHeight,
  _In_  REFWICPixelFormatGUID      pixelFormat,
  _In_  WICBitmapCreateCacheOption option,
  _Out_ IWICBitmap                 **ppIBitmap
);
```



## <a name="parameters"></a><span data-ttu-id="91d68-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="91d68-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="91d68-107">*pFactory* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="91d68-107">*pFactory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="91d68-108">Tipo: \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) \** _</span><span class="sxs-lookup"><span data-stu-id="91d68-108">Type: \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)\** _</span></span>

</dd> <dt>

<span data-ttu-id="91d68-109">_uiWidth \* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="91d68-109">_uiWidth\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="91d68-110">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="91d68-110">Type: **UINT**</span></span>

<span data-ttu-id="91d68-111">A largura do novo bitmap.</span><span class="sxs-lookup"><span data-stu-id="91d68-111">The width of the new bitmap .</span></span>

</dd> <dt>

<span data-ttu-id="91d68-112">*uiHeight* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="91d68-112">*uiHeight* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="91d68-113">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="91d68-113">Type: **UINT**</span></span>

<span data-ttu-id="91d68-114">A altura do novo bitmap.</span><span class="sxs-lookup"><span data-stu-id="91d68-114">The height of the new bitmap.</span></span>

</dd> <dt>

<span data-ttu-id="91d68-115">*PixelFormat* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="91d68-115">*pixelFormat* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="91d68-116">Tipo: **REFWICPixelFormatGUID**</span><span class="sxs-lookup"><span data-stu-id="91d68-116">Type: **REFWICPixelFormatGUID**</span></span>

<span data-ttu-id="91d68-117">O formato de pixel do novo bitmap.</span><span class="sxs-lookup"><span data-stu-id="91d68-117">The pixel format of the new bitmap.</span></span>

</dd> <dt>

<span data-ttu-id="91d68-118">*opção* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="91d68-118">*option* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="91d68-119">Tipo: **[ **WICBitmapCreateCacheOption**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapcreatecacheoption)**</span><span class="sxs-lookup"><span data-stu-id="91d68-119">Type: **[**WICBitmapCreateCacheOption**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapcreatecacheoption)**</span></span>

<span data-ttu-id="91d68-120">As opções de criação de cache do novo bitmap.</span><span class="sxs-lookup"><span data-stu-id="91d68-120">The cache creation options of the new bitmap.</span></span>

</dd> <dt>

<span data-ttu-id="91d68-121">*ppIBitmap* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="91d68-121">*ppIBitmap* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="91d68-122">Tipo: **[ **IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap)\*\***</span><span class="sxs-lookup"><span data-stu-id="91d68-122">Type: **[**IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap)\*\***</span></span>

<span data-ttu-id="91d68-123">Um ponteiro que recebe um ponteiro para o novo bitmap.</span><span class="sxs-lookup"><span data-stu-id="91d68-123">A pointer that receives a pointer to the new bitmap.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="91d68-124">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="91d68-124">Return value</span></span>

<span data-ttu-id="91d68-125">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="91d68-125">Type: **HRESULT**</span></span>

<span data-ttu-id="91d68-126">Se essa função for bem sucedido, ela retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="91d68-126">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="91d68-127">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="91d68-127">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="91d68-128">Comentários</span><span class="sxs-lookup"><span data-stu-id="91d68-128">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="91d68-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="91d68-129">Requirements</span></span>



| <span data-ttu-id="91d68-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="91d68-130">Requirement</span></span> | <span data-ttu-id="91d68-131">Valor</span><span class="sxs-lookup"><span data-stu-id="91d68-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="91d68-132">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="91d68-132">Minimum supported client</span></span><br/> | <span data-ttu-id="91d68-133">Windows XP com SP2, \[ somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="91d68-133">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="91d68-134">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="91d68-134">Minimum supported server</span></span><br/> | <span data-ttu-id="91d68-135">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="91d68-135">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="91d68-136">DLL</span><span class="sxs-lookup"><span data-stu-id="91d68-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="91d68-137"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="91d68-137"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




