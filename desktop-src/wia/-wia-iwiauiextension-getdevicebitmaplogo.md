---
description: Obtém um logotipo de bitmap personalizado para o dispositivo.
ms.assetid: 56b3c7c9-64f4-4853-9eb7-d876d02a851f
title: 'Método IWiaUIExtension:: GetDeviceBitmapLogo (Wiadevd. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaUIExtension.GetDeviceBitmapLogo
api_type:
- COM
api_location:
- Wiadevd.h
ms.openlocfilehash: 51db237c93a2167eb3c4bdae648f9d79da13319a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105763257"
---
# <a name="iwiauiextensiongetdevicebitmaplogo-method"></a><span data-ttu-id="2e399-103">Método IWiaUIExtension:: GetDeviceBitmapLogo</span><span class="sxs-lookup"><span data-stu-id="2e399-103">IWiaUIExtension::GetDeviceBitmapLogo method</span></span>

<span data-ttu-id="2e399-104">Obtém um logotipo de bitmap personalizado para o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2e399-104">Gets a custom bitmap logo for the device.</span></span>

## <a name="syntax"></a><span data-ttu-id="2e399-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2e399-105">Syntax</span></span>


```C++
HRESULT GetDeviceBitmapLogo(
  [in]  BSTR    bstrDeviceId,
  [out] HBITMAP *phBitmap,
  [in]  ULONG   nMaxWidth,
  [in]  ULONG   nMaxHeight
);
```



## <a name="parameters"></a><span data-ttu-id="2e399-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2e399-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2e399-107">*bstrDeviceId* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="2e399-107">*bstrDeviceId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2e399-108">Tipo: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="2e399-108">Type: **BSTR**</span></span>

<span data-ttu-id="2e399-109">Especifica a ID do dispositivo WIA para o qual o ícone deve ser obtido.</span><span class="sxs-lookup"><span data-stu-id="2e399-109">Specifies the device ID of the WIA device for which the icon is to be obtained.</span></span>

</dd> <dt>

<span data-ttu-id="2e399-110">*phBitmap* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="2e399-110">*phBitmap* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2e399-111">Tipo: \**HBITMAP \** _</span><span class="sxs-lookup"><span data-stu-id="2e399-111">Type: \**HBITMAP\** _</span></span>

<span data-ttu-id="2e399-112">Aponta para um local de memória que receberá um identificador para o logotipo de bitmap do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2e399-112">Points to a memory location that will receive a handle for the bitmap logo for the device.</span></span>

</dd> <dt>

<span data-ttu-id="2e399-113">_nMaxWidth \* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2e399-113">_nMaxWidth\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2e399-114">Tipo: **ULONG**</span><span class="sxs-lookup"><span data-stu-id="2e399-114">Type: **ULONG**</span></span>

<span data-ttu-id="2e399-115">Especifica a largura desejada do bitmap.</span><span class="sxs-lookup"><span data-stu-id="2e399-115">Specifies the desired width of the bitmap.</span></span>

</dd> <dt>

<span data-ttu-id="2e399-116">*nMaxHeight* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="2e399-116">*nMaxHeight* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2e399-117">Tipo: **ULONG**</span><span class="sxs-lookup"><span data-stu-id="2e399-117">Type: **ULONG**</span></span>

<span data-ttu-id="2e399-118">Especifica a altura desejada do bitmap.</span><span class="sxs-lookup"><span data-stu-id="2e399-118">Specifies the desired height of the bitmap.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2e399-119">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="2e399-119">Return value</span></span>

<span data-ttu-id="2e399-120">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="2e399-120">Type: **HRESULT**</span></span>

<span data-ttu-id="2e399-121">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="2e399-121">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="2e399-122">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="2e399-122">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="2e399-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2e399-123">Requirements</span></span>



| <span data-ttu-id="2e399-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="2e399-124">Requirement</span></span> | <span data-ttu-id="2e399-125">Valor</span><span class="sxs-lookup"><span data-stu-id="2e399-125">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="2e399-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2e399-126">Minimum supported client</span></span><br/> | <span data-ttu-id="2e399-127">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="2e399-127">Windows XP \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="2e399-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2e399-128">Minimum supported server</span></span><br/> | <span data-ttu-id="2e399-129">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="2e399-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="2e399-130">parâmetro</span><span class="sxs-lookup"><span data-stu-id="2e399-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="2e399-131"><dt>Wiadevd. h</dt></span><span class="sxs-lookup"><span data-stu-id="2e399-131"><dt>Wiadevd.h</dt></span></span> </dl> |



 

 




