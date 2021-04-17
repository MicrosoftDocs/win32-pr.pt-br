---
description: Inicializa um IWICColorTransform com um IWICBitmapSource e o transforma de um IWICColorContext para outro.
ms.assetid: 68C8EF36-DFFF-4FF3-BD9A-583508F9C2B1
title: Função IWICColorTransform_Initialize_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICColorTransform_Initialize_Proxy
api_type:
- DllExport
api_location:
- WindowsCodecsExt.dll
ms.openlocfilehash: 29d29bfd925d979897b22711c748083b94673142
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105782517"
---
# <a name="iwiccolortransform_initialize_proxy-function"></a><span data-ttu-id="ce98b-103">Função de proxy de \_ inicialização IWICColorTransform \_</span><span class="sxs-lookup"><span data-stu-id="ce98b-103">IWICColorTransform\_Initialize\_Proxy function</span></span>

<span data-ttu-id="ce98b-104">Inicializa um [**IWICColorTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolortransform) com um [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) e o transforma de um [**IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext) para outro.</span><span class="sxs-lookup"><span data-stu-id="ce98b-104">Initializes an [**IWICColorTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolortransform) with a [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) and transforms it from one [**IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext) to another.</span></span>

## <a name="syntax"></a><span data-ttu-id="ce98b-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ce98b-105">Syntax</span></span>


```C++
HRESULT IWICColorTransform_Initialize_Proxy(
  _In_ IWICColorTransform    *pIColorTransform,
  _In_ IWICBitmapSource      *pIBitmapSource,
  _In_ IWICColorContext      *pIContextSource,
  _In_ IWICColorContext      *pIContextDest,
  _In_ REFWICPixelFormatGUID pixelFmtDest
);
```



## <a name="parameters"></a><span data-ttu-id="ce98b-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ce98b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ce98b-107">*pIColorTransform* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ce98b-107">*pIColorTransform* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ce98b-108">Tipo: **[ **IWICColorTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolortransform)\***</span><span class="sxs-lookup"><span data-stu-id="ce98b-108">Type: **[**IWICColorTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolortransform)\***</span></span>

<span data-ttu-id="ce98b-109">A transformação de cor a ser inicializada.</span><span class="sxs-lookup"><span data-stu-id="ce98b-109">The color transform to initialize.</span></span>

</dd> <dt>

<span data-ttu-id="ce98b-110">*pIBitmapSource* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ce98b-110">*pIBitmapSource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ce98b-111">Tipo: **[ **IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\***</span><span class="sxs-lookup"><span data-stu-id="ce98b-111">Type: **[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\***</span></span>

<span data-ttu-id="ce98b-112">A origem do bitmap usada para inicializar a transformação de cor.</span><span class="sxs-lookup"><span data-stu-id="ce98b-112">The bitmap source used to initialize the color transform.</span></span>

</dd> <dt>

<span data-ttu-id="ce98b-113">*pIContextSource* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ce98b-113">*pIContextSource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ce98b-114">Tipo: **[ **IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext)\***</span><span class="sxs-lookup"><span data-stu-id="ce98b-114">Type: **[**IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext)\***</span></span>

<span data-ttu-id="ce98b-115">A origem do contexto de cor.</span><span class="sxs-lookup"><span data-stu-id="ce98b-115">The color context source.</span></span>

</dd> <dt>

<span data-ttu-id="ce98b-116">*pIContextDest* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ce98b-116">*pIContextDest* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ce98b-117">Tipo: **[ **IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext)\***</span><span class="sxs-lookup"><span data-stu-id="ce98b-117">Type: **[**IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext)\***</span></span>

<span data-ttu-id="ce98b-118">O destino do contexto de cor.</span><span class="sxs-lookup"><span data-stu-id="ce98b-118">The color context destination.</span></span>

</dd> <dt>

<span data-ttu-id="ce98b-119">*pixelFmtDest* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ce98b-119">*pixelFmtDest* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ce98b-120">Tipo: **REFWICPixelFormatGUID**</span><span class="sxs-lookup"><span data-stu-id="ce98b-120">Type: **REFWICPixelFormatGUID**</span></span>

<span data-ttu-id="ce98b-121">O GUID do formato de pixel desejado.</span><span class="sxs-lookup"><span data-stu-id="ce98b-121">The GUID of the desired pixel format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ce98b-122">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ce98b-122">Return value</span></span>

<span data-ttu-id="ce98b-123">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="ce98b-123">Type: **HRESULT**</span></span>

<span data-ttu-id="ce98b-124">Se essa função for bem sucedido, ela retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="ce98b-124">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="ce98b-125">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="ce98b-125">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="ce98b-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ce98b-126">Requirements</span></span>



| <span data-ttu-id="ce98b-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="ce98b-127">Requirement</span></span> | <span data-ttu-id="ce98b-128">Valor</span><span class="sxs-lookup"><span data-stu-id="ce98b-128">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ce98b-129">DLL</span><span class="sxs-lookup"><span data-stu-id="ce98b-129">DLL</span></span><br/> | <dl> <span data-ttu-id="ce98b-130"><dt>WindowsCodecsExt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ce98b-130"><dt>WindowsCodecsExt.dll</dt></span></span> </dl> |



 

 




