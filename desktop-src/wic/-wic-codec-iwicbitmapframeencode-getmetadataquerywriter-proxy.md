---
description: Função de proxy de função IWICBitmapFrameEncode_GetMetadataQueryWriter_Proxy para o método GetMetadataQueryWriter.
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
ms.openlocfilehash: 89eb7342277d335c78ee2bc6807f2fc4d170bb9b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108113604"
---
# <a name="iwicbitmapframeencode_getmetadataquerywriter_proxy-function"></a><span data-ttu-id="6276b-103">\_Função de proxy GetMetadataQueryWriter de IWICBitmapFrameEncode \_</span><span class="sxs-lookup"><span data-stu-id="6276b-103">IWICBitmapFrameEncode\_GetMetadataQueryWriter\_Proxy function</span></span>

<span data-ttu-id="6276b-104">Função de proxy para o método [**GetMetadataQueryWriter**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-getmetadataquerywriter) .</span><span class="sxs-lookup"><span data-stu-id="6276b-104">Proxy function for the [**GetMetadataQueryWriter**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-getmetadataquerywriter) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="6276b-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6276b-105">Syntax</span></span>


```C++
HRESULT IWICBitmapFrameEncode_GetMetadataQueryWriter_Proxy(
  _In_  IWICBitmapFrameEncode   *THIS_PTR,
  _Out_ IWICMetadataQueryWriter **ppIMetadataQueryWriter
);
```



## <a name="parameters"></a><span data-ttu-id="6276b-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6276b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6276b-107">*Isso \_ PTR* \[\]</span><span class="sxs-lookup"><span data-stu-id="6276b-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6276b-108">Tipo: **[ **IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)\***</span><span class="sxs-lookup"><span data-stu-id="6276b-108">Type: **[**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)\***</span></span>

<span data-ttu-id="6276b-109">Ponteiro para este objeto [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) .</span><span class="sxs-lookup"><span data-stu-id="6276b-109">Pointer to this [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) object.</span></span>

</dd> <dt>

<span data-ttu-id="6276b-110">*ppIMetadataQueryWriter* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="6276b-110">*ppIMetadataQueryWriter* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6276b-111">Tipo: **[ **IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)\*\***</span><span class="sxs-lookup"><span data-stu-id="6276b-111">Type: **[**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)\*\***</span></span>

<span data-ttu-id="6276b-112">Um ponteiro que recebe um gravador de consulta de metadados para o quadro.</span><span class="sxs-lookup"><span data-stu-id="6276b-112">A pointer that receives a metadata query writer for the frame.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6276b-113">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="6276b-113">Return value</span></span>

<span data-ttu-id="6276b-114">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="6276b-114">Type: **HRESULT**</span></span>

<span data-ttu-id="6276b-115">Se essa função for bem sucedido, ela retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="6276b-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="6276b-116">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="6276b-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="6276b-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="6276b-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="6276b-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6276b-118">Requirements</span></span>



| <span data-ttu-id="6276b-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="6276b-119">Requirement</span></span> | <span data-ttu-id="6276b-120">Valor</span><span class="sxs-lookup"><span data-stu-id="6276b-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6276b-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6276b-121">Minimum supported client</span></span><br/> | <span data-ttu-id="6276b-122">Windows XP com SP2, \[ somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="6276b-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="6276b-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6276b-123">Minimum supported server</span></span><br/> | <span data-ttu-id="6276b-124">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="6276b-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="6276b-125">DLL</span><span class="sxs-lookup"><span data-stu-id="6276b-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6276b-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6276b-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




