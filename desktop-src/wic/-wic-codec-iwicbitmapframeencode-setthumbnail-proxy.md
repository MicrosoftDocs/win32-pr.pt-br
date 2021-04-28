---
description: Função IWICBitmapFrameEncode_SetThumbnail_Proxy function-proxy para o método SetThumbnail.
ms.assetid: 3ad473ec-9218-4ed1-961d-a2aa0d542119
title: Função IWICBitmapFrameEncode_SetThumbnail_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapFrameEncode_SetThumbnail_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 9af9dd2d4f8fe71a6dc94420db17383a5da6da28
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116594"
---
# <a name="iwicbitmapframeencode_setthumbnail_proxy-function"></a><span data-ttu-id="ac350-103">Função de proxy de IWICBitmapFrameEncode \_ SetThumbnail \_</span><span class="sxs-lookup"><span data-stu-id="ac350-103">IWICBitmapFrameEncode\_SetThumbnail\_Proxy function</span></span>

<span data-ttu-id="ac350-104">Função de proxy para o método [**SetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setthumbnail) .</span><span class="sxs-lookup"><span data-stu-id="ac350-104">Proxy function for the [**SetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setthumbnail) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="ac350-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ac350-105">Syntax</span></span>


```C++
HRESULT IWICBitmapFrameEncode_SetThumbnail_Proxy(
  _In_ IWICBitmapFrameEncode *THIS_PTR,
  _In_ IWICBitmapSource      *pIThumbnail
);
```



## <a name="parameters"></a><span data-ttu-id="ac350-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ac350-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ac350-107">*Isso \_ PTR* \[\]</span><span class="sxs-lookup"><span data-stu-id="ac350-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ac350-108">Tipo: **[ **IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)\***</span><span class="sxs-lookup"><span data-stu-id="ac350-108">Type: **[**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)\***</span></span>

<span data-ttu-id="ac350-109">Ponteiro para este objeto [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) .</span><span class="sxs-lookup"><span data-stu-id="ac350-109">Pointer to this [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) object.</span></span>

</dd> <dt>

<span data-ttu-id="ac350-110">*pIThumbnail* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ac350-110">*pIThumbnail* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ac350-111">Tipo: **[ **IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\***</span><span class="sxs-lookup"><span data-stu-id="ac350-111">Type: **[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\***</span></span>

<span data-ttu-id="ac350-112">A origem do bitmap a ser usada como miniatura.</span><span class="sxs-lookup"><span data-stu-id="ac350-112">The bitmap source to use as the thumbnail.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ac350-113">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="ac350-113">Return value</span></span>

<span data-ttu-id="ac350-114">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="ac350-114">Type: **HRESULT**</span></span>

<span data-ttu-id="ac350-115">Se essa função for bem sucedido, ela retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="ac350-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="ac350-116">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="ac350-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="ac350-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="ac350-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="ac350-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ac350-118">Requirements</span></span>



| <span data-ttu-id="ac350-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="ac350-119">Requirement</span></span> | <span data-ttu-id="ac350-120">Valor</span><span class="sxs-lookup"><span data-stu-id="ac350-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ac350-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ac350-121">Minimum supported client</span></span><br/> | <span data-ttu-id="ac350-122">Windows XP com SP2, \[ somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ac350-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="ac350-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ac350-123">Minimum supported server</span></span><br/> | <span data-ttu-id="ac350-124">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="ac350-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="ac350-125">DLL</span><span class="sxs-lookup"><span data-stu-id="ac350-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ac350-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ac350-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




