---
description: Um retorno de chamada que notifica o host do número de threads e grupos do sombreador de computação na solicitação associada.
MS-HAID: vspixengine.IPipeLineStagesCallback2\_ThreadDataDimensionCallback\_ThreadData3D\_ThreadData3D
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Método IPipeLineStagesCallback2:: ThreadDataDimensionCallback'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: E8765C14-0A55-468D-BCA8-3E28E5476DFB
api_name:
- IPipeLineStagesCallback2.ThreadDataDimensionCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 93a8ee64c863128513563f3ce50dd2bfcdd77714
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104370301"
---
# <a name="span-idvspixengineipipelinestagescallback2_threaddatadimensioncallback_threaddata3d_threaddata3dspanipipelinestagescallback2threaddatadimensioncallback-method"></a><span data-ttu-id="d7c60-103"><span id="vspixengine.ipipelinestagescallback2_threaddatadimensioncallback_threaddata3d_threaddata3d"></span>Método IPipeLineStagesCallback2:: ThreadDataDimensionCallback</span><span class="sxs-lookup"><span data-stu-id="d7c60-103"><span id="vspixengine.ipipelinestagescallback2_threaddatadimensioncallback_threaddata3d_threaddata3d"></span>IPipeLineStagesCallback2::ThreadDataDimensionCallback method</span></span>

<span data-ttu-id="d7c60-104">Um retorno de chamada que notifica o host do número de threads e grupos do sombreador de computação na solicitação associada.</span><span class="sxs-lookup"><span data-stu-id="d7c60-104">A callback that notifies the host of the number of threads and groups of the compute shader in the associated request.</span></span>

## <a name="syntax"></a><span data-ttu-id="d7c60-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d7c60-105">Syntax</span></span>


```C++
HRESULT ThreadDataDimensionCallback(
   ThreadData3D threadGroupCount,
   ThreadData3D threadGroupSize
);
```

## <a name="parameters"></a><span data-ttu-id="d7c60-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d7c60-106">Parameters</span></span>

<span data-ttu-id="d7c60-107">*threadGroupCount* </span><span class="sxs-lookup"><span data-stu-id="d7c60-107">*threadGroupCount* </span></span>  
<span data-ttu-id="d7c60-108">A contagem multidimensional de grupos de threads.</span><span class="sxs-lookup"><span data-stu-id="d7c60-108">The multi-dimensional count of thread groups.</span></span>

<span data-ttu-id="d7c60-109">*threadGroupSize* </span><span class="sxs-lookup"><span data-stu-id="d7c60-109">*threadGroupSize* </span></span>  
<span data-ttu-id="d7c60-110">O tamanho multidimensional de cada grupo de threads.</span><span class="sxs-lookup"><span data-stu-id="d7c60-110">The multi-dimensional size of each thread group.</span></span>

## <a name="return-value"></a><span data-ttu-id="d7c60-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d7c60-111">Return value</span></span>

<span data-ttu-id="d7c60-112">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="d7c60-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="d7c60-113">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="d7c60-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="d7c60-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d7c60-114">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="d7c60-115">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d7c60-115">Header</span></span></p></td><td><span data-ttu-id="d7c60-116">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="d7c60-116">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="d7c60-117"><span id="see_also"></span>Confira também</span><span class="sxs-lookup"><span data-stu-id="d7c60-117"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="d7c60-118">**IPipeLineStagesCallback2**</span><span class="sxs-lookup"><span data-stu-id="d7c60-118">**IPipeLineStagesCallback2**</span></span>](/windows/desktop/direct3dtools/ipipelinestagescallback2)

 

 
