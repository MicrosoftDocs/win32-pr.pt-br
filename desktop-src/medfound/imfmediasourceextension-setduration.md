---
description: Define a duração da origem de mídia em unidades de 100 a nanossegundos.
ms.assetid: dc3dc600-ca81-40da-9edb-0af283ba9221
title: 'Método IMFMediaSourceExtension:: setduration'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFMediaSourceExtension.SetDuration
api_type:
- COM
api_location:
- mfmediaengine.h
ms.openlocfilehash: ae669bf19f531034eacafac7fb89f3c07fa1e0e9
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "105763974"
---
# <a name="imfmediasourceextensionsetduration-method"></a><span data-ttu-id="e4a3e-103">Método IMFMediaSourceExtension:: setduration</span><span class="sxs-lookup"><span data-stu-id="e4a3e-103">IMFMediaSourceExtension::SetDuration method</span></span>

<span data-ttu-id="e4a3e-104">Define a duração da origem de mídia em unidades de 100 a nanossegundos.</span><span class="sxs-lookup"><span data-stu-id="e4a3e-104">Sets the duration of the media source in 100-nanosecond units.</span></span>

## <a name="syntax"></a><span data-ttu-id="e4a3e-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e4a3e-105">Syntax</span></span>


```C++
HRESULT SetDuration(
  [in] double duration
);
```



## <a name="parameters"></a><span data-ttu-id="e4a3e-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e4a3e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e4a3e-107">*duração* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e4a3e-107">*duration* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e4a3e-108">A duração da origem de mídia em unidades de 100 nanossegundos.</span><span class="sxs-lookup"><span data-stu-id="e4a3e-108">The duration of the media source in 100-nanosecond units.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e4a3e-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e4a3e-109">Return value</span></span>

<span data-ttu-id="e4a3e-110">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="e4a3e-110">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="e4a3e-111">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="e4a3e-111">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="e4a3e-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e4a3e-112">Requirements</span></span>



| <span data-ttu-id="e4a3e-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="e4a3e-113">Requirement</span></span> | <span data-ttu-id="e4a3e-114">Valor</span><span class="sxs-lookup"><span data-stu-id="e4a3e-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="e4a3e-115">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e4a3e-115">Minimum supported client</span></span><br/> | <span data-ttu-id="e4a3e-116">Windows 8.1 \[ apenas aplicativos de área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="e4a3e-116">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="e4a3e-117">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e4a3e-117">Minimum supported server</span></span><br/> | <span data-ttu-id="e4a3e-118">\[Somente aplicativos da área de trabalho do Windows Server 2012 R2\]</span><span class="sxs-lookup"><span data-stu-id="e4a3e-118">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="e4a3e-119">INSERI</span><span class="sxs-lookup"><span data-stu-id="e4a3e-119">IDL</span></span><br/>                      | <dl> <span data-ttu-id="e4a3e-120"><dt>Mfmediaengine. idl</dt></span><span class="sxs-lookup"><span data-stu-id="e4a3e-120"><dt>Mfmediaengine.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e4a3e-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="e4a3e-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e4a3e-122">**IMFMediaSourceExtension**</span><span class="sxs-lookup"><span data-stu-id="e4a3e-122">**IMFMediaSourceExtension**</span></span>](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediasourceextension)
</dt> </dl>

 

 




