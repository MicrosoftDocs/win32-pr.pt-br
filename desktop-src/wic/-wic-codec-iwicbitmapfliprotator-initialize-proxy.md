---
description: Função IWICBitmapFlipRotator_Initialize_Proxy function-proxy para o método Initialize.
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
ms.openlocfilehash: 4a260d6e60c0ffdeb05aa064ae8abbb38818ac8c
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108091154"
---
# <a name="iwicbitmapfliprotator_initialize_proxy-function"></a><span data-ttu-id="be545-103">Função de proxy de \_ inicialização IWICBitmapFlipRotator \_</span><span class="sxs-lookup"><span data-stu-id="be545-103">IWICBitmapFlipRotator\_Initialize\_Proxy function</span></span>

<span data-ttu-id="be545-104">Função de proxy para o método [**Initialize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapfliprotator-initialize) .</span><span class="sxs-lookup"><span data-stu-id="be545-104">Proxy function for the [**Initialize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapfliprotator-initialize) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="be545-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="be545-105">Syntax</span></span>


```C++
HRESULT IWICBitmapFlipRotator_Initialize_Proxy(
  _In_ IWICBitmapFlipRotator     *THIS_PTR,
  _In_ IWICBitmapSource          *pISource,
  _In_ WICBitmapTransformOptions options
);
```



## <a name="parameters"></a><span data-ttu-id="be545-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="be545-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="be545-107">*Isso \_ PTR* \[\]</span><span class="sxs-lookup"><span data-stu-id="be545-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="be545-108">Tipo: **[ **IWICBitmapFlipRotator**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapfliprotator)\***</span><span class="sxs-lookup"><span data-stu-id="be545-108">Type: **[**IWICBitmapFlipRotator**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapfliprotator)\***</span></span>

<span data-ttu-id="be545-109">Ponteiro para este objeto [**IWICBitmapFlipRotator**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapfliprotator) .</span><span class="sxs-lookup"><span data-stu-id="be545-109">Pointer to this [**IWICBitmapFlipRotator**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapfliprotator) object.</span></span>

</dd> <dt>

<span data-ttu-id="be545-110">*pISource* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="be545-110">*pISource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="be545-111">Tipo: **[ **IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\***</span><span class="sxs-lookup"><span data-stu-id="be545-111">Type: **[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\***</span></span>

<span data-ttu-id="be545-112">A origem do bitmap de entrada.</span><span class="sxs-lookup"><span data-stu-id="be545-112">The input bitmap source.</span></span>

</dd> <dt>

<span data-ttu-id="be545-113">*Opções* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="be545-113">*options* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="be545-114">Tipo: **[ **WICBitmapTransformOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions)**</span><span class="sxs-lookup"><span data-stu-id="be545-114">Type: **[**WICBitmapTransformOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions)**</span></span>

<span data-ttu-id="be545-115">O [**WICBitmapTransformOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions) para inverter ou girar a imagem.</span><span class="sxs-lookup"><span data-stu-id="be545-115">The [**WICBitmapTransformOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions) to flip or rotate the image.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="be545-116">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="be545-116">Return value</span></span>

<span data-ttu-id="be545-117">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="be545-117">Type: **HRESULT**</span></span>

<span data-ttu-id="be545-118">Se essa função for bem sucedido, ela retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="be545-118">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="be545-119">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="be545-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="be545-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="be545-120">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="be545-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="be545-121">Requirements</span></span>



| <span data-ttu-id="be545-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="be545-122">Requirement</span></span> | <span data-ttu-id="be545-123">Valor</span><span class="sxs-lookup"><span data-stu-id="be545-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="be545-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="be545-124">Minimum supported client</span></span><br/> | <span data-ttu-id="be545-125">Windows XP com SP2, \[ somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="be545-125">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="be545-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="be545-126">Minimum supported server</span></span><br/> | <span data-ttu-id="be545-127">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="be545-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="be545-128">DLL</span><span class="sxs-lookup"><span data-stu-id="be545-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="be545-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="be545-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




