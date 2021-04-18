---
description: Função de proxy para o método GetMetadataQueryReader.
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
ms.openlocfilehash: e549fdfbacb5bd508a442c70c203595b8819750f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105789237"
---
# <a name="iwicbitmapframedecode_getmetadataqueryreader_proxy-function"></a><span data-ttu-id="f9135-103">\_Função de \_ proxy GetMetadataQueryReader IWICBitmapFrameDecode</span><span class="sxs-lookup"><span data-stu-id="f9135-103">IWICBitmapFrameDecode\_GetMetadataQueryReader\_Proxy function</span></span>

<span data-ttu-id="f9135-104">Função de proxy para o método [**GetMetadataQueryReader**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getmetadataqueryreader) .</span><span class="sxs-lookup"><span data-stu-id="f9135-104">Proxy function for the [**GetMetadataQueryReader**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getmetadataqueryreader) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="f9135-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f9135-105">Syntax</span></span>


```C++
HRESULT IWICBitmapFrameDecode_GetMetadataQueryReader_Proxy(
  _In_  IWICBitmapFrameDecode   *THIS_PTR,
  _Out_ IWICMetadataQueryReader **ppIMetadataQueryReader
);
```



## <a name="parameters"></a><span data-ttu-id="f9135-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f9135-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f9135-107">*Isso \_ PTR* \[\]</span><span class="sxs-lookup"><span data-stu-id="f9135-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f9135-108">Tipo: \**[**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) \** _</span><span class="sxs-lookup"><span data-stu-id="f9135-108">Type: \**[**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)\** _</span></span>

<span data-ttu-id="f9135-109">Ponteiro para este objeto [_ *IWICBitmapFrameDecode* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) .</span><span class="sxs-lookup"><span data-stu-id="f9135-109">Pointer to this [_ *IWICBitmapFrameDecode*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) object.</span></span>

</dd> <dt>

<span data-ttu-id="f9135-110">*ppIMetadataQueryReader* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="f9135-110">*ppIMetadataQueryReader* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f9135-111">Tipo: **[ **IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader)\*\***</span><span class="sxs-lookup"><span data-stu-id="f9135-111">Type: **[**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader)\*\***</span></span>

<span data-ttu-id="f9135-112">Um ponteiro que recebe um ponteiro para um [**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader).</span><span class="sxs-lookup"><span data-stu-id="f9135-112">A pointer that receives a pointer to an [**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f9135-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f9135-113">Return value</span></span>

<span data-ttu-id="f9135-114">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="f9135-114">Type: **HRESULT**</span></span>

<span data-ttu-id="f9135-115">Se essa função for bem sucedido, ela retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="f9135-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="f9135-116">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="f9135-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="f9135-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="f9135-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="f9135-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f9135-118">Requirements</span></span>



| <span data-ttu-id="f9135-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="f9135-119">Requirement</span></span> | <span data-ttu-id="f9135-120">Valor</span><span class="sxs-lookup"><span data-stu-id="f9135-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f9135-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f9135-121">Minimum supported client</span></span><br/> | <span data-ttu-id="f9135-122">Windows XP com SP2, \[ somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f9135-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="f9135-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f9135-123">Minimum supported server</span></span><br/> | <span data-ttu-id="f9135-124">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="f9135-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="f9135-125">DLL</span><span class="sxs-lookup"><span data-stu-id="f9135-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f9135-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f9135-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




