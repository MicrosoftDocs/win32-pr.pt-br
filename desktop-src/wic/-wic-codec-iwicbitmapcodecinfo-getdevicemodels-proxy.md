---
description: Função de proxy para o método GetDeviceModels.
ms.assetid: de8f91f7-fef7-48bc-94fc-34c43175248b
title: Função IWICBitmapCodecInfo_GetDeviceModels_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapCodecInfo_GetDeviceModels_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: b8fa6d6df6984569aa3fe49fc734f7699aa504d8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105812296"
---
# <a name="iwicbitmapcodecinfo_getdevicemodels_proxy-function"></a><span data-ttu-id="151f2-103">\_Função de \_ proxy IWICBitmapCodecInfo GetDeviceModels</span><span class="sxs-lookup"><span data-stu-id="151f2-103">IWICBitmapCodecInfo\_GetDeviceModels\_Proxy function</span></span>

<span data-ttu-id="151f2-104">Função de proxy para o método [**GetDeviceModels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapcodecinfo-getdevicemodels) .</span><span class="sxs-lookup"><span data-stu-id="151f2-104">Proxy function for the [**GetDeviceModels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapcodecinfo-getdevicemodels) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="151f2-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="151f2-105">Syntax</span></span>


```C++
HRESULT IWICBitmapCodecInfo_GetDeviceModels_Proxy(
  _In_    IWICBitmapCodecInfo *THIS_PTR,
  _In_    UINT                cchDeviceModels,
  _Inout_ WCHAR               *wzDeviceModels,
  _Inout_ UINT                *pcchActual
);
```



## <a name="parameters"></a><span data-ttu-id="151f2-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="151f2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="151f2-107">*Isso \_ PTR* \[\]</span><span class="sxs-lookup"><span data-stu-id="151f2-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="151f2-108">Tipo: \**[**IWICBitmapCodecInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo) \** _</span><span class="sxs-lookup"><span data-stu-id="151f2-108">Type: \**[**IWICBitmapCodecInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo)\** _</span></span>

<span data-ttu-id="151f2-109">Ponteiro para este objeto [_ *IWICBitmapCodecInfo* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo) .</span><span class="sxs-lookup"><span data-stu-id="151f2-109">Pointer to this [_ *IWICBitmapCodecInfo*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo) object.</span></span>

</dd> <dt>

<span data-ttu-id="151f2-110">*cchDeviceModels* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="151f2-110">*cchDeviceModels* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="151f2-111">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="151f2-111">Type: **UINT**</span></span>

<span data-ttu-id="151f2-112">O tamanho do buffer de modelos de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="151f2-112">The size of the device models buffer.</span></span>

</dd> <dt>

<span data-ttu-id="151f2-113">*wzDeviceModels* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="151f2-113">*wzDeviceModels* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="151f2-114">Tipo: \**WCHAR \** _</span><span class="sxs-lookup"><span data-stu-id="151f2-114">Type: \**WCHAR\** _</span></span>

<span data-ttu-id="151f2-115">Um ponteiro que recebe uma lista delimitada por vírgulas de nomes de modelo de dispositivo associados ao codec.</span><span class="sxs-lookup"><span data-stu-id="151f2-115">A pointer that receives a comma delimited list of device model names associated with the codec.</span></span>

</dd> <dt>

<span data-ttu-id="151f2-116">_pcchActual \* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="151f2-116">_pcchActual\* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="151f2-117">Tipo: \**uint \** _</span><span class="sxs-lookup"><span data-stu-id="151f2-117">Type: \**UINT\** _</span></span>

<span data-ttu-id="151f2-118">O tamanho de buffer real necessário para recuperar todos os nomes de modelo de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="151f2-118">The actual buffer size needed to retrieve all of the device model names.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="151f2-119">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="151f2-119">Return value</span></span>

<span data-ttu-id="151f2-120">Tipo: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="151f2-120">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="151f2-121">Se essa função for bem sucedido, ela retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="151f2-121">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="151f2-122">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="151f2-122">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="151f2-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="151f2-123">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="151f2-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="151f2-124">Requirements</span></span>



| <span data-ttu-id="151f2-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="151f2-125">Requirement</span></span> | <span data-ttu-id="151f2-126">Valor</span><span class="sxs-lookup"><span data-stu-id="151f2-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="151f2-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="151f2-127">Minimum supported client</span></span><br/> | <span data-ttu-id="151f2-128">Windows XP com SP2, \[ somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="151f2-128">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="151f2-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="151f2-129">Minimum supported server</span></span><br/> | <span data-ttu-id="151f2-130">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="151f2-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="151f2-131">DLL</span><span class="sxs-lookup"><span data-stu-id="151f2-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="151f2-132"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="151f2-132"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




