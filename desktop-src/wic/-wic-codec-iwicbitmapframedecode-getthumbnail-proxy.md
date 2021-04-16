---
description: Função de proxy para o método GetThumbnail.
ms.assetid: 377f8aac-3cdc-44dc-8c60-9b6bce915486
title: Função IWICBitmapFrameDecode_GetThumbnail_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapFrameDecode_GetThumbnail_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: c29b62b4d3839b7cd3db51574f38ab824b215310
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105765182"
---
# <a name="iwicbitmapframedecode_getthumbnail_proxy-function"></a><span data-ttu-id="b435a-103">Função de proxy de IWICBitmapFrameDecode \_ GetThumbnail \_</span><span class="sxs-lookup"><span data-stu-id="b435a-103">IWICBitmapFrameDecode\_GetThumbnail\_Proxy function</span></span>

<span data-ttu-id="b435a-104">Função de proxy para o método [**GetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getthumbnail) .</span><span class="sxs-lookup"><span data-stu-id="b435a-104">Proxy function for the [**GetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getthumbnail) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="b435a-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b435a-105">Syntax</span></span>


```C++
HRESULT IWICBitmapFrameDecode_GetThumbnail_Proxy(
  _In_  IWICBitmapFrameDecode *THIS_PTR,
  _Out_ IWICBitmapSource      **ppIThumbnail
);
```



## <a name="parameters"></a><span data-ttu-id="b435a-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b435a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b435a-107">*Isso \_ PTR* \[\]</span><span class="sxs-lookup"><span data-stu-id="b435a-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b435a-108">Tipo: \**[**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) \** _</span><span class="sxs-lookup"><span data-stu-id="b435a-108">Type: \**[**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)\** _</span></span>

<span data-ttu-id="b435a-109">Ponteiro para este objeto [_ *IWICBitmapFrameDecode* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) .</span><span class="sxs-lookup"><span data-stu-id="b435a-109">Pointer to this [_ *IWICBitmapFrameDecode*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) object.</span></span>

</dd> <dt>

<span data-ttu-id="b435a-110">*ppIThumbnail* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="b435a-110">*ppIThumbnail* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b435a-111">Tipo: **[ **IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\*\***</span><span class="sxs-lookup"><span data-stu-id="b435a-111">Type: **[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\*\***</span></span>

<span data-ttu-id="b435a-112">Um ponteiro que recebe um ponteiro para o [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) da miniatura.</span><span class="sxs-lookup"><span data-stu-id="b435a-112">A pointer that receives a pointer to the [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) of the thumbnail.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b435a-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b435a-113">Return value</span></span>

<span data-ttu-id="b435a-114">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="b435a-114">Type: **HRESULT**</span></span>

<span data-ttu-id="b435a-115">Se essa função for bem sucedido, ela retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="b435a-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="b435a-116">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="b435a-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="b435a-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="b435a-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="b435a-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b435a-118">Requirements</span></span>



| <span data-ttu-id="b435a-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="b435a-119">Requirement</span></span> | <span data-ttu-id="b435a-120">Valor</span><span class="sxs-lookup"><span data-stu-id="b435a-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b435a-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b435a-121">Minimum supported client</span></span><br/> | <span data-ttu-id="b435a-122">Windows XP com SP2, \[ somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b435a-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="b435a-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b435a-123">Minimum supported server</span></span><br/> | <span data-ttu-id="b435a-124">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="b435a-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="b435a-125">DLL</span><span class="sxs-lookup"><span data-stu-id="b435a-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b435a-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b435a-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




