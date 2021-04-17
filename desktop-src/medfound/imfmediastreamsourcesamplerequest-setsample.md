---
description: Define o exemplo para a origem do fluxo de mídia.
ms.assetid: a35c5e18-f307-4e40-bc92-f91aa9eb80ba
title: 'Método IMFMediaStreamSourceSampleRequest:: setsample'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFMediaStreamSourceSampleRequest.SetSample
api_type:
- COM
api_location:
- mfidl.h
ms.openlocfilehash: bc3b2693a4690207f0b39d7f1b846e1e63069a8c
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "105811896"
---
# <a name="imfmediastreamsourcesamplerequestsetsample-method"></a><span data-ttu-id="b33ee-103">Método IMFMediaStreamSourceSampleRequest:: setsample</span><span class="sxs-lookup"><span data-stu-id="b33ee-103">IMFMediaStreamSourceSampleRequest::SetSample method</span></span>

<span data-ttu-id="b33ee-104">Define o exemplo para a origem do fluxo de mídia.</span><span class="sxs-lookup"><span data-stu-id="b33ee-104">Sets the sample for the media stream source.</span></span>

## <a name="syntax"></a><span data-ttu-id="b33ee-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b33ee-105">Syntax</span></span>


```C++
HRESULT SetSample(
  [in] IMFSample *value
);
```



## <a name="parameters"></a><span data-ttu-id="b33ee-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b33ee-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b33ee-107">*valor* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="b33ee-107">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b33ee-108">O exemplo para a origem do fluxo de mídia.</span><span class="sxs-lookup"><span data-stu-id="b33ee-108">The sample for the media stream source.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b33ee-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b33ee-109">Return value</span></span>

<span data-ttu-id="b33ee-110">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="b33ee-110">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="b33ee-111">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="b33ee-111">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="b33ee-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b33ee-112">Requirements</span></span>



| <span data-ttu-id="b33ee-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="b33ee-113">Requirement</span></span> | <span data-ttu-id="b33ee-114">Valor</span><span class="sxs-lookup"><span data-stu-id="b33ee-114">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="b33ee-115">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b33ee-115">Minimum supported client</span></span><br/> | <span data-ttu-id="b33ee-116">Aplicativos Windows 8.1 aplicativos de \[ área de trabalho \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="b33ee-116">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="b33ee-117">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b33ee-117">Minimum supported server</span></span><br/> | <span data-ttu-id="b33ee-118">\[Aplicativos UWP para aplicativos da área de trabalho do Windows Server 2012 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="b33ee-118">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                       |
| <span data-ttu-id="b33ee-119">INSERI</span><span class="sxs-lookup"><span data-stu-id="b33ee-119">IDL</span></span><br/>                      | <dl> <span data-ttu-id="b33ee-120"><dt>Mfidl. idl</dt></span><span class="sxs-lookup"><span data-stu-id="b33ee-120"><dt>Mfidl.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b33ee-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="b33ee-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b33ee-122">**IMFMediaStreamSourceSampleRequest**</span><span class="sxs-lookup"><span data-stu-id="b33ee-122">**IMFMediaStreamSourceSampleRequest**</span></span>](imfmediastreamsourcesamplerequest.md)
</dt> </dl>

 

 




