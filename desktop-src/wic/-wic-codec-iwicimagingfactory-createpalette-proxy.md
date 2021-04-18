---
description: Função de proxy para o método CreatePalette.
ms.assetid: c83b4239-ce6b-4a4c-ab70-df31dfcdd26c
title: Função IWICImagingFactory_CreatePalette_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICImagingFactory_CreatePalette_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 626c05ec5e4e365cf61304c4b33e621967cea5e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105788673"
---
# <a name="iwicimagingfactory_createpalette_proxy-function"></a><span data-ttu-id="17c82-103">\_Função de proxy CreatePalette IWICImagingFactory \_</span><span class="sxs-lookup"><span data-stu-id="17c82-103">IWICImagingFactory\_CreatePalette\_Proxy function</span></span>

<span data-ttu-id="17c82-104">Função de proxy para o método [**CreatePalette**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createpalette) .</span><span class="sxs-lookup"><span data-stu-id="17c82-104">Proxy function for the [**CreatePalette**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createpalette) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="17c82-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="17c82-105">Syntax</span></span>


```C++
HRESULT IWICImagingFactory_CreatePalette_Proxy(
  _In_  IWICImagingFactory *pFactory,
  _Out_ IWICPalette        **ppIPalette
);
```



## <a name="parameters"></a><span data-ttu-id="17c82-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="17c82-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="17c82-107">*pFactory* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="17c82-107">*pFactory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="17c82-108">Tipo: \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) \** _</span><span class="sxs-lookup"><span data-stu-id="17c82-108">Type: \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)\** _</span></span>

</dd> <dt>

<span data-ttu-id="17c82-109">_ppIPalette \* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="17c82-109">_ppIPalette\* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="17c82-110">Tipo: **[ **IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette)\*\***</span><span class="sxs-lookup"><span data-stu-id="17c82-110">Type: **[**IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette)\*\***</span></span>

<span data-ttu-id="17c82-111">Um ponteiro que recebe um ponteiro para um novo [**IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette).</span><span class="sxs-lookup"><span data-stu-id="17c82-111">A pointer that receives a pointer to a new [**IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="17c82-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="17c82-112">Return value</span></span>

<span data-ttu-id="17c82-113">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="17c82-113">Type: **HRESULT**</span></span>

<span data-ttu-id="17c82-114">Se essa função for bem sucedido, ela retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="17c82-114">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="17c82-115">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="17c82-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="17c82-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="17c82-116">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="17c82-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="17c82-117">Requirements</span></span>



| <span data-ttu-id="17c82-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="17c82-118">Requirement</span></span> | <span data-ttu-id="17c82-119">Valor</span><span class="sxs-lookup"><span data-stu-id="17c82-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="17c82-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="17c82-120">Minimum supported client</span></span><br/> | <span data-ttu-id="17c82-121">Windows XP com SP2, \[ somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="17c82-121">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="17c82-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="17c82-122">Minimum supported server</span></span><br/> | <span data-ttu-id="17c82-123">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="17c82-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="17c82-124">DLL</span><span class="sxs-lookup"><span data-stu-id="17c82-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="17c82-125"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="17c82-125"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




