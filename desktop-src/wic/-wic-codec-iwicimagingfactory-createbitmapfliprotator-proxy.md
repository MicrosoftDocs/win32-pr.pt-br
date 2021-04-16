---
description: Função de proxy para o método CreateBitmapFlipRotator.
ms.assetid: 1dc55744-8ae1-4d8b-9ffd-735ee45ceb47
title: Função IWICImagingFactory_CreateBitmapFlipRotator_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICImagingFactory_CreateBitmapFlipRotator_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: dea33ea75ad9d9626b327ee0173abc2f28a3e417
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105758896"
---
# <a name="iwicimagingfactory_createbitmapfliprotator_proxy-function"></a><span data-ttu-id="06397-103">\_Função de \_ proxy IWICImagingFactory CreateBitmapFlipRotator</span><span class="sxs-lookup"><span data-stu-id="06397-103">IWICImagingFactory\_CreateBitmapFlipRotator\_Proxy function</span></span>

<span data-ttu-id="06397-104">Função de proxy para o método [**CreateBitmapFlipRotator**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createbitmapfliprotator) .</span><span class="sxs-lookup"><span data-stu-id="06397-104">Proxy function for the [**CreateBitmapFlipRotator**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createbitmapfliprotator) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="06397-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="06397-105">Syntax</span></span>


```C++
HRESULT IWICImagingFactory_CreateBitmapFlipRotator_Proxy(
  _In_  IWICImagingFactory    *pFactory,
  _Out_ IWICBitmapFlipRotator **ppIBitmapFlipRotator
);
```



## <a name="parameters"></a><span data-ttu-id="06397-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="06397-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="06397-107">*pFactory* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="06397-107">*pFactory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="06397-108">Tipo: \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) \** _</span><span class="sxs-lookup"><span data-stu-id="06397-108">Type: \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)\** _</span></span>

</dd> <dt>

<span data-ttu-id="06397-109">_ppIBitmapFlipRotator \* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="06397-109">_ppIBitmapFlipRotator\* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="06397-110">Tipo: **[ **IWICBitmapFlipRotator**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapfliprotator)\*\***</span><span class="sxs-lookup"><span data-stu-id="06397-110">Type: **[**IWICBitmapFlipRotator**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapfliprotator)\*\***</span></span>

<span data-ttu-id="06397-111">Um ponteiro que recebe um ponteiro para um novo [**IWICBitmapFlipRotator**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapfliprotator).</span><span class="sxs-lookup"><span data-stu-id="06397-111">A pointer that receives a pointer to a new [**IWICBitmapFlipRotator**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapfliprotator).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="06397-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="06397-112">Return value</span></span>

<span data-ttu-id="06397-113">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="06397-113">Type: **HRESULT**</span></span>

<span data-ttu-id="06397-114">Se essa função for bem sucedido, ela retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="06397-114">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="06397-115">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="06397-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="06397-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="06397-116">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="06397-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="06397-117">Requirements</span></span>



| <span data-ttu-id="06397-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="06397-118">Requirement</span></span> | <span data-ttu-id="06397-119">Valor</span><span class="sxs-lookup"><span data-stu-id="06397-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="06397-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="06397-120">Minimum supported client</span></span><br/> | <span data-ttu-id="06397-121">Windows XP com SP2, \[ somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="06397-121">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="06397-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="06397-122">Minimum supported server</span></span><br/> | <span data-ttu-id="06397-123">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="06397-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="06397-124">DLL</span><span class="sxs-lookup"><span data-stu-id="06397-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="06397-125"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="06397-125"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




