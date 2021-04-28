---
description: Função IWICBitmapClipper_Initialize_Proxy function-proxy para o método Initialize.
ms.assetid: 60925f5c-aca4-4f49-96d2-9b58d8310e3c
title: Função IWICBitmapClipper_Initialize_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapClipper_Initialize_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: ce3c745d27928765fdfdf664c423f7e2146cbd5f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108086384"
---
# <a name="iwicbitmapclipper_initialize_proxy-function"></a><span data-ttu-id="55ddb-103">Função de proxy de \_ inicialização IWICBitmapClipper \_</span><span class="sxs-lookup"><span data-stu-id="55ddb-103">IWICBitmapClipper\_Initialize\_Proxy function</span></span>

<span data-ttu-id="55ddb-104">Função de proxy para o método [**Initialize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapclipper-initialize) .</span><span class="sxs-lookup"><span data-stu-id="55ddb-104">Proxy function for the [**Initialize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapclipper-initialize) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="55ddb-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="55ddb-105">Syntax</span></span>


```C++
HRESULT IWICBitmapClipper_Initialize_Proxy(
  _In_       IWICBitmapClipper *THIS_PTR,
  _In_       IWICBitmapSource  *pISource,
  _In_ const WICRect           *prc
);
```



## <a name="parameters"></a><span data-ttu-id="55ddb-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="55ddb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="55ddb-107">*Isso \_ PTR* \[\]</span><span class="sxs-lookup"><span data-stu-id="55ddb-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="55ddb-108">Tipo: **[ **IWICBitmapClipper**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapclipper)\***</span><span class="sxs-lookup"><span data-stu-id="55ddb-108">Type: **[**IWICBitmapClipper**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapclipper)\***</span></span>

<span data-ttu-id="55ddb-109">Ponteiro para este objeto [**IWICBitmapClipper**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapclipper) .</span><span class="sxs-lookup"><span data-stu-id="55ddb-109">Pointer to this [**IWICBitmapClipper**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapclipper) object.</span></span>

</dd> <dt>

<span data-ttu-id="55ddb-110">*pISource* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="55ddb-110">*pISource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="55ddb-111">Tipo: **[ **IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\***</span><span class="sxs-lookup"><span data-stu-id="55ddb-111">Type: **[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\***</span></span>

<span data-ttu-id="55ddb-112">A origem do bitmap de entrada.</span><span class="sxs-lookup"><span data-stu-id="55ddb-112">The input bitmap source.</span></span>

</dd> <dt>

<span data-ttu-id="55ddb-113">*prc* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="55ddb-113">*prc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="55ddb-114">Tipo: **const [**WICRect**](/windows/desktop/api/Wincodec/ns-wincodec-wicrect) \***</span><span class="sxs-lookup"><span data-stu-id="55ddb-114">Type: **const [**WICRect**](/windows/desktop/api/Wincodec/ns-wincodec-wicrect)\***</span></span>

<span data-ttu-id="55ddb-115">O retângulo da origem do bitmap a ser recortado.</span><span class="sxs-lookup"><span data-stu-id="55ddb-115">The rectangle of the bitmap source to clip.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="55ddb-116">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="55ddb-116">Return value</span></span>

<span data-ttu-id="55ddb-117">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="55ddb-117">Type: **HRESULT**</span></span>

<span data-ttu-id="55ddb-118">Se essa função for bem sucedido, ela retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="55ddb-118">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="55ddb-119">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="55ddb-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="55ddb-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="55ddb-120">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="55ddb-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="55ddb-121">Requirements</span></span>



| <span data-ttu-id="55ddb-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="55ddb-122">Requirement</span></span> | <span data-ttu-id="55ddb-123">Valor</span><span class="sxs-lookup"><span data-stu-id="55ddb-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="55ddb-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="55ddb-124">Minimum supported client</span></span><br/> | <span data-ttu-id="55ddb-125">Windows XP com SP2, \[ somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="55ddb-125">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="55ddb-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="55ddb-126">Minimum supported server</span></span><br/> | <span data-ttu-id="55ddb-127">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="55ddb-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="55ddb-128">DLL</span><span class="sxs-lookup"><span data-stu-id="55ddb-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="55ddb-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="55ddb-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




