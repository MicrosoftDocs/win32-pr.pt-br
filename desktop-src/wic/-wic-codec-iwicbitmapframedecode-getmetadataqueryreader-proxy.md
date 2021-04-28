---
description: Função de proxy de função IWICBitmapFrameDecode_GetMetadataQueryReader_Proxy para o método GetMetadataQueryReader.
ms.assetid: 2a3e0a59-3524-4da4-993a-607a3727faba
title: Função IWICBitmapFrameDecode_GetMetadataQueryReader_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapFrameDecode_GetMetadataQueryReader_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: c6c00cc4463bd8540e5baeb41a10577e9f67e85c
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108091134"
---
# <a name="iwicbitmapframedecode_getmetadataqueryreader_proxy-function"></a><span data-ttu-id="42b54-103">\_Função de \_ proxy GetMetadataQueryReader IWICBitmapFrameDecode</span><span class="sxs-lookup"><span data-stu-id="42b54-103">IWICBitmapFrameDecode\_GetMetadataQueryReader\_Proxy function</span></span>

<span data-ttu-id="42b54-104">Função de proxy para o método [**GetMetadataQueryReader**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getmetadataqueryreader) .</span><span class="sxs-lookup"><span data-stu-id="42b54-104">Proxy function for the [**GetMetadataQueryReader**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getmetadataqueryreader) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="42b54-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="42b54-105">Syntax</span></span>


```C++
HRESULT IWICBitmapFrameDecode_GetMetadataQueryReader_Proxy(
  _In_  IWICBitmapFrameDecode   *THIS_PTR,
  _Out_ IWICMetadataQueryReader **ppIMetadataQueryReader
);
```



## <a name="parameters"></a><span data-ttu-id="42b54-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="42b54-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="42b54-107">*Isso \_ PTR* \[\]</span><span class="sxs-lookup"><span data-stu-id="42b54-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="42b54-108">Tipo: **[ **IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)\***</span><span class="sxs-lookup"><span data-stu-id="42b54-108">Type: **[**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)\***</span></span>

<span data-ttu-id="42b54-109">Ponteiro para este objeto [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) .</span><span class="sxs-lookup"><span data-stu-id="42b54-109">Pointer to this [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) object.</span></span>

</dd> <dt>

<span data-ttu-id="42b54-110">*ppIMetadataQueryReader* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="42b54-110">*ppIMetadataQueryReader* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="42b54-111">Tipo: **[ **IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader)\*\***</span><span class="sxs-lookup"><span data-stu-id="42b54-111">Type: **[**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader)\*\***</span></span>

<span data-ttu-id="42b54-112">Um ponteiro que recebe um ponteiro para um [**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader).</span><span class="sxs-lookup"><span data-stu-id="42b54-112">A pointer that receives a pointer to an [**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="42b54-113">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="42b54-113">Return value</span></span>

<span data-ttu-id="42b54-114">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="42b54-114">Type: **HRESULT**</span></span>

<span data-ttu-id="42b54-115">Se essa função for bem sucedido, ela retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="42b54-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="42b54-116">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="42b54-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="42b54-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="42b54-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="42b54-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="42b54-118">Requirements</span></span>



| <span data-ttu-id="42b54-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="42b54-119">Requirement</span></span> | <span data-ttu-id="42b54-120">Valor</span><span class="sxs-lookup"><span data-stu-id="42b54-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="42b54-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="42b54-121">Minimum supported client</span></span><br/> | <span data-ttu-id="42b54-122">Windows XP com SP2, \[ somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="42b54-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="42b54-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="42b54-123">Minimum supported server</span></span><br/> | <span data-ttu-id="42b54-124">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="42b54-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="42b54-125">DLL</span><span class="sxs-lookup"><span data-stu-id="42b54-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="42b54-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="42b54-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




