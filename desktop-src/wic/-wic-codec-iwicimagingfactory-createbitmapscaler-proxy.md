---
description: Função de proxy para o método CreateBitmapScaler.
ms.assetid: 27fcb17e-bdcd-44cc-9fe6-f93816589b50
title: Função IWICImagingFactory_CreateBitmapScaler_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICImagingFactory_CreateBitmapScaler_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: ac831427901de481d313833e4ca8459ccd333384
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922476"
---
# <a name="iwicimagingfactory_createbitmapscaler_proxy-function"></a><span data-ttu-id="9582c-103">\_Função de \_ proxy IWICImagingFactory CreateBitmapScaler</span><span class="sxs-lookup"><span data-stu-id="9582c-103">IWICImagingFactory\_CreateBitmapScaler\_Proxy function</span></span>

<span data-ttu-id="9582c-104">Função de proxy para o método [**CreateBitmapScaler**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createbitmapscaler) .</span><span class="sxs-lookup"><span data-stu-id="9582c-104">Proxy function for the [**CreateBitmapScaler**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createbitmapscaler) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="9582c-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9582c-105">Syntax</span></span>


```C++
HRESULT IWICImagingFactory_CreateBitmapScaler_Proxy(
  _In_  IWICImagingFactory *pFactory,
  _Out_ IWICBitmapScaler   **ppIBitmapScaler
);
```



## <a name="parameters"></a><span data-ttu-id="9582c-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9582c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9582c-107">*pFactory* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="9582c-107">*pFactory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9582c-108">Tipo: \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) \** _</span><span class="sxs-lookup"><span data-stu-id="9582c-108">Type: \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)\** _</span></span>

</dd> <dt>

<span data-ttu-id="9582c-109">_ppIBitmapScaler \* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="9582c-109">_ppIBitmapScaler\* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9582c-110">Tipo: **[ **IWICBitmapScaler**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapscaler)\*\***</span><span class="sxs-lookup"><span data-stu-id="9582c-110">Type: **[**IWICBitmapScaler**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapscaler)\*\***</span></span>

<span data-ttu-id="9582c-111">Um ponteiro que recebe um ponteiro para um novo [**IWICBitmapScaler**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapscaler).</span><span class="sxs-lookup"><span data-stu-id="9582c-111">A pointer that receives a pointer to a new [**IWICBitmapScaler**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapscaler).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9582c-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="9582c-112">Return value</span></span>

<span data-ttu-id="9582c-113">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="9582c-113">Type: **HRESULT**</span></span>

<span data-ttu-id="9582c-114">Se essa função for bem sucedido, ela retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="9582c-114">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="9582c-115">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="9582c-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="9582c-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="9582c-116">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="9582c-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9582c-117">Requirements</span></span>



| <span data-ttu-id="9582c-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="9582c-118">Requirement</span></span> | <span data-ttu-id="9582c-119">Valor</span><span class="sxs-lookup"><span data-stu-id="9582c-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9582c-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9582c-120">Minimum supported client</span></span><br/> | <span data-ttu-id="9582c-121">Windows XP com SP2, \[ somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="9582c-121">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="9582c-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9582c-122">Minimum supported server</span></span><br/> | <span data-ttu-id="9582c-123">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="9582c-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="9582c-124">DLL</span><span class="sxs-lookup"><span data-stu-id="9582c-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9582c-125"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9582c-125"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




