---
description: Função de proxy para o método CreateStream.
ms.assetid: c827e1aa-13ae-459e-a1dc-5ff8c31a54bc
title: Função IWICImagingFactory_CreateStream_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICImagingFactory_CreateStream_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 61670dbe3c1689a3d5b8030585a2b13d281efd19
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105814109"
---
# <a name="iwicimagingfactory_createstream_proxy-function"></a><span data-ttu-id="90826-103">\_Função de proxy CreateStream IWICImagingFactory \_</span><span class="sxs-lookup"><span data-stu-id="90826-103">IWICImagingFactory\_CreateStream\_Proxy function</span></span>

<span data-ttu-id="90826-104">Função de proxy para o método [**CreateStream**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createstream) .</span><span class="sxs-lookup"><span data-stu-id="90826-104">Proxy function for the [**CreateStream**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createstream) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="90826-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="90826-105">Syntax</span></span>


```C++
HRESULT IWICImagingFactory_CreateStream_Proxy(
  _In_  IWICImagingFactory *pFactory,
  _Out_ IWICStream         **ppIWICStream
);
```



## <a name="parameters"></a><span data-ttu-id="90826-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="90826-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="90826-107">*pFactory* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="90826-107">*pFactory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="90826-108">Tipo: \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) \** _</span><span class="sxs-lookup"><span data-stu-id="90826-108">Type: \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)\** _</span></span>

</dd> <dt>

<span data-ttu-id="90826-109">_ppIWICStream \* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="90826-109">_ppIWICStream\* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="90826-110">Tipo: **[ **IWICStream**](/windows/desktop/api/Wincodec/nn-wincodec-iwicstream)\*\***</span><span class="sxs-lookup"><span data-stu-id="90826-110">Type: **[**IWICStream**](/windows/desktop/api/Wincodec/nn-wincodec-iwicstream)\*\***</span></span>

<span data-ttu-id="90826-111">Um ponteiro que recebe um ponteiro para um novo [**IWICStream**](/windows/desktop/api/Wincodec/nn-wincodec-iwicstream).</span><span class="sxs-lookup"><span data-stu-id="90826-111">A pointer that receives a pointer to a new [**IWICStream**](/windows/desktop/api/Wincodec/nn-wincodec-iwicstream).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="90826-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="90826-112">Return value</span></span>

<span data-ttu-id="90826-113">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="90826-113">Type: **HRESULT**</span></span>

<span data-ttu-id="90826-114">Se essa função for bem sucedido, ela retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="90826-114">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="90826-115">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="90826-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="90826-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="90826-116">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="90826-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="90826-117">Requirements</span></span>



| <span data-ttu-id="90826-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="90826-118">Requirement</span></span> | <span data-ttu-id="90826-119">Valor</span><span class="sxs-lookup"><span data-stu-id="90826-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="90826-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="90826-120">Minimum supported client</span></span><br/> | <span data-ttu-id="90826-121">Windows XP com SP2, \[ somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="90826-121">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="90826-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="90826-122">Minimum supported server</span></span><br/> | <span data-ttu-id="90826-123">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="90826-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="90826-124">DLL</span><span class="sxs-lookup"><span data-stu-id="90826-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="90826-125"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="90826-125"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




