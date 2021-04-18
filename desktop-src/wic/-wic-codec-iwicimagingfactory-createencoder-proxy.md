---
description: Função de proxy para o método CreateEncoder.
ms.assetid: e3ffad7f-eb0e-481d-81ee-caf18e14ba59
title: Função IWICImagingFactory_CreateEncoder_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICImagingFactory_CreateEncoder_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 38e5dd19ddc07de42f8be9e8c887a4f412a853b5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105814110"
---
# <a name="iwicimagingfactory_createencoder_proxy-function"></a><span data-ttu-id="a80b4-103">\_Função de proxy Createencoderr IWICImagingFactory \_</span><span class="sxs-lookup"><span data-stu-id="a80b4-103">IWICImagingFactory\_CreateEncoder\_Proxy function</span></span>

<span data-ttu-id="a80b4-104">Função de proxy para o método [**CreateEncoder**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createencoder) .</span><span class="sxs-lookup"><span data-stu-id="a80b4-104">Proxy function for the [**CreateEncoder**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createencoder) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="a80b4-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a80b4-105">Syntax</span></span>


```C++
HRESULT IWICImagingFactory_CreateEncoder_Proxy(
  _In_           IWICImagingFactory *pFactory,
  _In_           REFGUID            guidContainerFormat,
  _In_opt_ const GUID               *pguidVendor,
  _Out_          IWICBitmapEncoder  **ppIEncoder
);
```



## <a name="parameters"></a><span data-ttu-id="a80b4-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a80b4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a80b4-107">*pFactory* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a80b4-107">*pFactory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a80b4-108">Tipo: \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) \** _</span><span class="sxs-lookup"><span data-stu-id="a80b4-108">Type: \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)\** _</span></span>

</dd> <dt>

<span data-ttu-id="a80b4-109">_guidContainerFormat \* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a80b4-109">_guidContainerFormat\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a80b4-110">Tipo: **REFGUID**</span><span class="sxs-lookup"><span data-stu-id="a80b4-110">Type: **REFGUID**</span></span>

<span data-ttu-id="a80b4-111">O GUID para o formato de contêiner desejado.</span><span class="sxs-lookup"><span data-stu-id="a80b4-111">The GUID for the desired container format.</span></span>

</dd> <dt>

<span data-ttu-id="a80b4-112">*pguidVendor* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="a80b4-112">*pguidVendor* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="a80b4-113">Tipo: \**const GUID \** _</span><span class="sxs-lookup"><span data-stu-id="a80b4-113">Type: \**const GUID\** _</span></span>

<span data-ttu-id="a80b4-114">O GUID do fornecedor para o codificador.</span><span class="sxs-lookup"><span data-stu-id="a80b4-114">The vendor GUID for the encoder.</span></span>

</dd> <dt>

<span data-ttu-id="a80b4-115">_ppIEncoder \* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="a80b4-115">_ppIEncoder\* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a80b4-116">Tipo: **[ **IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)\*\***</span><span class="sxs-lookup"><span data-stu-id="a80b4-116">Type: **[**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)\*\***</span></span>

<span data-ttu-id="a80b4-117">Um ponteiro que recebe um ponteiro para um novo [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder).</span><span class="sxs-lookup"><span data-stu-id="a80b4-117">A pointer that receives a pointer to a new [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a80b4-118">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a80b4-118">Return value</span></span>

<span data-ttu-id="a80b4-119">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="a80b4-119">Type: **HRESULT**</span></span>

<span data-ttu-id="a80b4-120">Se essa função for bem sucedido, ela retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="a80b4-120">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="a80b4-121">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="a80b4-121">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="a80b4-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="a80b4-122">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="a80b4-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a80b4-123">Requirements</span></span>



| <span data-ttu-id="a80b4-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="a80b4-124">Requirement</span></span> | <span data-ttu-id="a80b4-125">Valor</span><span class="sxs-lookup"><span data-stu-id="a80b4-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a80b4-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a80b4-126">Minimum supported client</span></span><br/> | <span data-ttu-id="a80b4-127">Windows XP com SP2, \[ somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a80b4-127">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="a80b4-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a80b4-128">Minimum supported server</span></span><br/> | <span data-ttu-id="a80b4-129">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="a80b4-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="a80b4-130">DLL</span><span class="sxs-lookup"><span data-stu-id="a80b4-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a80b4-131"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a80b4-131"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




