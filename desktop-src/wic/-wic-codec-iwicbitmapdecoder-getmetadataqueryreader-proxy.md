---
description: Função de proxy de função IWICBitmapDecoder_GetMetadataQueryReader_Proxy para o método GetMetadataQueryReader.
ms.assetid: cc32bdf1-d807-46ac-87b7-77bf2d498e72
title: Função IWICBitmapDecoder_GetMetadataQueryReader_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapDecoder_GetMetadataQueryReader_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: ebda8edb5c2007b1dfb39ca9f406855da05c456a
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108100644"
---
# <a name="iwicbitmapdecoder_getmetadataqueryreader_proxy-function"></a><span data-ttu-id="5e1b0-103">\_Função de \_ proxy IWICBitmapDecoder GetMetadataQueryReader</span><span class="sxs-lookup"><span data-stu-id="5e1b0-103">IWICBitmapDecoder\_GetMetadataQueryReader\_Proxy function</span></span>

<span data-ttu-id="5e1b0-104">Função de proxy para o método [**GetMetadataQueryReader**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getmetadataqueryreader) .</span><span class="sxs-lookup"><span data-stu-id="5e1b0-104">Proxy function for the [**GetMetadataQueryReader**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getmetadataqueryreader) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="5e1b0-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5e1b0-105">Syntax</span></span>


```C++
HRESULT IWICBitmapDecoder_GetMetadataQueryReader_Proxy(
  _In_  IWICBitmapDecoder       *THIS_PTR,
  _Out_ IWICMetadataQueryReader **ppIMetadataQueryReader
);
```



## <a name="parameters"></a><span data-ttu-id="5e1b0-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5e1b0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5e1b0-107">*Isso \_ PTR* \[\]</span><span class="sxs-lookup"><span data-stu-id="5e1b0-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5e1b0-108">Tipo: **[ **IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)\***</span><span class="sxs-lookup"><span data-stu-id="5e1b0-108">Type: **[**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)\***</span></span>

<span data-ttu-id="5e1b0-109">Ponteiro para este objeto [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) .</span><span class="sxs-lookup"><span data-stu-id="5e1b0-109">Pointer to this [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) object.</span></span>

</dd> <dt>

<span data-ttu-id="5e1b0-110">*ppIMetadataQueryReader* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="5e1b0-110">*ppIMetadataQueryReader* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5e1b0-111">Tipo: **[ **IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader)\*\***</span><span class="sxs-lookup"><span data-stu-id="5e1b0-111">Type: **[**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader)\*\***</span></span>

<span data-ttu-id="5e1b0-112">Um ponteiro que recebe um ponteiro para os metadados.</span><span class="sxs-lookup"><span data-stu-id="5e1b0-112">A pointer that receives a pointer to the metadata.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5e1b0-113">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="5e1b0-113">Return value</span></span>

<span data-ttu-id="5e1b0-114">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="5e1b0-114">Type: **HRESULT**</span></span>

<span data-ttu-id="5e1b0-115">Se essa função for bem sucedido, ela retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="5e1b0-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="5e1b0-116">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="5e1b0-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="5e1b0-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="5e1b0-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="5e1b0-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5e1b0-118">Requirements</span></span>



| <span data-ttu-id="5e1b0-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="5e1b0-119">Requirement</span></span> | <span data-ttu-id="5e1b0-120">Valor</span><span class="sxs-lookup"><span data-stu-id="5e1b0-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5e1b0-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5e1b0-121">Minimum supported client</span></span><br/> | <span data-ttu-id="5e1b0-122">Windows XP com SP2, \[ somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="5e1b0-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="5e1b0-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5e1b0-123">Minimum supported server</span></span><br/> | <span data-ttu-id="5e1b0-124">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="5e1b0-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="5e1b0-125">DLL</span><span class="sxs-lookup"><span data-stu-id="5e1b0-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5e1b0-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5e1b0-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




