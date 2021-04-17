---
description: Função de proxy para o método CreateNewFrame.
ms.assetid: b23e8689-0fdc-49a7-a004-148b50420127
title: Função IWICBitmapEncoder_CreateNewFrame_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapEncoder_CreateNewFrame_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: c0ddf0141e5b13e370f199e3f211e74c3a0e6e77
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105764017"
---
# <a name="iwicbitmapencoder_createnewframe_proxy-function"></a><span data-ttu-id="5bf50-103">\_Função de \_ proxy IWICBitmapEncoder CreateNewFrame</span><span class="sxs-lookup"><span data-stu-id="5bf50-103">IWICBitmapEncoder\_CreateNewFrame\_Proxy function</span></span>

<span data-ttu-id="5bf50-104">Função de proxy para o método [**CreateNewFrame**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-createnewframe) .</span><span class="sxs-lookup"><span data-stu-id="5bf50-104">Proxy function for the [**CreateNewFrame**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-createnewframe) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="5bf50-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5bf50-105">Syntax</span></span>


```C++
HRESULT IWICBitmapEncoder_CreateNewFrame_Proxy(
  _In_    IWICBitmapEncoder     *THIS_PTR,
  _Out_   IWICBitmapFrameEncode **ppIFrameEncode,
  _Inout_ IPropertyBag2         **ppIEncoderOptions
);
```



## <a name="parameters"></a><span data-ttu-id="5bf50-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5bf50-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5bf50-107">*Isso \_ PTR* \[\]</span><span class="sxs-lookup"><span data-stu-id="5bf50-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5bf50-108">Tipo: \**[**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) \** _</span><span class="sxs-lookup"><span data-stu-id="5bf50-108">Type: \**[**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)\** _</span></span>

<span data-ttu-id="5bf50-109">Ponteiro para este objeto [_ *IWICBitmapEncoder* \*](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) .</span><span class="sxs-lookup"><span data-stu-id="5bf50-109">Pointer to this [_ *IWICBitmapEncoder*\*](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) object.</span></span>

</dd> <dt>

<span data-ttu-id="5bf50-110">*ppIFrameEncode* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="5bf50-110">*ppIFrameEncode* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5bf50-111">Tipo: **[ **IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)\*\***</span><span class="sxs-lookup"><span data-stu-id="5bf50-111">Type: **[**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)\*\***</span></span>

<span data-ttu-id="5bf50-112">Um ponteiro que recebe um ponteiro para a nova instância de um [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode).</span><span class="sxs-lookup"><span data-stu-id="5bf50-112">A pointer that receives a pointer to the new instance of an [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode).</span></span>

</dd> <dt>

<span data-ttu-id="5bf50-113">*ppIEncoderOptions* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="5bf50-113">*ppIEncoderOptions* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="5bf50-114">Tipo: **[IPropertyBag2](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85))\*\***</span><span class="sxs-lookup"><span data-stu-id="5bf50-114">Type: **[IPropertyBag2](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85))\*\***</span></span>

<span data-ttu-id="5bf50-115">As propriedades nomeadas a serem usadas para a inicialização do quadro.</span><span class="sxs-lookup"><span data-stu-id="5bf50-115">The named properties to use for frame initialization.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5bf50-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="5bf50-116">Return value</span></span>

<span data-ttu-id="5bf50-117">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="5bf50-117">Type: **HRESULT**</span></span>

<span data-ttu-id="5bf50-118">Se essa função for bem sucedido, ela retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="5bf50-118">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="5bf50-119">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="5bf50-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="5bf50-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="5bf50-120">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="5bf50-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5bf50-121">Requirements</span></span>



| <span data-ttu-id="5bf50-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="5bf50-122">Requirement</span></span> | <span data-ttu-id="5bf50-123">Valor</span><span class="sxs-lookup"><span data-stu-id="5bf50-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5bf50-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5bf50-124">Minimum supported client</span></span><br/> | <span data-ttu-id="5bf50-125">Windows XP com SP2, \[ somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="5bf50-125">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="5bf50-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5bf50-126">Minimum supported server</span></span><br/> | <span data-ttu-id="5bf50-127">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="5bf50-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="5bf50-128">DLL</span><span class="sxs-lookup"><span data-stu-id="5bf50-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5bf50-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5bf50-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

