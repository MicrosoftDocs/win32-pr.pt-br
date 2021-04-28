---
description: Função de proxy de função IWICBitmapCodecInfo_GetContainerFormat_Proxy para o método GetContainerFormat.
ms.assetid: d8a2387a-fb75-4812-b046-51359071281d
title: Função IWICBitmapCodecInfo_GetContainerFormat_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapCodecInfo_GetContainerFormat_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 729b4e2fe0f21fd1e96082e53194fd49bbc39ae1
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108086364"
---
# <a name="iwicbitmapcodecinfo_getcontainerformat_proxy-function"></a><span data-ttu-id="26f97-103">\_Função de \_ proxy IWICBitmapCodecInfo GetContainerFormat</span><span class="sxs-lookup"><span data-stu-id="26f97-103">IWICBitmapCodecInfo\_GetContainerFormat\_Proxy function</span></span>

<span data-ttu-id="26f97-104">Função de proxy para o método [**GetContainerFormat**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapcodecinfo-getcontainerformat) .</span><span class="sxs-lookup"><span data-stu-id="26f97-104">Proxy function for the [**GetContainerFormat**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapcodecinfo-getcontainerformat) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="26f97-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="26f97-105">Syntax</span></span>


```C++
HRESULT IWICBitmapCodecInfo_GetContainerFormat_Proxy(
  _In_  IWICBitmapCodecInfo *THIS_PTR,
  _Out_ GUID                *pguidContainerFormat
);
```



## <a name="parameters"></a><span data-ttu-id="26f97-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="26f97-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="26f97-107">*Isso \_ PTR* \[\]</span><span class="sxs-lookup"><span data-stu-id="26f97-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="26f97-108">Tipo: **[ **IWICBitmapCodecInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo)\***</span><span class="sxs-lookup"><span data-stu-id="26f97-108">Type: **[**IWICBitmapCodecInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo)\***</span></span>

<span data-ttu-id="26f97-109">Ponteiro para este objeto [**IWICBitmapCodecInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo) .</span><span class="sxs-lookup"><span data-stu-id="26f97-109">Pointer to this [**IWICBitmapCodecInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo) object.</span></span>

</dd> <dt>

<span data-ttu-id="26f97-110">*pguidContainerFormat* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="26f97-110">*pguidContainerFormat* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="26f97-111">Tipo: **GUID \***</span><span class="sxs-lookup"><span data-stu-id="26f97-111">Type: **GUID\***</span></span>

<span data-ttu-id="26f97-112">Um ponteiro que recebe o GUID do contêiner.</span><span class="sxs-lookup"><span data-stu-id="26f97-112">A pointer that receives the container GUID.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="26f97-113">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="26f97-113">Return value</span></span>

<span data-ttu-id="26f97-114">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="26f97-114">Type: **HRESULT**</span></span>

<span data-ttu-id="26f97-115">Se essa função for bem sucedido, ela retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="26f97-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="26f97-116">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="26f97-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="26f97-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="26f97-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="26f97-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="26f97-118">Requirements</span></span>



| <span data-ttu-id="26f97-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="26f97-119">Requirement</span></span> | <span data-ttu-id="26f97-120">Valor</span><span class="sxs-lookup"><span data-stu-id="26f97-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="26f97-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="26f97-121">Minimum supported client</span></span><br/> | <span data-ttu-id="26f97-122">Windows XP com SP2, \[ somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="26f97-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="26f97-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="26f97-123">Minimum supported server</span></span><br/> | <span data-ttu-id="26f97-124">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="26f97-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="26f97-125">DLL</span><span class="sxs-lookup"><span data-stu-id="26f97-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="26f97-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="26f97-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




