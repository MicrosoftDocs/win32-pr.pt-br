---
description: Função de proxy para o método Initialize.
ms.assetid: 860e8092-054d-489e-8ca1-fec43a039eca
title: Função IWICBitmapFlipRotator_Initialize_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapFlipRotator_Initialize_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 82a1aa5648edd47d0b635a407adc001c25183b50
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105771598"
---
# <a name="iwicbitmapfliprotator_initialize_proxy-function"></a><span data-ttu-id="14de1-103">Função de proxy de \_ inicialização IWICBitmapFlipRotator \_</span><span class="sxs-lookup"><span data-stu-id="14de1-103">IWICBitmapFlipRotator\_Initialize\_Proxy function</span></span>

<span data-ttu-id="14de1-104">Função de proxy para o método [**Initialize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapfliprotator-initialize) .</span><span class="sxs-lookup"><span data-stu-id="14de1-104">Proxy function for the [**Initialize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapfliprotator-initialize) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="14de1-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="14de1-105">Syntax</span></span>


```C++
HRESULT IWICBitmapFlipRotator_Initialize_Proxy(
  _In_ IWICBitmapFlipRotator     *THIS_PTR,
  _In_ IWICBitmapSource          *pISource,
  _In_ WICBitmapTransformOptions options
);
```



## <a name="parameters"></a><span data-ttu-id="14de1-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="14de1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="14de1-107">*Isso \_ PTR* \[\]</span><span class="sxs-lookup"><span data-stu-id="14de1-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="14de1-108">Tipo: \**[**IWICBitmapFlipRotator**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapfliprotator) \** _</span><span class="sxs-lookup"><span data-stu-id="14de1-108">Type: \**[**IWICBitmapFlipRotator**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapfliprotator)\** _</span></span>

<span data-ttu-id="14de1-109">Ponteiro para este objeto [_ *IWICBitmapFlipRotator* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapfliprotator) .</span><span class="sxs-lookup"><span data-stu-id="14de1-109">Pointer to this [_ *IWICBitmapFlipRotator*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapfliprotator) object.</span></span>

</dd> <dt>

<span data-ttu-id="14de1-110">*pISource* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="14de1-110">*pISource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="14de1-111">Tipo: \**[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) \** _</span><span class="sxs-lookup"><span data-stu-id="14de1-111">Type: \**[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\** _</span></span>

<span data-ttu-id="14de1-112">A origem do bitmap de entrada.</span><span class="sxs-lookup"><span data-stu-id="14de1-112">The input bitmap source.</span></span>

</dd> <dt>

<span data-ttu-id="14de1-113">_options \* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="14de1-113">_options\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="14de1-114">Tipo: **[ **WICBitmapTransformOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions)**</span><span class="sxs-lookup"><span data-stu-id="14de1-114">Type: **[**WICBitmapTransformOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions)**</span></span>

<span data-ttu-id="14de1-115">O [**WICBitmapTransformOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions) para inverter ou girar a imagem.</span><span class="sxs-lookup"><span data-stu-id="14de1-115">The [**WICBitmapTransformOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions) to flip or rotate the image.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="14de1-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="14de1-116">Return value</span></span>

<span data-ttu-id="14de1-117">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="14de1-117">Type: **HRESULT**</span></span>

<span data-ttu-id="14de1-118">Se essa função for bem sucedido, ela retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="14de1-118">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="14de1-119">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="14de1-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="14de1-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="14de1-120">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="14de1-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="14de1-121">Requirements</span></span>



| <span data-ttu-id="14de1-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="14de1-122">Requirement</span></span> | <span data-ttu-id="14de1-123">Valor</span><span class="sxs-lookup"><span data-stu-id="14de1-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="14de1-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="14de1-124">Minimum supported client</span></span><br/> | <span data-ttu-id="14de1-125">Windows XP com SP2, \[ somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="14de1-125">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="14de1-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="14de1-126">Minimum supported server</span></span><br/> | <span data-ttu-id="14de1-127">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="14de1-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="14de1-128">DLL</span><span class="sxs-lookup"><span data-stu-id="14de1-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="14de1-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="14de1-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




