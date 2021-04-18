---
description: Indica que o fim do fluxo de mídia foi atingido.
ms.assetid: 6d6bffcc-aa3c-4825-9268-00dcd2a347e6
title: 'Método IMFMediaSourceExtension:: SetEndOfStream'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFMediaSourceExtension.SetEndOfStream
api_type:
- COM
api_location:
- mfmediaengine.h
ms.openlocfilehash: 9018d76ce13bf441ea98134eb751f9e472f6bca8
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "105793700"
---
# <a name="imfmediasourceextensionsetendofstream-method"></a><span data-ttu-id="7a076-103">Método IMFMediaSourceExtension:: SetEndOfStream</span><span class="sxs-lookup"><span data-stu-id="7a076-103">IMFMediaSourceExtension::SetEndOfStream method</span></span>

<span data-ttu-id="7a076-104">Indica que o fim do fluxo de mídia foi atingido.</span><span class="sxs-lookup"><span data-stu-id="7a076-104">Indicate that the end of the media stream has been reached.</span></span>

## <a name="syntax"></a><span data-ttu-id="7a076-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7a076-105">Syntax</span></span>


```C++
HRESULT SetEndOfStream(
  [in] MF_MSE_ERROR error
);
```



## <a name="parameters"></a><span data-ttu-id="7a076-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7a076-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7a076-107">*erro* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="7a076-107">*error* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7a076-108">Usado para passar informações de erro.</span><span class="sxs-lookup"><span data-stu-id="7a076-108">Used to pass error information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7a076-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="7a076-109">Return value</span></span>

<span data-ttu-id="7a076-110">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="7a076-110">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="7a076-111">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="7a076-111">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="7a076-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7a076-112">Requirements</span></span>



| <span data-ttu-id="7a076-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="7a076-113">Requirement</span></span> | <span data-ttu-id="7a076-114">Valor</span><span class="sxs-lookup"><span data-stu-id="7a076-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="7a076-115">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7a076-115">Minimum supported client</span></span><br/> | <span data-ttu-id="7a076-116">Windows 8.1 \[ apenas aplicativos de área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="7a076-116">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="7a076-117">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7a076-117">Minimum supported server</span></span><br/> | <span data-ttu-id="7a076-118">\[Somente aplicativos da área de trabalho do Windows Server 2012 R2\]</span><span class="sxs-lookup"><span data-stu-id="7a076-118">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="7a076-119">INSERI</span><span class="sxs-lookup"><span data-stu-id="7a076-119">IDL</span></span><br/>                      | <dl> <span data-ttu-id="7a076-120"><dt>Mfmediaengine. idl</dt></span><span class="sxs-lookup"><span data-stu-id="7a076-120"><dt>Mfmediaengine.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7a076-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="7a076-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7a076-122">**IMFMediaSourceExtension**</span><span class="sxs-lookup"><span data-stu-id="7a076-122">**IMFMediaSourceExtension**</span></span>](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediasourceextension)
</dt> <dt>

[<span data-ttu-id="7a076-123">**erro do MF \_ MSE \_**</span><span class="sxs-lookup"><span data-stu-id="7a076-123">**MF\_MSE\_ERROR**</span></span>](mf-mse-error.md)
</dt> </dl>

 

 




