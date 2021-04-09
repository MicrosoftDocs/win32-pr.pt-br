---
description: Executa um experimento.
MS-HAID: vspixengine.IPixEngine\_RunExperiment\_Experiment\_IRunExperimentCallback\_ptr\_INewFramesCallback\_ptr\_IFileIOCallback\_ptr\_DWORD\_ExperimentTrigger\_arr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Método IPixEngine:: RunExperiment'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: A2EEC278-C074-44B3-94DC-E2D9DC770576
api_name:
- IPixEngine.RunExperiment
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: c656d57dda496b6c1d8c128dc5e832ec40ef13f7
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104087543"
---
# <a name="span-idvspixengineipixengine_runexperiment_experiment_irunexperimentcallback_ptr_inewframescallback_ptr_ifileiocallback_ptr_dword_experimenttrigger_arrspanipixenginerunexperiment-method"></a><span data-ttu-id="c75f9-103"><span id="vspixengine.ipixengine_runexperiment_experiment_irunexperimentcallback_ptr_inewframescallback_ptr_ifileiocallback_ptr_dword_experimenttrigger_arr"></span>Método IPixEngine:: RunExperiment</span><span class="sxs-lookup"><span data-stu-id="c75f9-103"><span id="vspixengine.ipixengine_runexperiment_experiment_irunexperimentcallback_ptr_inewframescallback_ptr_ifileiocallback_ptr_dword_experimenttrigger_arr"></span>IPixEngine::RunExperiment method</span></span>

<span data-ttu-id="c75f9-104">Executa um experimento.</span><span class="sxs-lookup"><span data-stu-id="c75f9-104">Runs an experiment.</span></span>

## <a name="syntax"></a><span data-ttu-id="c75f9-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c75f9-105">Syntax</span></span>


```C++
HRESULT RunExperiment(
   Experiment               experiment,
   IRunExperimentCallback * pRequestCallback,
   INewFramesCallback*      callbacks,
   IFileIOCallback*         pFileIOCallback,
   DWORD                    triggersCount,
   ExperimentTrigger []     count4_triggersBuffer
);
```

## <a name="parameters"></a><span data-ttu-id="c75f9-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c75f9-106">Parameters</span></span>

<span data-ttu-id="c75f9-107">*testes* </span><span class="sxs-lookup"><span data-stu-id="c75f9-107">*experiment* </span></span>  
<span data-ttu-id="c75f9-108">Descreve o teste a ser executado.</span><span class="sxs-lookup"><span data-stu-id="c75f9-108">Describes the experiment to be run.</span></span>

<span data-ttu-id="c75f9-109">*pRequestCallback* </span><span class="sxs-lookup"><span data-stu-id="c75f9-109">*pRequestCallback* </span></span>  
<span data-ttu-id="c75f9-110">O endereço de uma função usada para notificar o host de que o mecanismo iniciou o experimento.</span><span class="sxs-lookup"><span data-stu-id="c75f9-110">The address of a function used to notify the host that engine has started the experiment.</span></span>

<span data-ttu-id="c75f9-111">*retornos* </span><span class="sxs-lookup"><span data-stu-id="c75f9-111">*callbacks* </span></span>  
<span data-ttu-id="c75f9-112">O endereço de uma função usada para notificar o host que novos quadros foram capturados.</span><span class="sxs-lookup"><span data-stu-id="c75f9-112">The address of a function used to notify the host that new frames have been captured.</span></span>

<span data-ttu-id="c75f9-113">*pFileIOCallback* </span><span class="sxs-lookup"><span data-stu-id="c75f9-113">*pFileIOCallback* </span></span>  
<span data-ttu-id="c75f9-114">O endereço de uma função usada para notificar o host de erros de e/s de arquivo durante a análise.</span><span class="sxs-lookup"><span data-stu-id="c75f9-114">The address of a function used to notify the host of file IO errors during parsing.</span></span>

<span data-ttu-id="c75f9-115">*triggersCount* </span><span class="sxs-lookup"><span data-stu-id="c75f9-115">*triggersCount* </span></span>  
<span data-ttu-id="c75f9-116">O número de gatilhos no experimento.</span><span class="sxs-lookup"><span data-stu-id="c75f9-116">The number of triggers in the experiment.</span></span>

<span data-ttu-id="c75f9-117">*count4 \_ triggersBuffer* </span><span class="sxs-lookup"><span data-stu-id="c75f9-117">*count4\_triggersBuffer* </span></span>  
<span data-ttu-id="c75f9-118">Capturar gatilhos.</span><span class="sxs-lookup"><span data-stu-id="c75f9-118">Capture triggers.</span></span>

## <a name="return-value"></a><span data-ttu-id="c75f9-119">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c75f9-119">Return value</span></span>

<span data-ttu-id="c75f9-120">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="c75f9-120">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="c75f9-121">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="c75f9-121">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="c75f9-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c75f9-122">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="c75f9-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c75f9-123">Header</span></span></p></td><td><span data-ttu-id="c75f9-124">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="c75f9-124">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="c75f9-125"><span id="see_also"></span>Consulte também</span><span class="sxs-lookup"><span data-stu-id="c75f9-125"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="c75f9-126">**IPixEngine**</span><span class="sxs-lookup"><span data-stu-id="c75f9-126">**IPixEngine**</span></span>](/windows/desktop/direct3dtools/ipixengine)

 

 
