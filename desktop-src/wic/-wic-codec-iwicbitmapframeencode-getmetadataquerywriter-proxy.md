---
description: Função de proxy para o método GetMetadataQueryWriter.
ms.assetid: b2c61dee-b72b-408c-8cb9-de2587587f1f
title: Função IWICBitmapFrameEncode_GetMetadataQueryWriter_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapFrameEncode_GetMetadataQueryWriter_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: b6668ffc4261310bfa76424afcae92e14c4ed921
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647080"
---
# <a name="iwicbitmapframeencode_getmetadataquerywriter_proxy-function"></a><span data-ttu-id="bc711-103">\_Função de proxy GetMetadataQueryWriter de IWICBitmapFrameEncode \_</span><span class="sxs-lookup"><span data-stu-id="bc711-103">IWICBitmapFrameEncode\_GetMetadataQueryWriter\_Proxy function</span></span>

<span data-ttu-id="bc711-104">Função de proxy para o método [**GetMetadataQueryWriter**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-getmetadataquerywriter) .</span><span class="sxs-lookup"><span data-stu-id="bc711-104">Proxy function for the [**GetMetadataQueryWriter**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-getmetadataquerywriter) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="bc711-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="bc711-105">Syntax</span></span>


```C++
HRESULT IWICBitmapFrameEncode_GetMetadataQueryWriter_Proxy(
  _In_  IWICBitmapFrameEncode   *THIS_PTR,
  _Out_ IWICMetadataQueryWriter **ppIMetadataQueryWriter
);
```



## <a name="parameters"></a><span data-ttu-id="bc711-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="bc711-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bc711-107">*Isso \_ PTR* \[\]</span><span class="sxs-lookup"><span data-stu-id="bc711-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bc711-108">Tipo: \**[**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) \** _</span><span class="sxs-lookup"><span data-stu-id="bc711-108">Type: \**[**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)\** _</span></span>

<span data-ttu-id="bc711-109">Ponteiro para este objeto [_ *IWICBitmapFrameEncode* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) .</span><span class="sxs-lookup"><span data-stu-id="bc711-109">Pointer to this [_ *IWICBitmapFrameEncode*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) object.</span></span>

</dd> <dt>

<span data-ttu-id="bc711-110">*ppIMetadataQueryWriter* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="bc711-110">*ppIMetadataQueryWriter* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bc711-111">Tipo: **[ **IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)\*\***</span><span class="sxs-lookup"><span data-stu-id="bc711-111">Type: **[**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)\*\***</span></span>

<span data-ttu-id="bc711-112">Um ponteiro que recebe um gravador de consulta de metadados para o quadro.</span><span class="sxs-lookup"><span data-stu-id="bc711-112">A pointer that receives a metadata query writer for the frame.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bc711-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="bc711-113">Return value</span></span>

<span data-ttu-id="bc711-114">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="bc711-114">Type: **HRESULT**</span></span>

<span data-ttu-id="bc711-115">Se essa função for bem sucedido, ela retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="bc711-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="bc711-116">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="bc711-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="bc711-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="bc711-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="bc711-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bc711-118">Requirements</span></span>



| <span data-ttu-id="bc711-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="bc711-119">Requirement</span></span> | <span data-ttu-id="bc711-120">Valor</span><span class="sxs-lookup"><span data-stu-id="bc711-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bc711-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bc711-121">Minimum supported client</span></span><br/> | <span data-ttu-id="bc711-122">Windows XP com SP2, \[ somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="bc711-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="bc711-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bc711-123">Minimum supported server</span></span><br/> | <span data-ttu-id="bc711-124">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="bc711-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="bc711-125">DLL</span><span class="sxs-lookup"><span data-stu-id="bc711-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bc711-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="bc711-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




