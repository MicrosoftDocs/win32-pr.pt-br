---
description: Função de proxy de função IWICBitmapEncoder_GetMetadataQueryWriter_Proxy para o método GetMetadataQueryWriter.
ms.assetid: 3186d473-f8a7-405a-8429-3f50104bee4a
title: Função IWICBitmapEncoder_GetMetadataQueryWriter_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapEncoder_GetMetadataQueryWriter_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 798a9b5bafb2f5011e42e603b8b2c98b0ba79b37
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108091164"
---
# <a name="iwicbitmapencoder_getmetadataquerywriter_proxy-function"></a><span data-ttu-id="4052d-103">\_Função de \_ proxy IWICBitmapEncoder GetMetadataQueryWriter</span><span class="sxs-lookup"><span data-stu-id="4052d-103">IWICBitmapEncoder\_GetMetadataQueryWriter\_Proxy function</span></span>

<span data-ttu-id="4052d-104">Função de proxy para o método [**GetMetadataQueryWriter**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-getmetadataquerywriter) .</span><span class="sxs-lookup"><span data-stu-id="4052d-104">Proxy function for the [**GetMetadataQueryWriter**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-getmetadataquerywriter) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="4052d-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4052d-105">Syntax</span></span>


```C++
HRESULT IWICBitmapEncoder_GetMetadataQueryWriter_Proxy(
  _In_  IWICBitmapEncoder       *THIS_PTR,
  _Out_ IWICMetadataQueryWriter **ppIMetadataQueryWriter
);
```



## <a name="parameters"></a><span data-ttu-id="4052d-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4052d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4052d-107">*Isso \_ PTR* \[\]</span><span class="sxs-lookup"><span data-stu-id="4052d-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4052d-108">Tipo: **[ **IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)\***</span><span class="sxs-lookup"><span data-stu-id="4052d-108">Type: **[**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)\***</span></span>

<span data-ttu-id="4052d-109">Ponteiro para este objeto [**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) .</span><span class="sxs-lookup"><span data-stu-id="4052d-109">Pointer to this [**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) object.</span></span>

</dd> <dt>

<span data-ttu-id="4052d-110">*ppIMetadataQueryWriter* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="4052d-110">*ppIMetadataQueryWriter* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4052d-111">Tipo: **[ **IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)\*\***</span><span class="sxs-lookup"><span data-stu-id="4052d-111">Type: **[**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)\*\***</span></span>

<span data-ttu-id="4052d-112">Um ponteiro que recebe um ponteiro para um [**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter).</span><span class="sxs-lookup"><span data-stu-id="4052d-112">A pointer that receives a pointer to an [**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4052d-113">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="4052d-113">Return value</span></span>

<span data-ttu-id="4052d-114">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="4052d-114">Type: **HRESULT**</span></span>

<span data-ttu-id="4052d-115">Se essa função for bem sucedido, ela retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="4052d-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="4052d-116">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="4052d-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="4052d-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="4052d-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="4052d-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4052d-118">Requirements</span></span>



| <span data-ttu-id="4052d-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="4052d-119">Requirement</span></span> | <span data-ttu-id="4052d-120">Valor</span><span class="sxs-lookup"><span data-stu-id="4052d-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4052d-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4052d-121">Minimum supported client</span></span><br/> | <span data-ttu-id="4052d-122">Windows XP com SP2, \[ somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="4052d-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="4052d-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4052d-123">Minimum supported server</span></span><br/> | <span data-ttu-id="4052d-124">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="4052d-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="4052d-125">DLL</span><span class="sxs-lookup"><span data-stu-id="4052d-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4052d-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4052d-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




