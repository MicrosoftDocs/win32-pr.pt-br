---
description: A suspensão real está prestes a ocorrer e nenhuma chamada será feita no módulo de descriptografia de conteúdo (CDM).
ms.assetid: 7a319fbb-9757-45da-8a8b-51dd48f08464
title: 'Método IMFCdmSuspendNotify:: End'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFCdmSuspendNotify.End
api_type:
- COM
api_location:
- mfmediaengine.h
ms.openlocfilehash: 71843b53fa85fded646fe71f2caa463a71c9415f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105790316"
---
# <a name="imfcdmsuspendnotifyend-method"></a><span data-ttu-id="15077-103">Método IMFCdmSuspendNotify:: End</span><span class="sxs-lookup"><span data-stu-id="15077-103">IMFCdmSuspendNotify::End method</span></span>

<span data-ttu-id="15077-104">A suspensão real está prestes a ocorrer e nenhuma chamada será feita no módulo de descriptografia de conteúdo (CDM).</span><span class="sxs-lookup"><span data-stu-id="15077-104">The actual suspend is about to occur and no more calls will be made into the Content Decryption Module (CDM).</span></span>

## <a name="syntax"></a><span data-ttu-id="15077-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="15077-105">Syntax</span></span>


```C++
HRESULT End();
```



## <a name="parameters"></a><span data-ttu-id="15077-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="15077-106">Parameters</span></span>

<span data-ttu-id="15077-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="15077-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="15077-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="15077-108">Return value</span></span>

<span data-ttu-id="15077-109">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="15077-109">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="15077-110">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="15077-110">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="15077-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="15077-111">Requirements</span></span>



| <span data-ttu-id="15077-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="15077-112">Requirement</span></span> | <span data-ttu-id="15077-113">Valor</span><span class="sxs-lookup"><span data-stu-id="15077-113">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="15077-114">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="15077-114">Minimum supported client</span></span><br/> | <span data-ttu-id="15077-115">Windows 8.1 \[ apenas aplicativos de área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="15077-115">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="15077-116">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="15077-116">Minimum supported server</span></span><br/> | <span data-ttu-id="15077-117">\[Somente aplicativos da área de trabalho do Windows Server 2012 R2\]</span><span class="sxs-lookup"><span data-stu-id="15077-117">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="15077-118">INSERI</span><span class="sxs-lookup"><span data-stu-id="15077-118">IDL</span></span><br/>                      | <dl> <span data-ttu-id="15077-119"><dt>Mfmediaengine. idl</dt></span><span class="sxs-lookup"><span data-stu-id="15077-119"><dt>Mfmediaengine.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="15077-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="15077-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="15077-121">**IMFCdmSuspendNotify**</span><span class="sxs-lookup"><span data-stu-id="15077-121">**IMFCdmSuspendNotify**</span></span>](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfcdmsuspendnotify)
</dt> </dl>

 

 




