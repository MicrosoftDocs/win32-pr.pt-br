---
description: Função IWICBitmapDecoder_GetThumbnail_Proxy function-proxy para o método GetThumbnail.
ms.assetid: 37a6ba78-0d1b-47f6-9b12-8ad123c8ee86
title: Função IWICBitmapDecoder_GetThumbnail_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapDecoder_GetThumbnail_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 3fb4d6ae050772bb6392e1d94c88ef5bfc23d2ba
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108100604"
---
# <a name="iwicbitmapdecoder_getthumbnail_proxy-function"></a><span data-ttu-id="9d624-103">\_Função de proxy de SetThumbnail de IWICBitmapDecoder \_</span><span class="sxs-lookup"><span data-stu-id="9d624-103">IWICBitmapDecoder\_GetThumbnail\_Proxy function</span></span>

<span data-ttu-id="9d624-104">Função de proxy para o método [**GetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getthumbnail) .</span><span class="sxs-lookup"><span data-stu-id="9d624-104">Proxy function for the [**GetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getthumbnail) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="9d624-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9d624-105">Syntax</span></span>


```C++
HRESULT IWICBitmapDecoder_GetThumbnail_Proxy(
  _In_  IWICBitmapDecoder *THIS_PTR,
  _Out_ IWICBitmapSource  **ppIThumbnail
);
```



## <a name="parameters"></a><span data-ttu-id="9d624-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9d624-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9d624-107">*Isso \_ PTR* \[\]</span><span class="sxs-lookup"><span data-stu-id="9d624-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9d624-108">Tipo: **[ **IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)\***</span><span class="sxs-lookup"><span data-stu-id="9d624-108">Type: **[**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)\***</span></span>

<span data-ttu-id="9d624-109">Ponteiro para este objeto [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) .</span><span class="sxs-lookup"><span data-stu-id="9d624-109">Pointer to this [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) object.</span></span>

</dd> <dt>

<span data-ttu-id="9d624-110">*ppIThumbnail* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="9d624-110">*ppIThumbnail* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9d624-111">Tipo: **[ **IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\*\***</span><span class="sxs-lookup"><span data-stu-id="9d624-111">Type: **[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\*\***</span></span>

<span data-ttu-id="9d624-112">Um ponteiro que recebe um ponteiro para o [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) da miniatura.</span><span class="sxs-lookup"><span data-stu-id="9d624-112">A pointer that receives a pointer to the [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) of the thumbnail.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9d624-113">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="9d624-113">Return value</span></span>

<span data-ttu-id="9d624-114">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="9d624-114">Type: **HRESULT**</span></span>

<span data-ttu-id="9d624-115">Se essa função for bem sucedido, ela retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="9d624-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="9d624-116">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="9d624-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="9d624-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="9d624-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="9d624-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9d624-118">Requirements</span></span>



| <span data-ttu-id="9d624-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="9d624-119">Requirement</span></span> | <span data-ttu-id="9d624-120">Valor</span><span class="sxs-lookup"><span data-stu-id="9d624-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9d624-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9d624-121">Minimum supported client</span></span><br/> | <span data-ttu-id="9d624-122">Windows XP com SP2, \[ somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="9d624-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="9d624-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9d624-123">Minimum supported server</span></span><br/> | <span data-ttu-id="9d624-124">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="9d624-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="9d624-125">DLL</span><span class="sxs-lookup"><span data-stu-id="9d624-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9d624-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9d624-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




