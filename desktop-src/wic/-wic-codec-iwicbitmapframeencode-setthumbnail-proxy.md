---
description: Função de proxy para o método SetThumbnail.
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
ms.openlocfilehash: 052e73911178ef0db957c5dd8edcf6e9d6892ace
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829214"
---
# <a name="iwicbitmapframeencode_setthumbnail_proxy-function"></a><span data-ttu-id="e3961-103">Função de proxy de IWICBitmapFrameEncode \_ SetThumbnail \_</span><span class="sxs-lookup"><span data-stu-id="e3961-103">IWICBitmapFrameEncode\_SetThumbnail\_Proxy function</span></span>

<span data-ttu-id="e3961-104">Função de proxy para o método [**SetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setthumbnail) .</span><span class="sxs-lookup"><span data-stu-id="e3961-104">Proxy function for the [**SetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setthumbnail) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="e3961-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e3961-105">Syntax</span></span>


```C++
HRESULT IWICBitmapFrameEncode_SetThumbnail_Proxy(
  _In_ IWICBitmapFrameEncode *THIS_PTR,
  _In_ IWICBitmapSource      *pIThumbnail
);
```



## <a name="parameters"></a><span data-ttu-id="e3961-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e3961-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e3961-107">*Isso \_ PTR* \[\]</span><span class="sxs-lookup"><span data-stu-id="e3961-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e3961-108">Tipo: \**[**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) \** _</span><span class="sxs-lookup"><span data-stu-id="e3961-108">Type: \**[**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)\** _</span></span>

<span data-ttu-id="e3961-109">Ponteiro para este objeto [_ *IWICBitmapFrameEncode* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) .</span><span class="sxs-lookup"><span data-stu-id="e3961-109">Pointer to this [_ *IWICBitmapFrameEncode*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) object.</span></span>

</dd> <dt>

<span data-ttu-id="e3961-110">*pIThumbnail* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e3961-110">*pIThumbnail* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e3961-111">Tipo: \**[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) \** _</span><span class="sxs-lookup"><span data-stu-id="e3961-111">Type: \**[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\** _</span></span>

<span data-ttu-id="e3961-112">A origem do bitmap a ser usada como miniatura.</span><span class="sxs-lookup"><span data-stu-id="e3961-112">The bitmap source to use as the thumbnail.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e3961-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e3961-113">Return value</span></span>

<span data-ttu-id="e3961-114">Tipo: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="e3961-114">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="e3961-115">Se essa função for bem sucedido, ela retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="e3961-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="e3961-116">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="e3961-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="e3961-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="e3961-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="e3961-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e3961-118">Requirements</span></span>



| <span data-ttu-id="e3961-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="e3961-119">Requirement</span></span> | <span data-ttu-id="e3961-120">Valor</span><span class="sxs-lookup"><span data-stu-id="e3961-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e3961-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e3961-121">Minimum supported client</span></span><br/> | <span data-ttu-id="e3961-122">Windows XP com SP2, \[ somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e3961-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="e3961-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e3961-123">Minimum supported server</span></span><br/> | <span data-ttu-id="e3961-124">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="e3961-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="e3961-125">DLL</span><span class="sxs-lookup"><span data-stu-id="e3961-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e3961-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e3961-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




