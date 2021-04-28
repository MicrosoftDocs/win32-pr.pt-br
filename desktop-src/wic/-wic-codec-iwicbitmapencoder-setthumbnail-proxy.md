---
description: Função IWICBitmapEncoder_SetThumbnail_Proxy function-proxy para o método SetThumbnail.
ms.assetid: 6c062eaf-27a4-4d48-8315-be9bf168f999
title: Função IWICBitmapEncoder_SetThumbnail_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapEncoder_SetThumbnail_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: a7666fffbac7813db8021daf38ebae9c4e68c57a
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108100594"
---
# <a name="iwicbitmapencoder_setthumbnail_proxy-function"></a><span data-ttu-id="9b11a-103">\_Função de proxy IWICBitmapEncoder SetThumbnail \_</span><span class="sxs-lookup"><span data-stu-id="9b11a-103">IWICBitmapEncoder\_SetThumbnail\_Proxy function</span></span>

<span data-ttu-id="9b11a-104">Função de proxy para o método [**SetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setthumbnail) .</span><span class="sxs-lookup"><span data-stu-id="9b11a-104">Proxy function for the [**SetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setthumbnail) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="9b11a-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9b11a-105">Syntax</span></span>


```C++
HRESULT IWICBitmapEncoder_SetThumbnail_Proxy(
  _In_ IWICBitmapEncoder *THIS_PTR,
  _In_ IWICBitmapSource  *pIThumbnail
);
```



## <a name="parameters"></a><span data-ttu-id="9b11a-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9b11a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9b11a-107">*Isso \_ PTR* \[\]</span><span class="sxs-lookup"><span data-stu-id="9b11a-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9b11a-108">Tipo: **[ **IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)\***</span><span class="sxs-lookup"><span data-stu-id="9b11a-108">Type: **[**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)\***</span></span>

<span data-ttu-id="9b11a-109">Ponteiro para este objeto [**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) .</span><span class="sxs-lookup"><span data-stu-id="9b11a-109">Pointer to this [**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) object.</span></span>

</dd> <dt>

<span data-ttu-id="9b11a-110">*pIThumbnail* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="9b11a-110">*pIThumbnail* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9b11a-111">Tipo: **[ **IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\***</span><span class="sxs-lookup"><span data-stu-id="9b11a-111">Type: **[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\***</span></span>

<span data-ttu-id="9b11a-112">O [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) a ser definido como a miniatura global.</span><span class="sxs-lookup"><span data-stu-id="9b11a-112">The [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) to set as the global thumbnail.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9b11a-113">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="9b11a-113">Return value</span></span>

<span data-ttu-id="9b11a-114">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="9b11a-114">Type: **HRESULT**</span></span>

<span data-ttu-id="9b11a-115">Se essa função for bem sucedido, ela retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="9b11a-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="9b11a-116">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="9b11a-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="9b11a-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="9b11a-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="9b11a-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9b11a-118">Requirements</span></span>



| <span data-ttu-id="9b11a-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="9b11a-119">Requirement</span></span> | <span data-ttu-id="9b11a-120">Valor</span><span class="sxs-lookup"><span data-stu-id="9b11a-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9b11a-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9b11a-121">Minimum supported client</span></span><br/> | <span data-ttu-id="9b11a-122">Windows XP com SP2, \[ somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="9b11a-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="9b11a-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9b11a-123">Minimum supported server</span></span><br/> | <span data-ttu-id="9b11a-124">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="9b11a-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="9b11a-125">DLL</span><span class="sxs-lookup"><span data-stu-id="9b11a-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9b11a-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9b11a-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




