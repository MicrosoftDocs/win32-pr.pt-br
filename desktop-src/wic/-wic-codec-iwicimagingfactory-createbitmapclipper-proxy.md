---
description: Função de proxy para o método CreateBitmapClipper.
ms.assetid: 163a8d7b-f22b-4ab5-9dba-00b0cdaab440
title: Função IWICImagingFactory_CreateBitmapClipper_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICImagingFactory_CreateBitmapClipper_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: fb722622ce9a8b3ad3144bcf9ea53942c8e611aa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922477"
---
# <a name="iwicimagingfactory_createbitmapclipper_proxy-function"></a><span data-ttu-id="cb46e-103">\_Função de \_ proxy IWICImagingFactory CreateBitmapClipper</span><span class="sxs-lookup"><span data-stu-id="cb46e-103">IWICImagingFactory\_CreateBitmapClipper\_Proxy function</span></span>

<span data-ttu-id="cb46e-104">Função de proxy para o método [**CreateBitmapClipper**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createbitmapclipper) .</span><span class="sxs-lookup"><span data-stu-id="cb46e-104">Proxy function for the [**CreateBitmapClipper**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createbitmapclipper) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="cb46e-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="cb46e-105">Syntax</span></span>


```C++
HRESULT IWICImagingFactory_CreateBitmapClipper_Proxy(
  _In_  IWICImagingFactory *pFactory,
  _Out_ IWICBitmapClipper  **ppIBitmapClipper
);
```



## <a name="parameters"></a><span data-ttu-id="cb46e-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="cb46e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cb46e-107">*pFactory* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="cb46e-107">*pFactory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cb46e-108">Tipo: \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) \** _</span><span class="sxs-lookup"><span data-stu-id="cb46e-108">Type: \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)\** _</span></span>

</dd> <dt>

<span data-ttu-id="cb46e-109">_ppIBitmapClipper \* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="cb46e-109">_ppIBitmapClipper\* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cb46e-110">Tipo: **[ **IWICBitmapClipper**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapclipper)\*\***</span><span class="sxs-lookup"><span data-stu-id="cb46e-110">Type: **[**IWICBitmapClipper**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapclipper)\*\***</span></span>

<span data-ttu-id="cb46e-111">Um ponteiro que recebe um ponteiro para um novo [**IWICBitmapClipper**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapclipper).</span><span class="sxs-lookup"><span data-stu-id="cb46e-111">A pointer that receives a pointer to a new [**IWICBitmapClipper**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapclipper).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cb46e-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="cb46e-112">Return value</span></span>

<span data-ttu-id="cb46e-113">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="cb46e-113">Type: **HRESULT**</span></span>

<span data-ttu-id="cb46e-114">Se essa função for bem sucedido, ela retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="cb46e-114">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="cb46e-115">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="cb46e-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="cb46e-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="cb46e-116">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="cb46e-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cb46e-117">Requirements</span></span>



| <span data-ttu-id="cb46e-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="cb46e-118">Requirement</span></span> | <span data-ttu-id="cb46e-119">Valor</span><span class="sxs-lookup"><span data-stu-id="cb46e-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cb46e-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cb46e-120">Minimum supported client</span></span><br/> | <span data-ttu-id="cb46e-121">Windows XP com SP2, \[ somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="cb46e-121">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="cb46e-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cb46e-122">Minimum supported server</span></span><br/> | <span data-ttu-id="cb46e-123">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="cb46e-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="cb46e-124">DLL</span><span class="sxs-lookup"><span data-stu-id="cb46e-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cb46e-125"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="cb46e-125"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




