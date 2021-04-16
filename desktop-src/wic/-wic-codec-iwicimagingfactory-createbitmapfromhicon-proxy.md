---
description: Função de proxy para o método CreateBitmapFromHICON.
ms.assetid: 5df3d9d9-1b23-4f38-b97e-0b77d6db99d8
title: Função IWICImagingFactory_CreateBitmapFromHICON_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICImagingFactory_CreateBitmapFromHICON_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 58f9f37dc27c76a9eaa55d6baec52efbb773343e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105765603"
---
# <a name="iwicimagingfactory_createbitmapfromhicon_proxy-function"></a><span data-ttu-id="d8765-103">\_Função de \_ proxy IWICImagingFactory CreateBitmapFromHICON</span><span class="sxs-lookup"><span data-stu-id="d8765-103">IWICImagingFactory\_CreateBitmapFromHICON\_Proxy function</span></span>

<span data-ttu-id="d8765-104">Função de proxy para o método [**CreateBitmapFromHICON**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createbitmapfromhicon) .</span><span class="sxs-lookup"><span data-stu-id="d8765-104">Proxy function for the [**CreateBitmapFromHICON**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createbitmapfromhicon) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="d8765-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d8765-105">Syntax</span></span>


```C++
HRESULT IWICImagingFactory_CreateBitmapFromHICON_Proxy(
  _In_  IWICImagingFactory *pFactory,
  _In_  HICON              hIcon,
  _Out_ IWICBitmap         **ppIBitmap
);
```



## <a name="parameters"></a><span data-ttu-id="d8765-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d8765-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d8765-107">*pFactory* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d8765-107">*pFactory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d8765-108">Tipo: \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) \** _</span><span class="sxs-lookup"><span data-stu-id="d8765-108">Type: \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)\** _</span></span>

</dd> <dt>

<span data-ttu-id="d8765-109">_hIcon \* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d8765-109">_hIcon\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d8765-110">Tipo: **HICON**</span><span class="sxs-lookup"><span data-stu-id="d8765-110">Type: **HICON**</span></span>

<span data-ttu-id="d8765-111">O identificador de ícone do qual criar o novo bitmap.</span><span class="sxs-lookup"><span data-stu-id="d8765-111">The icon handle to create the new bitmap from.</span></span>

</dd> <dt>

<span data-ttu-id="d8765-112">*ppIBitmap* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="d8765-112">*ppIBitmap* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d8765-113">Tipo: **[ **IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap)\*\***</span><span class="sxs-lookup"><span data-stu-id="d8765-113">Type: **[**IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap)\*\***</span></span>

<span data-ttu-id="d8765-114">Um ponteiro que recebe um ponteiro para o novo bitmap.</span><span class="sxs-lookup"><span data-stu-id="d8765-114">A pointer that receives a pointer to the new bitmap.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d8765-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d8765-115">Return value</span></span>

<span data-ttu-id="d8765-116">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="d8765-116">Type: **HRESULT**</span></span>

<span data-ttu-id="d8765-117">Se essa função for bem sucedido, ela retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="d8765-117">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="d8765-118">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="d8765-118">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="d8765-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="d8765-119">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="d8765-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d8765-120">Requirements</span></span>



| <span data-ttu-id="d8765-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="d8765-121">Requirement</span></span> | <span data-ttu-id="d8765-122">Valor</span><span class="sxs-lookup"><span data-stu-id="d8765-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d8765-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d8765-123">Minimum supported client</span></span><br/> | <span data-ttu-id="d8765-124">Windows XP com SP2, \[ somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d8765-124">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="d8765-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d8765-125">Minimum supported server</span></span><br/> | <span data-ttu-id="d8765-126">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="d8765-126">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="d8765-127">DLL</span><span class="sxs-lookup"><span data-stu-id="d8765-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d8765-128"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d8765-128"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




