---
description: Função de proxy para o método GetDeviceManufacturer.
ms.assetid: f4dbf67a-eb67-4138-a77a-7386567b95e6
title: Função IWICBitmapCodecInfo_GetDeviceManufacturer_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapCodecInfo_GetDeviceManufacturer_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 3dc10df32325fd0ffc5bb24d1a4c7927b1adc7e3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105788659"
---
# <a name="iwicbitmapcodecinfo_getdevicemanufacturer_proxy-function"></a><span data-ttu-id="5d370-103">\_Função de \_ proxy IWICBitmapCodecInfo GetDeviceManufacturer</span><span class="sxs-lookup"><span data-stu-id="5d370-103">IWICBitmapCodecInfo\_GetDeviceManufacturer\_Proxy function</span></span>

<span data-ttu-id="5d370-104">Função de proxy para o método [**GetDeviceManufacturer**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapcodecinfo-getdevicemanufacturer) .</span><span class="sxs-lookup"><span data-stu-id="5d370-104">Proxy function for the [**GetDeviceManufacturer**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapcodecinfo-getdevicemanufacturer) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="5d370-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5d370-105">Syntax</span></span>


```C++
HRESULT IWICBitmapCodecInfo_GetDeviceManufacturer_Proxy(
  _In_    IWICBitmapCodecInfo *THIS_PTR,
  _In_    UINT                cchDeviceManufacturer,
  _Inout_ WCHAR               *wzDeviceManufacturer,
  _Inout_ UINT                *pcchActual
);
```



## <a name="parameters"></a><span data-ttu-id="5d370-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5d370-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5d370-107">*Isso \_ PTR* \[\]</span><span class="sxs-lookup"><span data-stu-id="5d370-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5d370-108">Tipo: \**[**IWICBitmapCodecInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo) \** _</span><span class="sxs-lookup"><span data-stu-id="5d370-108">Type: \**[**IWICBitmapCodecInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo)\** _</span></span>

<span data-ttu-id="5d370-109">Ponteiro para este objeto [_ *IWICBitmapCodecInfo* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo) .</span><span class="sxs-lookup"><span data-stu-id="5d370-109">Pointer to this [_ *IWICBitmapCodecInfo*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo) object.</span></span>

</dd> <dt>

<span data-ttu-id="5d370-110">*cchDeviceManufacturer* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="5d370-110">*cchDeviceManufacturer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5d370-111">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="5d370-111">Type: **UINT**</span></span>

<span data-ttu-id="5d370-112">O tamanho do nome do fabricante do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5d370-112">The size of the device manufacture's name.</span></span>

</dd> <dt>

<span data-ttu-id="5d370-113">*wzDeviceManufacturer* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="5d370-113">*wzDeviceManufacturer* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="5d370-114">Tipo: \**WCHAR \** _</span><span class="sxs-lookup"><span data-stu-id="5d370-114">Type: \**WCHAR\** _</span></span>

<span data-ttu-id="5d370-115">Um ponteiro que recebe o nome do fabricante do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5d370-115">A pointer that receives the device manufacture's name.</span></span>

</dd> <dt>

<span data-ttu-id="5d370-116">_pcchActual \* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="5d370-116">_pcchActual\* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="5d370-117">Tipo: \**uint \** _</span><span class="sxs-lookup"><span data-stu-id="5d370-117">Type: \**UINT\** _</span></span>

<span data-ttu-id="5d370-118">O tamanho real do buffer necessário para recuperar o nome do fabricante do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5d370-118">The actual buffer size needed to retrieve the device manufacture's name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5d370-119">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="5d370-119">Return value</span></span>

<span data-ttu-id="5d370-120">Tipo: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="5d370-120">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="5d370-121">Se essa função for bem sucedido, ela retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="5d370-121">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="5d370-122">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="5d370-122">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="5d370-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="5d370-123">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="5d370-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5d370-124">Requirements</span></span>



| <span data-ttu-id="5d370-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="5d370-125">Requirement</span></span> | <span data-ttu-id="5d370-126">Valor</span><span class="sxs-lookup"><span data-stu-id="5d370-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5d370-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5d370-127">Minimum supported client</span></span><br/> | <span data-ttu-id="5d370-128">Windows XP com SP2, \[ somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="5d370-128">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="5d370-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5d370-129">Minimum supported server</span></span><br/> | <span data-ttu-id="5d370-130">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="5d370-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="5d370-131">DLL</span><span class="sxs-lookup"><span data-stu-id="5d370-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5d370-132"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5d370-132"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




