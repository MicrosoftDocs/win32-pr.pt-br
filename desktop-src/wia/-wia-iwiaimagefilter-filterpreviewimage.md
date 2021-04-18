---
description: Filtra a imagem de visualização.
ms.assetid: 1710211a-a35c-4a51-b3bb-6f03f234f247
title: 'Método IWiaImageFilter:: FilterPreviewImage (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaImageFilter.FilterPreviewImage
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 882aaf0d131ae6fe062c00c0181e2f913a0e1bc5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105791450"
---
# <a name="iwiaimagefilterfilterpreviewimage-method"></a><span data-ttu-id="c91fe-103">Método IWiaImageFilter:: FilterPreviewImage</span><span class="sxs-lookup"><span data-stu-id="c91fe-103">IWiaImageFilter::FilterPreviewImage method</span></span>

<span data-ttu-id="c91fe-104">Filtra a imagem de visualização.</span><span class="sxs-lookup"><span data-stu-id="c91fe-104">Filters the preview image.</span></span>

## <a name="syntax"></a><span data-ttu-id="c91fe-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c91fe-105">Syntax</span></span>


```C++
HRESULT FilterPreviewImage(
  [in] LONG      lFlags,
  [in] IWiaItem2 *pWiaChildItem2,
  [in] RECT      InputImageExtents,
  [in] IStream   *pInputStream
);
```



## <a name="parameters"></a><span data-ttu-id="c91fe-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c91fe-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c91fe-107">*lFlags* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c91fe-107">*lFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c91fe-108">Tipo: **longo**</span><span class="sxs-lookup"><span data-stu-id="c91fe-108">Type: **LONG**</span></span>

<span data-ttu-id="c91fe-109">Não usado.</span><span class="sxs-lookup"><span data-stu-id="c91fe-109">Not used.</span></span> <span data-ttu-id="c91fe-110">Defina como 0.</span><span class="sxs-lookup"><span data-stu-id="c91fe-110">Set to 0.</span></span>

</dd> <dt>

<span data-ttu-id="c91fe-111">*pWiaChildItem2* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c91fe-111">*pWiaChildItem2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c91fe-112">Tipo: \**[**IWiaItem2**](-wia-iwiaitem2.md) \** _</span><span class="sxs-lookup"><span data-stu-id="c91fe-112">Type: \**[**IWiaItem2**](-wia-iwiaitem2.md)\** _</span></span>

<span data-ttu-id="c91fe-113">O item que é processado.</span><span class="sxs-lookup"><span data-stu-id="c91fe-113">The item that is processed.</span></span>

</dd> <dt>

<span data-ttu-id="c91fe-114">_InputImageExtents \* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c91fe-114">_InputImageExtents\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c91fe-115">Tipo: **Rect**</span><span class="sxs-lookup"><span data-stu-id="c91fe-115">Type: **RECT**</span></span>

<span data-ttu-id="c91fe-116">As coordenadas (na área de aquisição física) da imagem que o componente de visualização armazena em cache internamente.</span><span class="sxs-lookup"><span data-stu-id="c91fe-116">The coordinates (on the physical acquisition area) of the image that the preview component caches internally.</span></span>

</dd> <dt>

<span data-ttu-id="c91fe-117">*pInputStream* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c91fe-117">*pInputStream* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c91fe-118">Tipo: \**[IStream](/windows/win32/api/objidl/nn-objidl-istream) \** _</span><span class="sxs-lookup"><span data-stu-id="c91fe-118">Type: \**[IStream](/windows/win32/api/objidl/nn-objidl-istream)\** _</span></span>

<span data-ttu-id="c91fe-119">Um ponteiro para a interface [IStream](/windows/win32/api/objidl/nn-objidl-istream) para os dados de imagem armazenados em cache que são filtrados.</span><span class="sxs-lookup"><span data-stu-id="c91fe-119">A pointer to the [IStream](/windows/win32/api/objidl/nn-objidl-istream) interface for the cached image data that is filtered.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c91fe-120">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c91fe-120">Return value</span></span>

<span data-ttu-id="c91fe-121">Tipo: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="c91fe-121">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="c91fe-122">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="c91fe-122">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="c91fe-123">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="c91fe-123">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="c91fe-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="c91fe-124">Remarks</span></span>

<span data-ttu-id="c91fe-125">Não chame esse método diretamente do seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="c91fe-125">Do not call this method directly from your application.</span></span>

<span data-ttu-id="c91fe-126">*pWiaChildItem2* deve ser um item filho do *pWiaItem2* que foi passado em [**IWiaImageFilter:: InitializeFilter**](-wia-iwiaimagefilter-initializefilter.md).</span><span class="sxs-lookup"><span data-stu-id="c91fe-126">*pWiaChildItem2* must be a child item of the *pWiaItem2* that was passed into [**IWiaImageFilter::InitializeFilter**](-wia-iwiaimagefilter-initializefilter.md).</span></span>

<span data-ttu-id="c91fe-127">*InputImageExtents* é necessário porque o filtro de processamento de imagem é responsável por recortar a área de imagem que o *pWiaChildItem2* representa dos dados de imagem passados por meio de *pInputStream*.</span><span class="sxs-lookup"><span data-stu-id="c91fe-127">*InputImageExtents* is needed because the image processing filter is responsible for cutting out the image area that *pWiaChildItem2* represents from the image data passed in through *pInputStream*.</span></span>

<span data-ttu-id="c91fe-128">Um aplicativo deve garantir que *pWiaChildItem2* tenha o mesmo formato de imagem ( \_ formato WIA IPA \_ ), resolução (WIA \_ IPS \_ XRES e WIA \_ IPS \_ YRES) e profundidade de bits (profundidade de IPA WIA \_ \_ ) como *pWiaItem2* tinha quando transmitida para [**GetNewPreview**](-wia-iwiapreview-getnewpreview.md).</span><span class="sxs-lookup"><span data-stu-id="c91fe-128">An application must ensure that *pWiaChildItem2* has the same image format (WIA\_IPA\_FORMAT), resolution (WIA\_IPS\_XRES and WIA\_IPS\_YRES) and bit depth (WIA\_IPA\_DEPTH) as *pWiaItem2* had when it was passed into [**GetNewPreview**](-wia-iwiapreview-getnewpreview.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c91fe-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c91fe-129">Requirements</span></span>



| <span data-ttu-id="c91fe-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="c91fe-130">Requirement</span></span> | <span data-ttu-id="c91fe-131">Valor</span><span class="sxs-lookup"><span data-stu-id="c91fe-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="c91fe-132">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c91fe-132">Minimum supported client</span></span><br/> | <span data-ttu-id="c91fe-133">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c91fe-133">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="c91fe-134">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c91fe-134">Minimum supported server</span></span><br/> | <span data-ttu-id="c91fe-135">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="c91fe-135">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="c91fe-136">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c91fe-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="c91fe-137"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="c91fe-137"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="c91fe-138">INSERI</span><span class="sxs-lookup"><span data-stu-id="c91fe-138">IDL</span></span><br/>                      | <dl> <span data-ttu-id="c91fe-139"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="c91fe-139"><dt>Wia.idl</dt></span></span> </dl> |



 

 
