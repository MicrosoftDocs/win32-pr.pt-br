---
description: Anula o processamento do segmento de mídia atual.
ms.assetid: 31253d0d-c53f-47bd-823a-fc564cb63b78
title: 'Método IMFSourceBuffer:: Abort'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFSourceBuffer.Abort
api_type:
- COM
api_location:
- mfmediaengine.h
ms.openlocfilehash: 3a8b5115032fb918af66094bb87c7118eb503da3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104502198"
---
# <a name="imfsourcebufferabort-method"></a><span data-ttu-id="704ad-103">Método IMFSourceBuffer:: Abort</span><span class="sxs-lookup"><span data-stu-id="704ad-103">IMFSourceBuffer::Abort method</span></span>

<span data-ttu-id="704ad-104">Anula o processamento do segmento de mídia atual.</span><span class="sxs-lookup"><span data-stu-id="704ad-104">Aborts the processing of the current media segment.</span></span>

## <a name="syntax"></a><span data-ttu-id="704ad-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="704ad-105">Syntax</span></span>


```C++
HRESULT Abort();
```



## <a name="parameters"></a><span data-ttu-id="704ad-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="704ad-106">Parameters</span></span>

<span data-ttu-id="704ad-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="704ad-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="704ad-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="704ad-108">Return value</span></span>

<span data-ttu-id="704ad-109">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="704ad-109">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="704ad-110">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="704ad-110">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="704ad-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="704ad-111">Requirements</span></span>



| <span data-ttu-id="704ad-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="704ad-112">Requirement</span></span> | <span data-ttu-id="704ad-113">Valor</span><span class="sxs-lookup"><span data-stu-id="704ad-113">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="704ad-114">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="704ad-114">Minimum supported client</span></span><br/> | <span data-ttu-id="704ad-115">Windows 8.1 \[ apenas aplicativos de área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="704ad-115">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="704ad-116">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="704ad-116">Minimum supported server</span></span><br/> | <span data-ttu-id="704ad-117">\[Somente aplicativos da área de trabalho do Windows Server 2012 R2\]</span><span class="sxs-lookup"><span data-stu-id="704ad-117">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="704ad-118">INSERI</span><span class="sxs-lookup"><span data-stu-id="704ad-118">IDL</span></span><br/>                      | <dl> <span data-ttu-id="704ad-119"><dt>Mfmediaengine. idl</dt></span><span class="sxs-lookup"><span data-stu-id="704ad-119"><dt>Mfmediaengine.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="704ad-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="704ad-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="704ad-121">**IMFSourceBuffer**</span><span class="sxs-lookup"><span data-stu-id="704ad-121">**IMFSourceBuffer**</span></span>](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfsourcebuffer)
</dt> </dl>

 

 




