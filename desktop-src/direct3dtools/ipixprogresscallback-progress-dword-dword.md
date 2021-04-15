---
description: Um retorno de chamada que notifica o host do progresso de uma solicitação associada.
MS-HAID: vspixengine.IPixProgressCallback\_Progress\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'IPixProgressCallback: método rogress de:P'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: BE74599B-C98F-4BDB-ACDF-641F77A35EEB
api_name:
- IPixProgressCallback.Progress
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 0379ad6fcb5f97825469c97af38453e55585d005
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104370221"
---
# <a name="span-idvspixengineipixprogresscallback_progress_dword_dwordspanipixprogresscallbackprogress-method"></a><span data-ttu-id="77ede-103"><span id="vspixengine.ipixprogresscallback_progress_dword_dword"></span>IPixProgressCallback: método rogress de:P</span><span class="sxs-lookup"><span data-stu-id="77ede-103"><span id="vspixengine.ipixprogresscallback_progress_dword_dword"></span>IPixProgressCallback::Progress method</span></span>

<span data-ttu-id="77ede-104">Um retorno de chamada que notifica o host do progresso de uma solicitação associada.</span><span class="sxs-lookup"><span data-stu-id="77ede-104">A callback that notifies the host of the progress of an associated request.</span></span>

## <a name="syntax"></a><span data-ttu-id="77ede-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="77ede-105">Syntax</span></span>


```C++
HRESULT Progress(
   DWORD current,
   DWORD maxSize
);
```

## <a name="parameters"></a><span data-ttu-id="77ede-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="77ede-106">Parameters</span></span>

<span data-ttu-id="77ede-107">*atualizados* </span><span class="sxs-lookup"><span data-stu-id="77ede-107">*current* </span></span>  
<span data-ttu-id="77ede-108">A parte de uma solicitação foi concluída, como uma contagem do número de etapas concluídas.</span><span class="sxs-lookup"><span data-stu-id="77ede-108">The portion of a request completed, as a count of the number of steps completed.</span></span>

<span data-ttu-id="77ede-109">*maxSize* </span><span class="sxs-lookup"><span data-stu-id="77ede-109">*maxSize* </span></span>  
<span data-ttu-id="77ede-110">O número total de etapas para concluir a solicitação.</span><span class="sxs-lookup"><span data-stu-id="77ede-110">The total number of steps to complete the request.</span></span>

## <a name="return-value"></a><span data-ttu-id="77ede-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="77ede-111">Return value</span></span>

<span data-ttu-id="77ede-112">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="77ede-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="77ede-113">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="77ede-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="77ede-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="77ede-114">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="77ede-115">parâmetro</span><span class="sxs-lookup"><span data-stu-id="77ede-115">Header</span></span></p></td><td><span data-ttu-id="77ede-116">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="77ede-116">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="77ede-117"><span id="see_also"></span>Confira também</span><span class="sxs-lookup"><span data-stu-id="77ede-117"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="77ede-118">**IPixProgressCallback**</span><span class="sxs-lookup"><span data-stu-id="77ede-118">**IPixProgressCallback**</span></span>](/windows/desktop/direct3dtools/ipixprogresscallback)

 

 
