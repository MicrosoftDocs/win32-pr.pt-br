---
description: Função de proxy para o método GetMetadataQueryReader.
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
ms.openlocfilehash: 72b47652c76934fdf3ea518925990d6d4d1d3eb0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296293"
---
# <a name="iwicbitmapdecoder_getmetadataqueryreader_proxy-function"></a><span data-ttu-id="0d104-103">\_Função de \_ proxy IWICBitmapDecoder GetMetadataQueryReader</span><span class="sxs-lookup"><span data-stu-id="0d104-103">IWICBitmapDecoder\_GetMetadataQueryReader\_Proxy function</span></span>

<span data-ttu-id="0d104-104">Função de proxy para o método [**GetMetadataQueryReader**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getmetadataqueryreader) .</span><span class="sxs-lookup"><span data-stu-id="0d104-104">Proxy function for the [**GetMetadataQueryReader**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getmetadataqueryreader) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="0d104-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0d104-105">Syntax</span></span>


```C++
HRESULT IWICBitmapDecoder_GetMetadataQueryReader_Proxy(
  _In_  IWICBitmapDecoder       *THIS_PTR,
  _Out_ IWICMetadataQueryReader **ppIMetadataQueryReader
);
```



## <a name="parameters"></a><span data-ttu-id="0d104-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0d104-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0d104-107">*Isso \_ PTR* \[\]</span><span class="sxs-lookup"><span data-stu-id="0d104-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0d104-108">Tipo: \**[**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) \** _</span><span class="sxs-lookup"><span data-stu-id="0d104-108">Type: \**[**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)\** _</span></span>

<span data-ttu-id="0d104-109">Ponteiro para este objeto [_ *IWICBitmapDecoder* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) .</span><span class="sxs-lookup"><span data-stu-id="0d104-109">Pointer to this [_ *IWICBitmapDecoder*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) object.</span></span>

</dd> <dt>

<span data-ttu-id="0d104-110">*ppIMetadataQueryReader* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="0d104-110">*ppIMetadataQueryReader* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0d104-111">Tipo: **[ **IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader)\*\***</span><span class="sxs-lookup"><span data-stu-id="0d104-111">Type: **[**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader)\*\***</span></span>

<span data-ttu-id="0d104-112">Um ponteiro que recebe um ponteiro para os metadados.</span><span class="sxs-lookup"><span data-stu-id="0d104-112">A pointer that receives a pointer to the metadata.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0d104-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="0d104-113">Return value</span></span>

<span data-ttu-id="0d104-114">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="0d104-114">Type: **HRESULT**</span></span>

<span data-ttu-id="0d104-115">Se essa função for bem sucedido, ela retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="0d104-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="0d104-116">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="0d104-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="0d104-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="0d104-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="0d104-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0d104-118">Requirements</span></span>



| <span data-ttu-id="0d104-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="0d104-119">Requirement</span></span> | <span data-ttu-id="0d104-120">Valor</span><span class="sxs-lookup"><span data-stu-id="0d104-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0d104-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0d104-121">Minimum supported client</span></span><br/> | <span data-ttu-id="0d104-122">Windows XP com SP2, \[ somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="0d104-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="0d104-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0d104-123">Minimum supported server</span></span><br/> | <span data-ttu-id="0d104-124">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="0d104-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="0d104-125">DLL</span><span class="sxs-lookup"><span data-stu-id="0d104-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0d104-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0d104-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




